# <p><strong><u>Logging – Best Practices</u></strong></p>
<ol>
	<li>Use key-value pairs.</li>
</ol>
<p>Using key-value pairs in logs makes parsing the data much easier.  This ensures that a program, and not just a human being, can make sense of the data being logged.</p>
<p>Example:</p>
<p>key1=value1, key2=value2, key3=value3</p>
<ol start="2">
	<li>Create events that humans can read.</li>
</ol>
<p>Avoid using complex encoding that would require lookups to make event information intelligible. For example, if logs are in a binary format, provide tools to easily convert them to a human-readable (ASCII) format. Don't use a format that requires an arbitrary code to decipher it. And, don't use different formats in the same file—split them out into individual files instead.</p>
<ol start="3">
	<li>Use timestamps for every event.</li>
</ol>
<p>The correct time is critical to understanding the proper sequence of events. Timestamps are critical for debugging, analytics, and deriving transactions.</p>
<ul>
	<li>Use the most verbose time granularity possible.</li>
	<li>Put the timestamp at the beginning of the line. The farther you place a timestamp from the beginning, the more difficult it is to tell it's a timestamp and not other data.</li>
	<li>Include a four-digit year.</li>
	<li>Include a time zone, preferably a GMT/UTC offset.</li>
	<li>Time should be rendered in microseconds in each event. The event could become detached from its original source file at some point, so having the most accurate data about an event is ideal.</li>
</ul>
<ol start="4">
	<li>Use unique identifiers (IDs) – [User ID, Transaction ID].</li>
</ol>
<p>Unique identifiers such as transaction IDs and user IDs are tremendously helpful when debugging, and even more helpful when you are gathering analytics. Unique IDs can point you to the exact transaction. Without them, you might only have a time range to use. When possible, carry these IDs through multiple touch points and avoid changing the format of these IDs between modules. That way, you can track transactions through the system and follow them across machines, networks, and services.</p>
<ol start="5">
	<li>Log in text format.</li>
</ol>
<p>Avoid logging binary information because it is difficult to meaningfully search or analyze binary data. Binary logs might seem preferable because they are compressed, but they require decoding and won't segment.  Instead of directly logging binary data, place textual meta-data in the event so that you can search through it.  For example, don't log the binary data of a JPG file, but do log its image size, creation tool, username, camera, GPS location, and so on.</p>
<ol start="6">
	<li>Use structured and developer-friendly logging formats.</li>
</ol>
<p>Developers like the ability to receive a stream of data over HTTP/S when possible, and with data structured so that it can be easily processed.  Developer-friendly formats like JSON are readable by humans and machines.</p>
<ol start="7">
	<li>Log more than just debugging events.</li>
</ol>
<p>Put semantic meaning in events to get more out of your data. Log audit trails, what users are doing, transactions, timing information, and so on. Log anything that can add value when aggregated, charted, or further analyzed. In other words, log anything that is interesting to the business.</p>
<ol start="8">
	<li>Categorize the event.</li>
</ol>
<p>Use the severity values TRACE, DEBUG, INFO, WARN, ERROR, and FATAL.</p>
<ul>
	<li>TRACE - Designates finer-grained informational events than the DEBUG.</li>
	<li>DEBUG - Designates fine-grained informational events that are most useful to debug an application.</li>
	<li>INFO - Designates informational messages that highlight the progress of the application at coarse-grained level.</li>
	<li>WARN - Designates potentially harmful situations.</li>
	<li>ERROR - Designates error events that might still allow the application to continue running.</li>
	<li>FATAL - Designates very severe error events that will presumably lead the application to abort.</li>
</ul>
<ol start="9">
	<li>Identify the source of the log event.</li>
</ol>
<p>Include the source of the log event, such as the class, function, or filename.</p>
<ol start="10">
	<li>Keep multi-line events to a minimum.</li>
</ol>
<p>Multi-line events generate a lot of segments, which can affect indexing and search speed, as well as disk compression. Consider breaking multi-line events into separate events.</p>
<p><strong><u>Operational Best Practices</u></strong></p>
<ol>
	<li>Log to local files first.</li>
