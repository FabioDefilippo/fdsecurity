# fdsecurity
This tool analizes a file o many files inside directory with yara and capa to find suspected file, without delete it.

## HOW TO USE IT:

fdsecurity.exe (file | folder) {-d}

-h --help /?&#9;&#9;show manual

-d --delete&#9;&#9;automatic zipping dangerous file in quarantine.zip

-u --update&#9;&#9;update capa, yara and yara-rules

-l --loop&#9;&#9;scan folder in loop

### examples:
1. Single file:
- to analize it, digit
```
.\fdsexurity.exe suspectedfile.exe
```
- to analize and zip it in quarantine.zip, digit
```
.\fdsexurity.exe suspectedfile.exe -d
```
- scanning folder in loop and delete dangerous files
```
.\fdsexurity.exe suspectedfolder -d -l
```
- update capa, yara and yara-rules
```
.\fdsexurity.exe -u
```

2. Many file inside folder:
- to analize them, digit
```
.\fdsecurity.exe C:\Users\Account\Download
```
- to analize and zip them, digit
```
.\fdsecurity.exe C:\Users\Account\Download -d
```

## NOTE:
This tool will:
1. create a folder inside Documents folder (if not exists);
2. download the last version of capa and yara and unzip them (if not exist);
3. download Yara rules (if not exist);
4. create a config file to customize some parameters (experimental);
5. scan file or files;

This tool will ZIP only dangerous file, but be carefull when You use it.

<strong>REMEMBER</strong>: You can recover your dangerous files unzipping them from quarantine.zip file.

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

<img crossorigin="anonymous" src="https://cdn.cms-twdigitalassets.com/content/dam/developer-twitter/images/Twitter_logo_blue_32.png"></img>: <a href="https://twitter.com/fabio_defilippo">@fabio_defilippo</a>

<img crossorigin="anonymous" src="https://www.paypalobjects.com/digitalassets/c/website/marketing/na/us/logo-center/Badge_1.png" width="30" height="30"></img>: If you want, you could <a href="https://www.paypal.com/donate?hosted_button_id=559D4CJB84KQJ">buy me a ☕</a>
