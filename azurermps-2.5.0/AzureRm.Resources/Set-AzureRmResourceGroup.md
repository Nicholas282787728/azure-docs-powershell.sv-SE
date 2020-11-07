---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresourcegroup
schema: 2.0.0
ms.openlocfilehash: 8070fd0dfc14396841865f726ef5a8d3a7630afa
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928670"
---
# Set-AzureRmResourceGroup

## Sammanfattning
Ändrar en resurs grupp.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### SetByResourceGroupName (standard)
```
Set-AzureRmResourceGroup [-Name] <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceGroupId
```
Set-AzureRmResourceGroup [-Tag] <Hashtable> [-Id] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureRmResourceGroup** ändrar egenskaperna för en resurs grupp.
Du kan använda denna cmdlet för att lägga till, ändra eller ta bort de Azure-taggar som tillämpas på en resurs grupp.
Ange parametern *Name* för att identifiera resurs gruppen och *märkningen* för att ändra taggarna.
Du kan inte använda denna cmdlet för att ändra namnet på en resurs grupp.

## BESKRIVS

### Exempel 1: använda en tagg för en resurs grupp
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

Det här kommandot lägger till en avdelning med ett värde i en resurs grupp som inte har befintliga taggar.

### Exempel 2: lägga till taggar i en resurs grupp
```
PS C:\>$Tags = (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzureRmResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

I det här exemplet läggs en status tagg till med ett godkänt och en FY2016-tagg till en resurs grupp med befintliga taggar. Eftersom de taggar du anger ersätter de befintliga taggarna måste du ta med de befintliga taggarna i den nya tag-samlingen eller förlora dem.
Det första kommandot får resurs gruppen ContosoRG och använder metoden dot för att hämta värdet på egenskapen Tags. Kommandot lagrar taggarna i variabeln $Tags.
Det andra kommandot får taggarna i variabeln $Tags.
I det tredje kommandot används operatorn + = tilldelning för att lägga till status-och FY2016-Taggar i matrisen med taggar i variabeln $Tags.
Det fjärde kommandot använder parametern *tagg* för **set-AzureRmResourceGroup** för att använda taggarna i $Tags-variabeln i resurs gruppen ContosoRG.
Det femte kommandot får alla märkningar som används i ContosoRG. Resultatet visar att resurs gruppen har avdelnings märket och de två nya taggarna, status och FY2015.

### Exempel 3: ta bort alla flaggor för en resurs grupp
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{}
```

Det här kommandot anger *märknings* parametern med ett tomt värde för hash-tabell för att ta bort alla Taggar från ContosoRG resurs grupp.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Anger ID: t för den resurs grupp som ska ändras.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger namnet på den resurs grupp som ska ändras.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
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

### -Tagg
Par med nyckelord i form av en hash-tabell. Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"} en tagg är ett namn värde par som du kan skapa och tillämpa på resurser och resurs grupper. När du har tilldelat taggar till resurser och grupper kan du använda parametern *tagg* för Get-AzureRmResource och Get-AzureRmResourceGroup för att söka efter resurser och grupper efter taggnamn eller namn och värde. Du kan använda taggar för att kategorisera dina resurser, till exempel efter avdelning eller kostnads ställe, eller för att spåra anteckningar eller kommentarer om resurserna.
Om du vill lägga till eller ändra en tagg måste du ersätta samlingen med taggar för resurs gruppen. Om du vill ta bort en tagg anger du en hash-tabell med alla Taggar som för närvarande används i resurs gruppen, från **AzureRmResourceGroup** , förutom den tagg du vill ta bort. Om du vill ta bort alla flaggor från en resurs grupp anger du en tom hash-tabell: `@{}` .

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen

## VÄRDEN

### Microsoft. Azure. commands. Resources. Models. PSResourceGroup

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmResource](./Get-AzureRmResource.md)

[Get-AzureRmResourceGroup](./Get-AzureRmResourceGroup.md)

[New-AzureRmResourceGroup](./New-AzureRmResourceGroup.md)

[Remove-AzureRmResourceGroup](./Remove-AzureRmResourceGroup.md)
