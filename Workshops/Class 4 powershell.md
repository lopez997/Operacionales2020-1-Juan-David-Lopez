# Class 4 on WINDOWS POWERSHELL 

En este archivo md se desarrolló las preguntas del taller de PowerShell de la clase 4

#1

Mostrar una tabla de procesos que incluya únicamente los nombres de los procesos, sus IDs, y si están respondiendo a Windows (la propiedad Responding muestra eso). Haga que la tabla tome el mínimo de espacio horizontal, pero no permita que la información se trunque.


`` Get-Process | select name,id,responding | ft -Wrap ``

Resultado

```
Name                                                              Id Responding
----                                                              -- ----------
ApplicationFrameHost                                            8972       True
armsvc                                                         11436       True
aswEngSrv                                                       9976       True
audiodg                                                         9940       True
AvastBrowserCrashHandler                                        8712       True
AvastBrowserCrashHandler64                                      9000       True
AvastSvc                                                        1612       True
AvastUI                                                          124       True
AvastUI                                                         9632       True
browser_assistant                                               2240       True
browser_assistant                                              10008       True
browser_broker                                                 12760       True
BtwRSupportService                                              3632       True
CAudioFilterAgent64                                             9328       True
chrome                                                          3732       True
chrome                                                          4624       True
chrome                                                          4896       True
chrome                                                          5192       True
chrome                                                          5568       True
chrome                                                          5944       True
chrome                                                          6160       True
chrome                                                          7864       True
chrome                                                          8548       True
chrome                                                          9268       True
chrome                                                         10612       True
chrome                                                         11116       True
chrome                                                         11948       True
chrome                                                         14432       True
chrome                                                         15784       True
chrome                                                         15916       True
chrome                                                         16432       True
chrome                                                         16708       True
conhost                                                        15692       True
csrss                                                            536       True
csrss                                                            628       True
ctfmon                                                          1684       True
CxAudMsg64                                                      3624       True
dasHost                                                         3240       True
dllhost                                                         9020       True
dllhost                                                        13032       True
dwm                                                              760       True
explorer                                                        5492       True
fontdrvhost                                                      948       True
fontdrvhost                                                      952       True
GoogleCrashHandler                                              7712       True
GoogleCrashHandler64                                            4788       True
googledrivesync                                                 7984       True
googledrivesync                                                10548       True
HxOutlook                                                       2784      False
HxTsr                                                           5544       True
Idle                                                               0       True
igfxCUIService                                                  2004       True
igfxEM                                                          5312       True
igfxHK                                                          2092       True
igfxTray                                                        5756       True
LockApp                                                         7836       True
lsass                                                            780       True
Memory Compression                                              1772       True
Microsoft.Photos                                               11396       True
MicrosoftEdge                                                  12980      False
MicrosoftEdgeCP                                                12592      False
MicrosoftEdgeSH                                                 9576       True
MsMpEng                                                         6528       True
NisSrv                                                          1240       True
notepad                                                        14112       True
OneDrive                                                        8944       True
powershell                                                     10064       True
Registry                                                          96       True
rundll32                                                        2028       True
RuntimeBroker                                                   2104       True
RuntimeBroker                                                   5008       True
RuntimeBroker                                                   7060       True
RuntimeBroker                                                   7208       True
RuntimeBroker                                                   7488       True
RuntimeBroker                                                   7912       True
RuntimeBroker                                                  11340       True
RuntimeBroker                                                  11900       True
RuntimeBroker                                                  12324       True
RuntimeBroker                                                  12848       True
RuntimeBroker                                                  13364       True
RuntimeBroker                                                  14280       True
SearchFilterHost                                                8056       True
SearchIndexer                                                  11528       True
SearchProtocolHost                                              1124       True
SearchUI                                                        9540       True
SecurityHealthHost                                              9712       True
SecurityHealthService                                           9220       True
SecurityHealthSystray                                           8912       True
services                                                         764       True
SettingSyncHost                                                 7736       True
SgrmBroker                                                      3584       True
ShellExperienceHost                                             9228       True
sihost                                                          5872       True
SkypeApp                                                       14196       True
SkypeBackgroundHost                                             7776       True
SkypeBridge                                                    13208       True
smartscreen                                                    12808       True
smss                                                             348       True
spoolsv                                                         3284       True
sqlwriter                                                       3676       True
StartMenuExperienceHost                                         6512       True
svchost                                                          460       True
svchost                                                          492       True
svchost                                                          496       True
svchost                                                          832       True
svchost                                                          904       True
svchost                                                          928       True
svchost                                                         1076       True
svchost                                                         1148       True
svchost                                                         1188       True
svchost                                                         1220       True
svchost                                                         1324       True
svchost                                                         1344       True
svchost                                                         1504       True
svchost                                                         1512       True
svchost                                                         1520       True
svchost                                                         1532       True
svchost                                                         1592       True
svchost                                                         1644       True
svchost                                                         1744       True
svchost                                                         1836       True
svchost                                                         1936       True
svchost                                                         2040       True
svchost                                                         2052       True
svchost                                                         2148       True
svchost                                                         2156       True
svchost                                                         2316       True
svchost                                                         2332       True
svchost                                                         2424       True
svchost                                                         2612       True
svchost                                                         2724       True
svchost                                                         2732       True
svchost                                                         2844       True
svchost                                                         2956       True
svchost                                                         2996       True
svchost                                                         3044       True
svchost                                                         3196       True
svchost                                                         3320       True
svchost                                                         3348       True
svchost                                                         3376       True
svchost                                                         3524       True
svchost                                                         3596       True
svchost                                                         3604       True
svchost                                                         3616       True
svchost                                                         3648       True
svchost                                                         3656       True
svchost                                                         3664       True
svchost                                                         3716       True
svchost                                                         3752       True
svchost                                                         3864       True
svchost                                                         3908       True
svchost                                                         3988       True
svchost                                                         4060       True
svchost                                                         4072       True
svchost                                                         4208       True
svchost                                                         4264       True
svchost                                                         5496       True
svchost                                                         5880       True
svchost                                                         5920       True
svchost                                                         6376       True
svchost                                                         6408       True
svchost                                                         6568       True
svchost                                                         6792       True
svchost                                                         6904       True
svchost                                                         7704       True
svchost                                                         7800       True
svchost                                                         8172       True
svchost                                                         8232       True
svchost                                                         8444       True
svchost                                                         8476       True
svchost                                                         8744       True
svchost                                                         9384       True
svchost                                                        11064       True
svchost                                                        11360       True
svchost                                                        11848       True
svchost                                                        12072       True
svchost                                                        12184       True
svchost                                                        12912       True
svchost                                                        14116       True
svchost                                                        15584       True
SynTPEnh                                                        6168       True
SynTPEnhService                                                 3692       True
SynTPHelper                                                     6556       True
System                                                             4       True
SystemSettings                                                 17208       True
SystemSettingsBroker                                            5080       True
taskhostw                                                       6104       True
unsecapp                                                        3876       True
Video.UI                                                       11336      False
vmnat                                                           3812       True
vmnetdhcp                                                       3788       True
vmware-authd                                                    3824       True
vmware-usbarbitrator64                                          3804       True
WhatsApp                                                       11960       True
WhatsApp                                                       14152       True
WhatsApp                                                       16916       True
WhatsApp                                                       17192       True
WindowsInternal.ComposableShell.Experiences.TextInput.InputApp 14328       True
wininit                                                          620       True
winlogon                                                         708       True
WmiPrvSE                                                        7620       True
WWAHost                                                        10652      False
YourPhone                                                       3068       True
YourPhoneServer                                                 6740       True
Zoom                                                            2352       True
Zoom                                                           11680       True

         
```

