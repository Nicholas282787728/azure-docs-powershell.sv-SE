---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: e59f09d44c1d6003122992cb5f14f51b411be25e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753985"
---
# Add-AzApplicationGatewayBackendAddressPool

## Sammanfattning
Lägger till en adresspool för en Programgateway.

## FRÅGESYNTAXEN

```
Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Add-AzApplicationGatewayBackendAddressPool** lägger till en backend-adresspool till en Programgateway.
En backend-adress kan anges med en IP-adress, ett fullkvalificerat domän namn (FQDN) eller IP-konfigurations-ID.

## BESKRIVS

### Exempel 1: lägga till en backend-adresspool med hjälp av en server för backend-servern
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabel. Det andra kommandot lägger till backend-adresspoolen för den Programgateway som lagras i $AppGw genom att använda FQDN-namn.

### Exempel 2: lägga till en backend-adresspool genom att använda IP-adresser för backend-servern
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add -AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabel. Det andra kommandot lägger till backend-adresspoolen för den Programgateway som lagras i $AppGw genom att använda IP-adresser.

### Exempel 3: Seta backend-adresspool genom att använda ID för backend-serverns IP-adress
```
PS C:\>$Nic01 = Get-AzNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

Det första kommandot får ett nätverks gränssnitts objekt med namnet Nic01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar det i variabeln $Nic 01. Det andra kommandot får ett nätverks gränssnitts objekt med namnet Nic02 som tillhör resurs gruppen med namnet ResourceGroup02 och lagrar det i $Nic 02-variabeln. Det tredje kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen "ResourceGroup01" och lagrar den i $AppGw variabel. Kommandot det sista använder IP-konfigurations-ID för backend från $Nic 01 och $Nic 02 för att lägga till backend-adresspoolen för Application Gateway som lagras i $AppGw.

## MALLPARAMETRAR

### -ApplicationGateway
Anger den Programgateway som denna cmdlet lägger till en backend-adresspool för.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -BackendFqdns
Anger en lista över FQDN-namn för Server delar som denna cmdlet lägger till som backend-adresspool.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendIPAddresses
Anger en lista över backend-IP-adresser som denna cmdlet lägger till som backend-server.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -Namn
Anger namnet på backend-serverpoolen som denna cmdlet lägger till.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. commands. Networks. Models. PSApplicationGateway

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSApplicationGateway

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzApplicationGatewayBackendAddressPool](./Get-AzApplicationGatewayBackendAddressPool.md)

[Get-AzApplicationGatewayBackendAddressPool](./Get-AzApplicationGatewayBackendAddressPool.md)

[New-AzApplicationGatewayBackendAddressPool](./New-AzApplicationGatewayBackendAddressPool.md)

[Remove-AzApplicationGatewayBackendAddressPool](./Remove-AzApplicationGatewayBackendAddressPool.md)

[Set-AzApplicationGatewayBackendAddressPool](./Set-AzApplicationGatewayBackendAddressPool.md)


