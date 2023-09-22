# FDSecurityAV

## WARNING
This software is released in <strong>beta-test</strong> and in <strong>unstable</strong> version. <strong>I DECLINE ALL RESPONSIBILITY about damage and corruption of your files</strong>.

I have released my Antimalware software based on Yara Rules, with yara scanner. Download the <a href="https://github.com/FabioDefilippo/fdsecurity/blob/main/FDSecurityAV/FDSecurityAV-v1.3.2.0-FULL-PACKAGE.zip">zip</a> file, decompress it and run the executable. This software will scan files and Processes to find evidence of malware.
### REMEMBER:
I update occasionally FDSecurityAV-update, so check new versions in name of zip file!

### WARNING:
if You must install net core runtime, please follow this <a href="https://github.com/FabioDefilippo/fdsecurity/blob/main/FDSecurityAV/runtime-desktop-6.0.21-windows-x64-installer">link</a>

<strong>Accepting the EULA, You will agree to use the software without my having any responsibility!</strong>

## What is FDSecurityAV?

It's a SPERIMENTAL Antimalware with many features!

1. The Yara scanner to scan Processes and Files;
2. A Sandbox to test suspicious files;
3. A detailed scan for single files;
4. A Web browser to navigate to NoMoreRanson siteweb to recovery your encrypted files;
5. A fast scan mode to have quickly results;
6. A File Watcher to monitor UserProfile Folder and Subdirectories;
7. A feature for filtering file extensions;

## How to use it?

Run the FDSecurityAV software and accept the EULA. Click yes to download database of signatures (malware.yarac file). Now, FDSecurityAV run and scan every Porcesses in your Windows Machine automatically. You can even control Downloads folder repeatly or scan a single folder.
Click the buttons to stop scanners when You want.

Q: May I add custom rules?

A: Yes! Use the compiler yarac64.exe in FDSecurityAV folder, download or create your rules and compile them in a single file called malware.yarac ! Move your malware.yarac file (with your compiled rules) in Rules folder, then run FDSecurityAV! The software will use your custom rules!

Command-line:
```
yarac64.exe .\NEW-YARA-RULE.yara .\Rules\malware.yarac
```

## Sandbox:

I have added a Sandbox to test suspicious files!
