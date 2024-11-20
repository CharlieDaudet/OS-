## 1. Programme, service, processus


🌞 **Lister tous les processus en cours d'exécution sur votre machine**
```bash 
PS C:\Users\Asus> Get-Process


Handles  NPM(K)    PM(K)      WS(K)     CPU(s)     Id  SI ProcessName
-------  ------    -----      -----     ------     --  -- -----------
    292      15     3924      12344       0,00   6332   8 AdobeCollabSync
    494      21     7228      11732       3,42  23432   8 AdobeCollabSync
    141       9     2480       9168              3516   0 AggregatorHost
    385      22     9208      32260       0,16   6716   8 ApplicationFrameHost
    141      10     1696       6736              4124   0 armsvc
    372      20     5440      23572              4176   0 AsusAppService
    258      12     2512      10020              3800   0 AsusOptimization
    138      10     1568       7632       0,02  18276   8 AsusOptimizationStartupTask
   3441      17     6576      20644              2200   0 AsusSoftwareManager
    749      36    40304      54984       1,11  16704   8 AsusSoftwareManagerAgent
    249      17    18184      20284       0,05   1960   8 AsusSupportService
    184      10     1860       7892              3136   0 AsusSwitch
    674      22     5756      18252              4108   0 AsusSystemAnalysis
    141       9     2408      10480       0,00  20396   8 AsusSystemAnalysis
    195      11     2620       9720              4144   0 AsusSystemDiagnosis
    312      33    18120       2688       0,08   2836   8 backgroundTaskHost
    313      33    17836       2680       0,20   4656   8 backgroundTaskHost
    312      33    17876       2832       0,19   4740   8 backgroundTaskHost
    300      16     4264      20452       0,02   6164   8 backgroundTaskHost
    310      33    17896       2348       0,09  11408   8 backgroundTaskHost
    321      33    17920       3184       0,14  12076   8 backgroundTaskHost
    319      33    18016       1668       0,08  17164   8 backgroundTaskHost
    315      33    18008       1792       0,06  21528   8 backgroundTaskHost
    246      41    57748      50904       0,09  14700   8 Canva
    172      12    14908      28920       0,00  19544   8 Canva
    790      65   312476     368664      19,55   1928   8 chrome
    288      27   125676     159972       3,08   4872   8 chrome
    389      26    56280     115092       0,75   8588   8 chrome
    212      15    11240      22312       0,25   8788   8 chrome
    229      19    15356      31532       0,02  10768   8 chrome
    361      28    62944     130972       2,45  14308   8 chrome
    566      41   182056     240180       4,61  16112   8 chrome
    579      43   192036     242480       5,19  16688   8 chrome
    400      28    68416     124924       2,14  16988   8 chrome
   1909      85   166712     282668      20,41  18368   8 chrome
    461      55   286836     349612      19,45  19316   8 chrome
    446      38    26756      55248       7,56  20796   8 chrome
    264      17    11976      23492       0,09  20936   8 chrome
   1801      48   341516     375440     108,64  21772   8 chrome
    306      23    21676      54784       0,05  22232   8 chrome
    246      11     6684       8796       0,02  23164   8 chrome
    572      26    41248      56852       0,08  23244   8 chrome
     93       7     5244       5724              3140   0 conhost
    116       8     5364      10988       0,00  22920   8 conhost
    794      85    27124      87704       1,44   1056   8 CrossDeviceService
    836      29     2344       5628               916   0 csrss
    805      29     3040       8596             15732   8 csrss
    564      21     7472      30356       2,78  20216   8 ctfmon
    162       9     1768       8000              4160   0 DiracAudSrv
    207      12    11496      33548       0,05   9448   8 Discord
   1099      46   103540     135008      21,36  12876   8 Discord
    367      20    16528      55180       3,02  15112   8 Discord
   1243     106   337432     333720   3 556,41  15840   8 Discord
    280      16    12424      80988       0,11  16676   8 Discord
   1335      33   156628     189160      10,33  18576   8 Discord
    132       8     1648       9380       0,02  11444   8 dllhost
    357      25     6952      18700       0,20  14544   8 dllhost
    133       8     1488       7764       0,00  22204   8 dllhost
   1696      69   221228     238436             12504   8 dwm
   5994     168   313692     449216      20,31  10008   8 explorer
     93       7     1156       5184              4284   0 focalFpSrvcDeamon
     42       7     1764       3980              1260   0 fontdrvhost
     42       8     2308       7676             11536   8 fontdrvhost
    818      27    11112      38156             10128   0 gamingservices
    144       7     1164       6208              5412   0 gamingservicesnet
      0       0       60          8                 0   0 Idle
    281      16    18824      21824              4136   0 IgoAudioService_x64
    173      13     5844       3144              3564   0 iGoSwServer
    253      14     3064       5292      17,72  15352   8 iGoSwServer
    442      37    39892      34796              4184   0 IntelAudioService
    155       8     1480       6176              1892   0 IntelCpHDCPSvc
    177      10     1976       9300       8,22  12648   8 ipf_helper
    144       9     2012       6900              4324   0 ipf_uf
    137      12     2612       6136              4244   0 ipfsvc
    147       9     1328       6688              4488   0 jhi_service
    197      12     2092       2768       0,27  19624   8 LocationNotificationWindows
     65      56     4280       5204              1088   0 LsaIso
   1858      34    12792      31108              1100   0 lsass
      0       0      668      51320              2984   0 Memory Compression
    477      21    38144      59732              9368   0 MoUsoCoreWorker
    499      19    15216      26376              4344   0 MpDefenderCoreService
    335      20    12500       4320       0,61   5404   8 msedgewebview2
    806      71   198576       7560       6,48   5528   8 msedgewebview2
    972      35   161068       8144       1,22   7000   8 msedgewebview2
    216      14     7484       3592       0,06  11188   8 msedgewebview2
    161      10     2204       8376       0,00  12428   8 msedgewebview2
   1331      52    43436       9552       2,38  14492   8 msedgewebview2
    177      12     8672       3264       0,14  15568   8 msedgewebview2
   1108     238   485708     352744              4660   0 MsMpEng
    355      21    13936      25416             11880   0 NisSrv
    408      29   130652     150472      29,89   4504   8 Obsidian
    741      25   126552     133044      21,03  10060   8 Obsidian
    300      16    16888      45324       0,06  20840   8 Obsidian
    858      39    76632      98184       8,91  21324   8 Obsidian
    438      24    33808      36904              4116   0 OneApp.IGCC.WinService
    167      11     2272      10120       0,09  19284   8 OpenConsole
    165      11     2280      10052       0,00  22220   8 OpenConsole
   2243     116    87020     199444       3,66  18308   8 PhoneExperienceHost
    731      32   187676     206176       1,13  13436   8 powershell
    646      27    52452      63792       0,03  21944   8 powershell
      0      20    13352      35784               172   0 Registry
    511      15     5316      14408              4464   0 RtkAudUService64
    404      14     3952      14604       0,11  11728   8 RtkAudUService64
    888      37    14156      54640       1,45   5700   8 RuntimeBroker
    271      14     3348      19692       0,28  13240   8 RuntimeBroker
    166      11     2272      11700       0,03  16108   8 RuntimeBroker
    510      21     5060      24932       0,05  17652   8 RuntimeBroker
    434      25     8780      36200       0,50  19520   8 RuntimeBroker
    155      10     2148      11096       0,00  23040   8 RuntimeBroker
   1820     148   235196     337368       3,77  12960   8 SearchHost
    766      20    19376      34312              9224   0 SearchIndexer
      0       0      184      65228               140   0 Secure System
    540      25     8324      20100             11068   0 SecurityHealthService
    191      10     1912      10852       0,08   8652   8 SecurityHealthSystray
   1019      19     9500      18360               920   0 services
    892      40    54280      99332       0,38   5364   8 ShellExperienceHost
    643      21     6728      34748       8,06  10172   8 sihost
     58       4     1136       1120               652   0 smss
    176      12     1972       9160       0,00  22096   8 soffice
    749      68    37664      94588       1,39   6724   8 soffice.bin
    419      21     5380      14440              3976   0 spoolsv
   1006      45    75284     141504       1,28   8356   8 StartMenuExperienceHost
   1014      95    45056      77172     333,95   9796   8 steam
    263      14     7592      15308             14816   0 steamservice
    297      20     9996      22272       0,20   2572   8 steamwebhelper
    720      31   329880     365180      72,06   7004   8 steamwebhelper
   1836      42   198968     214828      65,13   7548   8 steamwebhelper
    272      17     9276      15684       0,05  10836   8 steamwebhelper
    261      18    11180      21644       0,08  10984   8 steamwebhelper
    510      24    24028      47804       0,22  12560   8 steamwebhelper
   1072      41    54428     161000      23,67  15772   8 steamwebhelper
    353      23    14172      33680       1,42  15812   8 steamwebhelper
   1463      31    16008      37172              1232   0 svchost
   1658      21    10536      18604              1408   0 svchost
    434      13     3248      11124              1452   0 svchost
    110      11     1228       5060              1588   0 svchost
    156      29     5876       9660              1604   0 svchost
    436      14     3168      10488              1676   0 svchost
   1031      23     8632      19212              1700   0 svchost
    254      14     3028      10864              1732   0 svchost
    328      10     2092       9620              1740   0 svchost
    242      12     3448       8664              1900   0 svchost
    365      13     3084       9276              1912   0 svchost
    334      18     5572      11112              2072   0 svchost
    199      11     2140       8280              2128   0 svchost
    414      20     6568      16756              2368   0 svchost
    193       8     3072       6744              2464   0 svchost
    211      11     2460      10748              2560   0 svchost
    291      13     3784      15676              2628   0 svchost
    245      17     3132       9348              2640   0 svchost
    456      16    17140      19744              2652   0 svchost
    244      17     3456      13132              2716   0 svchost
    275       8     1352       5636              2736   0 svchost
    184      10     2048       7800              2752   0 svchost
    122       8     1536       6528              2880   0 svchost
    232      15     2304       9772              3068   0 svchost
    254      12     2844       9716              3080   0 svchost
    201      13     2332       8972              3100   0 svchost
    504      36    12172      24732              3208   0 svchost
    312      12    22656      26420              3296   0 svchost
    194      11     2528      12192       0,02   3396   8 svchost
    185      11     1800       7772              3408   0 svchost
    226      13     3376      14624              3412   0 svchost
    264      14    12400      16436              3432   0 svchost
    565      16     5352      16388              3496   0 svchost
    167       9     1540       7148              3524   0 svchost
    170       9     1824       6764              3692   0 svchost
    583      31     8672      25472              3768   0 svchost
    257      14     2860      12748              3816   0 svchost
    151       9     1732       8584              3856   0 svchost
    393      28     4788      15648              4152   0 svchost
    370      21     2980      11428              4168   0 svchost
    393      24    31724      38536              4232   0 svchost
    735      29    29848      53844              4256   0 svchost
    202      11     2200       9836              4512   0 svchost
    174      10     1756       7676              4520   0 svchost
    208      12     2324       9316              4596   0 svchost
    136       9     1320       5916              4612   0 svchost
    436      19     9980      19860              4704   0 svchost
    262      13     4148      18976              4716   0 svchost
    442      21     5244      21508              4756   0 svchost
    176      10     1772       8100              5472   0 svchost
    154      10     2068       9536       0,16   5792   8 svchost
    218      11     2076      10116              5940   0 svchost
    299      15     4156      17268              6516   0 svchost
    211      13     2940      14120              6824   0 svchost
    338      16     3668      15264              6912   0 svchost
    301      15     3776      20112       0,09   6940   8 svchost
    480      18     7648      28064       0,94   7448   8 svchost
    269      12     2728       9176              7456   0 svchost
    150       9     1756       9900       0,03   7812   8 svchost
    462      26     6112      23592              7864   0 svchost
    253      12     2228      12256              7956   0 svchost
    489      27     3944      14892              7996   0 svchost
    159      42     1668       6972              8036   0 svchost
    271      17     2892       9352              8232   0 svchost
    515      20     5468      23776              8272   0 svchost
    476      20     7564      33212       1,20   8576   8 svchost
    312      17     4284      18784              8876   0 svchost
    561      25     8592      34116              9004   0 svchost
    229      13     3112      10488              9048   0 svchost
    224      12     2904      13240              9324   0 svchost
    423      25     5464      22048       0,42   9356   8 svchost
     94       6      988       4780              9856   0 svchost
    204      16     7060      10876             10364   0 svchost
    301      32    29104      28300             10532   0 svchost
    545      34    11724      24780             11432   0 svchost
    196      11     1956       9628             11984   0 svchost
    286      17     3964      16892             12284   0 svchost
    527      17     5528      14892             13092   0 svchost
    202      12     2212       8172             13168   0 svchost
    126       9     1976       7640             15376   0 svchost
    183     114     2240       7604             17732   0 svchost
    150       9     2040       9464       0,05  18020   8 svchost
    213      13     2836      13532             18980   0 svchost
    197      12     1652       8148             19024   0 svchost
    735      26     6852      21656             19628   0 svchost
    264      15     3620      18184       0,06  19904   8 svchost
    285      15     2704      12844             21672   0 svchost
    147       9     1612       7092             21700   0 svchost
    123       8     1260       6136             21776   0 svchost
   5425       0       48        136                 4   0 System
   1528      76   161408       4416       1,38  17192   8 SystemSettings
    559      26     7472      35368       0,05  16848   8 SystemSettingsBroker
    324      35     8032      20944       0,94   9724   8 taskhostw
    139       9     1724       8468             13144   0 unsecapp
    146      10     2028       9944       0,02   6356   8 UserOOBEBroker
    855      51    60816      40624       0,91   5280   8 WhatsApp
    874      37    12640      55184       1,08  16620   8 Widgets
    324      19     4740      22500       0,25   8780   8 WidgetService
    749      34    97488     143064       4,00  12400   8 WindowsTerminal
    161      12     1600       6972              1004   0 wininit
    277      13     2536      11884              4028   8 winlogon
    134       8     1472       6808              2404   0 wlanext
    191      13     2448      10524             17964   0 WmiApSrv
    480      28    34844      39472              5932   0 WmiPrvSE
    181      12     4048      11808             21268   0 WmiPrvSE
    272      14     2844      13544              4728   0 WMIRegistrationService
     95      94     6344       6328              3240   0 WUDFCompanionHost
     94      48     4040       4992              7020   0 WUDFCompanionHost
    498      28     7536      17888              1292   0 WUDFHost
    276      14     4904      12904              1536   0 WUDFHost
    343      14     6412      11556              1956   0 WUDFHost
    215       8     1408       5564              2820   0 WUDFHost
    373      19     5024      22368       0,00  20668   8 XboxPcAppFT

```
🌞 **Trouver les 3 processus qui ont le plus petit identifiant** 

