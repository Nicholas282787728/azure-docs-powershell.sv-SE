---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/new-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
ms.openlocfilehash: cd9700a633f1a9c09c5fafd060d318b35eaeaabb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584824"
---
# New-AzureRmTag

## Sammanfattning
Skapar en fördefinierad Azure-tagg eller lägger till värden i en befintlig tagg.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
New-AzureRmTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmTag** skapar en fördefinierad Azure-tagg med ett valfritt fördefinierat värde.
Du kan också använda det för att lägga till fler värden i befintliga fördefinierade taggar.
Om du vill skapa en fördefinierad tagg anger du ett unikt taggnamn.
Om du vill lägga till ett värde i en befintlig fördefinierad tagg anger du namnet på den befintliga taggen och det nya värdet.
Denna cmdlet returnerar ett objekt som representerar den nya eller ändrade taggen med dess värden och antalet resurser som den har använts på.
Modulerna för Azure-taggar som **New-AzureRmTag** är en del av kan hjälpa dig att hantera fördefinierade Azure-taggar.
En Azure-tagg är ett namn värde par som du kan använda för att kategorisera dina Azure-resurser och resurs grupper, till exempel efter avdelning eller kostnads ställe, eller för att spåra anteckningar eller kommentarer om resurserna och grupperna.
Du kan definiera och använda taggar i ett enda steg, men fördefinierade Taggar låter dig fastställa standard, konsekventa, förutsägbara namn och värden för taggarna i ditt abonnemang.
Om du vill använda en fördefinierad tagg för en resurs-eller resurs grupp använder du parametern *tagg* för New-AzureRmTag cmdlet.
Om du vill söka efter resurs grupper med ett angivet taggnamn eller namn och värde använder du parametern *tagg* för Get-AzureRMResourceGroup cmdlet.
Varje tagg har ett namn.
Värdena är valfria.
En fördefinierad Azure-tagg kan ha flera värden, men när du använder taggen i en resurs eller resurs grupp kan du använda taggnamnet och bara ett av dess värden.
Du kan till exempel skapa ett fördefinierat avdelnings märke med ett värde för varje avdelning, till exempel ekonomi, mänskliga resurser och det.
När du använder taggen avdelning för en resurs, kan du bara använda ett fördefinierat värde, till exempel ekonomi.

## BESKRIVS

### Exempel 1: skapa en fördefinierad tagg
```
PS C:\>New-AzureRmTag -Name "FY2015"
Name:   FY2015
Count:  0
Values: 

        Name        Count
        =========   =====

        Finance     0
```

Det här kommandot skapar en fördefinierad tagg med namnet FY2015.
Den här taggen har inga värden.
Du kan använda en tagg utan värden för en resurs eller resurs grupp eller använda **ny-AzureRmTag** för att lägga till värden i taggen.
Du kan också ange ett värde när du använder taggen i resursen eller resurs gruppen.

### Exempel 2: skapa en fördefinierad tagg med ett värde
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
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
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzureRmTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

De här kommandona skapar en fördefinierad tagg med namnet avdelning med två värden.
Om taggnamnet finns lägger **AzureRmTag** till värdet till den befintliga taggen i stället för att skapa ett nytt.

### Exempel 4: använda en fördefinierad tagg
```
PS C:\>New-AzureRmTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzureRmResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
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
PS C:\>Get-AzureRmTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzureRmResourceGroup -Tag @{Name="CostCenter"}
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Om en befintlig fördefinierad tagg har det angivna namnet lägger **AzureRmTag** till det angivna värdet, om det finns något, till taggen med det namnet i stället för att skapa en ny tagg.

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

[Get-AzureRmTag](./Get-AzureRmTag.md)

[Remove-AzureRmTag](./Remove-AzureRmTag.md)


