---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: 9c4bdfe189c16f3e2f6f90d3197149bdc57c78c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226798"
---
# New-AzResourceGroup

## SYNOPSIS
Skapar en Azure-resursgrupp.

## SYNTAX

```
New-AzResourceGroup [-Name] <String> [-Location] <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **New-AzResourceGroup** skapar en Azure-resursgrupp.
Du kan skapa en resursgrupp med bara ett namn och en plats och sedan använda cmdleten New-AzResource för att skapa resurser som ska läggas till i resursgruppen.
Om du vill lägga till en distribution i en befintlig resursgrupp använder du New-AzResourceGroupDeployment-cmdleten. Om du vill lägga till en resurs i en befintlig resursgrupp använder du cmdleten **New-AzResource.** En Azure-resurs är en användar hanterad Azure-enhet, till exempel en databasserver, databas eller webbplats. En Azure-resursgrupp är en samling Azure-resurser som distribueras som en enhet.

## EXEMPEL

### Exempel 1: Skapa en tom resursgrupp
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

Med det här kommandot skapas en resursgrupp som inte har några resurser. Du kan lägga till resurser och distributioner i resursgruppen med cmdletarna **New-AzResource** eller **New-AzResourceGroupDeployment.**

### Exempel 2: Skapa en tom resursgrupp med hjälp av positionella parametrar
```
PS> New-AzResourceGroup RG01 "South Central US"
```

Med det här kommandot skapas en resursgrupp som inte har några resurser.

### Exempel 3: Skapa en resursgrupp med taggar
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

Med det här kommandot skapas en tom resursgrupp. Det här kommandot är detsamma som kommandot i exempel 1, förutom att det tilldelar taggar till resursgruppen. Den första taggen, som heter Tom, kan användas för att identifiera resursgrupper som inte har några resurser. Den andra taggen heter Avdelning och har värdet Marknadsföring. Du kan använda en tagg som den här om du vill kategorisera resursgrupper för administration eller budgetering.

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

### -Force
Tvingar kommandot att köras utan att användaren uppmanas att bekräfta.

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

### -Plats
Anger resursgruppens plats. Ange en Azure-datacenterplats, till exempel Västra USA eller Sydostasien. Du kan placera en resursgrupp på valfri plats. Resursgruppen måste inte finnas på samma plats som Din Azure-prenumeration eller på samma plats som dess resurser.
Använd cmdleten Get-AzResourceProvider *ProviderNamespace-parametern* för att avgöra vilken plats som stöder varje resurstyp.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Anger ett namn för resursgruppen. Resursnamnet måste vara unikt i prenumerationen. Om det redan finns en resursgrupp med det namnet uppmanas du att bekräfta kommandot innan du ersätter den befintliga resursgruppen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
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
Nyckelvärdepar i form av en hash-tabell. Exempel: @{key0="value0";key1=$null;key2="value2"} Om du vill lägga till eller ändra en tagg måste du ersätta samlingen med taggar för resursgruppen.
När du har tilldelar taggar till  resurser och grupper kan du använda taggparametern för Get-AzResource och Get-AzResourceGroup för att söka efter resurser och grupper efter taggnamn eller efter namn och värde. Du kan använda taggar för att kategorisera dina resurser, till exempel efter avdelning eller kostnadsställe, eller för att spåra anteckningar eller kommentarer om resurserna.
Använd cmdleten Get-AzTag för att få dina fördefinierade taggar.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Frågar dig om bekräftelse innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som skulle hända om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
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

[Get-AzResourceProvider](./Get-AzResourceProvider.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResource](./New-AzResource.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)

[Set-AzResourceGroup](./Set-AzResourceGroup.md)
