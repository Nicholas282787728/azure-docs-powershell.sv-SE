---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-AzCloudServicePublicIPAddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
ms.openlocfilehash: 2a3b643a9ad9d9c588589003e5edb24ceddc4ae1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215871"
---
# Get-AzCloudServicePublicIPAddress

## SYNOPSIS
Hämta den offentliga IP-adressen för en molntjänst.

## SYNTAX

### CloudServiceName (standard)
```
Get-AzCloudServicePublicIPAddress -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [<CommonParameters>]
```

### CloudService
```
Get-AzCloudServicePublicIPAddress -CloudService <CloudService> [-SubscriptionId <String>] [<CommonParameters>]
```

## BESKRIVNING
Hämta den offentliga IP-adressen för en molntjänst.

## EXEMPEL

### Exempel 1: Hämta offentliga IP-adresser på instansnivå för ett visst molntjänstnamn.
```powershell
PS C:\> Get-AzCloudServicePublicIPAddress -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

Hämtar offentliga IP-adresser på instansnivån för ett visst molntjänstnamn.

### Exempel 2: Hämta offentliga IP-adresser på instansnivå för ett visst molntjänstobjekt.
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Get-AzCloudServicePublicIPAddress -CloudService $cs

```

Hämtar offentliga IP-adresser på instansnivån för ett visst molntjänstobjekt.

## PARAMETERS

### -CloudService
CloudService-instans.
Skapa genom att gå till avsnittet ANTECKNINGAR för MOLNTJÄNST-egenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudService
Parameter Sets: CloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CloudServiceName
CloudServiceName.

```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
ResourceGroupName.

```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Prenumeration.

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

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

## UTDATA

## ANTECKNINGAR

ALIAS

KOMPLEXA PARAMETEREGENSKAPER

Skapa de parametrar som beskrivs nedan genom att skapa en hash-tabell som innehåller rätt egenskaper. Om du vill ha information om hash-tabeller kör du Get-Help about_Hash_Tables.


<CloudService>CLOUDSERVICE: CloudService-instans.
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
      - `[TypeHandlerVersion <String>]`: Anger versionen av tillägget. Anger versionen av tillägget. Om det här elementet inte anges eller en asterisk (*) används som värde används den senaste versionen av tillägget. Om värdet anges med ett huvudversionsnummer och en asterisk som delversionsnummer (X. ) väljs den senaste delversionen av den angivna huvudversionen. Om ett huvudversionsnummer och ett delversionsnummer har angetts (X.Y) väljs den specifika tilläggsversionen. Om en version anges utförs en automatisk uppgradering i rollinstansen.
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
        - `[CertificateUrl <String>]`: Det här är URL-adressen till ett certifikat som har laddats upp till nyckelvalv som en hemligt.
  - `[PackageUrl <String>]`: Anger en URL som refererar till platsen för tjänstpaketet i Blob-tjänsten. SERVICE package URL kan vara SAS -URI (Shared Access Signature) från alla lagringskonto.         Det här är en skrivskyddsegenskap som inte returneras i HÄMTA-samtal.
  - `[RoleProfile <ICloudServiceRoleProfile>]`: Beskriver rollprofilen för molntjänsten.
    - `[Role <ICloudServiceRoleProfileProperties[]>]`: Lista över roller för molntjänsten.
      - `[Name <String>]`: Resursnamn.
      - `[SkuCapacity <Int64?>]`: Anger antalet rollinstanser i molntjänsten.
      - `[SkuName <String>]`: SKU-namnet. Obs! Om den nya SKU:n inte stöds på den maskinvara som molntjänsten för närvarande är på, måste du ta bort och återskapa molntjänsten eller flytta tillbaka till den gamla SKU:n.
      - `[SkuTier <String>]`: Anger nivån för molntjänsten. Möjliga värden är <br /><br /> **Standard** <br /><br /> **Grundläggande**
  - `[StartCloudService <Boolean?>]`: (Valfritt) Anger om molntjänsten ska startas direkt efter att den har skapats. Standardvärdet är `true` .         Om det är falskt distribueras tjänstmodellen fortfarande, men koden körs inte omedelbart. I stället är tjänsten PoweredOff tills du ringer Start, då tjänsten startas. En distribuerad tjänst medför fortfarande kostnader, även om den är avstängd.
  - `[Tag <ICloudServiceTags>]`: Resurstaggar.
    - `[(Any) <String>]`: Detta anger att alla egenskapen kan läggas till i objektet.
  - `[UpgradeMode <CloudServiceUpgradeMode?>]`: Uppdateringsläge för molntjänsten. Rollinstanser tilldelas uppdatera domäner när tjänsten distribueras. Uppdateringar kan initieras manuellt i varje uppdateringsdomän eller initieras automatiskt i alla uppdateringsdomäner.         Möjliga värden är <br /><br />**Auto**<br /><br />**Manuellt** <br /><br />**Samtidig**<br /><br />         Om det inte anges anges standardvärdet automatiskt. Om PUT UpdateDomain är inställt på Manuell måste du anropa PUT UpdateDomain för att installera uppdateringen. Om den anges till Automatisk tillämpas uppdateringen automatiskt på varje uppdateringsdomän i följd.

## RELATERADE LÄNKAR

