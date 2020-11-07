---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: fbcb93ec75dc0e136c1c18743a8686f7642ef02f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744396"
---
# Get-AzDeploymentManagerRollout

## Sammanfattning
Hämtar installationen.

## FRÅGESYNTAXEN

### Interaktivt (standard)
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ID
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzDeploymentManagerRollout** hämtar en introduktion och returnerar ett objekt som representerar en installation med all detaljerad information om hur installationen fortskrider.
Ange utgivningen med dess namn och resurs grupps namn. Du kan också ange ett installations objekt eller ResourceId.

Det hämtade installations-objektet innehåller tjänster, tjänste enheter och steg som har distribuerats och de som pågår. De som ännu inte ska distribueras är inte i svaret.

## BESKRIVS

### Exempel 1 kom igång
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

Det här kommandot får en installation med namnet ContosoRollout i ContosoResourceGroup. 

### Exempel 2 Hämta och Visa information om installationen
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

Det här kommandot får en installation med namnet ContosoRollout i ContosoResourceGroup. Växeln-verbose visar alla utgivnings uppgifter hierarkiskt; visar tjänsterna, ServiceUnits och stegen under varje ServiceUnit och kontextuell information för varje steg i en helhets vy av lanseringen.

### Exempel 3: komma igång med resurs-ID
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

Det här kommandot får en installation med namnet ContosoRollout i ContosoResourceGroup.

### Exempel 4: kom igång med installations objekt.
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

Det här kommandot får en installation vars namn och ResourceGroup matchar $rolloutObjectens namn och ResourceGroupName-egenskaper.

## MALLPARAMETRAR

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

### -InputObject
Introduktions objekt.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Namn
Namnet på installationen.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Resurs gruppen.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Resurs-ID.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetryAttempt
Försök igen.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

### System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

### Microsoft. Azure. commands. DeploymentManager. Models. PSRollout

## VÄRDEN

### Microsoft. Azure. commands. DeploymentManager. Models. PSRollout

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
