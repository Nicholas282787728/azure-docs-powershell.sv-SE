---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: ee880422e01b68bb595c709c1642038f75003c49
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747095"
---
# New-AzTag

## Sammanfattning
Skapar en fördefinierad Azure-tagg eller lägger till värden i en befintlig tagg.

## FRÅGESYNTAXEN

```
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzTag** skapar en fördefinierad Azure-tagg med ett valfritt fördefinierat värde.
Du kan också använda det för att lägga till fler värden i befintliga fördefinierade taggar.
Om du vill skapa en fördefinierad tagg anger du ett unikt taggnamn.
Om du vill lägga till ett värde i en befintlig fördefinierad tagg anger du namnet på den befintliga taggen och det nya värdet.
Denna cmdlet returnerar ett objekt som representerar den nya eller ändrade taggen med dess värden och antalet resurser som den har använts på.
Modulerna för Azure-taggar som **New-AzTag** är en del av kan hjälpa dig att hantera fördefinierade Azure-taggar.
En Azure-tagg är ett namn värde par som du kan använda för att kategorisera dina Azure-resurser och resurs grupper, till exempel efter avdelning eller kostnads ställe, eller för att spåra anteckningar eller kommentarer om resurserna och grupperna.
Du kan definiera och använda taggar i ett enda steg, men fördefinierade Taggar låter dig fastställa standard, konsekventa, förutsägbara namn och värden för taggarna i ditt abonnemang.
Om du vill använda en fördefinierad tagg för en resurs-eller resurs grupp använder du parametern *tagg* för New-AzTag cmdlet.
Om du vill söka efter resurs grupper med ett angivet taggnamn eller namn och värde använder du parametern *tagg* för Get-AzResourceGroup cmdlet.
Varje tagg har ett namn.
Värdena är valfria.
En fördefinierad Azure-tagg kan ha flera värden, men när du använder taggen i en resurs eller resurs grupp kan du använda taggnamnet och bara ett av dess värden.
Du kan till exempel skapa ett fördefinierat avdelnings märke med ett värde för varje avdelning, till exempel ekonomi, mänskliga resurser och det.
När du använder taggen avdelning för en resurs, kan du bara använda ett fördefinierat värde, till exempel ekonomi.

## BESKRIVS

### Exempel 1: skapa en fördefinierad tagg
```
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

Det här kommandot skapar en fördefinierad tagg med namnet FY2015.
Den här taggen har inga värden.
Du kan använda en tagg utan värden för en resurs eller resurs grupp eller använda **ny-AzTag** för att lägga till värden i taggen.
Du kan också ange ett värde när du använder taggen i resursen eller resurs gruppen.

### Exempel 2: skapa en fördefinierad tagg med ett värde
```
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

Det här kommandot skapar en fördefinierad tagg med namnet avdelning med ett finansierings värde.

### Exempel 3: lägga till ett värde i en fördefinierad tagg
```
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

De här kommandona skapar en fördefinierad tagg med namnet avdelning med två värden.
Om taggnamnet finns lägger **AzTag** till värdet till den befintliga taggen i stället för att skapa ett nytt.

### Exempel 4: använda en fördefinierad tagg
```
PS C:\>New-AzTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
Name:      EngineerBlog
Location:  East US
Resources: 
            
  Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US
    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001 
PS C:\>Get-AzTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzResourceGroup -Tag @{Name="CostCenter"}
Name:      EngineerBlog
Location:  East US
Resources: 
     Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US

    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001
```

Kommandona i det här exemplet skapar och använder en fördefinierad tagg.

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
Anger taggnamnet.
Om du vill skapa en ny fördefinierad tagg anger du ett unikt namn.
Om du vill lägga till ett värde i en befintlig tagg anger du namnet på den befintliga taggen.
Om en befintlig fördefinierad tagg har det angivna namnet lägger **AzTag** till det angivna värdet, om det finns något, till taggen med det namnet i stället för att skapa en ny tagg.

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

### -Värde
Anger ett taggvärde.
Fördefinierade taggar kan ha flera värden, men det går bara att ange ett värde i varje kommando.
Den här parametern är valfri eftersom taggar kan ha namn utan värden.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. commands. ResourceManager. Common. taggar. PSTag

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzTag](./Get-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)


