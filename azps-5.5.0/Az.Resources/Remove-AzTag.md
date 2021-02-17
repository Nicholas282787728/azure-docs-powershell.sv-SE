---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 22a43739ec63f8287ce51c4c4f4a125b4e5b1c65
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223287"
---
# Remove-AzTag

## SYNOPSIS
Tar bort fördefinierade Azure-taggar eller -värden | Tar bort hela uppsättningen med taggar för en resurs eller prenumeration.

## SYNTAX

### RemovePredefinedTagParameterSet

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveByResourceIdParameterSet

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## BESKRIVNING

**RemovePredefinedTagSet:** **Cmdleten Remove-AzTag** tar bort fördefinierade Azure-taggar och -värden från din prenumeration.
Om du vill ta bort vissa värden från en fördefinierad tagg använder du *Värdeparametern.*
Ta bort **AzTag tar bort** den angivna taggen och alla dess värden som standard. Du kan inte ta bort en tagg eller ett värde som för närvarande används för en resurs eller resursgrupp.
Innan du **använder Remove-AzTag** använder du taggparametern för cmdleten Set-AzResourceGroup ta bort taggen eller värdena från resursen eller resursgruppen. 
Modulen Azure-taggar som **Ta bort-AzTag** är en del av kan hjälpa dig att hantera dina fördefinierade Azure-taggar.
En Azure-tagg är ett namnvärdespar som du kan använda för att kategorisera Dina Azure-resurser och resursgrupper, till exempel efter avdelning eller kostnadsställe, eller för att spåra anteckningar eller kommentarer om resurser och grupper.
Du kan definiera och använda taggar i ett enda steg, men med fördefinierade taggar kan du ange standard, konsekventa, förutsägbara namn och värden för taggarna i din prenumeration.

**RemoveByResourceIdParameterSet:** **Cmdleten Remove-AzTag** med ett **ResourceId** tar bort hela uppsättningen med taggar för en resurs eller prenumeration.

## EXEMPEL

### Exempel 1: Ta bort en fördefinierad tagg
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

Det här kommandot tar bort den fördefinierade taggen Avdelning och alla dess värden.
Om taggen har använts på några resurser eller resursgrupper misslyckas kommandot.

### Exempel 2: Ta bort ett värde från en fördefinierad tagg
```powershell
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

Det här kommandot tar bort värdet för HumanResources från den fördefinierade Department-taggen.
Taggen tas inte bort.
Om värdet har tillämpats på några resurser eller resursgrupper misslyckas kommandot.

### Exempel 3: Tar bort hela uppsättningen taggar för en prenumeration

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

Det här kommandot tar bort hela uppsättningen taggar för prenumerationen med {subId}. Det returnerar inte det objekt som tagits bort om det inte passerar i "-PassThru".

### Exempel 4: Tar bort hela uppsättningen med taggar för en resurs

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -PassThru

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

Det här kommandot tar bort hela uppsättningen med taggar för resursen med {resourceId}. Den returnerar det borttagna egten vid passning i "-PassThru".

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
Anger namnet på den fördefinierade taggen som ska tas bort.
Ta bort **AzTag tar bort** den angivna taggen och alla dess värden som standard.
Om du vill ta bort markerade värden, men inte ta bort taggen, använder du *värdeparametern.*

```yaml
Type: System.String
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Värde
Tar bort angivna värden från den fördefinierade taggen, men taggen tas inte bort.

```yaml
Type: System.String[]
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Resursidentifieraren för den taggade enheten. En resurs, en resursgrupp eller en prenumeration kan vara taggad.

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Returnerar ett objekt som representerar den borttagna taggen eller den resulterande taggen med borttagna värden.

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

### System.String[]

### System.Management.Automation.SwitchParameter

## UTDATA

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzTag](./Get-AzTag.md)

[New-AzTag](./New-AzTag.md)

[Update-AzTag](./Update-AzTag.md)