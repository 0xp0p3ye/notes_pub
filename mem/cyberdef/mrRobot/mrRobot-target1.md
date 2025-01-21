

## Findings:

process of interest 



## proc:


```

Volatility 3 Framework 2.8.0

PID	PPID	ImageFileName	Offset(V)	Threads	Handles	SessionId	Wow64	CreateTime	ExitTime	Audit	Cmd	Path

4	0	System	0x83d334e8	94	500	N/A	False	2015-10-09 11:30:44.000000 UTC	N/A	-	-	-
* 276	4	smss.exe	0x84edcbf0	2	30	N/A	False	2015-10-09 11:30:44.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\smss.exe	\SystemRoot\System32\smss.exe	\SystemRoot\System32\smss.exe
368	360	csrss.exe	0x84ecbb18	9	366	0	False	2015-10-09 11:30:47.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\csrss.exe	%SystemRoot%\system32\csrss.exe ObjectDirectory=\Windows SharedSection=1024,12288,512 Windows=On SubSystemType=Windows ServerDll=basesrv,1 ServerDll=winsrv:UserServerDllInitialization,3 ServerDll=winsrv:ConServerDllInitialization,2 ServerDll=sxssrv,4 ProfileControl=Off MaxRequestThreads=16	C:\Windows\system32\csrss.exe
420	360	wininit.exe	0x84f97628	3	77	0	False	2015-10-09 11:30:48.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\wininit.exe	wininit.exe	C:\Windows\system32\wininit.exe
* 528	420	services.exe	0x84e979f8	9	200	0	False	2015-10-09 11:30:48.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\services.exe	C:\Windows\system32\services.exe	C:\Windows\system32\services.exe
** 864	528	svchost.exe	0x85978940	30	1036	0	False	2015-10-09 11:30:52.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\system32\svchost.exe -k netsvcs	C:\Windows\system32\svchost.exe
** 1888	528	dllhost.exe	0x85ae0cb0	13	196	0	False	2015-10-09 11:30:54.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\dllhost.exe	C:\Windows\system32\dllhost.exe /Processid:{02D4B3F1-FD88-11D1-960D-00805FC79235}	C:\Windows\system32\dllhost.exe
** 3232	528	svchost.exe	0x85d01510	9	131	0	False	2015-10-09 11:31:34.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\system32\svchost.exe -k LocalServiceAndNoImpersonation	C:\Windows\system32\svchost.exe
** 644	528	svchost.exe	0x8586fd40	11	351	0	False	2015-10-09 11:30:48.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\system32\svchost.exe -k DcomLaunch	C:\Windows\system32\svchost.exe
** 836	528	svchost.exe	0x85969030	17	405	0	False	2015-10-09 11:30:52.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\System32\svchost.exe -k LocalSystemNetworkRestricted	C:\Windows\System32\svchost.exe
*** 2088	836	dwm.exe	0x85c09968	3	93	1	False	2015-10-09 11:31:04.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\dwm.exe	"C:\Windows\system32\Dwm.exe"	C:\Windows\system32\Dwm.exe
** 1124	528	svchost.exe	0x85a138f0	16	484	0	False	2015-10-09 11:30:53.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\system32\svchost.exe -k NetworkService	C:\Windows\system32\svchost.exe
** 3900	528	sppsvc.exe	0x85b43a58	4	153	0	False	2015-10-09 11:32:54.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\sppsvc.exe	C:\Windows\system32\sppsvc.exe	C:\Windows\system32\sppsvc.exe
** 1256	528	svchost.exe	0x85a55d40	17	304	0	False	2015-10-09 11:30:53.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\system32\svchost.exe -k LocalServiceNoNetwork	C:\Windows\system32\svchost.exe
** 1980	528	msdtc.exe	0x858b69e8	12	145	0	False	2015-10-09 11:30:55.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\msdtc.exe	C:\Windows\System32\msdtc.exe	C:\Windows\System32\msdtc.exe
** 1228	528	spoolsv.exe	0x8582c8d8	12	273	0	False	2015-10-09 11:30:53.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\spoolsv.exe	C:\Windows\System32\spoolsv.exe	C:\Windows\System32\spoolsv.exe
** 2252	528	taskhost.exe	0x85c39030	7	150	1	False	2015-10-09 11:31:04.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\taskhost.exe	"taskhost.exe"	C:\Windows\system32\taskhost.exe
** 720	528	svchost.exe	0x84e01448	6	276	0	False	2015-10-09 11:30:50.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\system32\svchost.exe -k RPCSS	C:\Windows\system32\svchost.exe
** 1008	528	svchost.exe	0x859cc2c0	13	650	0	False	2015-10-09 11:30:52.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\system32\svchost.exe -k LocalService	C:\Windows\system32\svchost.exe
** 1784	528	svchost.exe	0x85976318	5	99	0	False	2015-10-09 11:30:54.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\system32\svchost.exe -k NetworkServiceNetworkRestricted	C:\Windows\system32\svchost.exe
** 2544	528	SearchIndexer.	0x8598c920	13	670	0	False	2015-10-09 11:31:10.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\SearchIndexer.exe	C:\Windows\system32\SearchIndexer.exe /Embedding	C:\Windows\system32\SearchIndexer.exe
** 1432	528	vmtoolsd.exe	0x85ae3030	8	274	0	False	2015-10-09 11:30:54.000000 UTC	N/A	\Device\HarddiskVolume2\Program Files\VMware\VMware Tools\vmtoolsd.exe	"C:\Program Files\VMware\VMware Tools\vmtoolsd.exe"	C:\Program Files\VMware\VMware Tools\vmtoolsd.exe
** 796	528	svchost.exe	0x85935030	19	446	0	False	2015-10-09 11:30:51.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\System32\svchost.exe -k LocalServiceNetworkRestricted	C:\Windows\System32\svchost.exe
* 536	420	lsass.exe	0x8583b030	9	851	0	False	2015-10-09 11:30:48.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\lsass.exe	C:\Windows\system32\lsass.exe	C:\Windows\system32\lsass.exe
* 544	420	lsm.exe	0x8583d960	10	163	0	False	2015-10-09 11:30:48.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\lsm.exe	C:\Windows\system32\lsm.exe	C:\Windows\system32\lsm.exe
432	412	csrss.exe	0x855f6d40	11	366	1	False	2015-10-09 11:30:48.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\csrss.exe	%SystemRoot%\system32\csrss.exe ObjectDirectory=\Windows SharedSection=1024,12288,512 Windows=On SubSystemType=Windows ServerDll=basesrv,1 ServerDll=winsrv:UserServerDllInitialization,3 ServerDll=winsrv:ConServerDllInitialization,2 ServerDll=sxssrv,4 ProfileControl=Off MaxRequestThreads=16	C:\Windows\system32\csrss.exe
* 1624	432	conhost.exe	0x83f13d40	3	81	1	False	2015-10-09 11:35:15.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\conhost.exe	\??\C:\Windows\system32\conhost.exe	C:\Windows\system32\conhost.exe
* 676	432	conhost.exe	0x83fa9030	3	83	1	False	2015-10-09 11:37:32.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\conhost.exe	\??\C:\Windows\system32\conhost.exe	C:\Windows\system32\conhost.exe
* 916	432	conhost.exe	0x83e5cd40	3	83	1	False	2015-10-09 11:33:42.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\conhost.exe	\??\C:\Windows\system32\conhost.exe	C:\Windows\system32\conhost.exe
* 1824	432	conhost.exe	0x83fc7c08	3	85	1	False	2015-10-09 11:39:22.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\conhost.exe	\??\C:\Windows\system32\conhost.exe	C:\Windows\system32\conhost.exe
480	412	winlogon.exe	0x8561d030	3	115	1	False	2015-10-09 11:30:48.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\winlogon.exe	winlogon.exe	C:\Windows\system32\winlogon.exe
2116	2060	explorer.exe	0x85c1e5f8	23	912	1	False	2015-10-09 11:31:04.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\explorer.exe	C:\Windows\Explorer.EXE	C:\Windows\Explorer.EXE
* 2496	2116	cmd.exe	0x83eb5d40	1	22	1	False	2015-10-09 11:33:42.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\cmd.exe	"C:\Windows\System32\cmd.exe" 	C:\Windows\System32\cmd.exe
* 2844	2116	mstsc.exe	0x83f1ed40	11	484	1	False	2015-10-09 12:12:03.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\mstsc.exe	"C:\Windows\system32\mstsc.exe" 	C:\Windows\system32\mstsc.exe
* 2388	2116	vmtoolsd.exe	0x859281f0	7	164	1	False	2015-10-09 11:31:04.000000 UTC	N/A	\Device\HarddiskVolume2\Program Files\VMware\VMware Tools\vmtoolsd.exe	"C:\Program Files\VMware\VMware Tools\vmtoolsd.exe" -n vmusr	C:\Program Files\VMware\VMware Tools\vmtoolsd.exe
* 3064	2116	cmd.exe	0x83fb86a8	1	22	1	False	2015-10-09 11:37:32.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\cmd.exe	"C:\Windows\System32\cmd.exe" 	C:\Windows\System32\cmd.exe
* 3196	2116	OUTLOOK.EXE	0x85cd3d40	22	1678	1	False	2015-10-09 11:31:32.000000 UTC	N/A	\Device\HarddiskVolume2\Program Files\Microsoft Office\Office15\OUTLOOK.EXE	"C:\Program Files\Microsoft Office\Office15\OUTLOOK.EXE" 	C:\Program Files\Microsoft Office\Office15\OUTLOOK.EXE
2996	2984	iexplore.exe	0x85d0d030	6	463	1	False	2015-10-09 11:31:27.000000 UTC	N/A	\Device\HarddiskVolume2\Program Files\Internet Explorer\iexplore.exe	"C:\Program Files\Internet Explorer\iexplore.exe"	C:\Program Files\Internet Explorer\iexplore.exe
* 1856	2996	cmd.exe	0x83f105f0	1	33	1	False	2015-10-09 11:35:15.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\cmd.exe	C:\Windows\system32\cmd.exe	C:\Windows\system32\cmd.exe
3784	2196	cmd.exe	0x83fb2d40	1	24	1	False	2015-10-09 11:39:22.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\cmd.exe	cmd	C:\Windows\system32\cmd.exe
2680	1696	TeamViewer.exe	0x84013598	28	632	1	False	2015-10-09 12:08:46.000000 UTC	N/A	\Device\HarddiskVolume2\Users\FRONTD~1\AppData\Local\Temp\TeamViewer\TeamViewer.exe	"C:\Users\FRONTD~1\AppData\Local\Temp\TeamViewer\TeamViewer.exe" 	C:\Users\FRONTD~1\AppData\Local\Temp\TeamViewer\TeamViewer.exe
* 4064	2680	tv_w32.exe	0x84017d40	2	83	1	False	2015-10-09 12:08:47.000000 UTC	N/A	\Device\HarddiskVolume2\Users\FRONTD~1\AppData\Local\Temp\TeamViewer\tv_w32.exe	"C:\Users\FRONTD~1\AppData\Local\Temp\TeamViewer\tv_w32.exe" --action hooks  --log C:\Users\frontdesk\AppData\Roaming\TeamViewer\TeamViewer10_Logfile.log  	C:\Users\FRONTD~1\AppData\Local\Temp\TeamViewer\tv_w32.exe
* 1092	2680	TeamViewer_Des	0x858bc278	16	405	1	False	2015-10-09 12:10:56.000000 UTC	N/A	\Device\HarddiskVolume2\Users\FRONTD~1\AppData\Local\Temp\TeamViewer\TeamViewer_Desktop.exe	"c:\users\frontd~1\appdata\local\temp\teamviewer\TeamViewer_Desktop.exe" --IPCport 6039	c:\users\frontd~1\appdata\local\temp\teamviewer\TeamViewer_Desktop.exe

```




## files:



## srvc:

