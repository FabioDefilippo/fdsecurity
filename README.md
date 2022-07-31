# fdsecurity
this tool analizes a file o many files inside directory with yara and capa to find suspected file

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
3. download Yara rules (if not exist);
4. create a config file to customize some parameters (experimental);
5. scan file or files;

This tool will not modify o delete any file, but be carefull when You use it.

## CONFIG FILE:
there are some parameters,
- <strong>warning</strong>, a numeric parameter to evaluate the score of a suspected file, if the score is less than <strong>warning</strong> value, that file is safe (<strong>warning</strong> has a default value);
- <strong>dangerous</strong>, another numeric parameter to evaluate the score of the suspected file, if the score is equal or greater than <strong>dangerous</strong> value, the suspected file is <strong>dangerous</strong> (<strong>dangerous</strong> has a default value);
- <strong>extensions</strong>, this string value contains the <strong>extensions</strong> of every files you could analize inside a folder (<strong>extensions</strong> has a default value);

This is the default config file inside fdsecurity folder, in Documents path:
fdsecurity.config
```
warning=50
dangerous=100
extensions=*.exe|*.dll|*.doc|*.docm|*.xlsm|*.xls
```
