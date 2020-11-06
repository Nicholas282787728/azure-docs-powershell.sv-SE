---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueKey.md
ms.openlocfilehash: 4faca15a0c348ee1011789db5acd227c06ee1b85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582187"
---
# Get-AzureRmServiceBusQueueKey

## Sammanfattning
Hämtar primära och sekundära anslutnings strängar för den angivna tjänst buss kön.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmServiceBusQueueKey [-ResourceGroup] <String> -Namespace <String> -Queue <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmServiceBusQueueKey** returnerar primära och sekundära anslutnings strängar för den angivna tjänst buss kön. 

## BESKRIVS

### Exempel 1
```
PS C:\> Get-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

Returnerar de primära och sekundära anslutnings strängarna för den angivna tjänst buss kön.

## MALLPARAMETRAR

### -ResourceGroup
Namnet på resurs gruppen.

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

### -Namn
ServiceBus AuthorizationRule namn.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namnrymd
Namn områdes namnet ServiceBus.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Kö
ServiceBus.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### -ResourceGroup
 System. String
 

### -NamespaceName
 System. String
 

### -QueueName
 System. String
 

### -AuthorizationRuleName
 System. String

## VÄRDEN

### Microsoft. Azure. commands. ServiceBus. Models. ListKeysAttributes
PrimaryConnectionString: slut punkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Queue_e xampl1 SecondaryConnectionString: slut punkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Queue_e xampl1 PrimaryKey: {PrimaryKey Value} SecondaryKey: {SecondaryKey värde} nyckel namn: SBAuthoRule1

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

