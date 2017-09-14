# Personal Password Management Guideline

<p>In today’s world, each individual needs to remember many passwords.  There is a password for the Windows network logon, e-mail accounts, online passwords (like website member account), SFTP passwords, etc. The list is endless. 

<p>For true security, one should use different passwords for different accounts.  Because if the same password is used everywhere, and if that password gets leaked due to a hack on one of the accounts, all your accounts become exposed!!! The attacker would have access to your e-mail accounts, websites, bank accounts, etc!!!

<p>People in today’s workplace resort to store their passwords in text files or excel files.  They assume that if ‘only they know the specific file’ in which passwords are kept, then the passwords will be safe.  However, Security experts advise that ‘Security through Obscurity’ is not a good Security Principle.

<p>Microsoft Excel do offer the ability to encrypt the document.  However, Excel encryption is deemed weak (version dependent).  Also, Excel is not custom made to support the features that a full-fledged Password Manager should offer.

<h2>KeePass Password Manager</h2>

<p>KeePass is a free open source password manager, which helps to manage passwords in a secure way.  It allows to put all your passwords in one database, which is locked with one master key and/or a key file.  So you only have to remember one single master password or select the key file to unlock the whole database.  The databases are encrypted using the best and most secure encryption algorithms currently known (AES and Twofish).

<p>Main advantages of KeePass are:
<ul>
	<li>Database is encrypted with industry leading encryption algorithms.</li>
	<li>Provides option for Multiple-factor authentication (supports Key file and Windows User Account Validation, on top of Master Password).</li>
	<li>Contains a Password Generation Mechanism which allows the generation of high entropy passwords from the chosen criteria.</li>
	<li>Passwords can be organized into Groups.  Supports better organization of data.</li>
	<li>Passwords are masked out, even when the application is open and unlocked.  Supports copying to clipboard without viewing the password.</li>
	<li>The KeePass application is cross-platform and is available in Windows and Linux.</li>
</ul>
For a full feature list, please see: <a href="http://keepass.info/features.html">http://keepass.info/features.html</a> and <a href="http://keepass.info/compare.html">http://keepass.info/compare.html</a>

<h2>KeePass Download</h2>

<p><a href="http://keepass.info/download.html">http://keepass.info/download.html</a>

<p> Download the <b>Portable Professional Edition</b> of KeyPass.  After downloading the zip file, please unpack to a location of your preference.

<h2>Creation of New Database</h2>

<p>Open File -> New.

![create](https://user-images.githubusercontent.com/15157883/30432761-24df9a76-9995-11e7-832f-81803edb3a02.jpg)

<p>Choose Folder Location where the new database should be stored.  Provide a name for the database and click  ‘Save’.

![choose folder](https://user-images.githubusercontent.com/15157883/30432802-4155f66e-9995-11e7-81ea-0f5c88269859.jpg)

<p>You may either create a Password Database for Personal Use or for Shared Use.  Below are the recommended authentication controls for each use case, respectively.

<ul>
	<li>For Personal Password Safe creation: </li>
</ul>

<p>Please enter a Master Password and select on ‘Windows user account’ option.  This ensures that only you, as the current Windows User, along with the pre-set master password can open the database.  Click ‘OK’.  Follow next steps.

![composite master key](https://user-images.githubusercontent.com/15157883/30432879-898aeb60-9995-11e7-9c35-2a9bc09c8f75.jpg)

<p>Enter Database Details and click ‘OK’.

![test-personal-db](https://user-images.githubusercontent.com/15157883/30432918-ae1aca9a-9995-11e7-934e-5a4637cee889.jpg)

<ul>
	<li>For a Shared Password Safe Creation (example – to be shared between team members):</li>
</ul>

<p>Create a Master password and a Key file.  (Do not tick on ‘Windows user account’ option).  Tick on ‘Key file / provider’ option and click ‘Create’.  

![composite master key](https://user-images.githubusercontent.com/15157883/30432960-d0b6e246-9995-11e7-9ec0-d74174f00aa1.jpg)

<p>Locate folder where database should be stored.  Give a name to the database.  Click ‘Save’.

![locate folder](https://user-images.githubusercontent.com/15157883/30433005-edb7e9e4-9995-11e7-8f0c-8ef460cc6acd.jpg)


<p> In order to generate randomness to be used for the underlying encryption, move your mouse randomly in the shown area until 256 bits are generated.  Also, feed in random keyboard input to the text area.

![randomness](https://user-images.githubusercontent.com/15157883/30433058-0fb8aee8-9996-11e7-9521-901b747b2c15.jpg)







