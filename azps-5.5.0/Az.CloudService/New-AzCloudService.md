---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/new-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
ms.openlocfilehash: 24e90ebae59c9d9a4449c57270b7ca69f9b05b88
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233503"
---
# New-AzCloudService

## SYNOPSIS
Skapa eller uppdatera en molntjänst.
Observera att vissa egenskaper endast kan anges när molntjänsten skapas.

## SYNTAX

```
New-AzCloudService -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Configuration <String>] [-ConfigurationUrl <String>] [-ExtensionProfile <ICloudServiceExtensionProfile>]
 [-NetworkProfile <ICloudServiceNetworkProfile>] [-OSProfile <ICloudServiceOSProfile>] [-PackageUrl <String>]
 [-RoleProfile <ICloudServiceRoleProfile>] [-StartCloudService] [-Tag <Hashtable>]
 [-UpgradeMode <CloudServiceUpgradeMode>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## BESKRIVNING
Skapa eller uppdatera en molntjänst.
Observera att vissa egenskaper endast kan anges när molntjänsten skapas.

## EXEMPEL

### Exempel 1: Skapa en ny molntjänst med en enda roll
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile
```

Ovanför uppsättningen kommandon skapas en molntjänst med en enda roll

### Exempel 2: Skapa en ny molntjänst med en enda roll och RDP-tillägg
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosoOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Create RDP extension object
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $extension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'
PS C:\> $extensionProfile = @{extension = @($extension)}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -ExtensionProfile $extensionProfile
```

Ovanför uppsättningen kommandon skapas en molntjänst med en enda roll och RDP-tillägg

### Exempel 3: Skapa ny molntjänst med en enda roll och certifikat från nyckelvalv
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create OS profile object
$keyVault = Get-AzKeyVault -ResourceGroupName ContosOrg -VaultName ContosKeyVault
$certificate=Get-AzKeyVaultCertificate -VaultName ContosKeyVault -Name ContosCert
$secretGroup = New-AzCloudServiceVaultSecretGroupObject -Id $keyVault.ResourceId -CertificateUrl $certificate.SecretId
$osProfile = @{secret = @($secretGroup)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -OSProfile $osProfile
```

Ovanför uppsättningen kommandon skapas en molntjänst med en enda roll och certifikat från nyckelvalv.

### Exempel 4: Skapa ny molntjänst med flera roller och tillägg
```powershell
# Create role profile object
PS C:\> $role1 = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $role2 = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoBackend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role1, $role2)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Create RDP extension object
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $rdpExtension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'

# Create Geneva extension object
PS C:\> $genevaExtension = New-AzCloudServiceExtensionObject -Name GenevaExtension -Publisher Microsoft.Azure.Geneva -Type GenevaMonitoringPaaS -TypeHandlerVersion "2.14.0.2"
PS C:\> $extensionProfile = @{extension = @($rdpExtension, $genevaExtension)}

# Add tags
$tag=@{"Owner" = "Contoso"}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -ExtensionProfile $extensionProfile                           `
                  -Tag $tag
