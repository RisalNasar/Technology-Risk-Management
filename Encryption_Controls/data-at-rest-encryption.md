# Encryption of Data-At-Rest
<p> <strong><u>Approaches for Encryption of Data-At-Rest</u></strong></p>
<ul>
	<li>Application Encryption</li>
	<li>Disk Encryption</li>
	<li>Database Encryption</li>
</ul>
<p><strong><u>Application Encryption</u></strong></p>
<p>You can task a given application with encrypting its own data. This encryption capability is designed into the application itself, and organizations will not have to add another solution for encrypting data across the network. By the time the database receives the data, it has already been encrypted and then stored in the database in this encrypted state.</p>
<p>The solution can be implemented at the application layer or the database layer via an API.</p>
<p>A benefit to application encryption is that the data is only accessible to authenticated, authorized application users. If an attacker, whether an insider or outsider, tried to access the data directly within the database without going through the application, the data would be encrypted and inaccessible.</p>
<p>The disadvantages to application encryption include:</p>
<ol>
	<li>Significant changes required in the application and/or database layer: First, to implement application encryption you must make significant changes in both the application layer and the database layer. Applications accessing the data need to be modified to understand and implement encryption. This could mean changing literally hundreds of applications for some organizations. In addition, the database tables and views that reside in the database and support the application need to be changed because the values being stored will no longer match the external data type representation. For example, a nine-digit SSN could not be encrypted and stored in the same field or data type that was originally used to store the unencrypted SSN. Complicating the situation further is the fact that many organizations do not even know all the applications that may be accessing the data. Some applications, such as legacy applications, may also make it extremely difficult, if not impossible, to implement this solution.</li>
	<li>Database performance issues: Second, database performance issues may arise because external applications control the encrypted data within the database. For example, if the application layer is doing the encryption, indexes and search capabilities within the database will not work. Alternatively, a database layer encryption solution can be implemented using an API, but that requires applicable triggers and views, which also introduce additional overhead, thus affecting database performance.</li>
	<li>Difficult Key Management: Finally, consider key management. Because multiple applications may be doing the encryption then sending to the database, keys are stored in many locations, introducing additional exposure points. When it is time to change the key, this may mean decrypting all the data with the old key and re-encrypting all the data with the new key—a significant impact to the environment.</li>
</ol>
<p><strong><u>Disk Encryption</u></strong></p>
<p>Typically, disk encryption requires operating system support hooks to encrypt database files or the media on which the files reside. In these cases, keys typically must be managed by system or storage administrators. With file and disk encryption, there is no need to change the application(s) to accommodate encryption to the database with application encryption. In addition, file/disk encryption is a concept that organizations tend to be familiar with because it is similar to laptop encryption that many organizations have already implemented.</p>
<p>Because the encryption is occurring at the file or disk level, everyone with access to the operating system typically has access to all the data encrypted on that system.</p>
<p><strong><u>Database Encryption</u></strong></p>
<p>Database encryption falls somewhere between application encryption and disk encryption.</p>
<p>With Transparent Database Encryption (TDE), the encryption process and associated encryption keys are created and managed by the database. This is transparent to database users who have authenticated to the database. At the operating system, however, attempts to access database files return data in an encrypted state. Therefore, for any operating system level users, the data remains inaccessible. Additionally, because the database is doing the encryption, there is no need to change the application(s), and there is a minimal performance overhead when changes occur in the database.</p>
<p>A disadvantage to TDE is that the data is not protected from authenticated, authorized database users, including the DBA.</p>
<p><strong><u>Encryption Approaches - Software Encryption vs Hardware (Appliance Based) Encryption</u></strong></p>
<p>Hardware based encryption is deemed faster and more efficient than Software based encryption as dedicated hardware components are used for the heavy data crunching instead of precious CPU cycles.</p>
<p><u>References:</u></p>
<p><a href="https://www.sans.org/reading-room/whitepapers/analyst/transparent-data-encryption-technologies-practices-database-encryption-34915" target="_blank" rel="noopener">https://www.sans.org/reading-room/whitepapers/analyst/transparent-data-encryption-technologies-practices-database-encryption-34915</a></p>
<p><a href="http://searchstorage.techtarget.com/What-you-need-to-know-about-storage-encryption-products" target="_blank" rel="noopener">http://searchstorage.techtarget.com/What-you-need-to-know-about-storage-encryption-products</a></p>
<p><a href="http://www.computerweekly.com/feature/Encryption-techniques-and-products-for-hardware-based-data-storage-security" target="_blank" rel="noopener">http://www.computerweekly.com/feature/Encryption-techniques-and-products-for-hardware-based-data-storage-security</a></p>
<p>&nbsp;</p>