#2

 Muestre una tabla de procesos que incluya los nombres de los procesos y sus IDs. También incluya columnas para uso de memoria virtual y física; exprese dichos valores en megabytes (MB).

``Get-Process | ft -Property name, id, @{n='VM (MB)'; e={$_.VM / 1MB -as [int]}}, @{n='PM (MB)' ; e={$_.PM / 1MB -as [int]}}``

Resultado
```
Name                                                              Id VM (MB) PM (MB)
----                                                              -- ------- -------
ApplicationFrameHost                                            8972 2101518      26
armsvc                                                         11436      42       1
aswEngSrv                                                       9976 2101563      15
audiodg                                                         9940 2101342       8
AvastBrowserCrashHandler                                        8712      48       2
AvastBrowserCrashHandler64                                      9000    4182       2
AvastSvc                                                        1612 2101942     134
AvastUI                                                          124    4536      14
AvastUI                                                         9632    4595      49
browser_assistant                                               2240     150       3
browser_assistant                                              10008     178       9
browser_broker                                                 12760 2101341       2
BtwRSupportService                                              3632    4195       2
CAudioFilterAgent64                                             9328    4198       2
chrome                                                          3732 2101668      30
chrome                                                          4624 2101391       2
chrome                                                          4896 2102188     166
chrome                                                          5192 2101373       2
chrome                                                          5568 2105676      12
chrome                                                          5944 2105790      68
chrome                                                          6160 2105835     119
chrome                                                          7864 2105781     153
chrome                                                          8548 2105717      35
chrome                                                          9268 2105812      64
chrome                                                         10612 2103136     276
chrome                                                         11116 2105702      27
chrome                                                         11948 2101582       7
chrome                                                         14432 2110005      73
chrome                                                         15784 2105732      36
chrome                                                         15916 2106191     227
chrome                                                         16432 2105810      67
chrome                                                         16708 2105780      55
conhost                                                        15692 2101400       5
csrss                                                            536 2101340       2
csrss                                                            628 2101371       2
ctfmon                                                          1684 2101371       5
CxAudMsg64                                                      3624    4187       2
dasHost                                                         3240 2101306       1
dllhost                                                         9020 2101493       5
dllhost                                                        13032 2101450      22
dwm                                                              760 2101698      71
explorer                                                        5492 2102307     375
fontdrvhost                                                      948 2101428       6
fontdrvhost                                                      952 2101316       2
GoogleCrashHandler                                              7712      48       2
GoogleCrashHandler64                                            4788    4182       2
googledrivesync                                                 7984    4181       3
googledrivesync                                                10548    4567     176
HxOutlook                                                       2784 2101842      38
HxTsr                                                           5544 2101479      15
Idle                                                               0       0       0
igfxCUIService                                                  2004    4206       5
igfxEM                                                          5312    4225       4
igfxHK                                                          2092    4195       2
igfxTray                                                        5756    4219       3
LockApp                                                         7836 2101620      17
lsass                                                            780 2101337       8
Memory Compression                                              1772     116       1
Microsoft.Photos                                               11396    5004      52
MicrosoftEdge                                                  12980 2101820      26
MicrosoftEdgeCP                                                12592 2134221       6
MicrosoftEdgeSH                                                 9576 2134169       4
MsMpEng                                                         6528 2102419     290
NisSrv                                                          1240 2101344       6
notepad                                                        14112 2101397       3
OneDrive                                                        8944     313      16
powershell                                                     10064 2101936      72
Registry                                                          96     129      11
rundll32                                                        2028 2101341       2
RuntimeBroker                                                   2104 2101399       6
RuntimeBroker                                                   5008 2101340       2
RuntimeBroker                                                   7060 2101398       7
RuntimeBroker                                                   7208 2101586      20
RuntimeBroker                                                   7488 2101382       4
RuntimeBroker                                                   7912 2101452       9
RuntimeBroker                                                  11340 2101388       3
RuntimeBroker                                                  11900 2101375       5
RuntimeBroker                                                  12324 2101390       4
RuntimeBroker                                                  12848 2101434       8
RuntimeBroker                                                  13364 2101449       9
RuntimeBroker                                                  14280 2101416       5
SearchFilterHost                                                8056 2101315       1
SearchIndexer                                                  11528 2101658      51
SearchProtocolHost                                              1124 2101343       2
SearchUI                                                        9540 2135078     125
SecurityHealthHost                                              9712 2101382       4
SecurityHealthService                                           9220 2101360       5
SecurityHealthSystray                                           8912 2101352       2
services                                                         764 2101329       6
SettingSyncHost                                                 7736 2101444      16
SgrmBroker                                                      3584 2101304       4
ShellExperienceHost                                             9228 2101687      46
sihost                                                          5872 2101461      18
SkypeApp                                                       14196   38194     163
SkypeBackgroundHost                                             7776 2101346       2
SkypeBridge                                                    13208    4862      42
smartscreen                                                    12808 2134698      14
smss                                                             348 2101288       1
spoolsv                                                         3284 2101349       6
sqlwriter                                                       3676    4173       2
StartMenuExperienceHost                                         6512 2101787      37
svchost                                                          460 2101373      11
svchost                                                          492 2101328       3
svchost                                                          496 2101343       9
svchost                                                          832 2101334       2
svchost                                                          904 2101304       1
svchost                                                          928 2101436      18
svchost                                                         1076 2101331       3
svchost                                                         1148 2101331       2
svchost                                                         1188 2101322       2
svchost                                                         1220 2101326       2
svchost                                                         1324 2101353      15
svchost                                                         1344 2101343       2
svchost                                                         1504 2101317       1
svchost                                                         1512 2101353       3
svchost                                                         1520 2105451       3
svchost                                                         1532 2101324       2
svchost                                                         1592 2101358       6
svchost                                                         1644 2101323       6
svchost                                                         1744 2101320       3
svchost                                                         1836 2101330       2
svchost                                                         1936 2101358       7
svchost                                                         2040 2101348       5
svchost                                                         2052 2101333       4
svchost                                                         2148 2101327       2
svchost                                                         2156 2101353       2
svchost                                                         2316 2101328       4
svchost                                                         2332 2101395      17
svchost                                                         2424 2101330       3
svchost                                                         2612 2101344       4
svchost                                                         2724 2101317       2
svchost                                                         2732 2101332       3
svchost                                                         2844 2101384       4
svchost                                                         2956 2101338       2
svchost                                                         2996 2101372       7
svchost                                                         3044 2101352       3
svchost                                                         3196 2101332       3
svchost                                                         3320 2101377      10
svchost                                                         3348 2101325       2
svchost                                                         3376 2101596       6
svchost                                                         3524 2101322       2
svchost                                                         3596 2101491       4
svchost                                                         3604 2101360       7
svchost                                                         3616 2101415      18
svchost                                                         3648 2101318       2
svchost                                                         3656 2101348       2
svchost                                                         3664 2101551      33
svchost                                                         3716 2101313       1
svchost                                                         3752 2101323       2
svchost                                                         3864 2101377       5
svchost                                                         3908 2101329       2
svchost                                                         3988 2101670       7
svchost                                                         4060 2101328       3
svchost                                                         4072 2101316       1
svchost                                                         4208 2101314       1
svchost                                                         4264 2101343       3
svchost                                                         5496 2101322       2
svchost                                                         5880 2101530      10
svchost                                                         5920 2101393      10
svchost                                                         6376 2101331       2
svchost                                                         6408 2101370       6
svchost                                                         6568 2101370       5
svchost                                                         6792 2101336       3
svchost                                                         6904 2101416       4
svchost                                                         7704 2101454      11
svchost                                                         7800 2101361       5
svchost                                                         8172 2101342       3
svchost                                                         8232 2101346       4
svchost                                                         8444 2101316       2
svchost                                                         8476 2101333       3
svchost                                                         8744 2101340       3
svchost                                                         9384 2101322       2
svchost                                                        10396 2101533      11
svchost                                                        11064 2101326       3
svchost                                                        11360 2101323       3
svchost                                                        11848 2101403       5
svchost                                                        12072 2101366      10
svchost                                                        12184 2101366       5
svchost                                                        12912 2101357       3
svchost                                                        14116 2101337       3
svchost                                                        15584 2101315       1
SynTPEnh                                                        6168    4252       7
SynTPEnhService                                                 3692    4166       1
SynTPHelper                                                     6556    4178       1
System                                                             4       4       0
SystemSettings                                                 17208 2101728      45
SystemSettingsBroker                                            5080 2101448       8
taskhostw                                                       6104 2101507       8
unsecapp                                                        3876 2101332       1
Video.UI                                                       11336 2101785      24
vmnat                                                           3812      77       3
vmnetdhcp                                                       3788      64       8
vmware-authd                                                    3824     119       7
vmware-usbarbitrator64                                          3804 2101357       5
WhatsApp                                                       11960 2102054      99
WhatsApp                                                       14152 2101891     108
WhatsApp                                                       16916 2101482       6
WhatsApp                                                       17192 2102185     214
WindowsInternal.ComposableShell.Experiences.TextInput.InputApp 14328 2101569      15
wininit                                                          620 2101314       1
winlogon                                                         708 2101346       3
WmiPrvSE                                                        7620 2101351      13
WWAHost                                                        10652 2134971      90
YourPhone                                                       3068 2101636      19
YourPhoneServer                                                 6740 2101371       3
Zoom                                                            2352     361      60
Zoom                                                           11680     355      58
```

