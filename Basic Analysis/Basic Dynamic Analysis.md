AKA Heuristic/Behavioural Analysis of [[Basic Dynamic Analysis]]
File name: Dropper.DownloadfromURL.exe
### Network artifacts
- URI![[Pasted image 20240528203001.png]]

### Host based Indicators
-  Procmon: Write file
	![[Pasted image 20240528204750.png]]
-  Procmon: Malware logical flow
	![[Pasted image 20240528210853.png]]
- Program Execution
	- If URL exists:
		- Download favicon.ico
		- Writes to disk (CR433101.dat.exe)
		- Run favicon.ico(CR433101.dat.exe)
	- If URL doesn't exist:
		- Delete from disk
		- Do not Run
