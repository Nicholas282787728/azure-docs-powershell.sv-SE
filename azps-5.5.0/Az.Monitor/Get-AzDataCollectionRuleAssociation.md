---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 144e67a2e58aeaa7fe7aa424ddc79bfca4aaa538
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214255"
---
# Get-AzDataCollectionRuleAssociation

## SYNOPSIS
Hämtar regler för datainsamling.

## SYNTAX

### ByAssociatedResource (standard)
```
Get-AzDataCollectionRuleAssociation 
   -TargetResourceId <string> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### ByName
```
Get-AzDataCollectionRuleAssociation 
   -TargetResourceId <string> 
   -AssociationName <string> 
   [-DefaultProfile <IAzureContextContainer>] 
   [<CommonParameters>]
```

### ByRule
```
Get-AzDataCollectionRuleAssociation 
   -ResourceGroupName <string> 
   -RuleName <string> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### ByInputObject
```
Get-AzDataCollectionRuleAssociation 
   -InputObject <PSDataCollectionRuleResource> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzDataCollectionRuleAssociation** får en eller flera DCRA-regelassociationer (DCRA).

Om du vill använda en DCR på en virtuell dator skapar du en koppling för den virtuella datorn. En virtuell dator kan ha en koppling till flera DCR-avtal och en DCR kan ha flera virtuella datorer kopplade till sig. På så sätt kan du definiera en uppsättning DCR-regler, som alla matchar ett visst krav, och bara tillämpa dem på de virtuella datorer där de gäller. Här är ["Konfigurera datainsamling för Azure Monitor-agenten"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) med DCRA-artikeln.

## EXEMPEL

### Exempel 1: Hämta regelassociationer för datainsamling efter målresurs-ID (associerad virtuell dator)
```
PS C:\>$vm = Get-AzVM -ResourceGroupName $rg -Name $vmName
PS C:\>Get-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

Det här kommandot visar alla regler för datainsamling för det givna målresurs-ID:t (virtuell dator).

### Exempel 2: Hämta regelassociationer för datainsamling efter regel (DCR)
```
PS C:\>Get-AzDataCollectionRuleAssociation -ResourceGroup $rg -RuleName $dcrName

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

Det här kommandot visar en lista över regelassociationer för den givna resursgruppen och regeln (DCR).

### Exempel 3: Hämta regelassociationer för datainsamling efter indataobjekt (PSDataCollectionRuleResource)
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName $rg -RuleName $dcrName
PS C:\>$dcr | Get-AzDataCollectionRuleAssociation

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

Det här kommandot visar en lista över regelassociationer för det givna indataobjektet.

### Exempel 4: Få en regelassociation för datainsamling genom målresurs-ID (associerad virtuell dator) och associationsnamn
```
PS C:\>Get-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id -AssociationName $assocName

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

Det här kommandot listar en (en lista med ett enda element) som regel för datainsamlingsregel.

## PARAMETERS

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure

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

### -TargetResourceId
Det associerade resurs-ID:t

```yaml
Type: System.String
Parameter Sets: ByAssociatedResource (Default)
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Resursgruppnamnet

```yaml
Type: System.String
Parameter Sets: ByRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RuleName
Namnet på datainsamlingsregeln

```yaml
Type: System.String
Parameter Sets: ByRule
Aliases: DataCollectionRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
PSDataCollectionRuleResource Object

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -AssociationName
Namnet på associationen.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String
### Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource

## UTDATA

### Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md) 
 [New-AzDataCollectionRuleAssociation](./New-AzDataCollectionRuleAssociation.md)
