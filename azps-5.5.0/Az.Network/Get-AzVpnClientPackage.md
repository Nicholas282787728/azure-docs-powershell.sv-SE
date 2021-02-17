---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: ec91fecd41138238bc4d89fa81d77bae4730c770
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407615"
---
# Get-AzVpnClientPackage

## SYNOPSIS
Hämtar information om ett VPN-klientpaket.

## SYNTAX

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzVpnClientPackage** hämtar information om VPN-klientpaket som är tillgängliga från en virtuell nätverksgateway.
Klientpaket innehåller konfigurationsdata som gör det möjligt för en klientdator att upprätta en VPN-anslutning till ett virtuellt Azure-nätverk. klientdatorer måste ha rätt konfigurationspaket installerat för att kunna upprätta en VPN-anslutning.
Olika konfigurationspaket är tillgängliga beroende på klientdatorns version av Windows (till exempel Windows 7 eller Windows 10) och på klientdatorns processorarkitektur (AMD64 eller x86).
Du måste ange arkitekturtypen när du kör **Get-AzVpnClientPackage.**

## EXEMPEL

### Exempel 1: Få information om ett VPN-klientpaket för processorarkitektur
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

Det här kommandot hämtar information om AMD64 VPN-klientpaketen som lagras på den virtuella nätverksgatewayen ContosoVirtualNetworkGateway.
Om du vill ha information om x86-klientpaketen anger du värdet för *parametern ProcessorArchitecture* till x86.

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

### -ProcessorArchitecture
Anger vilken typ av CPU-arkitektur som klientpaketet är avsett för.
Giltiga värden är Amd64 och X86.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på resursgruppen som den virtuella nätverksgatewayen är tilldelad till.
Resursgrupper kategoriserar objekt för att förenkla lagerhantering och allmän Azure-administration.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
Anger namnet på den virtuella nätverksgatewayen där informationen om klientpaketet lagras.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

[Resize-AzVirtualNetworkGateway](./Resize-AzVirtualNetworkGateway.md)



