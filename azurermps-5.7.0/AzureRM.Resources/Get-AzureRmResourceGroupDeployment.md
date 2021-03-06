---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: dd61700c5f064a7bc1db84286252a57c18a212db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756462"
---
# Get-AzureRmResourceGroupDeployment

## Sammanfattning
Hämtar distributionerna i en resurs grupp.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### GetByResourceGroupDeploymentName (standard)
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupDeploymentId
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmResourceGroupDeployment** hämtar distributionerna i en Azure-resurs grupp.
Ange parametern *namn* eller *ID* för att filtrera resultaten.
Som standard får **Get-AzureRmResourceGroupDeployment** alla distributioner för en viss resurs grupp.

En Azure-resurs är en användardefinierad Azure-enhet, till exempel en databas server, en databas eller en webbplats.
En Azure-resurs grupp är en samling Azure-resurser som distribueras som en enhet.

En distribution är den åtgärd som gör resurserna i resurs gruppen tillgängliga för användning.
Mer information om Azure-resurser och Azure resurs grupper finns i New-AzureRmResourceGroup cmdlet.

Du kan använda denna cmdlet för att spåra.
För fel sökning kan du använda denna cmdlet med Get-AzureRmLog cmdlet.

## BESKRIVS

### Exempel 1: Hämta alla distributioner för en resurs grupp
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

Det här kommandot får alla distributioner för resurs gruppen ContosoLabsRG.
Resultatet visar en distribution av en WordPress-blogg som använde en mall.

### Exempel 2: skaffa en distribution utifrån namn
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

Det här kommandot får DeployWebsite01 distributionen av ContosoLabsRG-resurs gruppen.
Du kan tilldela en distribution ett namn när du skapar den med hjälp av cmdletarna **New-AzureRmResourceGroup** eller **New-AzureRmResourceGroupDeployment** .
Om du inte tilldelar ett namn anger cmdletarna ett standard namn baserat på mallen som används för att skapa distributionen.

### Exempel 3: Hämta distributioner av alla resurs grupper
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

Det här kommandot får alla resurs grupper i ditt abonnemang med hjälp av Get-AzureRmResourceGroup cmdlet.
Kommandot skickar resurs grupperna till den aktuella cmdleten med hjälp av pipeline-operatorn.
Den aktuella cmdleten hämtar alla resurs grupper i prenumerationen och skickar resultaten till Format-Table cmdlet för att visa deras egenskaps värden för **ResourceGroupName** , **DeploymentName** och **ProvisioningState** .

## MALLPARAMETRAR

### -ApiVersion
Anger den API-version som stöds av resurs leverantören.
Du kan ange en annan version än standard versionen.

```yaml
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Anger ID för den resurs grupps distribution som ska erhållas.

```yaml
Type: String
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
Type: String
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
Type: SwitchParameter
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
Type: String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen

## VÄRDEN

### Microsoft. Azure. commands. ResourceManagement. Models. PSResourceGroupDeployment
Cmdleten returnerar distributioner av resurs grupper.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmResourceGroup](./Get-AzureRmResourceGroup.md)

[New-AzureRmResourceGroup](./New-AzureRmResourceGroup.md)

[New-AzureRmResourceGroupDeployment](./New-AzureRmResourceGroupDeployment.md)

[Remove-AzureRmResourceGroupDeployment](./Remove-AzureRmResourceGroupDeployment.md)

[Stopp-AzureRmResourceGroupDeployment](./Stop-AzureRmResourceGroupDeployment.md)

[Test-AzureRmResourceGroupDeployment](./Test-AzureRmResourceGroupDeployment.md)