#3 

Emplee Get-EventLog para mostrar una lista de los logs de eventos disponibles (revise la ayuda para encontrar el parámetro que le permitirá obtener dicha información). Formatee la salida como una tabla que incluya el nombre de despliegue del log y el período de retención. Los encabezados de columna deben ser NombreLog y Per-Retencion.

`` Get-EventLog -List | fl -Property @{n='nombreLog'; e={$_.Log}}, @{n='Per-Retencion';e={$_.minimumRetentionDays}}``

Resultado 

```
nombreLog     : Application
Per-Retencion : 0

nombreLog     : HardwareEvents
Per-Retencion : 0

nombreLog     : Internet Explorer
Per-Retencion : 7

nombreLog     : Key Management Service
Per-Retencion : 0

nombreLog     : OAlerts
Per-Retencion : 0

nombreLog     : Security
Per-Retencion : 0

nombreLog     : System
Per-Retencion : 0

nombreLog     : Windows Azure
Per-Retencion : 7

nombreLog     : Windows PowerShell
Per-Retencion : 0

```

#4

Muestre una lista de servicios, de tal manera que aparezcan agrupados los servicios que están iniciados y los que están detenidos. Los que están iniciados deben aparecer primero.

`` Get-Service |Sort-Object status | fl -GroupBy status ``

