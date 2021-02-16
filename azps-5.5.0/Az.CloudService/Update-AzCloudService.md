---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/update-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
ms.openlocfilehash: e0f9ad794f1631c5c8615480c6074f040f7fe749
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211878"
---
# Update-AzCloudService

## SYNOPSIS
Skapa eller uppdatera en molntjänst.
Observera att vissa egenskaper endast kan anges när molntjänsten skapas.

## SYNTAX

```
Update-AzCloudService -InputObject <ICloudServiceIdentity> -Parameter <ICloudService>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## BESKRIVNING
Skapa eller uppdatera en molntjänst.
Observera att vissa egenskaper endast kan anges när molntjänsten skapas.

## EXEMPEL

### Exempel 1: Lägga till RDP-tillägg för befintlig molntjänst
```powershell
# Create RDP extension object
PS C:\> $rdpExtension = New-AzCloudServiceRemoteDesktopExtensionObject -Name "RDPExtension" -Credential $credential -Expiration $expiration -TypeHandlerVersion "1.2.1"
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Add RDP extension to existing cloud service extension object
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension + $rdpExtension
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

Ovanför uppsättningen kommandon läggs ett RDP-tillägg till redan befintlig molntjänst med namnet ContosoCS som tillhör resursgruppen ContosOrg.

### Exempel 2: Ta bort alla tillägg från molntjänsten
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Set extension to empty list
PS C:\> $cloudService.ExtensionProfile.Extension = @()
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

Ovanför uppsättningen kommandon tas alla tillägg bort från den befintliga molntjänsten ContosoCS som tillhör resursgruppen ContosOrg.

### Exempel 3: Ta bort RDP-tillägg från molntjänsten
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Remove extension by name RDPExtension
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension | Where-Object { $_.Name -ne "RDPExtension" }
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

Ovanför uppsättningen kommandon tar du bort RDP-tillägget från den befintliga molntjänsten ContosoCS som tillhör resursgruppen ContosOrg.

### Exempel 4: Scale-Out/ Scale-In rollinstanser
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"

# Scale-out all role instance count by 1
PS C:\> $cloudService.RoleProfile.Role | ForEach-Object {$_.SkuCapacity += 1}

# Scale-in ContosoFrontend role instance count by 1
PS C:\> $role = $cloudService.RoleProfile.Role | Where-Object {$_.Name -eq "ContosoFrontend"}
PS C:\> $role.SkuCapacity -= 1

# Update cloud service configuration as per the new role instance count
PS C:\> $cloudService.Configuration = $configuration

# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

Ovanför uppsättningen kommandon visas hur du kan skala ut och skala in rollinstansantal för molntjänsten ContosoCS som tillhör resursgruppen ContosOrg.

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

### -InputObject
Identitetsparameter att skapa finns i avsnittet ANTECKNINGAR för INPUTOBJECT-egenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -Parameter
Beskriver molntjänsten.
Skapa genom att gå till avsnittet ANTECKNINGAR för PARAMETERegenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### Microsoft.Azure.PowerShell.cmdlets.CloudService.Models.Api20201001Preview.ICloudService

### Microsoft.Azure.PowerShell.cmdlets.CloudService.Models.iCloudServiceIdentity

## UTDATA

### Microsoft.Azure.PowerShell.cmdlets.CloudService.Models.Api20201001Preview.ICloudService

## ANTECKNINGAR

ALIAS

KOMPLEXA PARAMETEREGENSKAPER

Skapa de parametrar som beskrivs nedan genom att skapa en hash-tabell som innehåller rätt egenskaper. Om du vill ha information om hash-tabeller kör du Get-Help about_Hash_Tables.


INPUTOBJECT <ICloudServiceIdentity> : Identity Parameter
  - `[CloudServiceName <String>]`: 
  - `[Id <String>]`: Resursidentitetssökväg
  - `[ResourceGroupName <String>]`: 
  - `[RoleInstanceName <String>]`: Namn på rollinstansen.
  - `[RoleName <String>]`: Namnet på rollen.
  - `[SubscriptionId <String>]`: Prenumerationsuppgifter som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID:t utgör en del av URI:n för varje servicesamtal.
  - `[UpdateDomain <Int32?>]`: Anger ett heltalsvärde som identifierar uppdateringsdomänen. Uppdateringsdomäner identifieras med ett nollbaserat index: den första uppdateringsdomänen har ID:t 0, det andra har ID:t 1 och så vidare.