PS C:\Users\Asus> Get-Process | Sort-Object Id | Select-Object -First 3 Name, Id
``` bash
Name           Id
----           --
Idle            0
System          4
Secure System 140
```

🌞 **Lister tous les services de la machine...**
```bash
PS C:\Users\Asus> Get-Service


Status   Name               DisplayName
------   ----               -----------
Stopped  AarSvc_630e019     Agent Activation Runtime_630e019
Running  AdobeARMservice    Adobe Acrobat Update Service
Stopped  AJRouter           Service de routeur AllJoyn
Stopped  ALG                Service de la passerelle de la couc...
Stopped  AppIDSvc           Identité de l’application
Running  Appinfo            Informations d’application
Stopped  AppMgmt            Gestion d’applications
Stopped  AppReadiness       Préparation des applications
Stopped  AppVClient         Microsoft App-V Client
Running  AppXSvc            Service de déploiement AppX (AppXSVC)
Stopped  AssignedAccessM... Service AssignedAccessManager
Running  AsusAppService     ASUS App Service
Running  ASUSOptimization   ASUS Optimization
Running  ASUSSoftwareMan... ASUS Software Manager
Running  ASUSSwitch         ASUS Switch
Running  ASUSSystemAnalysis ASUS System Analysis
Running  ASUSSystemDiagn... ASUS System Diagnosis
Running  AudioEndpointBu... Générateur de points de terminaison...
Running  Audiosrv           Audio Windows
Stopped  autotimesvc        Heure cellulaire
Stopped  AxInstSV           Programme d’installation ActiveX (A...
Stopped  BcastDVRUserSer... Service utilisateur de diffusion et...
Running  BDESVC             Service de chiffrement de lecteur B...
Running  BFE                Moteur de filtrage de base
Running  BITS               Service de transfert intelligent en...
Running  BluetoothUserSe... Service de support des utilisateurs...
Running  BrokerInfrastru... Service d’infrastructure des tâches...
Running  BTAGService        Service de passerelle audio Bluetooth
Running  BthAvctpSvc        Service AVCTP
Running  bthserv            Service de prise en charge Bluetooth
Running  camsvc             Service Gestionnaire d’accès aux fo...
Stopped  CaptureService_... CaptureService_630e019
Running  cbdhsvc_630e019    Service utilisateur du Presse-papie...
Running  CDPSvc             Service de plateforme des appareils...
Running  CDPUserSvc_630e019 Service pour utilisateur de platefo...
Stopped  CertPropSvc        Propagation du certificat
Stopped  ClipSVC            Service de licences de client (Clip...
Stopped  CloudBackupRest... Service de restauration et de sauve...
Stopped  cloudidsvc         Service d’identité de Microsoft Cloud
Stopped  COMSysApp          Application système COM+
Stopped  ConsentUxUserSv... Service utilisateur ConsentUX_630e019
Running  CoreMessagingRe... CoreMessaging
Running  cplspcon           Intel(R) Content Protection HDCP Se...
Stopped  CredentialEnrol... CredentialEnrollmentManagerUserSvc_...
Running  CryptSvc           Services de chiffrement
Stopped  CscService         Fichiers hors connexion
Running  DcomLaunch         Lanceur de processus serveur DCOM
Stopped  dcsvc              Service de configuration (DC) déclaré
Stopped  defragsvc          Optimiser les lecteurs
Stopped  DeviceAssociati... DeviceAssociationBroker_630e019
Running  DeviceAssociati... Service d’association de périphérique
Running  DeviceInstall      Service d’installation de périphérique
Stopped  DevicePickerUse... DevicePicker_630e019
Running  DevicesFlowUser... Flux d’appareils_630e019
Stopped  DevQueryBroker     Service Broker de découverte en arr...
Running  Dhcp               Client DHCP
Stopped  diagnosticshub.... Service Collecteur standard du conc...
Stopped  diagsvc            Diagnostic Execution Service
Running  DiagTrack          Expériences des utilisateurs connec...
Stopped  DialogBlockingS... DialogBlockingService
Running  DiracAudSrv        Dirac Audio Service
Running  DispBrokerDeskt... Service de stratégie d'affichage
Running  DisplayEnhancem... Service d'amélioration de l'affichage
Stopped  DmEnrollmentSvc    Service d'inscription de la gestion...
Stopped  dmwappushservice   Service de routage de messages Push...
Running  Dnscache           Client DNS
Running  DoSvc              Optimisation de livraison
Stopped  dot3svc            Configuration automatique de réseau...
Running  DPS                Service de stratégie de diagnostic
Running  dptftcs            Intel(R) Dynamic Tuning Technology ...
Stopped  DsmSvc             Gestionnaire d’installation de péri...
Running  DsSvc              Service de partage des données
Running  DusmSvc            Consommation des données
Running  EapHost            Protocole EAP (Extensible Authentic...
Stopped  edgeupdate         Microsoft Edge Update Service (edge...
Stopped  edgeupdatem        Microsoft Edge Update Service (edge...
Running  EFS                Système de fichiers EFS (Encrypting...
Stopped  embeddedmode       Mode incorporé
Stopped  EntAppSvc          Service de gestion des applications...
Running  EventLog           Journal d’événements Windows
Running  EventSystem        Système d’événement COM+
Stopped  fdPHost            Hôte du fournisseur de découverte d...
Stopped  FDResPub           Publication des ressources de décou...
Stopped  fhsvc              Service d’historique des fichiers
Running  focalFpSrvcDeamon  Focalfp Service
Running  FontCache          Service de cache de police Windows
Stopped  FrameServer        Serveur de trame de la Caméra Windows
Stopped  FrameServerMonitor Moniteur de serveur de trame Caméra...
Stopped  GameInputSvc       GameInput Service
Running  GamingServices     Gaming Services
Running  GamingServicesNet  Gaming Services
Stopped  GoogleChromeEle... Google Chrome Elevation Service (Go...
Stopped  GoogleUpdaterIn... Service interne de mise à jour Goog...
Stopped  GoogleUpdaterSe... Service de mise à jour Google (Goog...
Running  gpsvc              Client de stratégie de groupe
Stopped  GraphicsPerfSvc    GraphicsPerfSvc
Stopped  hidserv            Service du périphérique d’interface...
Running  HvHost             Service d'hôte HV
Stopped  icssvc             Service Point d'accès sans fil mobi...
Running  igccservice        Intel(R) Graphics Command Center Se...
Running  IgoAudioService    Intelligo Audio Service
Stopped  IKEEXT             Modules de génération de clés IKE e...
Running  InstallService     Installation du service Microsoft S...
Stopped  Intel(R) Platfo... Intel(R) Platform License Manager S...
Running  IntelAudioService  Intel(R) Audio Service
Running  InventorySvc       Service d’Appraisal inventaire et c...
Running  ipfsvc             Intel(R) Innovation Platform Framew...
Running  iphlpsvc           Assistance IP
Stopped  IpxlatCfgSvc       Service de configuration de convers...
Running  jhi_service        Intel(R) Dynamic Application Loader...
Running  KeyIso             Isolation de clé CNG
Stopped  KtmRm              Service KtmRm pour Distributed Tran...
Running  LanmanServer       Serveur
Running  LanmanWorkstation  Station de travail
Running  lfsvc              Service de géolocalisation
Running  LicenseManager     Serveur Gestionnaire de licences Wi...
Stopped  lltdsvc            Mappage de découverte de topologie ...
Running  lmhosts            Assistance NetBIOS sur TCP/IP
Running  LSM                Gestionnaire de session locale
Stopped  LxpSvc             Service d'expérience linguistique
Stopped  MapsBroker         Gestionnaire des cartes téléchargées
Stopped  McpManagementSe... McpManagementService
Running  MDCoreSvc          Microsoft Defender Service de base
Stopped  MessagingServic... MessagingService_630e019
Stopped  MicrosoftEdgeEl... Microsoft Edge Elevation Service (M...
Stopped  MixedRealityOpe... Service Windows Mixed Reality OpenXR
Running  mpssvc             Pare-feu Windows Defender
Stopped  MSDTC              Coordinateur de transactions distri...
Stopped  MSiSCSI            Service Initiateur iSCSI de Microsoft
Stopped  msiserver          Windows Installer
Stopped  MsKeyboardFilter   Filtre clavier Microsoft
Stopped  NaturalAuthenti... Authentification naturelle
Stopped  NcaSvc             Assistant Connectivité réseau
Running  NcbService         Service Broker pour les connexions ...
Stopped  NcdAutoSetup       Configuration automatique des périp...
Stopped  Netlogon           Netlogon
Running  Netman             Connexions réseau
Running  netprofm           Service Liste des réseaux
Running  NetSetupSvc        Service Configuration du réseau
Stopped  NetTcpPortSharing  Service de partage de ports Net.Tcp
Stopped  NgcCtnrSvc         Conteneur Microsoft Passport
Stopped  NgcSvc             Microsoft Passport
Stopped  NlaSvc             Connaissance des emplacements réseau
Running  NPSMSvc_630e019    NPSMSvc_630e019
Running  nsi                Service Interface du magasin réseau
Running  OneSyncSvc_630e019 Hôte de synchronisation_630e019
Stopped  p2pimsvc           Identity Manager réseau homologue
Stopped  p2psvc             Groupement de mise en réseau de pairs
Stopped  P9RdrService_63... P9RdrService_630e019
Running  PcaSvc             Service de l’Assistant Compatibilit...
Stopped  PeerDistSvc        BranchCache
Stopped  PenService_630e019 PenService_630e019
Stopped  perceptionsimul... Service de simulation de perception...
Stopped  PerfHost           Hôte de DLL de compteur de performance
Running  PhoneSvc           Service téléphonique
Running  PimIndexMainten... Données de contacts_630e019
Stopped  pla                Journaux & alertes de performance
Running  PlugPlay           Plug-and-Play
Stopped  PNRPAutoReg        Service de publication des noms d’o...
Stopped  PNRPsvc            Protocole PNRP
Stopped  PolicyAgent        Agent de stratégie IPsec
Running  Power              Alimentation
Stopped  PrintNotify        Extensions et notifications d’impri...
Stopped  PrintWorkflowUs... PrintWorkflow_630e019
Running  ProfSvc            Service de profil utilisateur
Stopped  PushToInstall      Service PushToInstall de Windows
Running  QWAVE              Expérience audio-vidéo haute qualit...
Stopped  RasAuto            Gestionnaire des connexions automat...
Running  RasMan             Gestionnaire des connexions d’accès...
Stopped  RemoteAccess       Routage et accès distant
Stopped  RemoteRegistry     Registre à distance
Stopped  RetailDemo         Service de démo du magasin
Running  RmSvc              Service de gestion radio
Running  RpcEptMapper       Mappeur de point de terminaison RPC
Stopped  RpcLocator         Localisateur d’appels de procédure ...
Running  RpcSs              Appel de procédure distante (RPC)
Running  RtkAudioUnivers... Realtek Audio Universal Service
Running  SamSs              Gestionnaire de comptes de sécurité
Stopped  SCardSvr           Carte à puce
Stopped  ScDeviceEnum       Service d’énumération de périphériq...
Running  Schedule           Planificateur de tâches
Stopped  SCPolicySvc        Stratégie de retrait de la carte à ...
Stopped  SDRSVC             Sauvegarde Windows
Stopped  seclogon           Ouverture de session secondaire
Running  SecurityHealthS... Service Sécurité Windows
Stopped  SEMgrSvc           Gestionnaires des paiements et des ...
Running  SENS               Service de notification d’événement...
Stopped  Sense              Service Protection avancée contre l...
Stopped  SensorDataService  Service Données de capteur
Stopped  SensorService      Service de capteur
Stopped  SensrSvc           Service de surveillance des capteurs
Stopped  SessionEnv         Configuration des services Bureau à...
Stopped  SgrmBroker         Service Broker du moniteur d'exécut...
Stopped  SharedAccess       Partage de connexion Internet (ICS)
Stopped  SharedRealitySvc   Service de données spatiales
Running  ShellHWDetection   Détection matériel noyau
Stopped  shpamsvc           Shared PC Account Manager
Stopped  smphost            SMP de l’Espace de stockages Microsoft
Stopped  SmsRouter          Service Routeur SMS Microsoft Windows.
Stopped  SNMPTrap           Interruption SNMP
Stopped  spectrum           Service de perception Windows
Running  Spooler            Spouleur d’impression
Stopped  sppsvc             Protection logicielle
Running  SSDPSRV            Découverte SSDP
Stopped  ssh-agent          OpenSSH Authentication Agent
Running  SstpSvc            Service SSTP (Secure Socket Tunneli...
Running  StateRepository    Service State Repository (StateRepo...
Running  Steam Client Se... Steam Client Service
Running  StiSvc             Acquisition d’image Windows (WIA)
Running  StorSvc            Service de stockage
Stopped  svsvc              Vérificateur de points
Stopped  swprv              Fournisseur de cliché instantané de...
Running  SysMain            SysMain
Running  SystemEventsBroker Service Broker des événements système
Running  TapiSrv            Téléphonie
Stopped  TermService        Services Bureau à distance
Running  TextInputManage... Service de gestion des entrées de t...
Running  Themes             Thèmes
Stopped  TieringEngineSe... Gestion des niveaux de stockage
Running  TimeBrokerSvc      Service Broker pour les événements ...
Running  TokenBroker        Gestionnaire de comptes web
Running  TrkWks             Client de suivi de lien distribué
Stopped  TroubleshootingSvc Service de résolution des problèmes...
Stopped  TrustedInstaller   Programme d’installation pour les m...
Stopped  tzautoupdate       Programme de mise à jour automatiqu...
Running  UdkUserSvc_630e019 Service utilisateur du kit de dével...
Stopped  UevAgentService    Service User Experience Virtualization
Stopped  uhssvc             Microsoft Update Health Service
Stopped  UmRdpService       Redirecteur de port du mode utilisa...
Running  UnistoreSvc_630... Stockage des données utilisateur_63...
Stopped  upnphost           Hôte de périphérique UPnP
Running  UserDataSvc_630... Accès aux données utilisateur_630e019
Running  UserManager        Gestionnaire des utilisateurs
Running  UsoSvc             Service Orchestrator pour les mises...
Stopped  VacSvc             Service de composition audio volumé...
Running  VaultSvc           Gestionnaire d’informations d’ident...
Stopped  vds                Disque virtuel
Stopped  vmicguestinterface Interface de services d’invité Hyper-V
Stopped  vmicheartbeat      Service Pulsation Microsoft Hyper-V
Stopped  vmickvpexchange    Service Échange de données Microsof...
Stopped  vmicrdv            Service de virtualisation Bureau à ...
Stopped  vmicshutdown       Service Arrêt de l’invité Microsoft...
Stopped  vmictimesync       Service Synchronisation date/heure ...
Stopped  vmicvmsession      Service Hyper-V PowerShell Direct
Stopped  vmicvss            Requête du service VSS Hyper-V
Stopped  VSS                Cliché instantané des volumes
Running  W32Time            Temps Windows
Stopped  WaaSMedicSvc       WaaSMedicSvc
Stopped  WalletService      WalletService
Stopped  WarpJITSvc         Warp JIT Service
Stopped  wbengine           Service de moteur de sauvegarde en ...
Stopped  WbioSrvc           Service de biométrie Windows
Running  Wcmsvc             Gestionnaire des connexions Windows
Stopped  wcncsvc            Windows Connect Now - Registre de c...
Stopped  WdiServiceHost     Service hôte WDIServiceHost
Running  WdiSystemHost      Hôte système de diagnostics
Running  WdNisSvc           Service d’inspection réseau de l’an...
Stopped  WebClient          WebClient
Running  webthreatdefsvc    Service Web Threat Defense
Running  webthreatdefuse... Service d’utilisateur Web Threat De...
Stopped  Wecsvc             Collecteur d’événements de Windows
Stopped  WEPHOSTSVC         Service hôte du fournisseur de chif...
Stopped  wercplsupport      Prise en charge du Panneau de confi...
Stopped  WerSvc             Service de rapport d’erreurs Windows
Stopped  WFDSConMgrSvc      Service Wi-Fi Direct Service de ges...
Stopped  WiaRpc             Événements d’acquisition d’images f...
Running  WinDefend          Service antivirus Microsoft Defender
Running  WinHttpAutoProx... Service de découverte automatique d...
Running  Winmgmt            Infrastructure de gestion Windows
Stopped  WinRM              Gestion à distance de Windows (Gest...
Stopped  wisvc              Service Windows Insider
Running  WlanSvc            Service de configuration automatiqu...
Stopped  wlidsvc            Assistant Connexion avec un compte ...
Stopped  wlpasvc            Service de l’Assistant de profil local
Stopped  WManSvc            Service de gestion de Windows
Running  wmiApSrv           Carte de performance WMI
Running  WMIRegistration... Intel(R) Management Engine WMI Prov...
Stopped  WMPNetworkSvc      Service de partage réseau du Lecteu...
Stopped  workfolderssvc     Dossiers de travail
Stopped  WpcMonSvc          Contrôle parental
Stopped  WPDBusEnum         Service Énumérateur d’appareil mobile
Running  WpnService         Service du système de notifications...
Running  WpnUserService_... Service utilisateur de notification...
Running  wscsvc             Centre de sécurité
Running  WSearch            Windows Search
Stopped  wuauserv           Windows Update
Stopped  WwanSvc            Service de configuration automatiqu...
Running  XblAuthManager     Gestionnaire d'authentification Xbo...
Stopped  XblGameSave        Jeu sauvegardé sur Xbox Live
Stopped  XboxGipSvc         Xbox Accessory Management Service
Stopped  XboxNetApiSvc      Service de mise en réseau Xbox Live
```
```bash 
PS C:\Users\Asus> Get-Service | Where-Object { $_.Status -eq 'Stopped' }

Status   Name               DisplayName
------   ----               -----------
Stopped  AarSvc_630e019     Agent Activation Runtime_630e019
Stopped  AJRouter           Service de routeur AllJoyn
Stopped  ALG                Service de la passerelle de la couc...
Stopped  AppIDSvc           Identité de l’application
Stopped  AppMgmt            Gestion d’applications
Stopped  AppReadiness       Préparation des applications
Stopped  AppVClient         Microsoft App-V Client
Stopped  AssignedAccessM... Service AssignedAccessManager
Stopped  autotimesvc        Heure cellulaire
Stopped  AxInstSV           Programme d’installation ActiveX (A...
Stopped  BcastDVRUserSer... Service utilisateur de diffusion et...
Stopped  CaptureService_... CaptureService_630e019
Stopped  CertPropSvc        Propagation du certificat
Stopped  ClipSVC            Service de licences de client (Clip...
Stopped  CloudBackupRest... Service de restauration et de sauve...
Stopped  cloudidsvc         Service d’identité de Microsoft Cloud
Stopped  COMSysApp          Application système COM+
Stopped  ConsentUxUserSv... Service utilisateur ConsentUX_630e019
Stopped  CredentialEnrol... CredentialEnrollmentManagerUserSvc_...
Stopped  CscService         Fichiers hors connexion
Stopped  dcsvc              Service de configuration (DC) déclaré
Stopped  defragsvc          Optimiser les lecteurs
Stopped  DeviceAssociati... DeviceAssociationBroker_630e019
Stopped  DevicePickerUse... DevicePicker_630e019
Stopped  DevQueryBroker     Service Broker de découverte en arr...
Stopped  diagnosticshub.... Service Collecteur standard du conc...
Stopped  diagsvc            Diagnostic Execution Service
Stopped  DialogBlockingS... DialogBlockingService
Stopped  DmEnrollmentSvc    Service d'inscription de la gestion...
Stopped  dmwappushservice   Service de routage de messages Push...
Stopped  dot3svc            Configuration automatique de réseau...
Stopped  DsmSvc             Gestionnaire d’installation de péri...
Stopped  edgeupdate         Microsoft Edge Update Service (edge...
Stopped  edgeupdatem        Microsoft Edge Update Service (edge...
Stopped  embeddedmode       Mode incorporé
Stopped  EntAppSvc          Service de gestion des applications...
Stopped  fdPHost            Hôte du fournisseur de découverte d...
Stopped  FDResPub           Publication des ressources de décou...
Stopped  fhsvc              Service d’historique des fichiers
Stopped  FrameServer        Serveur de trame de la Caméra Windows
Stopped  FrameServerMonitor Moniteur de serveur de trame Caméra...
Stopped  GameInputSvc       GameInput Service
Stopped  GoogleChromeEle... Google Chrome Elevation Service (Go...
Stopped  GoogleUpdaterIn... Service interne de mise à jour Goog...
Stopped  GoogleUpdaterSe... Service de mise à jour Google (Goog...
Stopped  GraphicsPerfSvc    GraphicsPerfSvc
Stopped  hidserv            Service du périphérique d’interface...
Stopped  icssvc             Service Point d'accès sans fil mobi...
Stopped  IKEEXT             Modules de génération de clés IKE e...
Stopped  Intel(R) Platfo... Intel(R) Platform License Manager S...
Stopped  IpxlatCfgSvc       Service de configuration de convers...
Stopped  KtmRm              Service KtmRm pour Distributed Tran...
Stopped  lltdsvc            Mappage de découverte de topologie ...
Stopped  LxpSvc             Service d'expérience linguistique
Stopped  MapsBroker         Gestionnaire des cartes téléchargées
Stopped  McpManagementSe... McpManagementService
Stopped  MessagingServic... MessagingService_630e019
Stopped  MicrosoftEdgeEl... Microsoft Edge Elevation Service (M...
Stopped  MixedRealityOpe... Service Windows Mixed Reality OpenXR
Stopped  MSDTC              Coordinateur de transactions distri...
Stopped  MSiSCSI            Service Initiateur iSCSI de Microsoft
Stopped  msiserver          Windows Installer
Stopped  MsKeyboardFilter   Filtre clavier Microsoft
Stopped  NaturalAuthenti... Authentification naturelle
Stopped  NcaSvc             Assistant Connectivité réseau
Stopped  NcdAutoSetup       Configuration automatique des périp...
Stopped  Netlogon           Netlogon
Stopped  NetTcpPortSharing  Service de partage de ports Net.Tcp
Stopped  NgcCtnrSvc         Conteneur Microsoft Passport
Stopped  NgcSvc             Microsoft Passport
Stopped  NlaSvc             Connaissance des emplacements réseau
Stopped  p2pimsvc           Identity Manager réseau homologue
Stopped  p2psvc             Groupement de mise en réseau de pairs
Stopped  P9RdrService_63... P9RdrService_630e019
Stopped  PeerDistSvc        BranchCache
Stopped  PenService_630e019 PenService_630e019
Stopped  perceptionsimul... Service de simulation de perception...
Stopped  PerfHost           Hôte de DLL de compteur de performance
Stopped  pla                Journaux & alertes de performance
Stopped  PNRPAutoReg        Service de publication des noms d’o...
Stopped  PNRPsvc            Protocole PNRP
Stopped  PolicyAgent        Agent de stratégie IPsec
Stopped  PrintNotify        Extensions et notifications d’impri...
Stopped  PrintWorkflowUs... PrintWorkflow_630e019
Stopped  PushToInstall      Service PushToInstall de Windows
Stopped  RasAuto            Gestionnaire des connexions automat...
Stopped  RemoteAccess       Routage et accès distant
Stopped  RemoteRegistry     Registre à distance
Stopped  RetailDemo         Service de démo du magasin
Stopped  RpcLocator         Localisateur d’appels de procédure ...
Stopped  SCardSvr           Carte à puce
Stopped  ScDeviceEnum       Service d’énumération de périphériq...
Stopped  SCPolicySvc        Stratégie de retrait de la carte à ...
Stopped  SDRSVC             Sauvegarde Windows
Stopped  seclogon           Ouverture de session secondaire
Stopped  SEMgrSvc           Gestionnaires des paiements et des ...
Stopped  Sense              Service Protection avancée contre l...
Stopped  SensorDataService  Service Données de capteur
Stopped  SensorService      Service de capteur
Stopped  SensrSvc           Service de surveillance des capteurs
Stopped  SessionEnv         Configuration des services Bureau à...
Stopped  SgrmBroker         Service Broker du moniteur d'exécut...
Stopped  SharedAccess       Partage de connexion Internet (ICS)
Stopped  SharedRealitySvc   Service de données spatiales
Stopped  shpamsvc           Shared PC Account Manager
Stopped  smphost            SMP de l’Espace de stockages Microsoft
Stopped  SmsRouter          Service Routeur SMS Microsoft Windows.
Stopped  SNMPTrap           Interruption SNMP
Stopped  spectrum           Service de perception Windows
Stopped  sppsvc             Protection logicielle
Stopped  ssh-agent          OpenSSH Authentication Agent
Stopped  svsvc              Vérificateur de points
Stopped  swprv              Fournisseur de cliché instantané de...
Stopped  TermService        Services Bureau à distance
Stopped  TieringEngineSe... Gestion des niveaux de stockage
Stopped  TroubleshootingSvc Service de résolution des problèmes...
Stopped  TrustedInstaller   Programme d’installation pour les m...
Stopped  tzautoupdate       Programme de mise à jour automatiqu...
Stopped  UevAgentService    Service User Experience Virtualization
Stopped  uhssvc             Microsoft Update Health Service
Stopped  UmRdpService       Redirecteur de port du mode utilisa...
Stopped  upnphost           Hôte de périphérique UPnP
Stopped  VacSvc             Service de composition audio volumé...
Stopped  vds                Disque virtuel
Stopped  vmicguestinterface Interface de services d’invité Hyper-V
Stopped  vmicheartbeat      Service Pulsation Microsoft Hyper-V
Stopped  vmickvpexchange    Service Échange de données Microsof...
Stopped  vmicrdv            Service de virtualisation Bureau à ...
Stopped  vmicshutdown       Service Arrêt de l’invité Microsoft...
Stopped  vmictimesync       Service Synchronisation date/heure ...
Stopped  vmicvmsession      Service Hyper-V PowerShell Direct
Stopped  vmicvss            Requête du service VSS Hyper-V
Stopped  VSS                Cliché instantané des volumes
Stopped  WaaSMedicSvc       WaaSMedicSvc
Stopped  WalletService      WalletService
Stopped  WarpJITSvc         Warp JIT Service
Stopped  wbengine           Service de moteur de sauvegarde en ...
Stopped  WbioSrvc           Service de biométrie Windows
Stopped  wcncsvc            Windows Connect Now - Registre de c...
Stopped  WdiServiceHost     Service hôte WDIServiceHost
Stopped  WebClient          WebClient
Stopped  Wecsvc             Collecteur d’événements de Windows
Stopped  WEPHOSTSVC         Service hôte du fournisseur de chif...
Stopped  wercplsupport      Prise en charge du Panneau de confi...
Stopped  WerSvc             Service de rapport d’erreurs Windows
Stopped  WFDSConMgrSvc      Service Wi-Fi Direct Service de ges...
Stopped  WiaRpc             Événements d’acquisition d’images f...
Stopped  WinRM              Gestion à distance de Windows (Gest...
Stopped  wisvc              Service Windows Insider
Stopped  wlpasvc            Service de l’Assistant de profil local
Stopped  WManSvc            Service de gestion de Windows
Stopped  WMPNetworkSvc      Service de partage réseau du Lecteu...
Stopped  workfolderssvc     Dossiers de travail
Stopped  WpcMonSvc          Contrôle parental
Stopped  WPDBusEnum         Service Énumérateur d’appareil mobile
Stopped  wuauserv           Windows Update
Stopped  WwanSvc            Service de configuration automatiqu...
Stopped  XblGameSave        Jeu sauvegardé sur Xbox Live
Stopped  XboxGipSvc         Xbox Accessory Management Service
Stopped  XboxNetApiSvc      Service de mise en réseau Xbox Live
```

