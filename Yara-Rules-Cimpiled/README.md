## Yara Rules Compiled

# Do you want to scan every files, folder and PID in your Windows OS with a scanner who you could control and improve?

Well, I have compiled yara rules for this reason and I will write ho to use yara cli to scan!

# SCAN WITH ALL RULES:
In these 3 examples, I will show ho to scan an exe file with all rules compiled, but can specify a single rule!

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
yara64.exe -C .\Yara-Rules-Compiled\all.yarac 1234
```
# CAN YOU ADD NEW YARA RULES?

Yes, add your compiled yara rules (for better performance) in Yara-Rules-Compiled and write the command line

```
yara64.exe -C .\Yara-Rules-Compiled\new-yara-rules.yarac FILE_TO_SCAN_exe