PARAMETER <ICloudService> : Beskriver molntjänsten.
  - `Location <String>`: Resursplats.
  - `[Configuration <String>]`: Anger XML-tjänstens konfiguration (.cscfg) för molntjänsten.
  - `[ConfigurationUrl <String>]`: Anger en URL som refererar till platsen för tjänstkonfigurationen i Blob-tjänsten. SERVICE package URL kan vara SAS -URI (Shared Access Signature) från alla lagringskonto.         Det här är en skrivskyddsegenskap som inte returneras i HÄMTA-samtal.
  - `[ExtensionProfile <ICloudServiceExtensionProfile>]`: Beskriver en profil för molntjänsttillägg.
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
      - `[TypeHandlerVersion <String>]`: Anger versionen av tillägget. Anger versionen av tillägget. Om det här elementet inte anges eller en asterisk (*) används som värde används den senaste versionen av tillägget. Om värdet anges med ett huvudversionsnummer och en asterisk som delversionsnummer (X.) väljs den senaste delversionen av den angivna huvudversionen. Om ett huvudversionsnummer och ett delversionsnummer har angetts (X.Y) väljs den specifika tilläggsversionen. Om en version anges utförs en automatisk uppgradering i rollinstansen.
  - `[NetworkProfile <ICloudServiceNetworkProfile>]`: Nätverksprofil för molntjänsten.
    - `[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: Lista över konfigurationer för belastningsutjämning för molntjänsten.
      - `[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Lista över IP
        - `[Name <String>]`: 
        - `[PrivateIPAddress <String>]`: Den privata IP-adressen som molntjänsten refererar till.
        - `[PublicIPAddressId <String>]`: Resurs-ID
        - `[SubnetId <String>]`: Resurs-ID
      - `[Name <String>]`: Resursnamn
    - `[SwappableCloudService <ISubResource>]`: 
      - `[Id <String>]`: Resurs-ID
  - `[OSProfile <ICloudServiceOSProfile>]`: Beskriver OS-profilen för molntjänsten.
    - `[Secret <ICloudServiceVaultSecretGroup[]>]`: Anger en uppsättning certifikat som ska installeras på rollinstanserna.
      - `[SourceVaultId <String>]`: Resurs-ID
      - `[VaultCertificate <ICloudServiceVaultCertificate[]>]`: Listan med viktiga valv-referenser i SourceVault som innehåller certifikat.
        - `[CertificateUrl <String>]`: Det här är URL-adressen till ett certifikat som har laddats upp till nyckelvalv som en hemlig.
  - `[PackageUrl <String>]`: Anger en URL som refererar till platsen för tjänstpaketet i Blob-tjänsten. SERVICE package URL kan vara SAS -URI (Shared Access Signature) från alla lagringskonto.         Det här är en skrivskyddsegenskap som inte returneras i HÄMTA-samtal.
  - `[RoleProfile <ICloudServiceRoleProfile>]`: Beskriver rollprofilen för molntjänsten.
    - `[Role <ICloudServiceRoleProfileProperties[]>]`: Lista över roller för molntjänsten.
      - `[Name <String>]`: Resursnamn.
      - `[SkuCapacity <Int64?>]`: Anger antalet rollinstanser i molntjänsten.
      - `[SkuName <String>]`: SKU-namnet. Obs! Om den nya SKU:n inte stöds på den maskinvara som molntjänsten för närvarande är på, måste du ta bort och återskapa molntjänsten eller flytta tillbaka till den gamla SKU:n.
      - `[SkuTier <String>]`: Anger nivån för molntjänsten. Möjliga värden är <br /><br /> **Standard** <br /><br /> **Grundläggande**
  - `[StartCloudService <Boolean?>]`: (Valfritt) Anger om molntjänsten ska startas direkt efter att den har skapats. Standardvärdet `true` är.         Om det är falskt distribueras tjänstmodellen fortfarande, men koden körs inte omedelbart. I stället är tjänsten PoweredOff tills du ringer Start, då tjänsten startas. En distribuerad tjänst medför fortfarande kostnader, även om den är avstängd.
  - `[Tag <ICloudServiceTags>]`: Resurstaggar.
    - `[(Any) <String>]`: Detta anger att alla egenskapen kan läggas till i objektet.
  - `[UpgradeMode <CloudServiceUpgradeMode?>]`: Uppdateringsläge för molntjänsten. Rollinstanser tilldelas uppdatera domäner när tjänsten distribueras. Uppdateringar kan initieras manuellt i varje uppdateringsdomän eller initieras automatiskt i alla uppdateringsdomäner.         Möjliga värden är <br /><br />**Auto**<br /><br />**Manuellt** <br /><br />**Samtidig**<br /><br />         Om det inte anges anges standardvärdet automatiskt. Om PUT UpdateDomain är inställt på Manuell måste du anropa PUT UpdateDomain för att installera uppdateringen. Om den anges till Automatisk tillämpas uppdateringen automatiskt på varje uppdateringsdomän i följd.

## RELATERADE LÄNKAR