## 2. Mémoire et CPU
🌞 **RAM**
```bash
PS C:\Users\Asus> Get-ComputerInfo | Select-Object TotalPhysicalMemory, AvailablePhysicalMemory

TotalPhysicalMemory AvailablePhysicalMemory
------------------- -----------------------
```

```bash
PS C:\Users\Asus> Get-CimInstance Win32_OperatingSystem | Select-Object FreePhysicalMemory

FreePhysicalMemory
------------------
          14978104
```

🌞 **CPU**
```bash
PS C:\Users\Asus> Get-CimInstance Win32_Processor | Select-Object LoadPercentage

LoadPercentage
--------------
             1
```

## 3. Stockage
🌞 **Périphériques**

```bash
PS C:\Users\Asus> Get-Disk | Select-Object Manufacturer, Model, Size

Manufacturer Model                          Size
------------ -----                          ----
             SOLIDIGM SSDPFKNU512GZ 512110190592
```

🌞 **Partitions**

```bash 
PS C:\Users\Asus> Get-Partition


   DiskPath : \\?\scsi#disk&ven_nvme&prod_solidigm_ssdpfkn#5&8c5c54c&0&000000#{53f56307-b6bf-11d0-94f2-00a0c91efb8b}

PartitionNumber  DriveLetter Offset                                        Size Type
---------------  ----------- ------                                        ---- ----
1                           17408                                       128 MB Reserved
2                           135266304                                   100 MB System
3                C           240123904                                475.96 GB Basic
4                           511292997632                                779 MB Recovery
```

