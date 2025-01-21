

```
Volatility 3 Framework 2.8.0

PID	PPID	ImageFileName	Offset(V)	Threads	Handles	SessionId	Wow64	CreateTime	ExitTime	Audit	Cmd	Path

4	0	System	0xbb8ecca7b040	104	-	N/A	False	2024-12-11 19:54:49.000000 UTC	N/A	-	-	-
* 72	4	Registry	0xbb8eccbaa040	4	-	N/A	False	2024-12-11 19:54:48.000000 UTC	N/A	Registry	-	-
* 324	4	smss.exe	0xbb8ece911040	2	-	N/A	False	2024-12-11 19:54:49.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\smss.exe	\SystemRoot\System32\smss.exe	\SystemRoot\System32\smss.exe
* 1400	4	MemCompression	0xbb8ed3928040	38	-	N/A	False	2024-12-11 19:54:54.000000 UTC	N/A	MemCompression	-	-
424	412	csrss.exe	0xbb8ed04ce140	10	-	0	False	2024-12-11 19:54:53.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\csrss.exe	%SystemRoot%\system32\csrss.exe ObjectDirectory=\Windows SharedSection=1024,20480,768 Windows=On SubSystemType=Windows ServerDll=basesrv,1 ServerDll=winsrv:UserServerDllInitialization,3 ServerDll=sxssrv,4 ProfileControl=Off MaxRequestThreads=16	C:\Windows\system32\csrss.exe
492	412	wininit.exe	0xbb8ed01bb080	1	-	0	False	2024-12-11 19:54:53.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\wininit.exe	-	-
* 584	492	services.exe	0xbb8ed0e08080	8	-	0	False	2024-12-11 19:54:53.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\services.exe	C:\Windows\system32\services.exe	C:\Windows\system32\services.exe
** 1792	584	svchost.exe	0xbb8ed3aee2c0	16	-	0	False	2024-12-11 19:54:55.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\system32\svchost.exe -k LocalServiceNoNetworkFirewall -p	C:\Windows\system32\svchost.exe
** 384	584	svchost.exe	0xbb8ecec7f2c0	11	-	1	False	2024-12-11 19:56:25.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\system32\svchost.exe -k ClipboardSvcGroup -p	C:\Windows\system32\svchost.exe
** 256	584	MpDefenderCore	0xbb8ed4942080	10	-	0	False	2024-12-16 20:55:01.000000 UTC	N/A	\Device\HarddiskVolume2\ProgramData\Microsoft\Windows Defender\Platform\4.18.24090.11-0\MpDefenderCoreService.exe	"C:\ProgramData\Microsoft\Windows Defender\platform\4.18.24090.11-0\MpDefenderCoreService.exe"	C:\ProgramData\Microsoft\Windows Defender\platform\4.18.24090.11-0\MpDefenderCoreService.exe
** 5496	584	svchost.exe	0xbb8ed440d080	4	-	0	False	2024-12-11 20:11:11.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\system32\svchost.exe -k LocalService	C:\Windows\system32\svchost.exe
** 4360	584	svchost.exe	0xbb8ed4487080	4	-	0	False	2024-12-11 19:56:36.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\system32\svchost.exe -k wusvcs -p	C:\Windows\system32\svchost.exe
** 4744	584	svchost.exe	0xbb8ed4a432c0	8	-	0	False	2024-12-11 19:56:53.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\System32\svchost.exe -k LocalServiceNetworkRestricted -p	C:\Windows\System32\svchost.exe
** 3336	584	svchost.exe	0xbb8ece175080	31	-	0	False	2024-12-11 20:09:07.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	-	-
** 1164	584	svchost.exe	0xbb8ed38bc2c0	20	-	0	False	2024-12-11 19:54:54.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\System32\svchost.exe -k NetworkService -p	C:\Windows\System32\svchost.exe
** 1804	584	SearchIndexer.	0xbb8ece64a240	17	-	0	False	2024-12-11 19:56:26.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\SearchIndexer.exe	C:\Windows\system32\SearchIndexer.exe /Embedding	C:\Windows\system32\SearchIndexer.exe
*** 3864	1804	SearchProtocol	0xbb8ed42ca080	7	-	0	False	2024-12-17 10:41:09.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\SearchProtocolHost.exe	"C:\Windows\system32\SearchProtocolHost.exe" Global\UsGthrFltPipeMssGthrPipe21_ Global\UsGthrCtrlFltPipeMssGthrPipe21 1 -2147483646 "Software\Microsoft\Windows Search" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT; MS Search 4.0 Robot)" "C:\ProgramData\Microsoft\Search\Data\Temp\usgthrsvc" "DownLevelDaemon" 	C:\Windows\system32\SearchProtocolHost.exe
*** 2164	1804	SearchFilterHo	0xbb8ed65e7080	5	-	0	False	2024-12-17 10:41:09.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\SearchFilterHost.exe	"C:\Windows\system32\SearchFilterHost.exe" 0 796 800 808 8192 804 780 	C:\Windows\system32\SearchFilterHost.exe
** 2192	584	svchost.exe	0xbb8ed3dde2c0	6	-	0	False	2024-12-11 19:54:56.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\System32\svchost.exe -k LocalServiceNetworkRestricted	C:\Windows\System32\svchost.exe
** 1308	584	VBoxService.ex	0xbb8ecca74300	11	-	0	False	2024-12-11 19:54:54.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\VBoxService.exe	C:\Windows\System32\VBoxService.exe	C:\Windows\System32\VBoxService.exe
** 2168	584	TrustedInstall	0xbb8ed6360080	7	-	0	False	2024-12-17 10:38:34.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\servicing\TrustedInstaller.exe	C:\Windows\servicing\TrustedInstaller.exe	C:\Windows\servicing\TrustedInstaller.exe
** 676	584	svchost.exe	0xbb8ed383b2c0	13	-	0	False	2024-12-11 19:54:54.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\system32\svchost.exe -k LocalServiceNetworkRestricted -p	C:\Windows\system32\svchost.exe
** 804	584	svchost.exe	0xbb8ed385e2c0	30	-	0	False	2024-12-11 19:54:54.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\system32\svchost.exe -k LocalService -p	C:\Windows\system32\svchost.exe
** 808	584	svchost.exe	0xbb8ed0ebe2c0	13	-	0	False	2024-12-11 19:54:53.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\system32\svchost.exe -k RPCSS -p	C:\Windows\system32\svchost.exe
** 2380	584	MsMpEng.exe	0xbb8ed3f7f300	23	-	0	False	2024-12-16 20:54:55.000000 UTC	N/A	\Device\HarddiskVolume2\ProgramData\Microsoft\Windows Defender\Platform\4.18.24090.11-0\MsMpEng.exe	"C:\ProgramData\Microsoft\Windows Defender\platform\4.18.24090.11-0\MsMpEng.exe"	C:\ProgramData\Microsoft\Windows Defender\platform\4.18.24090.11-0\MsMpEng.exe
** 3796	584	svchost.exe	0xbb8ed6bf5080	4	-	0	False	2024-12-12 08:01:03.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\system32\svchost.exe -k WbioSvcGroup	C:\Windows\system32\svchost.exe
** 1624	584	svchost.exe	0xbb8ed39f02c0	4	-	0	False	2024-12-11 19:54:54.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\System32\svchost.exe -k LocalServiceNetworkRestricted -p	C:\Windows\System32\svchost.exe
** 1752	584	svchost.exe	0xbb8ed3ad72c0	3	-	0	False	2024-12-11 19:54:55.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\system32\svchost.exe -k LocalService -p	C:\Windows\system32\svchost.exe
** 728	584	svchost.exe	0xbb8ed0e9a240	16	-	0	False	2024-12-11 19:54:53.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\system32\svchost.exe -k DcomLaunch -p	C:\Windows\system32\svchost.exe
*** 6912	728	RuntimeBroker.	0xbb8ed4973080	2	-	1	False	2024-12-17 09:48:48.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\RuntimeBroker.exe	C:\Windows\System32\RuntimeBroker.exe -Embedding	C:\Windows\System32\RuntimeBroker.exe
*** 3088	728	smartscreen.ex	0xbb8ed4729080	11	-	1	False	2024-12-17 10:41:30.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\smartscreen.exe	C:\Windows\System32\smartscreen.exe -Embedding	C:\Windows\System32\smartscreen.exe
*** 2712	728	ShellExperienc	0xbb8ed4741080	14	-	1	False	2024-12-17 09:48:47.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\SystemApps\ShellExperienceHost_cw5n1h2txyewy\ShellExperienceHost.exe	-	-
*** 3100	728	TextInputHost.	0xbb8ed3b14080	11	-	1	False	2024-12-11 20:01:15.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\SystemApps\MicrosoftWindows.Client.CBS_cw5n1h2txyewy\TextInputHost.exe	"C:\Windows\SystemApps\MicrosoftWindows.Client.CBS_cw5n1h2txyewy\TextInputHost.exe" -ServerName:InputApp.AppXjd5de1g66v206tj52m9d0dtpppx4cgpn.mca	C:\Windows\SystemApps\MicrosoftWindows.Client.CBS_cw5n1h2txyewy\TextInputHost.exe
*** 2332	728	TiWorker.exe	0xbb8ed56c1080	7	-	0	False	2024-12-17 10:40:59.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\WinSxS\amd64_microsoft-windows-servicingstack_31bf3856ad364e35_10.0.19041.5071_none_7e3c4e707c6a2679\TiWorker.exe	C:\Windows\winsxs\amd64_microsoft-windows-servicingstack_31bf3856ad364e35_10.0.19041.5071_none_7e3c4e707c6a2679\TiWorker.exe -Embedding	C:\Windows\winsxs\amd64_microsoft-windows-servicingstack_31bf3856ad364e35_10.0.19041.5071_none_7e3c4e707c6a2679\TiWorker.exe
*** 3620	728	SearchApp.exe	0xbb8ed447c080	43	-	1	False	2024-12-11 19:56:28.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\SystemApps\Microsoft.Windows.Search_cw5n1h2txyewy\SearchApp.exe	"C:\Windows\SystemApps\Microsoft.Windows.Search_cw5n1h2txyewy\SearchApp.exe" -ServerName:CortanaUI.AppX8z9r6jm96hw4bsbneegw0kyxx296wr9t.mca	C:\Windows\SystemApps\Microsoft.Windows.Search_cw5n1h2txyewy\SearchApp.exe
*** 2988	728	dllhost.exe	0xbb8ed440c080	7	-	1	False	2024-12-11 19:59:57.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\dllhost.exe	C:\Windows\system32\DllHost.exe /Processid:{973D20D7-562D-44B9-B70B-5A0F49CCDF3F}	C:\Windows\system32\DllHost.exe
*** 3888	728	dllhost.exe	0xbb8ed60d4080	4	-	0	False	2024-12-16 20:55:02.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\dllhost.exe	C:\Windows\system32\DllHost.exe /Processid:{3EB3C877-1F16-487C-9050-104DBCD66683}	C:\Windows\system32\DllHost.exe
*** 3764	728	RuntimeBroker.	0xbb8ed45932c0	7	-	1	False	2024-12-11 19:56:29.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\RuntimeBroker.exe	C:\Windows\System32\RuntimeBroker.exe -Embedding	C:\Windows\System32\RuntimeBroker.exe
*** 3384	728	SearchApp.exe	0xbb8ed42cf080	32	-	1	False	2024-12-11 19:59:59.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\SystemApps\Microsoft.Windows.Search_cw5n1h2txyewy\SearchApp.exe	-	-
*** 3900	728	RuntimeBroker.	0xbb8ed5bcf080	12	-	1	False	2024-12-17 09:53:32.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\RuntimeBroker.exe	C:\Windows\System32\RuntimeBroker.exe -Embedding	C:\Windows\System32\RuntimeBroker.exe
*** 4284	728	HxTsr.exe	0xbb8ed69ed080	0	-	1	False	2024-12-11 20:15:30.000000 UTC	2024-12-11 20:15:48.000000 UTC	\Device\HarddiskVolume2\Program Files\WindowsApps\microsoft.windowscommunicationsapps_16005.11629.20316.0_x64__8wekyb3d8bbwe\HxTsr.exe	-	-
*** 3260	728	ApplicationFra	0xbb8ed075a080	6	-	1	False	2024-12-12 10:35:21.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\ApplicationFrameHost.exe	C:\Windows\system32\ApplicationFrameHost.exe -Embedding	C:\Windows\system32\ApplicationFrameHost.exe
*** 5056	728	RuntimeBroker.	0xbb8ed46cc2c0	1	-	1	False	2024-12-11 19:56:40.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\RuntimeBroker.exe	C:\Windows\System32\RuntimeBroker.exe -Embedding	C:\Windows\System32\RuntimeBroker.exe
*** 5832	728	GameBar.exe	0xbb8ed3f6c080	0	-	1	False	2024-12-16 20:10:36.000000 UTC	2024-12-16 20:20:48.000000 UTC	\Device\HarddiskVolume2\Program Files\WindowsApps\Microsoft.XboxGamingOverlay_7.224.11211.0_x64__8wekyb3d8bbwe\GameBar.exe	-	-
*** 6092	728	dllhost.exe	0xbb8ece4c6080	2	-	1	True	2024-12-12 10:35:40.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\SysWOW64\dllhost.exe	"C:\Windows\SysWOW64\DllHost.exe" /Processid:{776DBC8D-7347-478C-8D71-791E12EF49D8}	C:\Windows\SysWOW64\DllHost.exe
*** 3920	728	Microsoft.Phot	0xbb8ed66f2080	28	-	1	False	2024-12-17 09:53:31.000000 UTC	N/A	\Device\HarddiskVolume2\Program Files\WindowsApps\Microsoft.Windows.Photos_2019.19071.12548.0_x64__8wekyb3d8bbwe\Microsoft.Photos.exe	-	-
*** 3292	728	StartMenuExper	0xbb8ed42f8080	9	-	1	False	2024-12-11 19:56:27.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\SystemApps\Microsoft.Windows.StartMenuExperienceHost_cw5n1h2txyewy\StartMenuExperienceHost.exe	"C:\Windows\SystemApps\Microsoft.Windows.StartMenuExperienceHost_cw5n1h2txyewy\StartMenuExperienceHost.exe" -ServerName:App.AppXywbrabmsek0gm3tkwpr5kwzbs55tkqay.mca	C:\Windows\SystemApps\Microsoft.Windows.StartMenuExperienceHost_cw5n1h2txyewy\StartMenuExperienceHost.exe
*** 3432	728	RuntimeBroker.	0xbb8ed43f32c0	3	-	1	False	2024-12-11 19:56:27.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\RuntimeBroker.exe	C:\Windows\System32\RuntimeBroker.exe -Embedding	C:\Windows\System32\RuntimeBroker.exe
*** 1640	728	dllhost.exe	0xbb8ed52dc080	7	-	1	False	2024-12-17 10:41:32.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\taskhostw.exe	-	-
*** 1648	728	MoUsoCoreWorke	0xbb8ed5517080	9	-	0	False	2024-12-17 10:41:21.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\MoUsoCoreWorker.exe	C:\Windows\System32\mousocoreworker.exe -Embedding	C:\Windows\System32\mousocoreworker.exe
** 2780	584	svchost.exe	0xbb8ececd02c0	12	-	1	False	2024-12-11 19:56:24.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\system32\svchost.exe -k UnistackSvcGroup	C:\Windows\system32\svchost.exe
** 1632	584	svchost.exe	0xbb8ed39f1080	10	-	0	False	2024-12-11 19:54:54.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\system32\svchost.exe -k LocalServiceNetworkRestricted -p	C:\Windows\system32\svchost.exe
** 1760	584	spoolsv.exe	0xbb8ed3ad30c0	6	-	0	False	2024-12-11 19:54:55.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\spoolsv.exe	C:\Windows\System32\spoolsv.exe	C:\Windows\System32\spoolsv.exe
** 3808	584	svchost.exe	0xbb8ed45f6080	7	-	0	False	2024-12-11 20:09:07.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\System32\svchost.exe -k netsvcs -p	C:\Windows\System32\svchost.exe
** 484	584	svchost.exe	0xbb8ed3854280	21	-	0	False	2024-12-11 19:54:54.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\System32\svchost.exe -k LocalSystemNetworkRestricted -p	C:\Windows\System32\svchost.exe
*** 560	484	winlogon.exe	0xbb8ed01f6080	6	-	1	False	2024-12-11 19:54:53.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\winlogon.exe	winlogon.exe	C:\Windows\system32\winlogon.exe
**** 712	560	fontdrvhost.ex	0xbb8ed0e95140	5	-	1	False	2024-12-11 19:54:53.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\fontdrvhost.exe	-	-
**** 2468	560	userinit.exe	0xbb8ece749340	0	-	1	False	2024-12-11 19:56:24.000000 UTC	2024-12-11 19:56:46.000000 UTC	\Device\HarddiskVolume2\Windows\System32\userinit.exe	-	-
***** 2012	2468	explorer.exe	0xbb8ecec4f340	106	-	1	False	2024-12-11 19:56:25.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\explorer.exe	C:\Windows\Explorer.EXE	C:\Windows\Explorer.EXE
****** 3684	2012	VBoxTray.exe	0xbb8ecef0a080	11	-	1	False	2024-12-11 19:56:46.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\VBoxTray.exe	"C:\Windows\System32\VBoxTray.exe" 	C:\Windows\System32\VBoxTray.exe
****** 4328	2012	SecurityHealth	0xbb8ed46ca0c0	1	-	1	False	2024-12-11 19:56:46.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\SecurityHealthSystray.exe	"C:\Windows\System32\SecurityHealthSystray.exe" 	C:\Windows\System32\SecurityHealthSystray.exe
****** 5128	2012	DumpIt.exe	0xbb8ed4630080	2	-	1	True	2024-12-17 10:41:31.000000 UTC	N/A	\Device\HarddiskVolume2\Users\fred\Pictures\DumpIt.exe	"C:\Users\fred\Pictures\DumpIt.exe" 	C:\Users\fred\Pictures\DumpIt.exe
******* 4776	5128	conhost.exe	0xbb8ed4752080	5	-	1	False	2024-12-17 10:41:31.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\conhost.exe	\??\C:\Windows\system32\conhost.exe 0x4	C:\Windows\system32\conhost.exe
****** 5032	2012	notepad.exe	0xbb8ed90d8080	1	-	1	False	2024-12-17 09:53:36.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\notepad.exe	"C:\Windows\system32\NOTEPAD.EXE" C:\Users\fred\Documents\readme.txt	C:\Windows\system32\NOTEPAD.EXE
****** 4300	2012	share.exe	0xbb8ed6cb2080	1	-	1	False	2024-12-17 10:25:00.000000 UTC	N/A	\Device\HarddiskVolume2\Users\fred\Documents\share.exe	"C:\Users\fred\Documents\share.exe" 	C:\Users\fred\Documents\share.exe
******* 7104	4300	share.exe	0xbb8ed55b1080	1	-	1	False	2024-12-17 10:25:02.000000 UTC	N/A	\Device\HarddiskVolume2\Users\fred\Documents\share.exe	"C:\Users\fred\Documents\share.exe" 	C:\Users\fred\Documents\share.exe
******* 204	4300	conhost.exe	0xbb8ed5aed080	4	-	1	False	2024-12-17 10:25:00.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\conhost.exe	\??\C:\Windows\system32\conhost.exe 0x4	C:\Windows\system32\conhost.exe
**** 892	560	dwm.exe	0xbb8ed0f61080	17	-	1	False	2024-12-11 19:54:53.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\dwm.exe	"dwm.exe"	C:\Windows\system32\dwm.exe
*** 3048	484	ctfmon.exe	0xbb8ece85a240	8	-	1	False	2024-12-11 19:56:24.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\ctfmon.exe	"ctfmon.exe"	C:\Windows\system32\ctfmon.exe
*** 500	484	csrss.exe	0xbb8ed01c0140	11	-	1	False	2024-12-11 19:54:53.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\csrss.exe	-	-
** 1000	584	svchost.exe	0xbb8ed0fd8240	71	-	0	False	2024-12-11 19:54:53.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\system32\svchost.exe -k netsvcs -p	C:\Windows\system32\svchost.exe
*** 3456	1000	taskhostw.exe	0xbb8ecefe62c0	6	-	1	False	2024-12-11 20:09:07.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\taskhostw.exe	taskhostw.exe Time	C:\Windows\system32\taskhostw.exe
*** 2920	1000	taskhostw.exe	0xbb8ecea4a300	9	-	1	False	2024-12-11 19:56:24.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\taskhostw.exe	taskhostw.exe {222A245B-E637-4AE9-A93F-A59CA119A75E}	C:\Windows\system32\taskhostw.exe
*** 2764	1000	sihost.exe	0xbb8ece82e340	11	-	1	False	2024-12-11 19:56:24.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\sihost.exe	sihost.exe	C:\Windows\system32\sihost.exe
*** 7020	1000	taskhostw.exe	0xbb8ed62df080	2	-	0	False	2024-12-17 10:37:21.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\taskhostw.exe	taskhostw.exe network	C:\Windows\system32\taskhostw.exe
*** 6488	1000	taskhostw.exe	0xbb8ed465f080	5	-	1	False	2024-12-17 10:33:52.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\taskhostw.exe	taskhostw.exe	C:\Windows\system32\taskhostw.exe
** 4076	584	SecurityHealth	0xbb8ed46d5080	8	-	0	False	2024-12-11 19:56:46.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\SecurityHealthService.exe	C:\Windows\system32\SecurityHealthService.exe	C:\Windows\system32\SecurityHealthService.exe
** 3948	584	svchost.exe	0xbb8ed4985080	5	-	0	False	2024-12-11 19:56:53.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\system32\svchost.exe -k LocalServiceAndNoImpersonation -p	C:\Windows\system32\svchost.exe
** 1008	584	svchost.exe	0xbb8ed0fe02c0	15	-	0	False	2024-12-11 19:54:53.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\system32\svchost.exe -k LocalServiceNoNetwork -p	C:\Windows\system32\svchost.exe
** 1520	584	svchost.exe	0xbb8ed39c52c0	12	-	0	False	2024-12-11 19:54:54.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\System32\svchost.exe -k LocalServiceNetworkRestricted -p	C:\Windows\System32\svchost.exe
*** 5948	1520	audiodg.exe	0xbb8ed472a080	8	-	0	False	2024-12-17 10:41:30.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\audiodg.exe	C:\Windows\system32\AUDIODG.EXE 0x49c	C:\Windows\system32\AUDIODG.EXE
** 2032	584	svchost.exe	0xbb8ed3b04240	14	-	0	False	2024-12-11 19:54:55.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\System32\svchost.exe -k utcsvc -p	C:\Windows\System32\svchost.exe
** 1652	584	svchost.exe	0xbb8ed39fd240	4	-	0	False	2024-12-11 19:54:54.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\svchost.exe	C:\Windows\system32\svchost.exe -k appmodel -p	C:\Windows\system32\svchost.exe
** 4984	584	SgrmBroker.exe	0xbb8ed4a40080	6	-	0	False	2024-12-11 19:56:53.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\SgrmBroker.exe	C:\Windows\system32\SgrmBroker.exe	C:\Windows\system32\SgrmBroker.exe
* 592	492	lsass.exe	0xbb8ed0e0c080	8	-	0	False	2024-12-11 19:54:53.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\lsass.exe	C:\Windows\system32\lsass.exe	C:\Windows\system32\lsass.exe
* 720	492	fontdrvhost.ex	0xbb8ed0e97080	5	-	0	False	2024-12-11 19:54:53.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\fontdrvhost.exe	-	-
4344	4320	notepad.exe	0xbb8ed45f2080	1	-	1	False	2024-12-11 20:02:10.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\notepad.exe	"C:\Windows\system32\NOTEPAD.EXE" C:\Users\fred\Downloads\Hereugo.pdf.spy	C:\Windows\system32\NOTEPAD.EXE
3968	4260	MicrosoftEdgeU	0xbb8ed4a74080	4	-	0	True	2024-12-11 20:14:57.000000 UTC	N/A	\Device\HarddiskVolume2\Program Files (x86)\Microsoft\EdgeUpdate\MicrosoftEdgeUpdate.exe	"C:\Program Files (x86)\Microsoft\EdgeUpdate\MicrosoftEdgeUpdate.exe" /c	C:\Program Files (x86)\Microsoft\EdgeUpdate\MicrosoftEdgeUpdate.exe
6968	6516	OneDrive.exe	0xbb8ed6cbd300	30	-	1	False	2024-12-16 20:11:53.000000 UTC	N/A	\Device\HarddiskVolume2\Users\fred\AppData\Local\Microsoft\OneDrive\OneDrive.exe	 /updateInstalled /background	C:\Users\fred\AppData\Local\Microsoft\OneDrive\OneDrive.exe
* 6900	6968	msedgewebview2	0xbb8ed61cb080	0	-	1	False	2024-12-17 09:48:40.000000 UTC	2024-12-17 09:52:41.000000 UTC	\Device\HarddiskVolume2\Program Files (x86)\Microsoft\EdgeWebView\Application\131.0.2903.99\msedgewebview2.exe	-	-
2760	6516	Microsoft.Shar	0xbb8ed75900c0	13	-	1	False	2024-12-16 20:12:00.000000 UTC	N/A	\Device\HarddiskVolume2\Users\fred\AppData\Local\Microsoft\OneDrive\24.226.1110.0004\Microsoft.SharePoint.exe	/silentConfig	C:\Users\fred\AppData\Local\Microsoft\OneDrive\24.226.1110.0004\Microsoft.SharePoint.exe
5408	5492	MusNotifyIcon.	0xbb8ed4ece080	3	-	1	False	2024-12-16 21:14:28.000000 UTC	N/A	\Device\HarddiskVolume2\Windows\System32\MusNotifyIcon.exe	%systemroot%\system32\MusNotifyIcon.exe NotifyTrayIcon 19	C:\Windows\system32\MusNotifyIcon.exe
```Volatility 3 Framework 2.8.0

