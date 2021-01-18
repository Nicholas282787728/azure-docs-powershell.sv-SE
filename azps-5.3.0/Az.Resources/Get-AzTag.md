---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521479"
---
# Get-AzTag

## Sammanfattning
Hämtar fördefinierade Azure-Taggar | Hämtar alla flaggor för en resurs eller ett abonnemang.

## FRÅGESYNTAXEN

### GetPredefinedTagParameterSet
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceIdParameterSet
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING

**GetPredefinedTagSet**: **Get-AzTag** -cmdleten får fördefinierade Azure-Taggar i ditt abonnemang.
Denna cmdlet returnerar grundläggande information om taggarna eller detaljerad information om taggarna och deras värden.
Alla utdatafiler innehåller en Count-egenskap som representerar antalet resurser och resurs grupper som taggarna och värdena har använts för.
Modulerna för Azure-taggar som **Get-AzTag** är en del av kan hjälpa dig att hantera fördefinierade Azure-taggar.
En Azure-tagg är ett namn värde par som du kan använda för att kategorisera dina Azure-resurser och resurs grupper, till exempel efter avdelning eller kostnads ställe, eller för att spåra anteckningar eller kommentarer om resurserna och grupperna.
Du kan definiera och använda taggar i ett enda steg, men fördefinierade Taggar låter dig fastställa standard, konsekventa, förutsägbara namn och värden för taggarna i ditt abonnemang.
Använd New-AzTag cmdlet för att skapa en fördefinierad tagg.
Om du vill använda en fördefinierad tagg för en resurs grupp använder du parametern *tagg* för New-AzTag cmdlet.
Om du vill söka efter resurs grupper för ett visst taggnamn eller namn och värde kan du använda parametern *tag* i Get-AzResourceGroup cmdlet.

**GetByResourceIdParameterSet**: cmdleten **Get-AzTag** med en **ResourceID** får hela uppsättningen taggar för en resurs eller ett abonnemang.

## BESKRIVS

### Exempel 1: Hämta alla fördefinierade Taggar
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

Det här kommandot får alla fördefinierade Taggar i prenumerationen.
Egenskapen Count visar hur många gånger märket har använts för resurser och resurs grupper i prenumerationen.

### Exempel 2: Hämta ett märkord efter namn
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

Det här kommandot får detaljerad information om avdelnings märket och dess värden.
Egenskapen Count visar hur många gånger taggen och alla dess värden har kopplats till resurser och resurs grupper i prenumerationen.

### Exempel 3: få värden för alla Taggar
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

Det här kommandot använder den *detaljerade* parametern för att få detaljerad information om alla fördefinierade Taggar i prenumerationen.
Om du använder en *detaljerad* parameter används parametern *Name* för varje tagg.

### Exempel 4: Hämta hela uppsättningen taggar för ett abonnemang

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

Det här kommandot får hela uppsättningen Taggar i prenumerationen med {subId}.

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

Det här kommandot får hela uppsättningen taggar på resursen med {resourceId}.

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

### -Detaljerad
Anger att den här åtgärden lägger till information om tagg värden i resultatet.

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

### -Namn
Namn på den fördefinierade taggen.
Som standard får **Get-AzTag** grundläggande information om alla fördefinierade Taggar i prenumerationen.
När du anger parametern *Name* har den *detaljerade* parametern ingen effekt.

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
Resurs-ID för den märkta enheten. En resurs, en resurs grupp eller ett abonnemang kan märkas.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### System. String

### System. Management. Automation. SwitchParameter

## VÄRDEN

### Microsoft. Azure. commands. ResourceManager. Common. taggar. PSTag | Microsoft. Azure. commands. taggar. Model. PSTagResource

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzTag](./New-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)
