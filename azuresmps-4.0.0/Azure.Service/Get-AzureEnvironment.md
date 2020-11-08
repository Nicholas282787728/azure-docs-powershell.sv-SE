---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: BF5E3E1A-14B6-4630-8168-628057009D5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284d1601746254b2e10fdfe042e5882e94ca1bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099582"
---
# Get-AzureEnvironment

## Sammanfattning
Hämtar Azure-miljöer

## FRÅGESYNTAXEN

```
Get-AzureEnvironment [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureEnvironment** hämtar Azure-miljörna som är tillgängliga för Windows PowerShell.

En Azure-miljö en oberoende distribution av Microsoft Azure, till exempel AzureCloud för globala Azure-och AzureChinaCloud för Azure som drivs av 21Vianet i Kina.
Du kan också skapa lokala Azure-miljöer med Azure Pack och WAPack cmdlets.
Mer information finns i [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

Cmdleten **Get-AzureEnvironment** hämtar miljöer från din prenumerations data fil, inte från Azure.
Om prenumerations data filen är inaktuell kör du cmdleten **Add-AzureAccount** eller **import-PublishSettingsFile** för att uppdatera den.

I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.
För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .

## BESKRIVS

### Exempel 1: Hämta alla miljöer
```
PS C:\> Get-AzureEnvironment

EnvironmentName               ServiceEndpoint               ResourceManagerEndpoint       PublishSettingsFileUrl
---------------               ---------------               -----------------------       ----------------------

AzureCloud                    https://management.core.wi... https://management.azure.com/ https://go.microsoft.com/fw... 
AzureChinaCloud               https://management.core.ch... https://not-supported-serv... https://go.microsoft.com/fw...
```

Det här kommandot får alla miljöer som är tillgängliga för Windows PowerShell.

### Exempel 2: skaffa en miljö med namn
```
PS C:\> Get-AzureEnvironment -Name AzureCloud

Name                          : AzureCloud

PublishSettingsFileUrl        : https://go.microsoft.com/fwlink/?LinkID=301775

ServiceEndpoint               : https://management.core.windows.net/

ResourceManagerEndpoint       : https://management.azure.com/

ManagementPortalUrl           : https://go.microsoft.com/fwlink/?LinkId=254433

ActiveDirectoryEndpoint       : https://login.windows.net/

ActiveDirectoryCommonTenantId : common

StorageEndpointSuffix         : core.windows.net

StorageBlobEndpointFormat     : {0}://{1}.blob.core.windows.net/

StorageQueueEndpointFormat    : {0}://{1}.queue.core.windows.net/

StorageTableEndpointFormat    : {0}://{1}.table.core.windows.net/

GalleryEndpoint               : https://gallery.azure.com/
```

Det här exemplet får du AzureCloud-miljön.

### Exempel 3: Hämta alla egenskaper för alla miljöer
```
PS C:\> Get-AzureEnvironment | ForEach-Object {Get-AzureEnvironment -Name $_.EnvironmentName}
```

Det här kommandot får alla egenskaper i alla miljöer.

Kommandot använder cmdleten **Get-AzureEnvironment** för att hämta alla Azure-miljöer för det här kontot.
Sedan använder den **förgrunds-objekt-** cmdleten för att köra kommandot **Get-AzureEnvironment** med parametern **Name** i varje miljö.
Värdet på parametern **Name** är egenskapen **EnvironmentName** för varje miljö.

Utan parametrar får **Get-AzureEnvironment** endast valda egenskaper för en miljö.

## MALLPARAMETRAR

### -Namn
Hämtar endast den angivna miljön.
Skriv miljö namnet.
Parametervärdet är Skift läges känsligt.
Jokertecken är inte tillåtna.

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

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser. Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.

## VÄRDEN

### System. Management. Automation. PSCustomObject
Som standard returnerar **Get-AzureEnvironment** ett anpassat objekt.

### Microsoft. WindowsAzure. commands. Utilitiess. Common. WindowsAzureEnvironment
När du kör **Get-AzureEnvironment** med parametern **Name** returnerar den ett  **WindowsAzureEnvironment** -objekt.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureAccount](./Add-AzureAccount.md)

[Add-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)

[Import-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Remove-AzureEnvironment](./Remove-AzureEnvironment.md)

[Set-AzureEnvironment](./Set-AzureEnvironment.md)


