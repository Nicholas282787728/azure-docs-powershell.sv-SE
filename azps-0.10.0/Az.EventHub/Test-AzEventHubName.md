---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 49b47e637d009eabac106679e81ec763b0898160
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924574"
---
# Test-AzEventHubName

## Sammanfattning
Kontrollerar tillgänglighet för det angivna namn området eller aliaset (DR-konfigurationsfilen)

## FRÅGESYNTAXEN

### NamespaceCheckNameAvailabilitySet (standard)
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AliasCheckNameAvailabilitySet
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
**Test-AzEventhubName** cmdlet kontrollerar tillgänglighet för namn områdes namnet eller aliaset (Dr-konfigurationsfilen)

## BESKRIVS

### Exempel 1
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

Returnerar statusen för tillgänglighet för namn områdes namnet "MyNameSapceName" som sant om tillgängligt

### Exempel 2
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

Returnerar status för tillgänglighet för namn områdes namnet "MyNameSapceName" som falskt med anledning

### Exempel 3
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

Returnerar statusen för tillgänglighet för aliasnamnet ' myAliasName ' för namn området ' MyNameSapceName ' som sant om tillgängligt

## MALLPARAMETRAR

### -AliasName
Namn på DR-konfiguration

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namnrymd
Namn område för Eventhub

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Resurs grupps namn

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. commands. EventHub. Models. PSCheckNameAvailabilityResultAttributes

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