Resultado

```
  Status: Stopped


Name                : ScDeviceEnum
DisplayName         : Servicio de enumeración de dispositivos de tarjeta inteligente
Status              : Stopped
DependentServices   : {}
ServicesDependedOn  : {}
CanPauseAndContinue : False
CanShutdown         : False
CanStop             : False
ServiceType         : Win32ShareProcess

Name                : SCardSvr
DisplayName         : Tarjeta inteligente
Status              : Stopped
DependentServices   : {}
ServicesDependedOn  : {}
CanPauseAndContinue : False
CanShutdown         : False
CanStop             : False
ServiceType         : Win32ShareProcess

Name                : RpcLocator
DisplayName         : Ubicador de llamada a procedimiento remoto (RPC)
Status              : Stopped
DependentServices   : {}
ServicesDependedOn  : {}
CanPauseAndContinue : False
CanShutdown         : False
CanStop             : False
ServiceType         : Win32OwnProcess

Name                : seclogon
DisplayName         : Inicio de sesión secundario
Status              : Stopped
DependentServices   : {}
ServicesDependedOn  : {}
CanPauseAndContinue : False
CanShutdown         : False
CanStop             : False
ServiceType         : Win32ShareProcess

Name                : SDRSVC
DisplayName         : Copias de seguridad de Windows
Status              : Stopped
DependentServices   : {}
ServicesDependedOn  : {RPCSS}
CanPauseAndContinue : False
CanShutdown         : False
CanStop             : False
ServiceType         : Win32OwnProcess

Name                : SCPolicySvc
DisplayName         : Directiva de extracción de tarjetas inteligentes
Status              : Stopped
DependentServices   : {}
ServicesDependedOn  : {RpcSs}
CanPauseAndContinue : False
CanShutdown         : False
CanStop             : False
ServiceType         : Win32ShareProcess

```

#5 

Mostrar una lista a cuatro columnas de todos los directorios que están en el raíz de la unidad C:

``ls -Path C:\ -Attributes directory| fw -Column 4``

Resultado 

```

    Directorio: C:\



Aeropuerto              DiseñoProyecto          EjercicioLab           Intel
masm32                  PerfLogs                Program Files          Program Files (x86)
quiz1                   Ruby26-x64              Users                  Windows                                                                    


```

#6

Cree una lista formateada de todos los archivos .exe del directorio C:\Windows. Debe mostrarse el nombre, la información de versión, y el tamaño del archivo. La propiedad de tamaño se llama length en Powershell, pero para mayor claridad, la columna se debe llamar Tamaño en su listado.

`` ls -Path C:\Windows |where -filter {$_.Name -like "*.exe"} | fl -Property name, @{n='tamaño';e={$_.length}}, versionInfo ``

Resultado

