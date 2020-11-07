---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
ms.openlocfilehash: 44e1571dbd6da015e163a69716f06d3ed3cebde5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755645"
---
# Get-AzureRmRelayKey

## Sammanfattning
Hämtar primära och sekundära anslutnings strängar för angivna relä enheter (namespace/WcfRelay/HybridConnection).

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### NamespaceAuthorizationRuleSet (standard)
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WcfRelayAuthorizationRuleSet
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### HybridConnectionAuthorizationRuleSet
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmRelayKey** returnerar de primära och sekundära anslutnings strängarna för angivna relä enheter (namnrymd/WcfRelay/HybridConnection).

## BESKRIVS

### Exempel 1 – namnrymd
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

### Exempel 2 – WcfRelay
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1
```

### Exempel 3 – HybridConnection
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

Primära och sekundära anslutnings strängar till angivna relä enheter (namespace/WcfRelay/HybridConnection).

## MALLPARAMETRAR

### -HybridConnection
HybridConnection namn.

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
AuthorizationRule namn.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namnrymd
Namn på namn området.

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Resurs grupps namn.

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

### -WcfRelay
WcfRelay namn.

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
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

### -ResourceGroupName
 System. String 

### -NamespaceName
 System. String 
 

### -HybridConnectionsName
 System. String 

### -WcfRelayName
 System. String 

### -Namn
 System. String

## VÄRDEN

### Microsoft. Azure. commands. Relay. Models. AuthorizationRuleKeysAttributes

### Exempel 1 – namnrymd
PrimaryConnectionString: slut punkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryConnectionString: slut punkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # 01 # # # # # # # # # # # # # PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # Filnamn: AuthoRule1

### Exempel 2 – WcfRelay
PrimaryConnectionString: slut punkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 SecondaryConnectionString: slut punkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # Filnamn: AuthoRule1

### Exempel 3 – HybridConnection
PrimaryConnectionString: slut punkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection SecondaryConnectionString: slut punkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # Filnamn: AuthoRule1

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

