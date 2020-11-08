---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: 1db46630ea4f864e1658eea8b789a79e6050fbbb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101285"
---
# Get-AzResourceGroupDeployment

## Sammanfattning
Hämtar distributionerna i en resurs grupp.

## FRÅGESYNTAXEN

### GetByResourceGroupDeploymentName (standard)
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupDeploymentId
```
Get-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzResourceGroupDeployment** hämtar distributionerna i en Azure-resurs grupp.
Ange parametern *namn* eller *ID* för att filtrera resultaten.
Som standard får **Get-AzResourceGroupDeployment** alla distributioner för en viss resurs grupp.
En Azure-resurs är en användardefinierad Azure-enhet, till exempel en databas server, en databas eller en webbplats.
En Azure-resurs grupp är en samling Azure-resurser som distribueras som en enhet.
En distribution är den åtgärd som gör resurserna i resurs gruppen tillgängliga för användning.
Mer information om Azure-resurser och Azure resurs grupper finns i New-AzResourceGroup cmdlet.
Du kan använda denna cmdlet för att spåra.
För fel sökning kan du använda denna cmdlet med Get-AzLog cmdlet.

## BESKRIVS

### Exempel 1: Hämta alla distributioner för en resurs grupp
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

Det här kommandot får alla distributioner för resurs gruppen ContosoLabsRG.
Resultatet visar en distribution av en WordPress-blogg som använde en mall.

### Exempel 2: skaffa en distribution utifrån namn
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

Det här kommandot får DeployWebsite01 distributionen av ContosoLabsRG-resurs gruppen.
Du kan tilldela en distribution ett namn när du skapar den med hjälp av cmdletarna **New-AzResourceGroup** eller **New-AzResourceGroupDeployment** .
Om du inte tilldelar ett namn anger cmdletarna ett standard namn baserat på mallen som används för att skapa distributionen.

### Exempel 3: Hämta distributioner av alla resurs grupper
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

Det här kommandot får alla resurs grupper i ditt abonnemang med hjälp av Get-AzResourceGroup cmdlet.
Kommandot skickar resurs grupperna till den aktuella cmdleten med hjälp av pipeline-operatorn.
Den aktuella cmdleten hämtar alla resurs grupper i prenumerationen och skickar resultaten till Format-Table cmdlet för att visa deras egenskaps värden för **ResourceGroupName** , **DeploymentName** och **ProvisioningState** .

## MALLPARAMETRAR

### -ApiVersion
Anger den API-version som stöds av resurs leverantören.
Du kan ange en annan version än standard versionen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

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

### -ID
Anger ID för den resurs grupps distribution som ska erhållas.

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

### -Namn
Anger namnet på den distribution du vill hämta.
Jokertecken är inte tillåtna.

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

### -För
Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.

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
Anger namnet på en resurs grupp.
Cmdleten får distributionerna för resurs gruppen som den här parametern anger.
Jokertecken är inte tillåtna.
Den här parametern är obligatorisk och du kan endast ange en resurs grupp för varje kommando.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceGroupDeployment

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResourceGroup](./New-AzResourceGroup.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroupDeployment](./Remove-AzResourceGroupDeployment.md)

[Stopp-AzResourceGroupDeployment](./Stop-AzResourceGroupDeployment.md)

[Test-AzResourceGroupDeployment](./Test-AzResourceGroupDeployment.md)


