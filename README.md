# fdsecurity
this tool analize a file o many files inside directory with yara and capa to find suspected file

## HOW TO USE IT:

- to analize a single file, digit
```
.\fdsexurity.exe suspectedfile.exe
```

- to analize many files inside a folder, digit
```
.\fdsecurity.exe C:\Users\Account\Download
```

## NOTE:
This tool will:
1. create a folder inside Documents folder (if not exists);
2. download the last version of capa and yara and unzip them (if not exist);
3. create a config file to customize some parameters (experimental);
4. scan file or files;

This tool will not modify o delete any file, but be carefull when You use it.

## CONFIG FILE:
