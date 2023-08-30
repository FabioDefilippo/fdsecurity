# fdsecurity

## These are IoC values!

Q: What are these XML files?

A: These are a collection of SHA256 checksum of many malwares for Windows in many file extensions. You could use them to create softwares, applications or projects.

Extensions: bat, cmd, dll, doc, docm, exe, hta, js, pdf, rar, rtf, vbe, vbs, xls, xlsm, zip

Q: How can I use these checksum values?

A: You can create your scripts o tools that use SHA256 Hash algorithm to calculate suspicious files in your computer.

Q: How can I calculate SHA256 checksum of a file?

A: digit this powershell commandlet!

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

Q: What are these Yara Rules?

A: These are Compiled Yara Rules. You can use them with yara cli to perform scanning in folders, a file o a process in your Windows OS.

Q: How?

A: Follow the instruction inside README.md file in Yara-Rules-Compiled folder!