```

Ovanför uppsättningen kommandon skapas en molntjänst med en enda roll och certifikat från nyckelvalv.

## PARAMETERS

### -As Ent
Köra kommandot som ett jobb

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Configuration
Anger XML-tjänstens konfiguration (.cscfg) för molntjänsten.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConfigurationUrl
Anger en URL som refererar till platsen för tjänstkonfigurationen i Blob-tjänsten.
SERVICE package URL kan vara SAS -URI (Shared Access Signature) från alla lagringskonto. Det här är en skrivskyddsegenskap som inte returneras i HÄMTA-samtal.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtensionProfile
Beskriver en profil för molntjänsttillägg.
Skapa genom att gå till avsnittet NOTES för EGENSKAPERNA EXTENSIONPROFILE och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceExtensionProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plats
Resursplats.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Namnet på molntjänsten.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkProfile
Nätverksprofil för molntjänsten.
Skapa genom att gå till avsnittet ANTECKNINGAR för NETWORKPROFILE-egenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceNetworkProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Köra kommandot asynkront

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OSProfile
Beskriver OS-profilen för molntjänsten.
Skapa genom att gå till avsnittet ANTECKNINGAR för OSPROFILE-egenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceOSProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackageUrl
Anger en URL som refererar till platsen för tjänstpaketet i Blob-tjänsten.
SERVICE package URL kan vara SAS -URI (Shared Access Signature) från alla lagringskonto. Det här är en skrivskyddsegenskap som inte returneras i HÄMTA-samtal.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Namn på resursgruppen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleProfile
Beskriver rollprofilen för molntjänsten.
Skapa genom att gå till avsnittet ANTECKNINGAR för ROLEPROFILE-egenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceRoleProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartCloudService
(Valfritt) Anger om molntjänsten ska startas direkt efter att den har skapats.
Standardvärdet är `true` . Om det är falskt distribueras tjänstmodellen fortfarande, men koden körs inte omedelbart.
I stället är tjänsten PoweredOff tills du ringer Start, då tjänsten startas.
En distribuerad tjänst medför kostnader även om den är avstängd.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Prenumerationsuppgifter som unikt identifierar Microsoft Azure-prenumerationen.
Prenumerations-ID:t utgör en del av URI:n för varje servicesamtal.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Resurstaggar.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpgradeMode
Uppdateringsläge för molntjänsten.
Rollinstanser tilldelas uppdatera domäner när tjänsten distribueras.
Uppdateringar kan initieras manuellt i varje uppdateringsdomän eller initieras automatiskt i alla uppdateringsdomäner. Möjliga värden är \<br /\> \<br /\> **automatiska** \<br /\> \<br /\>  \<br /\> \<br /\> **manuella** \<br /\> \<br /\> samtidiga om de inte anges, standardvärdet är Automatiskt. Om PUT UpdateDomain är inställt på Manuell måste du anropa PUT UpdateDomain för att installera uppdateringen.
Om den anges till Automatisk tillämpas uppdateringen automatiskt på varje uppdateringsdomän i följd.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Support.CloudServiceUpgradeMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bekräfta
Frågar dig om bekräftelse innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som skulle hända om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

## UTDATA

### Microsoft.Azure.PowerShell.cmdlets.CloudService.Models.Api20201001Preview.ICloudService

## ANTECKNINGAR

ALIAS

KOMPLEXA PARAMETEREGENSKAPER

Skapa de parametrar som beskrivs nedan genom att skapa en hash-tabell som innehåller rätt egenskaper. Om du vill ha information om hash-tabeller kör du Get-Help about_Hash_Tables.


EXTENSIONPROFILE: <ICloudServiceExtensionProfile> Beskriver en molntjänsttilläggsprofil.
  - `[Extension <IExtension[]>]`: Lista över tillägg för molntjänsten.
    - `[AutoUpgradeMinorVersion <Boolean?>]`: Uttryckligen ange om plattformen kan automatiskt uppgradera TypeHandlerVersion till högre delversioner när de blir tillgängliga.
    - `[ForceUpdateTag <String>]`: Kod för att tillämpa de angivna offentliga och skyddade inställningarna.         Om du ändrar taggvärdet kan du köra tillägget igen utan att ändra några av de offentliga eller skyddade inställningarna.         Om forceUpdateTag inte ändras tillämpas uppdateringar av offentliga eller skyddade inställningar fortfarande av hanterare.         Om varken forceUpdateTag eller någon av de offentliga eller skyddade inställningarna ändras flödar tillägg till rollinstansen med samma sekvensnummer och det är upp till hanterarimplementering om det ska köras igen eller inte
    - `[Name <String>]`: Namnet på tillägget.
    - `[ProtectedSetting <String>]`: Skyddade inställningar för tillägget som krypteras innan det skickas till rollinstansen.
    - `[ProtectedSettingFromKeyVaultSecretUrl <String>]`: 
    - `[Publisher <String>]`: Namnet på tilläggshanterarens utgivare.
    - `[RolesAppliedTo <String[]>]`: Valfri lista över roller för att använda det här tillägget. Om egenskap inte anges eller "*" anges, tillämpas tillägget på alla roller i molntjänsten.
    - `[Setting <String>]`: Offentliga inställningar för tillägget. För JSON-tillägg är det här JSON-inställningarna för tillägget. För XML-tillägg (t.ex. RDP) är det här XML-inställningen för tillägget.
    - `[SourceVaultId <String>]`: Resurs-ID
    - `[Type <String>]`: Anger typ av filnamnstillägg.
    - `[TypeHandlerVersion <String>]`: Anger versionen av tillägget. Anger versionen av tillägget. Om det här elementet inte anges eller en asterisk (*) används som värde används den senaste versionen av tillägget. Om värdet anges med ett huvudversionsnummer och en asterisk som delversionsnummer (X. ) väljs den senaste delversionen av den angivna huvudversionen. Om ett huvudversionsnummer och ett delversionsnummer har angetts (X.Y) väljs den specifika tilläggsversionen. Om en version anges utförs en automatisk uppgradering i rollinstansen.

NETWORKPROFILE <ICloudServiceNetworkProfile> : Nätverksprofil för molntjänsten.
  - `[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: Lista över konfigurationer för belastningsutjämning för molntjänsten.
    - `[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Lista över IP
      - `[Name <String>]`: 
      - `[PrivateIPAddress <String>]`: Den privata IP-adressen som molntjänsten refererar till.
      - `[PublicIPAddressId <String>]`: Resurs-ID
      - `[SubnetId <String>]`: Resurs-ID
    - `[Name <String>]`: Resursnamn
  - `[SwappableCloudService <ISubResource>]`: 
    - `[Id <String>]`: Resurs-ID

OSPROFILE <ICloudServiceOSProfile> : Beskriver OS-profilen för molntjänsten.
  - `[Secret <ICloudServiceVaultSecretGroup[]>]`: Anger en uppsättning certifikat som ska installeras på rollinstanserna.
    - `[SourceVaultId <String>]`: Resurs-ID
    - `[VaultCertificate <ICloudServiceVaultCertificate[]>]`: Listan med viktiga valv-referenser i SourceVault som innehåller certifikat.
      - `[CertificateUrl <String>]`: Det här är URL-adressen till ett certifikat som har laddats upp till nyckelvalv som en hemlig.

ROLEPROFILE <ICloudServiceRoleProfile> : Beskriver rollprofilen för molntjänsten.
  - `[Role <ICloudServiceRoleProfileProperties[]>]`: Lista över roller för molntjänsten.
    - `[Name <String>]`: Resursnamn.
    - `[SkuCapacity <Int64?>]`: Anger antalet rollinstanser i molntjänsten.
    - `[SkuName <String>]`: SKU-namnet. Obs! Om den nya SKU:n inte stöds på den maskinvara som molntjänsten för närvarande är på, måste du ta bort och återskapa molntjänsten eller flytta tillbaka till den gamla SKU:n.
    - `[SkuTier <String>]`: Anger nivån för molntjänsten. Möjliga värden är <br /><br /> **Standard** <br /><br /> **Grundläggande**

## RELATERADE LÄNKAR

