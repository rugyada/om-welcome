# om-welcome

Designed to introduce new users to OM distro and
also integrate common tasks for post-installation distro.


### Running OM-Welcome
Run om-welcome for debugging with following command:
```sh
$ htmlscript -s 1020x600 -i /usr/share/icons/openmandriva.svg index.sh.htm
```

##### translations
* inside the folder ```usr/share/om-welcome/ ```
* there is a file called translation, all texts om-welcome are it is from it that will 
* generate the translation files
* format it is as follows
```variavel=$"text that will be shown in the om-welcome"```

with the command
```sh
bash --dump-po-strings translation > om-welcome.pot
```

om-welcome.pot is the translation file.

To execute a command within the html files (sh.htm) using the following command:
```sh
$(command to be executed)
```

example: 
```
     $(lsb_release -d | cut -d":" -f2) #shows the name of the Linux distribution
```      

