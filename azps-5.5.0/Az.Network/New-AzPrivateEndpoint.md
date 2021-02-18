---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: df298b41ea1efa4915cb7556b9fd07b1d8f3e2de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218455"
---
# New-AzPrivateEndpoint

## SYNOPSIS
Skapar en privat slutpunkt.

## SYNTAX

### Alla

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING

**Cmdleten New-AzPrivateEndpoint** skapar en privat slutpunkt.

## EXEMPEL

### Exempel 1: Skapa en privat slutpunkt

I följande exempel skapas en privat slutpunkt med ett specifikt tjänste-ID för den privata länken i det angivna undernätet i ett virtuellt nätverk.

```powershell
$virtualNetwork = Get-AzVirtualNetwork -ResourceName 'myVirtualNetwork' -ResourceGroupName 'myResourceGroup'
$subnet = $virtualNetwork | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mySubnet'
$plsConnection= New-AzPrivateLinkServiceConnection -Name 'MyPLSConnections' -PrivateLinkServiceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService' -RequestMessage 'Please Approve my request'
New-AzPrivateEndpoint -Name 'MyPrivateEndpoint' -ResourceGroup 'myResourceGroup' -Location 'centralus' -PrivateLinkServiceConnection $plsConnection -Subnet $subnet
```

## PARAMETERS

### -As Ent fån

Kör cmdleten som ett jobb i bakgrunden.

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

### -ByManualRequest

Använd manuell begäran för att upprätta anslutningen.

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

Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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

Be inte om bekräftelse om att skriva över en resurs.

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

### -Plats

Anger en plats för den privata slutpunkten. Använd [Get-AzLocation till](/powershell/module/az.resources/get-azlocation) att fastställa giltiga värden för den här parametern.

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

### -Name

Namn på den privata slutpunkten.

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

### -PrivateLinkServiceConnection

Resurs-ID för att ansluta den privata slutpunkten.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName

Anger namnet på resursgruppen.

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

### -Subnet

Undernätet till den privata slutpunkten.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag

Nyckelvärdepar i form av en hash-tabell. Till exempel: @{key0='value0';key1=$null;key2='value2'}

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

### -Bekräfta

Frågar dig om bekräftelse innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)

## INDATA

### System.String

### Microsoft.Azure.Commands.Network.Models.PSSubnet

### Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]

## UTDATA

### Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzPrivateEndpoint](./Get-AzPrivateEndpoint.md)

[Remove-AzPrivateEndpoint](./Remove-AzPrivateEndpoint.md)

[New-AzPrivateLinkServiceConnection](./New-AzPrivateLinkServiceConnection.md)