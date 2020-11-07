---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 3ba27cf26ccc555ea79a2b46100bee6be7e3c7fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754213"
---
# Remove-AzDeploymentManagerServiceUnit

## Sammanfattning
Tar bort tjänst enheten.

## FRÅGESYNTAXEN

### Interaktivt (standard)
```
Remove-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByTopologyObjectAndServiceName
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByTopologyResourceAndServiceName
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByServiceObject
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByServiceResourceId
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ID
```
Remove-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Remove-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzDeploymentManagerServiceUnit** tar bort en tjänst enhet i en tjänst.

Ange tjänst enheten efter dess namn, den tjänst som den har definierats under, namnet på tjänst sto pol Ogin och resurs grupp namnet. Du kan också ange ServiceUnit-objektet eller ResourceId.

## BESKRIVS

### Exempel 1
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

Det här kommandot tar bort en tjänst enhet med namnet ContosoService1Storage under en tjänst-ContosoService1 i en tjänstmall som heter ContosoServiceTopology i ContosoResourceGroup.

### Exempel 2: ta bort en tjänst enhet med resurs-ID.
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

Det här kommandot får en tjänst enhet som heter ContosoService1Storage under en tjänst ContosoService1 i en tjänstmall som heter ContosoServiceTopology i ContosoResourceGroup.

### Exempel 3: ta bort en tjänst enhet med hjälp av serviceobjektet.
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

Det här kommandot tar bort en tjänst enhet vars namn, tjänst namn, namn på tjänste topologi och ResourceGroup matchar namnet, ServiceName, ServiceTopologyName och ResourceGroupName för $serviceUnitObject.

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
Tjänst enhetens resurs objekt.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Namn
Namnet på tjänste enheten.

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName, ByServiceObject, ByServiceResourceId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
{{Fill PassThru Description}}

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

### -ServiceName
Namnet på tjänsten som tjänst enheten är en del av.

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceObject
Serviceobjektet där tjänste enheten ska skapas.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceResourceId
ID för tjänste resursen där tjänste enheten ska skapas.

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceTopologyName
Namnet på den tjänstmall som tjänst enheten är en del av.

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

### -ServiceTopologyObject
Det tjänst Topology-objekt där tjänste enheten ska skapas.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceTopologyResourceId
Resurs-ID för tjänste topologi där tjänst enheten ska skapas.

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
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
Visar vad som händer om cmdleten körs.
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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

### Microsoft. Azure. commands. DeploymentManager. Models. PSServiceUnitResource

## VÄRDEN

### System. Boolean

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