```
Name        : bfsvc.exe
tamaño      : 73216
VersionInfo : File:             C:\Windows\bfsvc.exe
              InternalName:     bfsvc.exe
              OriginalFilename: bfsvc.exe.mui
              FileVersion:      10.0.18362.718 (WinBuild.160101.0800)
              FileDescription:  Utilidad de servicio de actualización del archivo de arranque
              Product:          Sistema operativo Microsoft® Windows®
              ProductVersion:   10.0.18362.718
              Debug:            False
              Patched:          False
              PreRelease:       False
              PrivateBuild:     False
              SpecialBuild:     False
              Language:         Español (España, internacional)


Name        : explorer.exe
tamaño      : 4622280
VersionInfo : File:             C:\Windows\explorer.exe
              InternalName:     explorer
              OriginalFilename: EXPLORER.EXE.MUI
              FileVersion:      10.0.18362.718 (WinBuild.160101.0800)
              FileDescription:  Explorador de Windows
              Product:          Sistema operativo Microsoft® Windows®
              ProductVersion:   10.0.18362.718
              Debug:            False
              Patched:          False
              PreRelease:       False
              PrivateBuild:     False
              SpecialBuild:     False
              Language:         Español (España, internacional)


Name        : HelpPane.exe
tamaño      : 1059840
VersionInfo : File:             C:\Windows\HelpPane.exe
              InternalName:     HelpPane.exe
              OriginalFilename: HelpPane.exe.mui
              FileVersion:      10.0.18362.718 (WinBuild.160101.0800)
              FileDescription:  Ayuda y soporte técnico de Microsoft
              Product:          Sistema operativo Microsoft® Windows®
              ProductVersion:   10.0.18362.718
              Debug:            False
              Patched:          False
              PreRelease:       False
              PrivateBuild:     False
              SpecialBuild:     False
              Language:         Español (España, internacional)


Name        : hh.exe
tamaño      : 18432
VersionInfo : File:             C:\Windows\hh.exe
              InternalName:     HH 1.41
              OriginalFilename: HH.exe.mui
              FileVersion:      10.0.18362.718 (WinBuild.160101.0800)
              FileDescription:  Archivo ejecutable de ayuda HTML de Microsoft®
              Product:          Ayuda de HTML
              ProductVersion:   10.0.18362.718
              Debug:            False
              Patched:          False
              PreRelease:       False
              PrivateBuild:     False
              SpecialBuild:     False
              Language:         Español (España, internacional)


Name        : notepad.exe
tamaño      : 181248
VersionInfo : File:             C:\Windows\notepad.exe
              InternalName:     Notepad
              OriginalFilename: NOTEPAD.EXE.MUI
              FileVersion:      10.0.18362.1 (WinBuild.160101.0800)
              FileDescription:  Bloc de notas
              Product:          Sistema operativo Microsoft® Windows®
              ProductVersion:   10.0.18362.1
              Debug:            False
              Patched:          False
              PreRelease:       False
              PrivateBuild:     False
              SpecialBuild:     False
              Language:         Español (España, internacional)


Name        : regedit.exe
tamaño      : 358400
VersionInfo : File:             C:\Windows\regedit.exe
              InternalName:     REGEDIT
              OriginalFilename: REGEDIT.EXE.MUI
              FileVersion:      10.0.18362.718 (WinBuild.160101.0800)
              FileDescription:  Editor del Registro
              Product:          Sistema operativo Microsoft® Windows®
              ProductVersion:   10.0.18362.718
              Debug:            False
              Patched:          False
              PreRelease:       False
              PrivateBuild:     False
              SpecialBuild:     False
              Language:         Español (España, internacional)


Name        : RtCRU64.exe
tamaño      : 4332032
VersionInfo : File:             C:\Windows\RtCRU64.exe
              InternalName:     RtCRU.exe
              OriginalFilename: RtCRU.exe
              FileVersion:      1.13.0.0
              FileDescription:  RtCRU
              Product:          RtCRU
              ProductVersion:   1.13.0.0
              Debug:            False
              Patched:          False
              PreRelease:       False
              PrivateBuild:     False
              SpecialBuild:     False
              Language:         Inglés (Estados Unidos)


Name        : splwow64.exe
tamaño      : 132608
VersionInfo : File:             C:\Windows\splwow64.exe
              InternalName:     splwow64.exe
              OriginalFilename: splwow64.exe
              FileVersion:      10.0.18362.476 (WinBuild.160101.0800)
              FileDescription:  Print driver host for applications
              Product:          Microsoft® Windows® Operating System
              ProductVersion:   10.0.18362.476
              Debug:            False
              Patched:          False
              PreRelease:       False
              PrivateBuild:     False
              SpecialBuild:     False
              Language:         Inglés (Estados Unidos)


Name        : winhlp32.exe
tamaño      : 11776
VersionInfo : File:             C:\Windows\winhlp32.exe
              InternalName:     WINHSTB
              OriginalFilename: WINHLP32.EXE.MUI
              FileVersion:      10.0.18362.718 (WinBuild.160101.0800)
              FileDescription:  Código auxiliar de Windows Winhlp32
              Product:          Sistema operativo Microsoft® Windows®
              ProductVersion:   10.0.18362.718
              Debug:            False
              Patched:          False
              PreRelease:       False
              PrivateBuild:     False
              SpecialBuild:     False
              Language:         Español (España, internacional)


Name        : write.exe
tamaño      : 11264
VersionInfo : File:             C:\Windows\write.exe
              InternalName:     write
              OriginalFilename: write
              FileVersion:      10.0.18362.1 (WinBuild.160101.0800)
              FileDescription:  Windows Write
              Product:          Microsoft® Windows® Operating System
              ProductVersion:   10.0.18362.1
              Debug:            False
              Patched:          False
              PreRelease:       False
              PrivateBuild:     False
              SpecialBuild:     False
              Language:         Inglés (Estados Unidos)

```

