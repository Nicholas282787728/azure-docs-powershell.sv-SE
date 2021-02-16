---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 34831104bc1b27aa115d56545c784e0fea856ba4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212334"
---
# Test-AzStackHCIConnection

## SYNOPSIS
Test-AzStackHCIConnection verifierar anslutningen från lokala grupperade noder till de Azure-tjänster som krävs av Azure Stack HCI.

## SYNTAX

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## BESKRIVNING
Test-AzStackHCIConnection verifierar anslutningen från lokala grupperade noder till de Azure-tjänster som krävs av Azure Stack HCI.

## EXEMPEL

### EXEMPEL 1
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Succeeded
```
Skapa en anrop på en av klusternoden. Ett lyckat ärende.

### EXEMPEL 2
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Failed
FailedNodes: Node1inClus2, Node2inClus3
```
Skapa en anrop på en av klusternoden. Misslyckades.

## PARAMETERS

### -Datornamn
Anger en av klusternoden i det lokala kluster som registreras i Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
Anger autentiseringsnamnet för Datornamn.
Standardvärdet är den aktuella användaren som kör Cmdleten.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnvironmentName
Anger Azure-miljön.
Standardvärdet är AzureCloud.
Giltiga värden är AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### -Region
Anger vilken region som ska anslutas till.
Används endast om det är en canary-region.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

## UTDATA

### PSCustomObject. Returnerar följande egenskaper i PSCustomObject
### Test: Namn på testet som utförs.
### EndpointTested: Slutpunkt som används i testet.
### IsRequired: True eller False
### Resultat: Lyckades eller misslyckades
### FailedNodes: Lista över noder där testet misslyckades.
## ANTECKNINGAR

## RELATERADE LÄNKAR