PID	Process	Args

4	System	Required memory at 0x20 is not valid (process exited?)
72	Registry	Required memory at 0x20 is not valid (process exited?)
324	smss.exe	\SystemRoot\System32\smss.exe
424	csrss.exe	%SystemRoot%\system32\csrss.exe ObjectDirectory=\Windows SharedSection=1024,20480,768 Windows=On SubSystemType=Windows ServerDll=basesrv,1 ServerDll=winsrv:UserServerDllInitialization,3 ServerDll=sxssrv,4 ProfileControl=Off MaxRequestThreads=16
492	wininit.exe	Required memory at 0x6c1b503020 is inaccessible (swapped)
500	csrss.exe	Required memory at 0x1d370c033ec is inaccessible (swapped)
560	winlogon.exe	winlogon.exe
584	services.exe	C:\Windows\system32\services.exe
592	lsass.exe	C:\Windows\system32\lsass.exe
712	fontdrvhost.ex	Required memory at 0x272c9441a28 is inaccessible (swapped)
720	fontdrvhost.ex	Required memory at 0xd359fbe020 is inaccessible (swapped)
728	svchost.exe	C:\Windows\system32\svchost.exe -k DcomLaunch -p
808	svchost.exe	C:\Windows\system32\svchost.exe -k RPCSS -p
892	dwm.exe	"dwm.exe"
1000	svchost.exe	C:\Windows\system32\svchost.exe -k netsvcs -p
1008	svchost.exe	C:\Windows\system32\svchost.exe -k LocalServiceNoNetwork -p
484	svchost.exe	C:\Windows\System32\svchost.exe -k LocalSystemNetworkRestricted -p
676	svchost.exe	C:\Windows\system32\svchost.exe -k LocalServiceNetworkRestricted -p
804	svchost.exe	C:\Windows\system32\svchost.exe -k LocalService -p
1164	svchost.exe	C:\Windows\System32\svchost.exe -k NetworkService -p
1308	VBoxService.ex	C:\Windows\System32\VBoxService.exe
1400	MemCompression	Required memory at 0x20 is not valid (process exited?)
1520	svchost.exe	C:\Windows\System32\svchost.exe -k LocalServiceNetworkRestricted -p
1624	svchost.exe	C:\Windows\System32\svchost.exe -k LocalServiceNetworkRestricted -p
1632	svchost.exe	C:\Windows\system32\svchost.exe -k LocalServiceNetworkRestricted -p
1652	svchost.exe	C:\Windows\system32\svchost.exe -k appmodel -p
1752	svchost.exe	C:\Windows\system32\svchost.exe -k LocalService -p
1760	spoolsv.exe	C:\Windows\System32\spoolsv.exe
1792	svchost.exe	C:\Windows\system32\svchost.exe -k LocalServiceNoNetworkFirewall -p
2032	svchost.exe	C:\Windows\System32\svchost.exe -k utcsvc -p
2192	svchost.exe	C:\Windows\System32\svchost.exe -k LocalServiceNetworkRestricted
2764	sihost.exe	sihost.exe
2780	svchost.exe	C:\Windows\system32\svchost.exe -k UnistackSvcGroup
2920	taskhostw.exe	taskhostw.exe {222A245B-E637-4AE9-A93F-A59CA119A75E}
3048	ctfmon.exe	"ctfmon.exe"
2468	userinit.exe	Required memory at 0xa7846c4020 is not valid (process exited?)
2012	explorer.exe	C:\Windows\Explorer.EXE
384	svchost.exe	C:\Windows\system32\svchost.exe -k ClipboardSvcGroup -p
1804	SearchIndexer.	C:\Windows\system32\SearchIndexer.exe /Embedding
3292	StartMenuExper	"C:\Windows\SystemApps\Microsoft.Windows.StartMenuExperienceHost_cw5n1h2txyewy\StartMenuExperienceHost.exe" -ServerName:App.AppXywbrabmsek0gm3tkwpr5kwzbs55tkqay.mca
3432	RuntimeBroker.	C:\Windows\System32\RuntimeBroker.exe -Embedding
3620	SearchApp.exe	"C:\Windows\SystemApps\Microsoft.Windows.Search_cw5n1h2txyewy\SearchApp.exe" -ServerName:CortanaUI.AppX8z9r6jm96hw4bsbneegw0kyxx296wr9t.mca
3764	RuntimeBroker.	C:\Windows\System32\RuntimeBroker.exe -Embedding
4360	svchost.exe	C:\Windows\system32\svchost.exe -k wusvcs -p
5056	RuntimeBroker.	C:\Windows\System32\RuntimeBroker.exe -Embedding
4328	SecurityHealth	"C:\Windows\System32\SecurityHealthSystray.exe" 
4076	SecurityHealth	C:\Windows\system32\SecurityHealthService.exe
3684	VBoxTray.exe	"C:\Windows\System32\VBoxTray.exe" 
3948	svchost.exe	C:\Windows\system32\svchost.exe -k LocalServiceAndNoImpersonation -p
4984	SgrmBroker.exe	C:\Windows\system32\SgrmBroker.exe
4744	svchost.exe	C:\Windows\System32\svchost.exe -k LocalServiceNetworkRestricted -p
2988	dllhost.exe	C:\Windows\system32\DllHost.exe /Processid:{973D20D7-562D-44B9-B70B-5A0F49CCDF3F}
3384	SearchApp.exe	Required memory at 0x1c16a2034a8 is inaccessible (swapped)
3100	TextInputHost.	"C:\Windows\SystemApps\MicrosoftWindows.Client.CBS_cw5n1h2txyewy\TextInputHost.exe" -ServerName:InputApp.AppXjd5de1g66v206tj52m9d0dtpppx4cgpn.mca
4344	notepad.exe	"C:\Windows\system32\NOTEPAD.EXE" C:\Users\fred\Downloads\Hereugo.pdf.spy
3456	taskhostw.exe	taskhostw.exe Time
3336	svchost.exe	Required memory at 0x182f88032f8 is inaccessible (swapped)
3808	svchost.exe	C:\Windows\System32\svchost.exe -k netsvcs -p
5496	svchost.exe	C:\Windows\system32\svchost.exe -k LocalService
3968	MicrosoftEdgeU	"C:\Program Files (x86)\Microsoft\EdgeUpdate\MicrosoftEdgeUpdate.exe" /c
4284	HxTsr.exe	Required memory at 0xc75639e020 is not valid (process exited?)
3796	svchost.exe	C:\Windows\system32\svchost.exe -k WbioSvcGroup
3260	ApplicationFra	C:\Windows\system32\ApplicationFrameHost.exe -Embedding
6092	dllhost.exe	"C:\Windows\SysWOW64\DllHost.exe" /Processid:{776DBC8D-7347-478C-8D71-791E12EF49D8}
5832	GameBar.exe	Required memory at 0x18301ed020 is not valid (process exited?)
6968	OneDrive.exe	 /updateInstalled /background
2760	Microsoft.Shar	/silentConfig
2380	MsMpEng.exe	"C:\ProgramData\Microsoft\Windows Defender\platform\4.18.24090.11-0\MsMpEng.exe"
256	MpDefenderCore	"C:\ProgramData\Microsoft\Windows Defender\platform\4.18.24090.11-0\MpDefenderCoreService.exe"
3888	dllhost.exe	C:\Windows\system32\DllHost.exe /Processid:{3EB3C877-1F16-487C-9050-104DBCD66683}
5408	MusNotifyIcon.	%systemroot%\system32\MusNotifyIcon.exe NotifyTrayIcon 19
6900	msedgewebview2	Required memory at 0xed67ac2020 is not valid (process exited?)
2712	ShellExperienc	Required memory at 0x1f6d54034f8 is inaccessible (swapped)
6912	RuntimeBroker.	C:\Windows\System32\RuntimeBroker.exe -Embedding
3920	Microsoft.Phot	Required memory at 0x4440ccc020 is inaccessible (swapped)
3900	RuntimeBroker.	C:\Windows\System32\RuntimeBroker.exe -Embedding
5032	notepad.exe	"C:\Windows\system32\NOTEPAD.EXE" C:\Users\fred\Documents\readme.txt
4300	share.exe	"C:\Users\fred\Documents\share.exe" 
204	conhost.exe	\??\C:\Windows\system32\conhost.exe 0x4
7104	share.exe	"C:\Users\fred\Documents\share.exe" 
6488	taskhostw.exe	taskhostw.exe
7020	taskhostw.exe	taskhostw.exe network
2168	TrustedInstall	C:\Windows\servicing\TrustedInstaller.exe
2332	TiWorker.exe	C:\Windows\winsxs\amd64_microsoft-windows-servicingstack_31bf3856ad364e35_10.0.19041.5071_none_7e3c4e707c6a2679\TiWorker.exe -Embedding
3864	SearchProtocol	"C:\Windows\system32\SearchProtocolHost.exe" Global\UsGthrFltPipeMssGthrPipe21_ Global\UsGthrCtrlFltPipeMssGthrPipe21 1 -2147483646 "Software\Microsoft\Windows Search" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT; MS Search 4.0 Robot)" "C:\ProgramData\Microsoft\Search\Data\Temp\usgthrsvc" "DownLevelDaemon" 
2164	SearchFilterHo	"C:\Windows\system32\SearchFilterHost.exe" 0 796 800 808 8192 804 780 
1648	MoUsoCoreWorke	C:\Windows\System32\mousocoreworker.exe -Embedding
3088	smartscreen.ex	C:\Windows\System32\smartscreen.exe -Embedding
5948	audiodg.exe	C:\Windows\system32\AUDIODG.EXE 0x49c
5128	DumpIt.exe	"C:\Users\fred\Pictures\DumpIt.exe" 
4776	conhost.exe	\??\C:\Windows\system32\conhost.exe 0x4
1640	dllhost.exe	Required memory at 0xcf91149020 is not valid (process exited?)
