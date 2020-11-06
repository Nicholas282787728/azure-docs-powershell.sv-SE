---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: EFBBFB60-D972-47B8-997E-B737F0CA007E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
ms.openlocfilehash: 029404938ba7a253b5130f5c807e4b66c3847d43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575863"
---
# Find-AzureRmResourceGroup

## Sammanfattning
Söker efter resurs grupper.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Find-AzureRmResourceGroup [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **find-AzureRmResourceGroup** söker efter resurs grupper med de angivna parametrarna.

## BESKRIVS

### Exempel 1: Sök efter alla resurs grupper
```
PS C:\>Find-AzureRmResourceGroup
```

Det här kommandot hittar alla resurs grupper.

### Exempel 2: Sök efter resurs grupper efter taggnamn
```
PS C:\>Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
```

Det här kommandot hittar alla resurs grupper som har en tagg som heter testtag.

### Exempel 3: Sök efter resurs grupper efter taggnamn och värde
```
PS C:\>Find-AzureRmResourceGroup -Tag @{"testtag" = "testval" }
```

Det här kommandot hittar alla resurs grupper som har en tagg med namnet testtag och värdet testval.

## MALLPARAMETRAR

### -ApiVersion
Anger vilken version av API för Resource provider som ska användas. Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.

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

### -För
Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.

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

### -Tagg
Anger taggnings information som en hash-tabell för att filtrera resultaten. Använd följande format:

@ {tagName = $null} eller @ {tagName = ' tagValue '}.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### System. Management. Automation. PSObject

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

