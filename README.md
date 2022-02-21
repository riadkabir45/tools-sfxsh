# Welp! Another useless tool



sfxsh tries to bring sfx to sh. Its almost independent. as it only needs busybox.
Accurate dependency is:
```
[
cpio
echo
find
grep
mkdir
rm
tail
touch
wc
```



## Manpage

```
Usage: sfxsh OPTION
Creates a script with files embedded.
  configure       Creates a workdir,
  build           Builds the workdir to script
```



### Configure

configure creates a workdir. The structure of workdir is:

```
workdir/
├── assets #Conatins files to be embeded. (!Folder supported with preserve attributes)
├── init #The Script to run when executed
└── out #The built scipt will be throwed here

```

### Build 

build will output the ready to run script in workdir/out/sfx

Beware! The script contains files embedded. So dont open in GUI editors or might crash

### Internal Function

Currently the script only supports one function which is `extract`

```
Usage: extract WHERE_TO_EXTRACT
Extracts the asset files from embedded structure to a file system.
```

