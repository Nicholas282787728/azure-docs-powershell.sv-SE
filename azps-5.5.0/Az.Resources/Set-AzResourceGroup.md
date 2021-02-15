---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: 0523041357becb38475bb496c94ba1fd48c5acaf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217710"
---
# Set-AzResourceGroup

## SYNOPSIS
Ändrar en resursgrupp.

## SYNTAX

### SetByResourceGroupName (standard)
```
Set-AzResourceGroup -Name <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceGroupId
```
Set-AzResourceGroup [-Tag] <Hashtable> -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Set-AzResourceGroup** ändrar egenskaperna för en resursgrupp.
Du kan använda denna cmdlet för att lägga till, ändra eller ta bort Azure-taggar som används för en resursgrupp.
Ange *namnparametern* för att identifiera resursgruppen och *taggparametern* för att ändra taggarna.
Du kan inte använda den här cmdleten till att ändra namnet på en resursgrupp.

## EXEMPEL

### Exempel 1: Använda en tagg i en resursgrupp
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

Det här kommandot använder en Avdelning-tagg med värdet IT för en resursgrupp som inte har befintliga taggar.

### Exempel 2: Lägga till taggar i en resursgrupp
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

Det här exemplet lägger till en statustagg med värdet Godkänd och taggen RÅ2016 i en resursgrupp som har befintliga taggar. Eftersom de taggar du anger ersätter de befintliga taggarna måste du ta med de befintliga taggarna i den nya taggsamlingen, annars förlorar du dem.
Det första kommandot får resursgruppen ContosoRG och använder punktmetoden för att få värdet för egenskapen Taggar. Kommandot lagrar taggarna i den $Tags variabeln.
Det andra kommandot hämtar taggarna i den $Tags variabeln.
Det tredje kommandot använder operatorn += för att lägga till taggarna Status och RÅ2016 i matrisen med taggar i $Tags variabeln.
Det fjärde kommandot använder *taggparametern* **Set-AzResourceGroup** för att använda taggarna i variabeln $Tags för resursgruppen ContosoRG.
Det femte kommandot får alla taggar som tillämpas på ContosoRG-resursgruppen. Resultatet visar att resursgruppen har avdelningstaggen och de två nya taggarna, Status och År2015.

### Exempel 3: Ta bort alla taggar för en resursgrupp
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

Det här kommandot anger *taggparametern* med ett tomt hash-tabellvärde för att ta bort alla taggar från resursgruppen ContosoRG.

## PARAMETERS

### -ApiVersion
Anger den API-version som stöds av resursleverantören.
Du kan ange en annan version än standardversionen.

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
Anger ID för den resursgrupp som ska ändras.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Anger namnet på den resursgrupp som ska ändras.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: Named
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

### -Tag
Nyckelvärdepar i form av en hash-tabell. Exempel: @{key0="value0";key1=$null;key2="value2"} En tagg är ett namnvärdespar som du kan skapa och använda för resurser och resursgrupper. När du har tilldelar taggar till  resurser och grupper kan du använda taggparametern för Get-AzResource och Get-AzResourceGroup för att söka efter resurser och grupper efter taggnamn eller namn och värde. Du kan använda taggar för att kategorisera dina resurser, till exempel efter avdelning eller kostnadsställe, eller för att spåra anteckningar eller kommentarer om resurserna.
Om du vill lägga till eller ändra en tagg måste du ersätta samlingen med taggar för resursgruppen. Om du vill ta bort en tagg anger du en hash-tabell med alla taggar som för närvarande används i resursgruppen, från **Get-AzResourceGroup,** förutom taggen du vill ta bort. Om du vill ta bort alla taggar från en resursgrupp anger du en tom hash-tabell: `@{}` .

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

### System.Collections.Hashtable

## UTDATA

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzResource](./Get-AzResource.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)
