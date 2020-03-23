# Class 5 on WINDOWS POWERSHELL 

En este archivo md se desarrolló las preguntas del taller de PowerShell de la clase 5

#1

¿Cuál clase puede emplearse para consultar la dirección IP de un adaptador de red? ¿Posee dicha clase algún método para liberar un préstamo de dirección (lease) DHCP?

Con la clase win32_NetworkAdapterconfiguration. En sí, no posee un método para liberar un préstamo de dirección DHCP, para encontrar los adaptadores sería tal que así

``Get-CimInstance win32_networkadapterconfiguration | Select-Object IP`` 

Resultado

```
Description             : Microsoft Kernel Debug Network Adapter
Index                   : 0
IPAddress               :
IPConnectionMetric      :
IPEnabled               : False
IPFilterSecurityEnabled :

Description             : Realtek PCIe FE Family Controller
Index                   : 1
IPAddress               :
IPConnectionMetric      :
IPEnabled               : False
IPFilterSecurityEnabled :

Description             : Adaptador de red 802.11n Broadcom
Index                   : 2
IPAddress               : {192.168.0.107, fe80::4d2c:7f80:ae0c:ea1a}
IPConnectionMetric      : 55
IPEnabled               : True
IPFilterSecurityEnabled : False

Description             : Microsoft Wi-Fi Direct Virtual Adapter
Index                   : 3
IPAddress               :
IPConnectionMetric      :
IPEnabled               : False
IPFilterSecurityEnabled :

Description             : Bluetooth Device (Personal Area Network)
Index                   : 4
IPAddress               :
IPConnectionMetric      :
IPEnabled               : False
IPFilterSecurityEnabled :

Description             : WAN Miniport (SSTP)
Index                   : 5
IPAddress               :
IPConnectionMetric      :
IPEnabled               : False
IPFilterSecurityEnabled :
```

#2

Despliegue una lista de parches empleando WMI (Microsoft se refiere a los parches con el nombre quick-fix engineering). Es diferente el listado al que produce el cmdlet Get-Hotfix?

Para desplegar la lista se usaría el siguiente comando

``Get-WmiObject win32_quickfixengineering``

Resultado
```
Source        Description      HotFixID      InstalledBy          InstalledOn
------        -----------      --------      -----------          -----------
DESKTOP-8F... Update           KB4534132     NT AUTHORITY\SYSTEM  21/02/2020 0:00:00
DESKTOP-8F... Security Update  KB4515383     NT AUTHORITY\SYSTEM  21/09/2019 0:00:00
DESKTOP-8F... Security Update  KB4516115     NT AUTHORITY\SYSTEM  25/09/2019 0:00:00
DESKTOP-8F... Security Update  KB4520390     NT AUTHORITY\SYSTEM  04/10/2019 0:00:00
DESKTOP-8F... Security Update  KB4521863     NT AUTHORITY\SYSTEM  15/10/2019 0:00:00
DESKTOP-8F... Security Update  KB4524569     NT AUTHORITY\SYSTEM  13/11/2019 0:00:00
DESKTOP-8F... Security Update  KB4528759     NT AUTHORITY\SYSTEM  16/01/2020 0:00:00
DESKTOP-8F... Security Update  KB4537759     NT AUTHORITY\SYSTEM  21/02/2020 0:00:00
DESKTOP-8F... Security Update  KB4538674     NT AUTHORITY\SYSTEM  14/02/2020 0:00:00
DESKTOP-8F... Security Update  KB4541338     NT AUTHORITY\SYSTEM  16/03/2020 0:00:00
DESKTOP-8F... Update           KB4551762     NT AUTHORITY\SYSTEM  19/03/2020 0:00:00
  
```
Hay pequeñas diferencias en cuanto a los métodos y propiedades, pero el listado es igual. 

#3 

Empleando WMI, muestre una lista de servicios, que incluya su status actual, su modalidad de inicio, y las cuentas que emplean para hacer login.

`` Get-WmiObject win32_service | Select-Object status, startmode, systemname ``

Resultado 

```
status startmode systemname
------ --------- ----------
OK     Auto      DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Auto      DESKTOP-8FOI51O
OK     Auto      DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Auto      DESKTOP-8FOI51O
OK     Auto      DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Auto      DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Auto      DESKTOP-8FOI51O
OK     Auto      DESKTOP-8FOI51O
OK     Auto      DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Auto      DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Auto      DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Auto      DESKTOP-8FOI51O
OK     Auto      DESKTOP-8FOI51O
OK     Auto      DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Auto      DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Auto      DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Auto      DESKTOP-8FOI51O
OK     Auto      DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Auto      DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O
OK     Manual    DESKTOP-8FOI51O 

```

#4

Empleando cmdlets de CIM, liste todas las clases del namespace SecurityCenter2, que tengan product como parte del nombre.

`` Get-CimClass -Namespace root/SecurityCenter2 | where -Filter {$_.CimClassName -like "*product*"} ``

Resultado

```
  NameSpace: ROOT/SecurityCenter2

CimClassName                        CimClassMethods      CimClassProperties
------------                        ---------------      ------------------
AntiSpywareProduct                  {}                   {displayName, instanceGuid, pathT...
AntiVirusProduct                    {}                   {displayName, instanceGuid, pathT...
FirewallProduct                     {}                   {displayName, instanceGuid, pathT...

```

#5 

Empleando cmdlets de CIM, y los resultados del ejercicio anterior, muestre los nombres de las aplicaciones antispyware instaladas en el sistema. También puede consultar si hay productos antivirus instalados en el sistema.

Con antispyware

``Get-CimInstance -Namespace root/SecurityCenter2 -ClassName AntiSpywareProduct | Select-Object displayName ``

Resultado 

```
displayName
-----------
Windows Defender
Avast Antivirus

```
Con antivirus

`` Get-CimInstance -Namespace root/SecurityCenter2 -ClassName AntiVirusProduct | Select-Object displayName  ``

Resultado 

```
displayName
-----------
Avast Antivirus
Windows Defender

```
