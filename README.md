# FDSecurity

## Welcome to the Official FDSecurityAV repository! If you want download FDSecurityAV software, click <a href="https://github.com/FabioDefilippo/fdsecurity/tree/main/FDSecurityAV">here</a> and download Download the <a href="https://github.com/FabioDefilippo/fdsecurity/blob/main/FDSecurityAV/FDSecurityAV-v1.3.2.0-FULL-PACKAGE.zip">zip</a> file!

### Click <a href="https://www.youtube.com/watch?v=-Bzcot3mmYI&pp=ygUKZmRzZWN1cml0eQ%3D%3D">here</a> to view the Instructions (Italian language)!

</hr>

## This repo also contains IoC values and Compiled Yara Rules!

<strong>Q:</strong> What are these XML files?

<strong>A:</strong> These are a collection of SHA256 checksum of many malwares for Windows in many file extensions. You could use them to create softwares, applications or projects.

Extensions: bat, cmd, dll, doc, docm, exe, hta, js, pdf, rar, rtf, vbe, vbs, xls, xlsm, zip

<strong>Q:</strong> How can I use these checksum values?

<strong>A:</strong> You can create your scripts o tools that use SHA256 Hash algorithm to calculate suspicious files in your computer.

<strong>Q:</strong> How can I calculate SHA256 checksum of a file?

<strong>A:</strong> digit this powershell commandlet!

NOTE: in this example, I will calculate SHA256 (the default algorithm) checksum of a file with exe extension, in List format:

```
Get-FileHash FILE_TO_CHECK.exe | Format-List
```
if SHA256 was not the default algorithm, digit:

```
Get-FileHash FILE_TO_CHECK.exe -Algorithm SHA256 | Format-List
```

## WARNING:

You could help me pulling missed SHA256 checksum values with tags!

### How?

EASY! Make a pull request! I will check if your checksum is right and I will add the new checksum in xml file!

<strong>Q:</strong> What are these Yara Rules?

<strong>A:</strong> These are Compiled Yara Rules. You can use them with yara cli to perform scanning in folders, a file o a process in your Windows OS.

<strong>Q:</strong> How?

<strong>A:</strong> Follow the instruction inside README.md file in Yara-Rules-Compiled folder!
