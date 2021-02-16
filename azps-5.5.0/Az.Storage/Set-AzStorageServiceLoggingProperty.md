---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 21c182dff12f8dd373000a295f964bd59484e337
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100252840"
---
# Set-AzStorageServiceLoggingProperty

## SYNOPSIS
Ändrar loggning för Azure Storage-tjänster.

## SYNTAX

```
Set-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Set-AzStorageServiceLoggingProperty** ändrar loggning för Azure-lagringstjänster.

## EXEMPEL

### Exempel 1: Ändra loggningsegenskaper för Blob-tjänsten
```
C:\PS>Set-AzStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

Det här kommandot ändrar version 1.0-loggning för blob-lagring för att inkludera läs- och skrivåtgärder.
Azure Storage-tjänstloggning behåller poster i 10 dagar.
Eftersom det här kommandot anger *parametern PassThru* visas de ändrade loggningsegenskaperna.

## PARAMETERS

### -Sammanhang
Anger ett Azure-lagringssammanhang.
Om du vill skapa ett lagringssammanhang använder New-AzStorageContext-cmdleten.

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

### -LoggingOperations
Anger en matris med Azure Storage-tjänståtgärder.
Azure Storage Services loggar åtgärderna som den här parametern anger.
De godtagbara värdena för den här parametern är:
- Ingen
- Läsa
- Skriva
- Ta bort
- Alla

```yaml
Type: Microsoft.Azure.Storage.Shared.Protocol.LoggingOperations[]
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Anger att denna cmdlet returnerar de uppdaterade loggningsegenskaperna.
Om du inte anger den här parametern returnerar cmdleten inte ett värde.

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

### -RetentionDays
Anger antalet dagar som Azure Storage-tjänsten bevarar loggad information.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceType
Anger lagringstjänsttypen.
Den här cmdleten ändrar loggningsegenskaperna för den tjänsttyp som den här parametern anger.
De godtagbara värdena för den här parametern är:
- Blob 
- Tabell
- Kö
- Filvärdet för Filen stöds inte för närvarande.

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
Anger versionen av Azure Storage-tjänstloggning.
Standardvärdet är 1,0.

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.iStorageContext

## UTDATA

### Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzStorageServiceLoggingProperty](./Get-AzStorageServiceLoggingProperty.md)

[New-AzStorageContext](./New-AzStorageContext.md)


