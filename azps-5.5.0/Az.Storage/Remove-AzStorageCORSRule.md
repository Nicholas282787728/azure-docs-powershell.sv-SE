---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
ms.openlocfilehash: aeae25ab3a8ff0b1fa3eb91db90497b44555631f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231590"
---
# Remove-AzStorageCORSRule

## SYNOPSIS
Tar bort CORS för en lagringstjänst.

## SYNTAX

```
Remove-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Remove-AzStorageCORSRule** tar bort resursdelning mellan ursprung (CORS) för en Azure-lagringstjänst.
Med den här cmdleten tas alla CORS-regler bort i en lagringstjänsttyp.
Typerna av lagringstjänster för den här cmdleten är Blob, Table, Queue och File.

## EXEMPEL

### Exempel 1: Ta bort CORS-regler för blob-tjänsten
```
PS C:\>Remove-AzStorageCORSRule -ServiceType Blob
```

Med det här kommandot tas KORS-regler bort för blob-tjänsttypen.

## PARAMETERS

### -ClientTimeoutPerRequest
Anger klienttidens time out-intervall i sekunder för en tjänstbegäran.
Om föregående samtal misslyckas i det angivna intervallet försöker den här cmdleten att göra om begäran.
Om denna cmdlet inte får ett lyckat svar innan intervallet gått returnerar denna cmdlet ett fel.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Anger maximalt antal samtidiga nätverkssamtal.
Du kan använda den här parametern för att begränsa samtidigheten för att begränsa den lokala CPU-belastningen och bandbreddsanvändningen genom att ange maximalt antal samtidiga nätverkssamtal.
Det angivna värdet är ett absolut antal och multipliceras inte med basantalet.
Den här parametern kan minska problem med nätverksanslutningen i miljöer med låg bandbredd, till exempel 100 kilobit per sekund.
Standardvärdet är 10.

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

### -Sammanhang
Anger Azure-lagringskontexten.
För att hämta lagringskontexten kan New-AzStorageContext cmdlet.

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

### -ServerTimeoutPerRequest
Anger längden på time out-perioden för serverdelen av en begäran.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceType
Anger den Azure Storage-tjänsttyp som cmdleten tar bort regler för.
De godtagbara värdena för den här parametern är:
- Blob 
- Tabell 
- Kö 
- Fil

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

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.iStorageContext

## UTDATA

### System.Void

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzStorageCORSRule](./Get-AzStorageCORSRule.md)

[Set-AzStorageCORSRule](./Set-AzStorageCORSRule.md)