🌞 **Espace disque**
```bash

PS C:\Users\Asus> Get-PSDrive C | Select-Object Used, Free, @{Name='Total'; Expression={[math]::round($_.Used + $_.Free, 2)}}

        Used         Free        Total
        ----         ----        -----
171556315136 339496554496 511052869632
```

## 4. Réseau

🌞 **Cartes réseau**
```bash
PS C:\Users\Asus> Get-NetAdapter | Select-Object Name, @{Name='IP Address'; Expression={(Get-NetIPAddress -InterfaceAlias $_.Name | Select-Object -ExpandProperty IPAddress)}}

Name       IP Address
----       ----------
Wi-Fi      {fe80::e7bb:428d:a8e:7301%16, 10.3.220.148}
Ethernet 2 {fe80::16e1:2f5b:1eda:3f2%6, 169.254.212.123}
```

🌞 **Connexions réseau**

```bash
PS C:\Users\Asus> Get-NetTCPConnection | Where-Object { $_.State -eq 'Established' } | Select-Object RemoteAddress, @{Name='ProcessId'; Expression={$_.OwningProcess}}, @{Name='ProcessName'; Expression={(Get-Process -Id $_.OwningProcess).Name}}

RemoteAddress   ProcessId ProcessName
-------------   --------- -----------
34.120.22.49        20796 chrome
44.194.214.249      20796 chrome
104.18.32.47        20796 chrome
104.18.32.47        20796 chrome
162.159.130.234     15112 Discord
52.112.100.64       20796 chrome
52.123.159.3        20796 chrome
172.65.251.78       20796 chrome
10.3.201.187        19628 svchost
74.125.71.188       20796 chrome
127.0.0.1           15812 steamwebhelper
127.0.0.1           15812 steamwebhelper
127.0.0.1            9796 steam
127.0.0.1            9796 steam
127.0.0.1            4244 ipfsvc
127.0.0.1            4244 ipfsvc
127.0.0.1            1536 WUDFHost
127.0.0.1            1536 WUDFHost
127.0.0.1            1292 WUDFHost
127.0.0.1            1292 WUDFHost
20.199.120.85        4756 svchost
10.3.220.143        19628 svchost
10.3.217.117        19628 svchost
10.3.205.63         19628 svchost
```

