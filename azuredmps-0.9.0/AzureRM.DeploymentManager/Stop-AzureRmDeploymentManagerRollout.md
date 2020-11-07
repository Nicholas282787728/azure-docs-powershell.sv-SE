---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/stop-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: 3c4f221fc00187c4faea2dbcc1a5014822c476c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754934"
---
# Stop-AzureRmDeploymentManagerRollout

## Sammanfattning
Avslutar en pågående installation.

## FRÅGESYNTAXEN

### Interaktivt (standard)
```
Stop-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ID
```
Stop-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Stop-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Stop-AzureRmDeploymentManagerRollout** stoppar en pågående installation och returnerar ett objekt som representerar det aktuella tillståndet för installationen.
Ange utgivningen med dess namn och resurs grupps namn. Du kan också ange ett installations objekt eller ResourceId.

Observera att när en introduktion har stoppats kan den inte återupptas eller startas om. Du kan bara skapa en ny installation.

## BESKRIVS

### Exempel 1
```powershell
PS C:\> Stop-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

Det här kommandot stoppar en installation med namnet ContosoRollout i ContosoResourceGroup. 

### Exempel 2: stoppa en lansering med resurs-ID
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

Det här kommandot stoppar en installation med namnet ContosoRollout i ContosoResourceGroup.

### Exempel 3: stoppa en installation med hjälp av installations objekt.
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

Det här kommandot stoppar en installation vars namn och ResourceGroup matchar $rolloutObjectens namn och ResourceGroupName-egenskaper.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Fråga inte efter bekräftelse.

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

### -Namn
Namnet på installationen.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
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

### -Lansering
Resursen som ska tas bort.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. commands. DeploymentManager. Models. PSRollout

## VÄRDEN

### Microsoft. Azure. commands. DeploymentManager. Models. PSRollout

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmDeploymentManagerRollout](./Get-AzureRmDeploymentManagerRollout.md)

[Restart-AzureRmDeploymentManagerRollout](./Restart-AzureRmDeploymentManagerRollout.md)

[Remove-AzureRmDeploymentManagerRollout](./Remove-AzureRmDeploymentManagerRollout.md)