---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 5421c33c4858c99be4dd84ba7f0c1bff401e1182
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218711"
---
# Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript

## SYNOPSIS
Den här kommandoleten tar anslutningsresursen, VPN-enhetsmärket, modellen, versionen av inbyggd programvara och returnerar motsvarande konfigurationsskript som kunder kan använda direkt på sina lokala VPN-enheter. Skriptet följer syntaxen för den valda enheten och fyller i nödvändiga parametrar, till exempel offentliga IP-adresser för Azure Gateway, prefix för virtuella nätverksadresser, VPN-tunnelfördelade nycklar osv. så att kunder helt enkelt kan kopiera och klistra in till sina VPN-enhetskonfigurationer.

## SYNTAX

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Den här kommandoleten tar anslutningsresursen, VPN-enhetsmärket, modellen, versionen av inbyggd programvara och returnerar motsvarande konfigurationsskript som kunder kan använda direkt på sina lokala VPN-enheter. Skriptet följer syntaxen för den valda enheten och fyller i nödvändiga parametrar, till exempel offentliga IP-adresser för Azure Gateway, prefix för virtuella nätverksadresser, VPN-tunnelfördelade nycklar osv. så att kunder helt enkelt kan kopiera och klistra in till sina VPN-enhetskonfigurationer.

## EXEMPEL

### Exempel 1
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

I exemplet ovan används Get-AzVirtualNetworkGatewaySupportedVpnDevice för att få vpn-enhets olika varumärken, modeller och versioner av inbyggd programvara som stöds.
Använder sedan någon av de returnerade modellinformationen för att generera ett VPN-enhetskonfigurationsskript för VirtualNetworkGatewayConnection "TestConnection". Enheten som används i det här exemplet har DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" och FirmwareVersion 20.

## PARAMETERS

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

### -DeviceFamily
Namnet på VPN-enhetsmodellen/-familjen.

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

### -DeviceVendor
Namnet på VPN-enhetsleverantören.

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

### -FirmwareVersion
Inbyggd version av VPN-enheten.

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
Resursnamnet för anslutningen som konfigurationen ska skapas för.

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

### -ResourceGroupName
Resursgruppens namn.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

## UTDATA

### System.String

## ANTECKNINGAR

## RELATERADE LÄNKAR
