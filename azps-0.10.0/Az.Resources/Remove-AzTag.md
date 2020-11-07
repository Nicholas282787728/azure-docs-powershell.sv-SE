---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 5b7e58545b2c463c08a961758ecdb3cbce7b222c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923798"
---
# Remove-AzTag

## Sammanfattning
Tar bort fördefinierade Azure-taggar eller-värden.

## FRÅGESYNTAXEN

```
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzTag** tar bort fördefinierade Azure-Taggar och värden från din prenumeration.
Om du vill ta bort vissa värden från en fördefinierad tagg använder du *värde* -parametern.
Som standard tar **Remove-AzTag** bort den angivna taggen och alla dess värden. Du kan inte ta bort en tagg eller ett värde som för närvarande används för en resurs-eller resurs grupp.
Innan du använder **Remove-AzTag** kan du använda parametern *tag* i Set-AzResourceGroup cmdlet för att ta bort märket eller värdena från resursen eller resurs gruppen.
Modulerna för Azure-taggar som **tar bort-AzTag** är en del av kan hjälpa dig att hantera dina fördefinierade Azure-taggar.
En Azure-tagg är ett namn värde par som du kan använda för att kategorisera dina Azure-resurser och resurs grupper, till exempel efter avdelning eller kostnads ställe, eller för att spåra anteckningar eller kommentarer om resurserna och grupperna.
Du kan definiera och använda taggar i ett enda steg, men fördefinierade Taggar låter dig fastställa standard, konsekventa, förutsägbara namn och värden för taggarna i ditt abonnemang.

## BESKRIVS

### Exempel 1: ta bort en fördefinierad tagg
```
PS C:\>Remove-AzTag -Name "Department"
```

Det här kommandot tar bort den fördefinierade taggen avdelning och alla dess värden.
Om taggen har lagts till i resurser eller resurs grupper Miss lyckas kommandot.

### Exempel 2: ta bort ett värde från en fördefinierad tagg
```
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

Det här kommandot tar bort värdet HumanResources från det fördefinierade avdelnings märket.
Taggen tas inte bort.
Om värdet har kopplats till resurser eller resurs grupper Miss lyckas kommandot.

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

### -Namn
Anger namnet på den tagg som ska tas bort.
Som standard tar **Remove-AzTag** bort den angivna taggen och alla dess värden.
Använd parametern *Value* för att ta bort markerade värden, men inte ta bort taggen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Returnerar ett objekt som representerar den borttagna taggen eller den resulterande taggen med borttagen värde.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Värde
Tar bort angivna värden från den fördefinierade taggen, men tar inte bort taggen.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
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

### System. String

### System. string []

### System. Management. Automation. SwitchParameter

## VÄRDEN

### Microsoft. Azure. commands. ResourceManager. Common. taggar. PSTag

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzTag](./Get-AzTag.md)

[New-AzTag](./New-AzTag.md)

