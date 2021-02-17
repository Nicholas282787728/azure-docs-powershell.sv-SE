---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: 82df573a658fda9af97778e59819e45359c226fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220526"
---
# Get-AzResourceGroupDeployment

## SYNOPSIS
Hämtar distributionerna i en resursgrupp.

## SYNTAX

### GetByResourceGroupDeploymentName (standard)
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupDeploymentId
```
Get-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzResourceGroupDeployment** hämtar distributionerna i en Azure-resursgrupp.
Ange *namn- eller* *Id-parametern* för att filtrera resultatet.
Som standard **hämtar Get-AzResourceGroupDeployment** alla distributioner för en angiven resursgrupp.
En Azure-resurs är en användar hanterad Azure-enhet, till exempel en databasserver, databas eller webbplats.
En Azure-resursgrupp är en samling Azure-resurser som distribueras som en enhet.
En distribution är den åtgärd som gör resurserna i resursgruppen tillgängliga för användning.
Mer information om Azure-resurser och Azure-resursgrupper finns i New-AzResourceGroup cmdlet.
Du kan använda den här cmdleten för spårning.
Använd den här cmdleten med cmdleten Get-AzLog felsökning.

## EXEMPEL

### Exempel 1: Hämta alla distributioner för en resursgrupp
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

Det här kommandot hämtar alla distributioner för resursgruppen ContosoLabsRG.
Resultatet visar en distribution för en WordPress-blogg som använde en gallerimall.

### Exempel 2: Hämta en distribution efter namn
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

Det här kommandot får distributionen DeployWebsite01 av resursgruppen ContosoLabsRG.
Du kan tilldela en distribution ett namn när du skapar den med cmdletsna **New-AzResourceGroup** eller **New-AzResourceGroupDeployment.**
Om du inte tilldelar ett namn tillhandahåller cmdletarna ett standardnamn baserat på mallen som används för att skapa distributionen.

### Exempel 3: Hämta distributionerna av alla resursgrupper
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

Med det här kommandot får du alla resursgrupper i din prenumeration med hjälp Get-AzResourceGroup cmdleten.
Kommandot skickar resursgrupperna till den aktuella cmdleten med hjälp av rörledningsoperatorn.
Den aktuella cmdleten hämtar alla distributioner av alla resursgrupper i prenumerationen och skickar resultatet till cmdleten Format-Table för att visa egenskapsvärdena **ResourceGroupName,** **DeploymentName** och **ProvisioningState.**

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

### -Id
Anger ID för den resursgruppdistribution som ska distribueras.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Anger namnet på den distribution som ska distribueras.
Jokertecken tillåts inte.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Anger att denna cmdlet tar hänsyn till förhandsversioner av API-versioner när den automatiskt avgör vilken version som ska användas.

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
Anger namnet på en resursgrupp.
Cmdleten hämtar distributionerna för resursgruppen som parametern anger.
Jokertecken tillåts inte.
Den här parametern är obligatorisk och du kan bara ange en resursgrupp i varje kommando.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

## UTDATA

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResourceGroup](./New-AzResourceGroup.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroupDeployment](./Remove-AzResourceGroupDeployment.md)

[Stop-AzResourceGroupDeployment](./Stop-AzResourceGroupDeployment.md)

[Test-AzResourceGroupDeployment](./Test-AzResourceGroupDeployment.md)


