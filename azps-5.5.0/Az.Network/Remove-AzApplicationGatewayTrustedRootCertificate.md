---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 3e8c4f6bc25ea5ff9b8efcee989937fb688fea57
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218391"
---
# Remove-AzApplicationGatewayTrustedRootCertificate

## SYNOPSIS
Tar bort ett betrott rotcertifikat från en programgateway.

## SYNTAX

```
Remove-AzApplicationGatewayTrustedRootCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Remove-AzApplicationGatewayTrustedRootCertificate** tar bort ett betrott rotcertifikat från en befintlig Application Gateway.

## EXEMPEL

### Exempel 1
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name "myRootCA"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

Det första kommandot hämtar en programgateway och lagrar den i $gw variabeln.
Det andra kommandot tar bort det betrodda rotcertifikatet myRootCA från programgatewayen som lagras i $gw.
Det tredje kommandot uppdaterar programmets gateway i Azure.

## PARAMETERS

### -ApplicationGateway
ApplicationGateway

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
Namnet på TrustedRoot-certifikatet

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## UTDATA

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Add-AzApplicationGatewayTrustedRootCertificate](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[Get-AzApplicationGatewayTrustedRootCertificate](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[New-AzApplicationGatewayTrustedRootCertificate](./New-AzApplicationGatewayTrustedRootCertificate.md)

[Set-AzApplicationGatewayTrustedRootCertificate](./Set-AzApplicationGatewayTrustedRootCertificate.md)