## 5. Utilisateurs

🌞 **Lister les utilisateurs de la machine**
```bash
PS C:\Users\Asus> Get-LocalUser

Name               Enabled Description
----               ------- -----------
Administrateur     False   Compte d’utilisateur d’administration
Asus               True
DefaultAccount     False   Compte utilisateur géré par le système.
Invité             False   Compte d’utilisateur invité
WDAGUtilityAccount False   Compte d’utilisateur géré et utilisé par le système pour les scénarios Windows Defender A...
```

🌞 **Heure de login**
```bash
PS C:\Users\Asus>  Get-CimInstance -ClassName ‘Win32_LogonSession’ | Where {$_.LogonType -eq ‘2’}

LogonId   Name LogonType StartTime           Status AuthenticationPackage
-------   ---- --------- ---------           ------ ---------------------
103787465      2         03/11/2024 18:52:44        NTLM
103787335      2         03/11/2024 18:52:44        NTLM
65692911       2         31/10/2024 18:35:06        NTLM
65692840       2         31/10/2024 18:35:06        NTLM
49929470       2         30/10/2024 14:31:34        NTLM
49929298       2         30/10/2024 14:31:34        NTLM
42673151       2         29/10/2024 18:58:02        NTLM
42673010       2         29/10/2024 18:58:02        NTLM
38723871       2         28/10/2024 22:23:01        NTLM
38723832       2         28/10/2024 22:23:01        NTLM
22029531       2         28/10/2024 14:15:20        NTLM
22029389       2         28/10/2024 14:15:20        NTLM
17735322       2         28/10/2024 13:59:09        NTLM
17735161       2         28/10/2024 13:59:09        NTLM
143183         2         27/10/2024 19:34:06        NTLM
142924         2         27/10/2024 19:34:06        NTLM
105293         2         27/10/2024 19:34:05        Negotiate
105159         2         27/10/2024 19:34:05        Negotiate
17552450       2         28/10/2024 00:14:46        Negotiate
17552406       2         28/10/2024 00:14:46        Negotiate
21881677       2         28/10/2024 14:08:46        Negotiate
21881649       2         28/10/2024 14:08:46        Negotiate
38517645       2         28/10/2024 19:29:01        Negotiate
38517611       2         28/10/2024 19:29:01        Negotiate
42530193       2         28/10/2024 22:50:57        Negotiate
42530157       2         28/10/2024 22:50:57        Negotiate
49783142       2         29/10/2024 19:28:00        Negotiate
49783100       2         29/10/2024 19:28:00        Negotiate
65525028       2         30/10/2024 17:08:32        Negotiate
65524980       2         30/10/2024 17:08:32        Negotiate
103626117      2         01/11/2024 01:09:13        Negotiate
103626091      2         01/11/2024 01:09:13        Negotiate
64022          2         27/10/2024 19:34:05        Negotiate
64006          2         27/10/2024 19:34:05        Negotiate
17548687       2         28/10/2024 00:14:46        Negotiate
21877958       2         28/10/2024 14:08:46        Negotiate
38515387       2         28/10/2024 19:29:01        Negotiate
42526980       2         28/10/2024 22:50:57        Negotiate
49779901       2         29/10/2024 19:28:00        Negotiate
65521822       2         30/10/2024 17:08:32        Negotiate
103622826      2         01/11/2024 01:09:13        Negotiate
```

