---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContextAutosaveSetting.md
ms.openlocfilehash: 2d867ab605d4b6c649e740736868782cde325596
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755469"
---
# Get-AzureRmContextAutosaveSetting

## Sammanfattning
Visa metadata om funktionen för Autospara med kontext, inklusive om kontexten sparas automatiskt och om Sparad kontext och autentiseringsinformation kan hittas.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmContextAutosaveSetting [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Visa metadata om funktionen för Autospara med kontext, inklusive om kontexten sparas automatiskt och om Sparad kontext och autentiseringsinformation kan hittas.

## BESKRIVS

### Hämta metadata för den aktuella sessionen
```
PS C:\> Get-AzureRmContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

Få information om huruvida kontexten sparas och om WEHERE.  I exemplet ovan har funktionen Spara automatiskt avaktiverats.

### Hämta metadata för den aktuella användaren
```
PS C:\> Get-AzureRmContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

Få information om huruvida kontexten sparas som standard för den aktuella användaren.  Observera att det här kan skilja sig från inställningarna som är aktiva i den aktuella sessionen. I exemplet ovan är funktionen Spara automatiskt aktive rad och data sparas på standard platsen.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Omfattning
Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

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

## VÄRDEN

### Microsoft. Azure. kommandon. Common. inloggningsautentisering. ContextAutosaveSettings

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
