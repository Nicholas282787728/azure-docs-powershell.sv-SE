---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100251981"
---
# Get-AzTag

## SYNOPSIS
Hämtar fördefinierade Azure-taggar | Hämtar hela uppsättningen med taggar för en resurs eller en prenumeration.

## SYNTAX

### GetPredefinedTagParameterSet
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceIdParameterSet
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING

**GetPredefinedTagSet:** **Cmdleten Get-AzTag** hämtar fördefinierade Azure-taggar i din prenumeration.
Den här cmdleten returnerar grundläggande information om taggarna eller detaljerad information om taggar och deras värden.
Alla utdataobjekt innehåller egenskapen Antal som representerar antalet resurser och resursgrupper som taggarna och värdena har använts på.
Modulen Azure-taggar som **Get-AzTag är** en del av kan hjälpa dig att hantera fördefinierade Azure-taggar.
En Azure-tagg är ett namnvärdespar som du kan använda för att kategorisera Dina Azure-resurser och resursgrupper, till exempel efter avdelning eller kostnadsställe, eller för att spåra anteckningar eller kommentarer om resurser och grupper.
Du kan definiera och använda taggar i ett enda steg, men med fördefinierade taggar kan du ange standard, konsekventa, förutsägbara namn och värden för taggarna i din prenumeration.
Om du vill skapa en fördefinierad tagg använder New-AzTag-cmdleten.
Om du vill använda en fördefinierad tagg för en resursgrupp använder du *taggparametern* för New-AzTag cmdleten.
Om du vill söka i resursgrupper efter ett  specifikt taggnamn eller namn och värde använder du taggparametern för Get-AzResourceGroup cmdleten.

**GetByResourceIdParameterSet:** **Cmdleten Get-AzTag** med ett **ResourceId** får hela uppsättningen taggar för en resurs eller prenumeration.

## EXEMPEL

### Exempel 1: Hämta alla fördefinierade taggar
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

Med det här kommandot får du alla fördefinierade taggar i prenumerationen.
Egenskapen Antal visar hur många gånger taggen har använts på resurser och resursgrupper i prenumerationen.

### Exempel 2: Hämta en tagg efter namn
```powershell
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

Med det här kommandot får du detaljerad information om avdelningstaggen och dess värden.
Egenskapen Antal visar hur många gånger taggen och vart och ett av dess värden har tillämpats på resurser och resursgrupper i prenumerationen.

### Exempel 3: Hämta värden för alla taggar
```powershell
PS C:\>Get-AzTag -Detailed

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3


Name:   FY2015
Count:  2


Name:   CostCenter
Count:  20
Values: 

        Name        Count
        ==========  =====

        0001          5
        0002         10
        0003          5
```

Det här kommandot använder *parametern Detaljerad* för att få detaljerad information om alla fördefinierade taggar i prenumerationen.
Att använda *den detaljerade* parametern motsvarar att använda *parametern Namn* för varje tagg.

### Exempel 4: Hämta hela uppsättningen taggar för en prenumeration

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

Med det här kommandot får du hela uppsättningen taggar för prenumerationen med {subId}.

### Exempel 5: Hämta hela uppsättningen taggar för en resurs

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

Med det här kommandot får du hela uppsättningen taggar för resursen med {resourceId}.

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

### -Detaljerad
Anger att den här åtgärden lägger till information om taggvärden i resultatet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Namnet på den fördefinierade taggen.
Som standard hämtar **Get-AzTag** grundläggande information om alla fördefinierade taggar i prenumerationen.
När du anger *parametern Name* har *den detaljerade* parametern ingen effekt.

```yaml
Type: System.String
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Resursidentifieraren för den taggade enheten. En resurs, en resursgrupp eller en prenumeration kan vara taggad.

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

### System.Management.Automation.SwitchParameter

## UTDATA

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## ANTECKNINGAR

## RELATERADE LÄNKAR

[New-AzTag](./New-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)
