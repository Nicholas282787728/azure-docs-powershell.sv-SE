---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 3d955b2133f4a262b69de1413c5a4bf4d8e719b9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922204"
---
# Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript

## Sammanfattning
Den här cmdleten tar anslutnings resursen, VPN-enhetens varumärke, modell, inbyggd program vara-version och returnerar motsvarande konfigurations skript som kunderna kan använda direkt på sina lokala VPN-enheter. Skriptet följer syntaxen för den valda enheten och fyller i nödvändiga parametrar, till exempel Azure Gateway offentlig IP-adresser, prefix för virtuell nätverks adress, VPN-tunnel i förväg, etc. så att kunder helt enkelt kan kopiera-klistra in till sina VPN-enheter.

## FRÅGESYNTAXEN

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Den här cmdleten tar anslutnings resursen, VPN-enhetens varumärke, modell, inbyggd program vara-version och returnerar motsvarande konfigurations skript som kunderna kan använda direkt på sina lokala VPN-enheter. Skriptet följer syntaxen för den valda enheten och fyller i nödvändiga parametrar, till exempel Azure Gateway offentlig IP-adresser, prefix för virtuell nätverks adress, VPN-tunnel i förväg, etc. så att kunder helt enkelt kan kopiera-klistra in till sina VPN-enheter.

## BESKRIVS

### Exempel 1
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

I exemplet ovan används Get-AzVirtualNetworkGatewaySupportedVpnDevice för att få VPN-enheternas varumärken, modeller och inbyggd program vara.
Sedan används en av den information som returneras för att skapa ett skript för VPN-enhets konfiguration för VirtualNetworkGatewayConnection "TestConnection". Enheten som används i det här exemplet har DeviceFamily "IOS-test", DeviceVendor "Cisco-test" och FirmwareVersion 20.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceFamily
Namn på VPN-enhetens modell/-familj.

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

### -DeviceVendor
Namn på VPN-enhetens tillverkare.

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

### -FirmwareVersion
Inbyggd program varu version för VPN-enheten.

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

### -Namn
Resurs namn för den anslutning vars konfiguration ska skapas.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Resurs gruppens namn.

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

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### System. String

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

