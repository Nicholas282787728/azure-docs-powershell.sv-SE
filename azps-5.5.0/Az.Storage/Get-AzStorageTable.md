---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: d501faaebcc5e381dc2a7270c8b55b148e2812b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229862"
---
# Get-AzStorageTable

## SYNOPSIS
Visar lagringstabellerna.

## SYNTAX

### TableName (standard)
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### TablePrefix
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzStorageTable** visar de lagringstabeller som är kopplade till lagringskontot i Azure.

## EXEMPEL

### Exempel 1: Lista alla Azure Storage-tabeller
```
PS C:\>Get-AzStorageTable
```

Med det här kommandot får du alla lagringstabeller för ett lagringskonto.

### Exempel 2: Lista Azure Storage-tabeller med ett jokertecken
```
PS C:\>Get-AzStorageTable -Name table*
```

Det här kommandot använder ett jokertecken för att hämta lagringstabeller vars namn börjar med en tabell.

### Exempel 3: Lista Azure Storage-tabeller med hjälp av tabellnamnsprefix
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

Det här kommandot använder *prefixparametern* för att hämta lagringstabeller vars namn börjar med en tabell.

## PARAMETERS

### -Sammanhang
Anger lagringskontexten.
Om du vill skapa den kan du använda New-AzStorageContext-cmdleten.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Anger tabellnamnet.
Om tabellnamnet är tomt visas alla tabeller i cmdleten.
Annars visas alla tabeller som matchar det angivna namnet eller det vanliga namnmönstret.

```yaml
Type: System.String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefix
Anger ett prefix som används i namnet på den eller de tabeller du vill hämta.
Du kan använda den för att hitta alla tabeller som börjar med samma sträng, till exempel en tabell.

```yaml
Type: System.String
Parameter Sets: TablePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.iStorageContext

## UTDATA

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable

## ANTECKNINGAR

## RELATERADE LÄNKAR

[New-AzStorageTable](./New-AzStorageTable.md)

[Remove-AzStorageTable](./Remove-AzStorageTable.md)