</ol>
<p>If you log to a local file, it provides a local buffer and you aren't blocked if the network goes down.  The logs could further be beamed to a remote secure log server once the local file has been created, in batch mode, or as close to the time of creation of the log as required.</p>
<ol start="2">
	<li>Use log rotation policies.</li>
</ol>
<p>Logs can take up a lot of space. Maybe compliance regulations require you to keep years of archival storage, but you don't want to fill up your file system on your production machines. So, set up good rotation strategies and decide whether to destroy or back up your logs.  This could be performed using housekeeping scripts.</p>
<ol start="3">
	<li>Collect data from as many sources as possible, which will give the log reviewer or the computer a bigger and fuller picture.</li>
</ol>
<ul>
	<li>Operating System logs</li>
	<li>Database logs</li>
	<li>Network logs</li>
	<li>Application logs</li>
	<li>Batch Execution logs</li>
	<li>Configuration files</li>
	<li>Performance data (iostat, vmstat, ps, etc.)</li>
</ul>
<p><u>References:</u></p>
<p><a href="http://dev.splunk.com/view/logging-best-practices/SP-CAAADP6" target="_blank" rel="noopener">http://dev.splunk.com/view/logging-best-practices/SP-CAAADP6</a></p>
<p><a href="https://journal.paul.querna.org/articles/2011/12/26/log-for-machines-in-json/" target="_blank" rel="noopener">https://journal.paul.querna.org/articles/2011/12/26/log-for-machines-in-json/</a></p>
<p><a href="https://en.wikipedia.org/wiki/Log4j" target="_blank" rel="noopener">https://en.wikipedia.org/wiki/Log4j</a></p>
<p><a href="http://www.tutorialspoint.com/log4j/log4j_logging_levels.htm" target="_blank" rel="noopener">http://www.tutorialspoint.com/log4j/log4j_logging_levels.htm</a></p>
<p><a href="http://arctecgroup.net/pdf/howtoapplogging.pdf" target="_blank" rel="noopener">http://arctecgroup.net/pdf/howtoapplogging.pdf</a></p>
<p><strong><u>JSON</u></strong></p>
<p>JSON is a lightweight data-interchange format. It is easy for humans to read and write. It is easy for machines to parse and generate.  JSON is an easier-to-use alternative to XML.  JSON is a text format that is completely language independent.</p>
<p>JSON is built on two structures:</p>
<ul>
	<li>A collection of name/value pairs. In various languages, this is realized as an object, record, struct, dictionary, hash table, keyed list, or associative array.</li>
	<li>An ordered list of values. In most languages, this is realized as an array, vector, list, or sequence.</li>
</ul>
<p>These are universal data structures. Virtually all modern programming languages support them in one form or another. It makes sense that a data format that is interchangeable with programming languages also be based on these structures.</p>
<p>JSON is much Like XML Because:</p>
<ul>
	<li>Both JSON and XML is "self-describing" (human readable)</li>
	<li>Both JSON and XML is hierarchical (values within values)</li>
	<li>Both JSON and XML can be parsed and used by lots of programming languages</li>
	<li>Both JSON and XML can be fetched with an XMLHttpRequest</li>
</ul>
<p>JSON is much Unlike XML Because:</p>
<ul>
	<li>JSON doesn't use end tag</li>
	<li>JSON is shorter</li>
	<li>JSON is quicker to read and write</li>
	<li>JSON can use arrays</li>
	<li>JSON is much easier to parse than XML</li>
</ul>
<p><u>References:</u></p>
<p><a href="http://www.json.org/" target="_blank" rel="noopener">http://www.json.org/</a></p>
<p><a href="http://www.w3schools.com/json/default.asp" target="_blank" rel="noopener">http://www.w3schools.com/json/default.asp</a></p>
<p><a href="http://programmers.stackexchange.com/questions/170522/logging-in-json-effect-on-performance" target="_blank" rel="noopener">http://programmers.stackexchange.com/questions/170522/logging-in-json-effect-on-performance</a></p>
