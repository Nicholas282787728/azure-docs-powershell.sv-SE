---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 125B6865-0022-4F88-BB0F-DDDDB2EDFF00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a1f1d033c3e8bae708310d12a1c4cb2b581bf80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099030"
---
# Set-AzureNetworkSecurityRule

## Sammanfattning
Lägger till eller ändrar en nätverks säkerhets regel i en nätverks säkerhets grupp.

## FRÅGESYNTAXEN

```
Set-AzureNetworkSecurityRule -Name <String> -Type <String> -Priority <Int32> -Action <String>
 -SourceAddressPrefix <String> -SourcePortRange <String> -DestinationAddressPrefix <String>
 -DestinationPortRange <String> -Protocol <String> -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureNetworkSecurityRule** lägger till eller ändrar en Azure Network Security-regel i en nätverks säkerhets grupp.

## BESKRIVS

## MALLPARAMETRAR

### -Åtgärd
Anger åtgärd för en nätverks säkerhets regel.
Giltiga värden är: Allow och Deny.

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

### -DestinationAddressPrefix
Anger CIDR-adressen (Classless Interdomain Routing) för mål-IP-adressintervallet för nätverks säkerhets regeln.
En asterisk (*) anger en IP-adress.

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

### -DestinationPortRange
Anger ett mål Port intervall för nätverks säkerhets regeln.
Giltiga värden är heltal från 0 till 65535.
Du kan ange ett enskilt värde eller ange ett område i formatet LowerNumber-HigherNumber.
Ett bindestreck avgränsar de två värdena.

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

### -Namn
Anger namnet på nätverks säkerhets regeln som denna cmdlet lägger till eller ändrar.

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

### -NetworkSecurityGroup
Anger den nätverks säkerhets grupp som denna cmdlet ändrar.
Använd Get-AzureNetworkSecurityGroup cmdlet för att få ett **INetworkSecurityGroup** -objekt.

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prioritet
Anger prioriteten för nätverks säkerhets regeln.
Giltiga värden är: heltal från 100 till 4096.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -Protokoll
Anger protokollet för nätverks säkerhets regeln.
Giltiga värden är: 

- TCP 
- UDP 
- *

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

### -SourceAddressPrefix
Anger CIDR-adressen för käll-IP-intervallet för nätverks säkerhets regeln.
En asterisk (*) anger en IP-adress.

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

### -SourcePortRange
Anger ett käll port intervall för nätverks säkerhets regeln.
Giltiga värden är heltal från 0 till 65535.
Du kan ange ett enskilt värde eller ange ett område i formatet LowerNumber-HigherNumber.
Ett bindestreck avgränsar de två värdena.

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

### – Skriv
Anger typen av anslutning för nätverks säkerhets regeln.
Giltiga värden är: inkommande och utgående.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Remove-AzureNetworkSecurityRule](./Remove-AzureNetworkSecurityRule.md)