#7

Importe el módulo NetAdapter (empleando el comando Import-Module NetAdapter). Empleando el cmdlet Get-NetAdapter, muestre una lista de adaptadores no virtuales (adaptadores cuya propiedad Virtual sea falsa. El valor lógico falso es representado por Powershell como $False).

``  Get-NetAdapter | Where -filter {$_.Virtual -eq $false} |fl ``

Resultado

```
Name                       : Wi-Fi
InterfaceDescription       : Adaptador de red 802.11n Broadcom
InterfaceIndex             : 20
MacAddress                 : 40-E2-30-41-0C-A3
MediaType                  : Native 802.11
PhysicalMediaType          : Native 802.11
InterfaceOperationalStatus : Up
AdminStatus                : Up
LinkSpeed(Mbps)            : 72
MediaConnectionState       : Connected
ConnectorPresent           : True
DriverInformation          : Driver Date 2013-06-02 Version 6.30.223.256 NDIS 6.40

Name                       : Ethernet
InterfaceDescription       : Realtek PCIe FE Family Controller
InterfaceIndex             : 8
MacAddress                 : 2C-60-0C-C5-6B-7F
MediaType                  : 802.3
PhysicalMediaType          : 802.3
InterfaceOperationalStatus : Down
AdminStatus                : Up
LinkSpeed(Mbps)            : 0
MediaConnectionState       : Disconnected
ConnectorPresent           : True
DriverInformation          : Driver Date 2015-05-05 Version 10.1.505.2015 NDIS 6.40

```

#8 

Importe el módulo DnsClient. Empleando el cmdlet Get-DnsClientCache, muestre una lista de los registros A y AAAA que estén en el caché. Sugerencia: Si el caché está vacío, visite algunos sitios web para poblarlo.

``
Get-DnsClientCache | where -filter {$_.Type -eq (28 ) -or $_.Type -eq 1} |fl
``

Resultado 

```
Entry      : r2---sn-cvb7lnee.googlevideo.com
RecordName : r2.sn-cvb7lnee.googlevideo.com
RecordType : A
Status     : Success
Section    : Answer
TimeToLive : 218
DataLength : 4
Data       : 74.125.165.103

Entry      : r3---sn-0ox-h1al.googlevideo.com
RecordName : r3.sn-0ox-h1al.googlevideo.com
RecordType : A
Status     : Success
Section    : Answer
TimeToLive : 300
DataLength : 4
Data       : 190.240.6.142

Entry      : update2.avastbrowser.com
RecordName : avast-omaha-prod-2143958876.us-east-1.elb.amazonaws.com
RecordType : A
Status     : Success
Section    : Answer
TimeToLive : 14
DataLength : 4
Data       : 34.202.250.195

Entry      : update2.avastbrowser.com
RecordName : avast-omaha-prod-2143958876.us-east-1.elb.amazonaws.com
RecordType : A
Status     : Success
Section    : Answer
TimeToLive : 14
DataLength : 4
Data       : 18.215.58.211

Entry      : update2.avastbrowser.com
RecordName : avast-omaha-prod-2143958876.us-east-1.elb.amazonaws.com
RecordType : A
Status     : Success
Section    : Answer
TimeToLive : 14
DataLength : 4
Data       : 54.88.93.136

Entry      : update2.avastbrowser.com
RecordName : avast-omaha-prod-2143958876.us-east-1.elb.amazonaws.com
RecordType : A
Status     : Success
Section    : Answer
TimeToLive : 14
DataLength : 4
Data       : 52.45.246.242

Entry      : update2.avastbrowser.com
RecordName : avast-omaha-prod-2143958876.us-east-1.elb.amazonaws.com
RecordType : A
Status     : Success
Section    : Answer
TimeToLive : 14
DataLength : 4
Data       : 52.2.206.12

Entry      : fcmconnection.googleapis.com
RecordName : fcmconnection.googleapis.com
RecordType : A
Status     : Success
Section    : Answer
TimeToLive : 129
DataLength : 4
Data       : 172.217.28.106

Entry      : clientservices.googleapis.com
RecordName : clientservices.googleapis.com
RecordType : A
Status     : Success
Section    : Answer
TimeToLive : 26
DataLength : 4
Data       : 216.58.222.195

Entry      : beacons.gcp.gvt2.com
RecordName : beacons-handoff.gcp.gvt2.com
RecordType : A
Status     : Success
Section    : Answer
TimeToLive : 19
DataLength : 4
Data       : 172.217.28.99

Entry      : www.icesi.edu.co
RecordName : webcache.icesi.edu.co
RecordType : A
Status     : Success
Section    : Answer
TimeToLive : 19405
DataLength : 4
Data       : 200.3.192.46

Entry      : ocsp.digicert.com
RecordName : cs9.wac.phicdn.net
RecordType : A
Status     : Success
Section    : Answer
TimeToLive : 859
DataLength : 4
Data       : 192.16.58.8

Entry      : r2---sn-0ox-h1al.googlevideo.com
RecordName : r2.sn-0ox-h1al.googlevideo.com
RecordType : A
Status     : Success
Section    : Answer
TimeToLive : 69
DataLength : 4
Data       : 190.240.6.141

Entry      : dummyimage.com
RecordName : dummyimage.com
RecordType : A
Status     : Success
Section    : Answer
TimeToLive : 2028
DataLength : 4
Data       : 208.113.135.33

Entry      : yt3.ggpht.com
RecordName : photos-ugc.l.googleusercontent.com
RecordType : A
Status     : Success
Section    : Answer
TimeToLive : 7
DataLength : 4
Data       : 172.217.30.193

Entry      : az725175.vo.msecnd.net
RecordName : cs22.wpc.v0cdn.net
RecordType : A
Status     : Success
Section    : Answer
TimeToLive : 2748
DataLength : 4
Data       : 192.16.48.200

Entry      : github.githubassets.com
RecordName : github.githubassets.com
RecordType : A
Status     : Success
Section    : Answer
TimeToLive : 1553
DataLength : 4
Data       : 185.199.109.154

Entry      : github.githubassets.com
RecordName : github.githubassets.com
RecordType : A
Status     : Success
Section    : Answer
TimeToLive : 1553
DataLength : 4
Data       : 185.199.110.154

Entry      : github.githubassets.com
RecordName : github.githubassets.com
RecordType : A
Status     : Success
Section    : Answer
TimeToLive : 1553
DataLength : 4
Data       : 185.199.108.154

Entry      : github.githubassets.com
RecordName : github.githubassets.com
RecordType : A
Status     : Success
Section    : Answer
TimeToLive : 1553
DataLength : 4
Data       : 185.199.111.154
```

