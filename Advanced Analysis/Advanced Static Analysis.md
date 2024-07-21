### Disassembly using cutter

1. Using cutter as the decompiler/disassembler we gain the main() controller code of the malware 
	1. Main function logic flow ![[Pasted image 20240609184240.png]]
	2. Graphical representation of code flow ![[Pasted image 20240609184421.png]]
2. Comparison with strings results
	1. Strings discovered in the disassembler ![[Pasted image 20240609184751.png]]
	2. Strings (contd.) ![[Pasted image 20240609184909.png]]
3. Comparison with URL results from basic dynamic analysis results
	![[Pasted image 20240609185326.png]]
4. Comparing Function Calls
	1. The main functions called includes APIs InternetOpenW, URLDownloadToFileW
		![[Pasted image 20240611201340.png]]
```C++
HINTERNET InternetOpenW(
  [in] LPCWSTR lpszAgent,
  [in] DWORD   dwAccessType,
  [in] LPCWSTR lpszProxy,
  [in] LPCWSTR lpszProxyBypass,
  [in] DWORD   dwFlags
);

HRESULT URLDownloadToFile(
             LPUNKNOWN            pCaller,
             LPCTSTR              szURL,
             LPCTSTR              szFileName,
  _Reserved_ DWORD                dwReserved,
             LPBINDSTATUSCALLBACK lpfnCB
);
```

### Stage0

#### Basic Static IOCs
- Indicators showcasing the file contains another file and exposes local storage ![[Pasted image 20240611203507.png]]
- Some possible files it may write ![[Pasted image 20240611203712.png]]
-  The creates and terminates processes multiple times (possibly multiple processes) and writes file ![[Pasted image 20240611203859.png]]
- Path where the file is dropped ![[Pasted image 20240611204303.png]]

#### Basic Dynamic IOCs
- The exe opens connection as follows:![[Pasted image 20240611205139.png]]
- The process it emulates {WerFault}: ![[Pasted image 20240611205427.png]]

#### Advanced Static Analysis: werflt.exe
- Defines 