🌞 **Lister les processus en cours d'exécution**

```bash



PS C:\Users\Asus> Get-Process | Select-Object Id, ProcessName, @{Name='UserName'; Expression={(Get-WmiObject Win32_Process -Filter "ProcessId=$($_.Id)").GetOwner().User}}

   Id ProcessName          UserName
   -- -----------          --------
 6332 AdobeCollabSync      Asus
23432 AdobeCollabSync      Asus
 3516 AggregatorHost
 6716 ApplicationFrameHost Asus
 4124 armsvc
 4176 AsusAppService
 3800 AsusOptimization
18276 AsusOptimizationS... Asus
 2200 AsusSoftwareManager
16704 AsusSoftwareManag... Asus
 1960 AsusSupportService   Asus
 3136 AsusSwitch
 4108 AsusSystemAnalysis
20396 AsusSystemAnalysis   Asus
 4144 AsusSystemDiagnosis
  664 backgroundTaskHost   Asus
 2836 backgroundTaskHost   Asus
 4656 backgroundTaskHost   Asus
 4740 backgroundTaskHost   Asus
11408 backgroundTaskHost   Asus
12076 backgroundTaskHost   Asus
17164 backgroundTaskHost   Asus
21528 backgroundTaskHost   Asus
22952 backgroundTaskHost   Asus
22232 chrome               Asus
22780 chrome               Asus
23164 chrome               Asus
23244 chrome               Asus
 3140 conhost
22920 conhost              Asus
 1056 CrossDeviceService   Asus
  916 csrss
15732 csrss
20216 ctfmon               Asus
 4160 DiracAudSrv
 9448 Discord              Asus
12876 Discord              Asus
15112 Discord              Asus
15840 Discord              Asus
16676 Discord              Asus
18576 Discord              Asus
11444 dllhost              Asus
14544 dllhost              Asus
22204 dllhost              Asus
12504 dwm
10008 explorer             Asus
 4284 focalFpSrvcDeamon
 1260 fontdrvhost
11536 fontdrvhost
10128 gamingservices
 5412 gamingservicesnet
    0 Idle
 4136 IgoAudioService_x64
 3564 iGoSwServer
15352 iGoSwServer          Asus
 4184 IntelAudioService
 1892 IntelCpHDCPSvc
12648 ipf_helper           Asus
 4324 ipf_uf
 4244 ipfsvc
 4488 jhi_service
19624 LocationNotificat... Asus
 1088 LsaIso
 1100 lsass
 2984 Memory Compression
 9368 MoUsoCoreWorker
 4344 MpDefenderCoreSer...
 5404 msedgewebview2       Asus
 5528 msedgewebview2       Asus
 7000 msedgewebview2       Asus
11188 msedgewebview2       Asus
12428 msedgewebview2       Asus
14492 msedgewebview2       Asus
15568 msedgewebview2       Asus
 4660 MsMpEng
11880 NisSrv
 4116 OneApp.IGCC.WinSe...
19284 OpenConsole          Asus
21936 OpenConsole          Asus
21988 OpenConsole          Asus
22220 OpenConsole          Asus
18308 PhoneExperienceHost  Asus
 6904 powershell           Asus
13436 powershell           Asus
21928 powershell           Asus
21944 powershell           Asus
  172 Registry
 4464 RtkAudUService64
11728 RtkAudUService64     Asus
 5700 RuntimeBroker        Asus
13240 RuntimeBroker        Asus
16108 RuntimeBroker        Asus
17652 RuntimeBroker        Asus
19520 RuntimeBroker        Asus
23040 RuntimeBroker        Asus
12960 SearchHost           Asus
 9224 SearchIndexer
  140 Secure System
11068 SecurityHealthSer...
 8652 SecurityHealthSys... Asus
  920 services
 5364 ShellExperienceHost  Asus
10172 sihost               Asus
  652 smss
 3976 spoolsv
 8356 StartMenuExperien... Asus
 9796 steam                Asus
14816 steamservice
 2572 steamwebhelper       Asus
 7004 steamwebhelper       Asus
 7548 steamwebhelper       Asus
10836 steamwebhelper       Asus
10984 steamwebhelper       Asus
12560 steamwebhelper       Asus
15772 steamwebhelper       Asus
15812 steamwebhelper       Asus
 3296 svchost
 3396 svchost              Asus
 4704 svchost
 4716 svchost
 4756 svchost
 5472 svchost
 5792 svchost              Asus
 5940 svchost
 6516 svchost
 6824 svchost
 6912 svchost
 6940 svchost              Asus
 7448 svchost              Asus
 7456 svchost
 7812 svchost              Asus
 7864 svchost
 8232 svchost
 8272 svchost
 8576 svchost              Asus
 8876 svchost
 9004 svchost
 9048 svchost
 9324 svchost
 9356 svchost              Asus
 9388 svchost
 9856 svchost
17732 svchost
18020 svchost              Asus
18980 svchost
19024 svchost
19628 svchost
19904 svchost              Asus
21672 svchost
21776 svchost
22848 svchost
23020 svchost
    4 System
17192 SystemSettings       Asus
16848 SystemSettingsBroker Asus
 9724 taskhostw            Asus
13144 unsecapp
 6356 UserOOBEBroker       Asus
 5280 WhatsApp             Asus
16620 Widgets              Asus
 8780 WidgetService        Asus
 9524 WindowsTerminal      Asus
12400 WindowsTerminal      Asus
 1004 wininit
 4028 winlogon
 2404 wlanext
17964 WmiApSrv
 5932 WmiPrvSE
21268 WmiPrvSE
 4728 WMIRegistrationSe...
 3240 WUDFCompanionHost
 7020 WUDFCompanionHost
 1292 WUDFHost
 1536 WUDFHost
 1956 WUDFHost
 2820 WUDFHost
20668 XboxPcAppFT          Asus
```

