---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
ms.openlocfilehash: 777e03a570f3915d6e0ebe4cbb5c84f9c1824120
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223630"
---
# Remove-AzVirtualNetwork

## SYNOPSIS
Tar bort ett virtuellt nätverk.

## SYNTAX

```
Remove-AzVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Remove-AzVirtualNetwork** tar bort ett virtuellt Azure-nätverk.

## EXEMPEL

### 1: Skapa och ta bort ett virtuellt nätverk
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
    
Remove-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

I det här exemplet skapas ett virtuellt nätverk i en resursgrupp och det tas sedan bort direkt. Om du vill utelämna uppmaningen när du tar bort det virtuella nätverket använder du flaggan -Force.

## PARAMETERS

### -As Ent
Kör cmdleten i bakgrunden

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

### -DefaultProfile
Autentiseringsuppgifterna, kontot, klientorganisationen och prenumerationen som används för kommunikation med Azure.

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

### -Force
Tvingar kommandot att köras utan att användaren uppmanas att bekräfta.

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

### -Name
Anger namnet på det virtuella nätverket som cmdleten tar bort.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Returnerar ett objekt som representerar det objekt som du arbetar med.
Som standard genererar inte den här cmdleten några utdata.

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

### -ResourceGroupName
Anger namnet på resursgruppen som innehåller det virtuella nätverket som cmdleten tar bort.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Frågar dig om bekräftelse innan du kör cmdleten.

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
Visar vad som skulle hända om cmdleten körs.
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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### System.String

## UTDATA

### System.Boolean

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)

[New-AzVirtualNetwork](./New-AzVirtualNetwork.md)

[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)


