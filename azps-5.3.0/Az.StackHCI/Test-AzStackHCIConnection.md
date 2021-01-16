---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 1183a2aa6bf452d77ebe3975024067244075e5fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98418923"
---
# Test-AzStackHCIConnection

## Sammanfattning
Test-AzStackHCIConnection verifiera anslutningar från lokala klustrade noder till de Azure-tjänster som krävs av Azure Stack HCI.

## FRÅGESYNTAXEN

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Test-AzStackHCIConnection verifiera anslutningar från lokala klustrade noder till de Azure-tjänster som krävs av Azure Stack HCI.

## BESKRIVS

### EXEMPEL 1
```
Invoking on one of the cluster node. Success case.
```

C:\PS \> test-AzStackHCIConnection-test: Anslut till Azure Stack HCI-tjänsten EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: true result: lyckades

### EXEMPEL 2
```
Invoking on one of the cluster node. Failed case.
```

C:\PS \> test-AzStackHCIConnection test: Anslut till Azure Stack HCI-tjänsten EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: true result: misslyckad FailedNodes: Node1inClus2, Node2inClus3

## MALLPARAMETRAR

### -ComputerName
Anger en av klusternoderna i det lokala klustret som registreras på Azure.

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

### -Autentiseringsuppgift
Anger autentiseringsuppgifter för dator namnet.
Standard är den aktuella användaren som kör cmdleten.

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
Standard är AzureCloud.
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
Anger vilken region du vill ansluta till.
Används inte såvida det inte är en Kanarie region.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

## VÄRDEN

### PSCustomObject. Returnerar följande egenskaper i PSCustomObject
### Test: namnet på testet som utförts.
### EndpointTested: slut punkt som används i testet.
### IsRequired: sant eller falskt
### Resultat: lyckades eller misslyckades
### FailedNodes: lista med noder där testet misslyckades.
## ANMÄRKNINGAR

## RELATERADE LÄNKAR
