---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F94584BC-EC02-412D-B089-B98A6FF8F505
online version: ''
schema: 2.0.0
ms.openlocfilehash: a5b7758a7316fa6c34ffe6b5225cd252f39c5d7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099139"
---
# New-AzureQuickVM

## Sammanfattning
Konfigurerar och skapar en virtuell Azure-dator.

## FRÅGESYNTAXEN

### Windows (standard)
```
New-AzureQuickVM [-Windows] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-AdminUsername <String>]
 [-Certificates <CertificateSettingList>] [-WaitForBoot] [-DisableWinRMHttps] [-EnableWinRMHttp]
 [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey]
 [-NoWinRMEndpoint] [-VNetName <String>] [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>]
 [-HostCaching <String>] [-AvailabilitySetName <String>] [-InstanceSize <String>] [-MediaLocation <String>]
 [-DisableGuestAgent] [-CustomDataFile <String>] [-ReservedIPName <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Linux
```
New-AzureQuickVM [-Linux] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-LinuxUser <String>] [-WaitForBoot]
 [-SSHPublicKeys <SSHPublicKeyList>] [-SSHKeyPairs <SSHKeyPairList>] [-VNetName <String>]
 [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>] [-HostCaching <String>] [-AvailabilitySetName <String>]
 [-InstanceSize <String>] [-MediaLocation <String>] [-DisableGuestAgent] [-CustomDataFile <String>]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
**New-AzureQuickVM** cmdlet konfigurerar och skapar en virtuell Azure-dator.
Denna cmdlet kan distribuera en virtuell dator till en befintlig Azure-tjänst.
Denna cmdlet kan alternativt skapa en Azure-tjänst som är värd för den nya virtuella datorn.

## BESKRIVS

### Exempel 1: skapa en virtuell dator
```
PS C:\> New-AzureQuickVM -Windows -ServiceName "ContosoService17" -Name "VirutalMachine01" -ImageName "Image07" -Password "password" -AdminUsername "AdminMain" -WaitForBoot
```

Det här kommandot skapar en virtuell dator som kör operativ systemet Windows i en befintlig tjänst.
Cmdleten baserar den virtuella datorn på den angivna bilden.
Kommandot anger parametern *WaitForBoot* .
Därför väntar cmdleten på att den virtuella datorn ska starta.

### Exempel 2: skapa en virtuell dator som använder certifikat
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
PS C:\> New-AzureQuickVM -Windows -ServiceName "MySvc1" -name "MyWinVM1" -ImageName "Image07" -Password "password" -AdminUserName "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] -WaitForBoot
```

Det första kommandot får certifikat från en butik och lagrar dem i $certs variabel.

Det andra kommandot skapar en virtuell dator som kör operativ systemet Windows i en befintlig tjänst från en bild.
Http https-lyssnaren är aktive rad som standard på den virtuella datorn.
Kommandot anger parametern *WaitForBoot* .
Därför väntar cmdleten på att den virtuella datorn ska starta.
Kommandot laddar upp ett WinRM-certifikat och X509Certificates till den värdbaserade tjänsten.

### Exempel 3: skapa en virtuell dator som kör Linux-operativsystemet
```
PS C:\> New-AzureQuickVM -Linux -ServiceName "ContosoServiceLinux01" -Name "LinuxVirtualMachine01" -ImageName "LinuxImage01" -LinuxUser "RootMain" -Password "password" -Location "Central US"
```

Det här kommandot skapar en virtuell dator som kör Linux-operativsystemet från en bild.
Det här kommandot skapar en tjänst som ska vara värd för den nya virtuella datorn.
Kommandot anger en plats för tjänsten.

### Exempel 4: skapa en virtuell dator och skapa en tjänst som värd för den nya virtuella datorn
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService03" -Name " VirtualMachine25" -ImageName $images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name
```

Det första kommandot får plats genom att använda cmdleten **Get-AzureLocation** och lagrar dem sedan i $locations mat ris variabel.

Med det andra kommandot hämtas tillgängliga bilder med cmdleten **Get-AzureVMImage** och sparas sedan i $images mat ris variabel.

Med kommandot slut skapas en stor virtuell dator med namnet VirtualMachine25.
Den virtuella datorn kör operativ systemet Windows.
Den är baserad på en av bilderna i $Images.
Kommandot skapar en tjänst med namnet ContosoService03 för den nya virtuella datorn.
Tjänsten är på en plats i $Locations.

### Exempel 5: skapa en virtuell dator som har ett reserverat IP-namn
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService04" -Name "VirtualMachine27" -ImageName $Images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name -ReservedIPName $ipName
```

Det första kommandot får plats och lagrar dem sedan i $Locations mat ris variabel.

Det andra kommandot hämtar tillgängliga bilder och lagrar dem sedan i $Images mat ris variabel.

Med kommandot slut skapas en virtuell dator med namnet VirtualMachine27 baserat på en av bilderna i $Images.
Kommandot skapar en tjänst på en plats i $Locations.
Den virtuella datorn har ett reserverat IP-namn som tidigare lagrats i $ipName variabel.

## MALLPARAMETRAR

### -AdminUsername
Anger användar namnet på det administratörs konto som den här cmdleten skapar på den virtuella datorn.

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AffinityGroup
Anger tillhörighets gruppen för den virtuella datorn.
Ange den här parametern eller parametern *plats* om den här cmdleten skapar en Azure-tjänst för den virtuella datorn.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AvailabilitySetName
Anger namnet på den tillgänglighets uppsättning där den här cmdleten skapar den virtuella datorn.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Certifikat
Anger en lista över de certifikat som används i den här cmdleten för att skapa tjänsten.

```yaml
Type: CertificateSettingList
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomDataFile
Anger en datafil för den virtuella datorn.
Denna cmdlet kodar innehållet i filen som base64.
Filen måste vara mindre än 64 kilobyte lång.

