---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C7F08804-E177-4BC5-8F0E-DEC1B467C4BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20cb37fbba8fd3789c0932f9ff1e9352334662e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099074"
---
# Update-AzureApplicationGateway

## Sammanfattning
Uppdaterar en Programgateway.

## FRÅGESYNTAXEN

```
Update-AzureApplicationGateway -Name <String> [-VnetName <String>]
 [-Subnets <System.Collections.Generic.List`1[System.String]>] [-InstanceCount <UInt32>]
 [-GatewaySize <String>] [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Update-AzureApplicationGateway** uppdaterar en befintlig Programgateway.

## BESKRIVS

### Exempel 1: ändra en Programgateway genom att använda dess namn
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork18" -Subnets @("Subnet05", "Subnet06")
```

Det första kommandot stoppar programgatewayen med namnet ApplicationGateway06.
En Programgateway måste stoppas innan du kan ändra virtuella nätverk eller undernät.

Det andra kommandot ändrar det virtuella undernät och undernät för programgatewayen med namnet ApplicationGateway06.

### Exempel 2: ändra ytterligare egenskaper för en Programgateway
```
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -InstanceCount 2 -GatewaySize "Large" -Description "Updated application gateway"
```

Det här kommandot ändrar antalet instanser, Gateway-storlek och beskrivning för den Programgateway som heter ApplicationGateway06.
Det här kommandot ändrar inte virtuella nätverk eller undernät för programgatewayen.
Därför behöver du inte stoppa programgatewayen innan du kör det här kommandot.

### Exempel 3: ändra en Programgateway genom att använda pipeline
```
PS C:\> $ApplicationGateway = Get-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> $ApplicationGateway.GatewaySize = "Medium"
PS C:\> $ApplicationGateway | Update-AzureApplicationGateway
```

Det första kommandot hämtar programgatewayen med namnet ApplicationGateway06 med hjälp av cmdleten **Get-AzureApplicationGateway** .
Kommandot sparar det i $ApplicationGateway variabel.

Det andra kommandot tilldelar värdet medium till egenskapen **GatewaySize** .

Det sista kommandot skickar den uppdaterade $ApplicationGateway till den aktuella cmdleten.

## MALLPARAMETRAR

### -Beskrivning
Anger en beskrivning av att denna cmdlet tilldelar programgatewayen.

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

### -GatewaySize
Anger den storlek som denna cmdlet tilldelar programgatewayen.
Giltiga värden är:

- Eld
- Risk
- Höga

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

### -InstanceCount
Anger antalet instanser som denna cmdlet tilldelar programgatewayen.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger namnet på den Application Gateway som uppdateras med den här cmdleten.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser.
Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

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

### -Undernät
Anger en matris med undernät där denna cmdlet distribuerar programgatewayen.

Du kan inte uppdatera undernät medan Application Gateway körs.
Om du vill stoppa programgatewayen använder du Stop-AzureApplicationGateway cmdleten.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VnetName
Anger det virtuella nätverk där denna cmdlet distribuerar programgatewayen.

Du kan inte uppdatera ett virtuellt nätverk när Application Gateway körs.
Stoppa programgatewayen genom att använda **Stop-AzureApplicationGateway**.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureApplicationGateway](./Get-AzureApplicationGateway.md)

[New-AzureApplicationGateway](./New-AzureApplicationGateway.md)

[Remove-AzureApplicationGateway](./Remove-AzureApplicationGateway.md)

[Start-AzureApplicationGateway](./Start-AzureApplicationGateway.md)

[Stopp-AzureApplicationGateway](./Stop-AzureApplicationGateway.md)
