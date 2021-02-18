---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: 11b18f0a0f12a82e88694fd91ce89956951a4eb6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223702"
---
# New-AzVpnClientConfiguration

## SYNOPSIS
Med det här kommandot kan användarna skapa VPN-profilpaketet baserat på förkonfigurerade VPN-inställningar på VPN-gatewayen, förutom några ytterligare inställningar som användare kan behöva konfigurera, till exempel vissa rotcertifikat.

## SYNTAX

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESKRIVNING
Då kan användarna skapa VPN-profilpaketet baserat på förkonfigurerade VPN-inställningar på VPN-gatewayen, förutom några ytterligare inställningar som användare kan behöva konfigurera, till exempel vissa rotcertifikat.

## EXEMPEL

### Exempel 1
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

Den här cmdleten används för att skapa en ZIP-fil med VPN-klientprofilen för "ContosoVirtualNetworkGateway" i ResourceGroup "ContosoResourceGroup". Profilen genereras för en förkonfigurerad radieserver som är konfigurerad för att använda autentiseringsmetoden EAPTLS med certifikatfilen VpnProfileRadiusCert.

## PARAMETERS

### -AuthenticationMethod
Autentiseringsmetod kan använda värden EAPMSCHAPv2 eller EAPTLS. När EAPMSCHAPv2 anges genererar cmdleten ett installationsprogram för klientkonfiguration för användarnamn/lösenordsautentisering som EAP-MSCHAPv2 autentiseringsprotokoll. Om EAPTLS har angetts genererar cmdleten ett installationsprogram för klientkonfiguration för certifikatautentisering som använder EAP-TLS-protokollet. Alternativet "EapTls" kan användas för både RADIE-baserad certifikatautentisering och certifieringsautentisering som utförs av den virtuella nätverksgatewayen genom att ladda upp den betrodda roten. Cmdleten identifierar automatiskt vad som är konfigurerat.

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
En lista med rotcertifikatsökvägar för klienten

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

### -Name
Resursnamnet.

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
Radieserverrotcertifikatsökväg. Det här är en obligatorisk parameter som måste anges när EAP-TLS med RADIE-autentisering används. Det här är den fullständiga sökvägen för .cer-filen som innehåller ROOT-rotcertifikatet som klienten använder för att verifiera RADIE-servern under autentiseringen.

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
Visar vad som skulle hända om cmdleten körs. Cmdleten körs inte.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### System.String

### System.String[]

## UTDATA

### Microsoft.Azure.Commands.Network.Models.PSVpnProfile

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzVpnClientConfiguration](./Get-AzVpnClientConfiguration.md)
