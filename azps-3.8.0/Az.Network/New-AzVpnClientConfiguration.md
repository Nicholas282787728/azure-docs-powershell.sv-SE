---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: 11b18f0a0f12a82e88694fd91ce89956951a4eb6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090945"
---
# New-AzVpnClientConfiguration

## Sammanfattning
Med det här kommandot kan användarna skapa ett VPN-grupppaket baserat på förkonfigurerade VPN-inställningar på VPN-gatewayen, utöver ytterligare inställningar som användarna kan behöva konfigurera, till exempel. vissa rot certifikat.

## FRÅGESYNTAXEN

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
då kan användarna skapa ett VPN-grupppaket baserat på förkonfigurerade VPN-inställningar på VPN-gatewayen, samt vissa ytterligare inställningar som användarna kan behöva konfigurera, till exempel. vissa rot certifikat.

## BESKRIVS

### Exempel 1
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

Denna cmdlet används för att skapa en zip-fil för VPN-klienter för "ContosoVirtualNetworkGateway" i ResourceGroup "ContosoResourceGroup". Profilen genereras för en förkonfigurerad RADIUS-server som är konfigurerad att använda autentiseringsmetoden "EAPTLS" med VpnProfileRadiusCert-certifikat filen.

## MALLPARAMETRAR

### -AuthenticationMethod
Autentiseringsmetoden kan ta värden EAPMSCHAPv2 eller EAPTLS. När EAPMSCHAPv2 anges genererar cmdleten ett installations program för klient konfiguration för användar namn/lösen ord som använder EAP-MSCHAPv2 autentiseringsprotokoll. Om EAPTLS anges genererar cmdleten ett installations program för klient konfiguration för certifikatautentisering som använder EAP-TLS-protokoll. Alternativet "EapTls" kan användas för både RADIUS-baserad certifikatautentisering och certifikatautentisering som utförs av den virtuella Nätverksgatewayen genom att överföra den betrodda roten. Cmdleten upptäcker automatiskt vad som är konfigurerat.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ClientRootCertificateFileList
En lista över sökvägar till klient rot certifikat

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Resurs namn.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProcessorArchitecture
ProcessorArchitecture

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RadiusRootCertificateFile
Sökväg till rot certifikat för RADIUS-server. Det här är en obligatorisk parameter som måste anges när EAP-TLS används för RADIUS-identifiering. Det här är den fullständiga sökvägen till CER-filen som innehåller RADIUS-rotcertifikatet som klienten använder för att validera RADIUS-servern vid verifiering.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Resurs gruppens namn.

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
Du uppmanas att bekräfta innan du kör cmdleten.

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
Visar vad som händer om cmdleten körs. Cmdleten körs inte.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

### System. string []

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSVpnProfile

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzVpnClientConfiguration](./Get-AzVpnClientConfiguration.md)