#9
Genere una lista de todos los archivos .exe del directorio C:\Windows\System32 que tengan más de 5 MB.

``ls -Path C:\Windows\System32 | where -filter {$_.Name -like "*exe"} | WHERE -filter {$_.length/1MB -gt 5} |fl ``

Resultado

```
 Directorio: C:\Windows\System32



Name           : MRT.exe
Length         : 121542864
CreationTime   : 11/07/2019 19:49:48
LastWriteTime  : 11/03/2020 12:12:29
LastAccessTime : 22/03/2020 19:28:32
Mode           : -a----
LinkType       :
Target         : {}
VersionInfo    : File:             C:\Windows\System32\MRT.exe
                 InternalName:     mrt.exe
                 OriginalFilename: mrt.exe
                 FileVersion:      5.81.16832.1
                 FileDescription:  Herramienta de eliminación de software malintencionado de
                 Microsoft Windows
                 Product:          Herramienta de eliminación de software malintencionado de
                 Microsoft Windows
                 ProductVersion:   5.81.16832.1
                 Debug:            False
                 Patched:          False
                 PreRelease:       False
                 PrivateBuild:     False
                 SpecialBuild:     False
                 Language:         Español (España, internacional)


Name           : ntoskrnl.exe
Length         : 9930552
CreationTime   : 15/03/2020 23:22:55
LastWriteTime  : 15/03/2020 23:22:55
LastAccessTime : 23/03/2020 11:09:12
Mode           : -a----
LinkType       : HardLink
Target         : {C:\Windows\WinSxS\amd64_microsoft-windows-os-kernel_31bf3856ad364e35_10.0.1
                 8362.720_none_c21908ac45b11b74\ntoskrnl.exe}
VersionInfo    : File:             C:\Windows\System32\ntoskrnl.exe
                 InternalName:     ntkrnlmp.exe
                 OriginalFilename: ntkrnlmp.exe
                 FileVersion:      10.0.18362.720 (WinBuild.160101.0800)
                 FileDescription:  NT Kernel & System
                 Product:          Microsoft® Windows® Operating System
                 ProductVersion:   10.0.18362.720
                 Debug:            False
                 Patched:          False
                 PreRelease:       False
                 PrivateBuild:     False
                 SpecialBuild:     False
                 Language:         Inglés (Estados Unidos)
```

#10
Muestre una lista de parches que sean actualizaciones de seguridad.

``Get-HotFix | where -filter {$_.description -like "*security*"} |fl ``

Resultado

