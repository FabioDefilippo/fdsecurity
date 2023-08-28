# Yara Rules Compiled

## Do you want to scan every files, folder and PID in your Windows OS with a scanner who you could control and improve?

Well, I have compiled yara rules for this reason and I will write how to use yara cli to scan!

### WARNING: to avoid problems with syntax errors, I have change the extension of compiled yara rules in yarac.

## How to use them?

Easy!
- Download yara from GitHub <a href="https://github.com/VirusTotal/yara/releases">link</a>;
- Download these compiled yara rules and paste them in a Folder;
- Use one of these examples under!

## SCAN WITH ALL RULES:
In these 3 examples, I will show how to scan a folder, a Process and an exe file with all compiled yara rules, but can specify a single rule!

1. To scan a folder recursively:
```
yara64.exe -r -C .\Yara-Rules-Compiled\all.yarac FOLDER_TO_SCAN\
```

2. To scan a single file:
```
yara64.exe -C .\Yara-Rules-Compiled\all.yarac FILE_TO_SCAN.exe
```

3. To scan a process (Process ID):
```
yara64.exe -C .\Yara-Rules-Compiled\all.yarac PID
```
## CAN YOU ADD NEW YARA RULES?

Yes, add your compiled yara rules (for better performance) in Yara-Rules-Compiled folder and digit the follow command line:

```
yara64.exe -C .\Yara-Rules-Compiled\NEW-YARA-RULE.yarac FILE_TO_SCAN_exe
```

## Add scanning feature in Context Menu in Windows:

### WARNING: these steps must be executed by an expert and after a backup of your Registry!

In this example, We will suppose You have yara cli in C:\Users\James path, in a specific folder called 'yara-cli'.

1. Open cmd with administrator right and digit these commands:

```
reg add HKCR\*\shell\fdsecurity /ve /t REG_SZ /d "Scan with FDSecurity" && reg add HKCR\*\shell\fdsecurity\command /ve /t REG_SZ /d "C:\Users\James\yara-cli\yara-scan.bat %1"
```

2. Now create a file batch in 'C:\Users\James\yara-cli' path with notepad and digit:

```
C:\Users\James\yara-cli\yara\yara64.exe -c -C C:\Users\James\yara-cli\COMPILED-YARA-RULES\malware.yarac %1 && pause
```

You will have your scanning in Context Menu! When You will download a suspicious file, click on it with right button of Your mouse and then click with left button in 'Scan with FDSecurity'!