Om gäst operativ systemet är Windows-operativsystem sparar denna cmdlet dessa data som en binärfil som heter%SYSTEMDRIVE%\AzureData\CustomData.bin.

Om gäst operativ systemet är Linux skickar denna cmdlet data med hjälp av ovf-env.xml-filen.
Installationen kopierar filen till/var/lib/waagent-katalogen.
Agenten lagrar också base64-kodade data i/var/lib/waagent/CustomData.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableGuestAgent
Anger att denna cmdlet inaktiverar infrastrukturen som en tjänst (IaaS).

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWinRMHttps
Anger att denna cmdlet inaktiverar Windows Remote Management (WinRM) på HTTPS.
WinRM är aktiverat som standard via HTTPS.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DnsSettings
Anger en matris med DNS-Server objekt som definierar DNS-inställningarna för den nya distributionen.
Om du vill skapa ett **DnsServer** -objekt använder du cmdleten **New-AzureDns** .

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWinRMHttp
Anger att denna cmdlet aktiverar WinRM över HTTP.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching
Anger läget för cachelagring av värden för operativ system disken.
Giltiga värden är: 

- ReadOnly
- Läs

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageName
Anger namnet på den disk avbildning som används för att skapa disketten för operativ systemet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
Anger hur den här cmdleten svarar på en informations händelse.

De acceptabla värdena för den här parametern är:

- Vidare
- Över
- Inquire
- SilentlyContinue
- Stanna
- Avbryt

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Anger en informations variabel.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceSize
Anger förekomstens storlek.
Giltiga värden är: 

- ExtraSmall
- Eld
- Risk
- Höga
- ExtraLarge
- A5
- A6
- A7
- A8
- A9
- Basic_A0
- Basic_A1
- Basic_A2
- Basic_A3
- Basic_A4
- Standard_D1
- Standard_D2
- Standard_D3
- Standard_D4
- Standard_D11
- Standard_D12
- Standard_D13
- Standard_D14

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
Anger att denna cmdlet skapar en Linux-baserad virtuell dator.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LinuxUser
Anger användar namnet på det administratörs konto för Linux som den här cmdleten skapar på den virtuella datorn.

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plats
Anger Azure-datacentret som är värd för den virtuella datorn.
Om du anger den här parametern skapar cmdleten en Azure-tjänst på den angivna platsen.
Ange den här parametern eller parametern *AffinityGroup* endast om den här cmdleten skapar en Azure-tjänst för den virtuella datorn.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaLocation
Anger plats för Azure-lagring där den här cmdleten skapar diskarna för virtuella datorer.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger namnet på den virtuella dator som denna cmdlet skapar.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoExportPrivateKey
Anger att den här konfigurationen inte laddar upp den privata knappen.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWinRMEndpoint
Anger att denna cmdlet inte lägger till en WinRM-slutpunkt för den virtuella datorn.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Lösen ord
Anger lösen ordet för administratörs kontot.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser.
Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReservedIPName
Anger det reserverade IP-namnet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReverseDnsFqdn
Anger det fullständigt kvalificerade domän namnet för omvänd DNS-uppkoppling.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Anger namnet på en ny eller befintlig Azure-tjänst dit den här cmdleten lägger till den nya virtuella datorn.

Om du anger en ny tjänst skapar denna cmdlets.
För att skapa en ny tjänst måste du ange *plats* -eller *AffinityGroup* -parameter.

Om du anger en befintlig tjänst ska du inte ange *plats* eller *AffinityGroup*.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHKeyPairs
Anger SSH-nyckelvärdena.

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHPublicKeys
Anger offentliga nycklar för SSH.

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetNames
Anger en matris med namn på en nätmask för den virtuella datorn.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VNetName
Anger namnet på ett virtuellt nätverk för den virtuella datorn.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForBoot
Anger att denna cmdlet väntar på att den virtuella datorn ska nå tillståndet ReadyRole.
Om den virtuella datorn uppfyller något av följande tillstånd Miss lyckas cmdleten: FailedStartingVM, ProvisioningFailed eller ProvisioningTimeout.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Windows
Anger att den här cmdleten skapar en virtuell Windows-dator.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WinRMCertificate
Anger ett certifikat som denna cmdlet associerar till en WinRM-slut punkt.

```yaml
Type: X509Certificate2
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -X509Certificates
Anger en matris med X509-certifikat som distribueras till en värdbaserad tjänst.

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureLocation](./Get-AzureLocation.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[New-AzureDns](./New-AzureDns.md)


