# Hades-Research

## Basic Static Analysis

### Hashing
File name: Malware.unknown.exe.malz

SHA256: 92730427321a1c4ccfc0d0580834daef98121efa9bb8963da332bfd6cf1f 
MD5: 1d8562c0adcaee734d63f7baaca02f7c

### Strings [Using Floss] :

```
FLOSS static Unicode strings
jjjj
cmd.exe /C ping 1.1.1.1 -n 1 -w 3000 > Nul & Del /f /q "%s"
 #http://ssl-6582datamanager.helpdeskbros.local/favicon.ico
C:\Users\Public\Documents\CR433101.dat.exe
Mozilla/5.0
 #http://huskyhacks.dev
cmd.exe /C ping 1.1.1.1 -n 1 -w 3000 > Nul & Del /f/q "%s" 
C:\Users\Public\Documents\CR433101.dat.exe
open
FLOSS decoded 0 strings
FLOSS extracted 2 stackstrings
<2_/
ineIGenu
```

### PEview:

- SECTION HEADER
	- Header![[Pasted image 20240516190445.png]]
-  winAPI : PEview and PEStudio
	- DownloadFromURL
	- InternetOpenURLA
	- ShellExec



