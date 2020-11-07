---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: b0d9d23b9563c38a985adfa3d12dfc2854319512
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923913"
---
# New-AzResourceGroup

## Sammanfattning
Skapar en Azure-resurspost.

## FRÅGESYNTAXEN

```
New-AzResourceGroup -Name <String> -Location <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzResourceGroup** skapar en Azure resurs grupp.
Du kan skapa en resurs grupp med hjälp av ett namn och en plats och sedan använda New-AzResource cmdlet för att skapa resurser som ska läggas till i resurs gruppen.
Använd New-AzResourceGroupDeployment cmdlet för att lägga till en distribution i en befintlig resurs grupp. Använd cmdleten **New-AzResource** om du vill lägga till en resurs i en befintlig resurs grupp. En Azure-resurs är en användardefinierad Azure-enhet, till exempel en databas server, en databas eller en webbplats. En Azure-resurs grupp är en samling Azure-resurser som distribueras som en enhet.

## BESKRIVS

### Exempel 1: skapa en tom resurs grupp
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

Det här kommandot skapar en resurs grupp som inte har några resurser. Du kan använda cmdletarna **New-AzResource** eller **New-AzResourceGroupDeployment** för att lägga till resurser och distributioner i den här resurs gruppen.

### Exempel 2: skapa en tom resurs grupp med hjälp av positions parametrar
```
PS> New-AzResourceGroup RG01 "South Central US"
```

Det här kommandot skapar en resurs grupp som inte har några resurser.

### Exempel 3: skapa en resurs grupp med Taggar
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

Det här kommandot skapar en tom resurs grupp. Det här kommandot är samma som kommandot i exempel 1, förutom att det tilldelar taggar till resurs gruppen. Den första taggen, namngiven tom, kan användas för att identifiera resurs grupper som inte har några resurser. Den andra taggen heter Department och har ett värde för marknadsföring. Du kan använda en tagg som den här för att kategorisera resurs grupper för administration eller budgetering.

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
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Tvingar kommandot att köras utan att fråga efter bekräftelse.

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
Anger platsen för resurs gruppen. Ange en plats för Azure Data Center, till exempel West US eller Sydostasien. Du kan placera en resurs grupp på vilken plats som helst. Resurs gruppen behöver inte finnas på samma plats som din Azure-prenumeration eller på samma plats som dess resurser.
Om du vill ta reda på vilken plats som har stöd för varje resurs typ använder du Get-AzResourceProvider cmdlet med parametern *ProviderNamespace* .

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger ett namn för resurs gruppen. Resurs namnet måste vara unikt i prenumerationen. Om det redan finns en resurs grupp med det namnet måste du bekräfta att du vill ersätta den befintliga resurs gruppen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: Named
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
Par med nyckelord i form av en hash-tabell. Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"} om du vill lägga till eller ändra en tagg måste du ersätta samlingen med taggar för resurs gruppen.
När du har tilldelat taggar till resurser och grupper kan du använda parametern *tagg* för Get-AzResource och Get-AzResourceGroup för att söka efter resurser och grupper efter taggnamn eller namn och värde. Du kan använda taggar för att kategorisera dina resurser, till exempel efter avdelning eller kostnads ställe, eller för att spåra anteckningar eller kommentarer om resurserna.
Använd Get-AzTag cmdlet för att få dina fördefinierade taggar.

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
Du uppmanas att bekräfta innan du kör cmdleten.

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
Visar vad som händer om cmdleten körs.
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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen

## VÄRDEN

### Microsoft. Azure. commands. ResourceManagement. Models. PSResourceGroup

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzResourceProvider](./Get-AzResourceProvider.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResource](./New-AzResource.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)

[Set-AzResourceGroup](./Set-AzResourceGroup.md)