🌞 **Sur un fichier random qui se trouve dans votre dossier Téléchargements/**

```bash
PS C:\Users\Asus> $path = "$env:USERPROFILE\Downloads\SteamSetup.exe"
PS C:\Users\Asus>  Get-Acl $path | Select-Object Owner

Owner
-----
ASUSEXPERTBOOK\Asus
```

## 6. Random
🌞 **Uptime**
```bash

PS C:\Users\Asus> (Get-CimInstance -ClassName Win32_OperatingSystem).LastBootUpTime

lundi 4 novembre 2024 14:03:42
```

🌞 **Device**

```bash
PS C:\Users\Asus> Get-CimInstance -ClassName Win32_Processor | Select-Object Name

Name
----
13th Gen Intel(R) Core(TM) i7-1355U
```

🌞 **Version**

```bash
PS C:\Users\Asus> Get-CimInstance -ClassName Win32_OperatingSystem | Select-Object Caption, Version

Caption                            Version
-------                            -------
Microsoft Windows 11 Professionnel 10.0.22631
```

🌞 **Mise à jour**
```bash
PS C:\Users\Asus> Get-CimInstance -ClassName Win32_OperatingSystem | Select-Object LastBootUpTime

LastBootUpTime
--------------
27/10/2024 19:33:49
```