```
Description         : Security Update
FixComments         :
HotFixID            : KB4515383
InstallDate         :
InstalledBy         : NT AUTHORITY\SYSTEM
InstalledOn         : 21/09/2019 0:00:00
Name                :
ServicePackInEffect :
Status              :

Description         : Security Update
FixComments         :
HotFixID            : KB4516115
InstallDate         :
InstalledBy         : NT AUTHORITY\SYSTEM
InstalledOn         : 25/09/2019 0:00:00
Name                :
ServicePackInEffect :
Status              :

Description         : Security Update
FixComments         :
HotFixID            : KB4520390
InstallDate         :
InstalledBy         : NT AUTHORITY\SYSTEM
InstalledOn         : 04/10/2019 0:00:00
Name                :
ServicePackInEffect :
Status              :

Description         : Security Update
FixComments         :
HotFixID            : KB4521863
InstallDate         :
InstalledBy         : NT AUTHORITY\SYSTEM
InstalledOn         : 15/10/2019 0:00:00
Name                :
ServicePackInEffect :
Status              :

Description         : Security Update
FixComments         :
HotFixID            : KB4524569
InstallDate         :
InstalledBy         : NT AUTHORITY\SYSTEM
InstalledOn         : 13/11/2019 0:00:00
Name                :
ServicePackInEffect :
Status              :

Description         : Security Update
FixComments         :
HotFixID            : KB4528759
InstallDate         :
InstalledBy         : NT AUTHORITY\SYSTEM
InstalledOn         : 16/01/2020 0:00:00
Name                :
ServicePackInEffect :
Status              :

Description         : Security Update
FixComments         :
HotFixID            : KB4537759
InstallDate         :
InstalledBy         : NT AUTHORITY\SYSTEM
InstalledOn         : 21/02/2020 0:00:00
Name                :
ServicePackInEffect :
Status              :

Description         : Security Update
FixComments         :
HotFixID            : KB4538674
InstallDate         :
InstalledBy         : NT AUTHORITY\SYSTEM
InstalledOn         : 14/02/2020 0:00:00
Name                :
ServicePackInEffect :
Status              :

Description         : Security Update
FixComments         :
HotFixID            : KB4541338
InstallDate         :
InstalledBy         : NT AUTHORITY\SYSTEM
InstalledOn         : 16/03/2020 0:00:00
Name                :
ServicePackInEffect :
Status              :
```
#11
Muestre una lista de parches que hayan sido instalados por el usuario Administrador, que sean actualizaciones. Si no tiene ninguno, busque parches instalados por el usuario System. Note que algunos parches no tienen valor en el campo Installed By.

`` Get-HotFix | where -filter {$_.installedBy -like "*SYSTEM*"} |fl ``

Resultado

```

Description         : Update
FixComments         :
HotFixID            : KB4534132
InstallDate         :
InstalledBy         : NT AUTHORITY\SYSTEM
InstalledOn         : 21/02/2020 0:00:00
Name                :
ServicePackInEffect :
Status              :

Description         : Security Update
FixComments         :
HotFixID            : KB4515383
InstallDate         :
InstalledBy         : NT AUTHORITY\SYSTEM
InstalledOn         : 21/09/2019 0:00:00
Name                :
ServicePackInEffect :
Status              :

Description         : Security Update
FixComments         :
HotFixID            : KB4516115
InstallDate         :
InstalledBy         : NT AUTHORITY\SYSTEM
InstalledOn         : 25/09/2019 0:00:00
Name                :
ServicePackInEffect :
Status              :

Description         : Security Update
FixComments         :
HotFixID            : KB4520390
InstallDate         :
InstalledBy         : NT AUTHORITY\SYSTEM
InstalledOn         : 04/10/2019 0:00:00
Name                :
ServicePackInEffect :
Status              :

Description         : Security Update
FixComments         :
HotFixID            : KB4521863
InstallDate         :
InstalledBy         : NT AUTHORITY\SYSTEM
InstalledOn         : 15/10/2019 0:00:00
Name                :
ServicePackInEffect :
Status              :

Description         : Security Update
FixComments         :
HotFixID            : KB4524569
InstallDate         :
InstalledBy         : NT AUTHORITY\SYSTEM
InstalledOn         : 13/11/2019 0:00:00
Name                :
ServicePackInEffect :
Status              :

Description         : Security Update
FixComments         :
HotFixID            : KB4528759
InstallDate         :
InstalledBy         : NT AUTHORITY\SYSTEM
InstalledOn         : 16/01/2020 0:00:00
Name                :
ServicePackInEffect :
Status              :

Description         : Security Update
FixComments         :
HotFixID            : KB4537759
InstallDate         :
InstalledBy         : NT AUTHORITY\SYSTEM
InstalledOn         : 21/02/2020 0:00:00
Name                :
ServicePackInEffect :
Status              :

Description         : Security Update
FixComments         :
HotFixID            : KB4538674
InstallDate         :
InstalledBy         : NT AUTHORITY\SYSTEM
InstalledOn         : 14/02/2020 0:00:00
Name                :
ServicePackInEffect :
Status              :

Description         : Security Update
FixComments         :
HotFixID            : KB4541338
InstallDate         :
InstalledBy         : NT AUTHORITY\SYSTEM
InstalledOn         : 16/03/2020 0:00:00
Name                :
ServicePackInEffect :
Status              :

Description         : Update
FixComments         :
HotFixID            : KB4551762
InstallDate         :
InstalledBy         : NT AUTHORITY\SYSTEM
InstalledOn         : 19/03/2020 0:00:00
Name                :
ServicePackInEffect :
Status              :

```
#12

Genere una lista de todos los procesos que estén corriendo con el nombre Conhost o Svchost.

`` Get-Process | where -filter {$_.Name -eq "Conhost" -or $_.Name -eq "Svchost"} | fl``

Resultado

```
Id      : 15692
Handles : 261
CPU     : 6,15625
SI      : 1
Name    : conhost

Id      : 460
Handles : 1517
CPU     : 224,203125
SI      : 0
Name    : svchost

Id      : 492
Handles : 288
CPU     : 25,0625
SI      : 0
Name    : svchost

Id      : 496
Handles : 261
CPU     : 146,359375
SI      : 0
Name    : svchost

Id      : 832
Handles : 208
CPU     : 0,046875
SI      : 0
Name    : svchost

Id      : 904
Handles : 86
CPU     : 0,015625
SI      : 0
Name    : svchost

```
