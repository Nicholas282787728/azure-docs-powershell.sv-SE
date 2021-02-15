---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 937ac50ac34f8b04912a0d500dedb5b490806b1a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217719"
---
# New-AzTag

## SYNOPSIS
Skapar en fördefinierad Azure-tagg eller lägger till värden i en befintlig tagg | Skapar eller uppdaterar hela uppsättningen med taggar för en resurs eller prenumeration.

## SYNTAX

### CreatePredefinedTagParameterSet

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CreateByResourceIdParameterSet

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## BESKRIVNING

**CreatePredefinedTagSet:** **Cmdleten New-AzTag** skapar en fördefinierad Azure-tagg med ett fördefinierat värde (valfritt).
Du kan också använda det för att lägga till ytterligare värden i befintliga fördefinierade taggar.
Om du vill skapa en fördefinierad tagg anger du ett unikt taggnamn.
Om du vill lägga till ett värde i en befintlig fördefinierad tagg anger du namnet på den befintliga taggen och det nya värdet.
Den här cmdleten returnerar ett objekt som representerar den nya eller ändrade taggen med dess värden och antalet resurser som den har använts på.
Azure-taggmodulen **som New-AzTag ingår** i kan hjälpa dig att hantera fördefinierade Azure-taggar.
En Azure-tagg är ett namnvärdespar som du kan använda för att kategorisera Dina Azure-resurser och resursgrupper, till exempel efter avdelning eller kostnadsställe, eller för att spåra anteckningar eller kommentarer om resurser och grupper.
Du kan definiera och använda taggar i ett enda steg, men med fördefinierade taggar kan du ange standard, konsekventa, förutsägbara namn och värden för taggarna i din prenumeration.
Om du vill använda en fördefinierad tagg för en resurs eller resursgrupp använder du *taggparametern* för New-AzTag-cmdleten.
Använd taggparametern för cmdleten Get-AzResourceGroup om  du vill söka efter resursgrupper med ett angivet taggnamn eller namn och värde.
Varje tagg har ett namn.
Värdena är valfria.
En fördefinierad Azure-tagg kan ha flera värden, men när du använder taggen för en resurs eller resursgrupp använder du taggnamnet och bara ett av dess värden.
Du kan till exempel skapa en fördefinierad avdelningstagg med ett värde för varje avdelning, till exempel ekonomi, personalavdelning och IT.
När du använder taggen Avdelning för en resurs använder du bara ett fördefinierat värde, till exempel Ekonomi.

**CreateByResourceIdParameterSet:** Cmdleten **New-AzTag** med ett **ResourceId** skapar eller uppdaterar hela uppsättningen med taggar för en resurs eller prenumeration.
Med den här åtgärden kan du lägga till eller ersätta hela uppsättningen taggar för den angivna resursen eller prenumerationen. Den angivna enheten kan ha högst 50 taggar.

## EXEMPEL

### Exempel 1: Skapa en fördefinierad tagg
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

Det här kommandot skapar en fördefinierad tagg med namnet RÅ2015.
Den här taggen har inga värden.
Du kan använda en tagg utan värden för en resurs eller resursgrupp eller använda **AzTag för** att lägga till värden i taggen.
Du kan också ange ett värde när du använder taggen för resursen eller resursgruppen.

### Exempel 2: Skapa en fördefinierad tagg med ett värde
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

Med det här kommandot skapas en fördefinierad tagg med namnet Avdelning med värdet Ekonomi.

### Exempel 3: Lägga till ett värde i en fördefinierad tagg
```powershell
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

Med de här kommandona skapas en fördefinierad tagg med namnet Avdelning med två värden.
Om taggnamnet finns läggs **värdet till i** den befintliga taggen i stället för att en ny skapas.

### Exempel 4: Använda en fördefinierad tagg
```powershell
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

Med kommandona i det här exemplet kan du skapa och använda en fördefinierad tagg.

### Exempel 5: Skapar eller uppdaterar hela uppsättningen taggar för en prenumeration

```powershell
PS C:\>$Tags = @{"tagKey1"="tagValue1"; "tagKey2"="tagValue2"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId} -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

Med det här kommandot skapas eller uppdateras hela uppsättningen taggar för prenumerationen med {subId}.

### Exempel 6: Skapar eller uppdaterar hela uppsättningen taggar för en resurs

```powershell
PS C:\>$Tags = @{"Dept"="Finance"; "Status"="Normal"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

Med det här kommandot skapas eller uppdateras hela uppsättningen med taggar för resursen med {resourceId}.

## PARAMETERS

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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

### -Name
Anger det fördefinierade taggnamnet.
Om du vill skapa en ny fördefinierad tagg anger du ett unikt namn.
Om du vill lägga till ett värde för en befintlig tagg anger du namnet på den befintliga taggen.
Om en befintlig fördefinierad  tagg har det angivna namnet läggs det angivna värdet , om det finns någon, till taggen med det namnet i stället för att en ny tagg skapas.

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Värde
Anger ett fördefinierat taggvärde.
Fördefinierade taggar kan ha flera värden, men du kan bara ange ett värde i varje kommando.
Den här parametern är valfri eftersom taggar kan ha namn utan värden.

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Resursidentifieraren för den enhet som taggas. En resurs, en resursgrupp eller en prenumeration kan vara taggad.

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
De taggar som ska sättas på resursen.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 1
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

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzTag](./Get-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)