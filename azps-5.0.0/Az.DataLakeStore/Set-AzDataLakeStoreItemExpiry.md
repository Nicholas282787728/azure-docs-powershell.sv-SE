---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
ms.openlocfilehash: ff769801c7a3496ab094e5c9877e0b53fb64fbfd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320496"
---
# Set-AzDataLakeStoreItemExpiry

## Sammanfattning
Anger eller tar bort förfallo tiden för en fil i ett Azure Data Lake Store-konto.

## FRÅGESYNTAXEN

### SetAbsoluteNeverExpireExpiry (standard)
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetRelativeExpiry
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-RelativeFileExpiryOption] <PathRelativeExpiryOptions> [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzDataLakeStoreItemExpiry** anger eller tar bort förfallo tiden för en fil i ett Azure Data Lake Store-konto.

## BESKRIVS

### Exempel 1: Ange förfallo tid för en fil
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

Ställer in utgångs datum på filen myfile.txt i konto ContosoADL till två timmar från nu.
Detta gör att filen upphör att gälla (markeras för borttagning) om två timmar.

### Exempel 2: ta bort utgångs datum för en fil
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

Tar bort eventuell utgångs datum som tidigare ställts in på filen myfile.txt i kontot ' ContosoADL '.
Det innebär att filen inte automatiskt upphör att gälla (markeras för borttagning) och måste tas bort manuellt eller ställas in på nytt.

### Exempel 3: Ange förfallo tid för en fil relativt nu
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

Det första kommandot ställer in förfallo tiden för filen per myfile.txt 240 sekunder i förhållande till aktuell tid på servern.
Det andra kommandot ställer in förfallo tiden för filen per myfile.txt 240 sekunder i förhållande till skapande tid på Server.

## MALLPARAMETRAR

### -Konto
Anger namnet på data Lake Store-butiken.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Utgång
Den absoluta förfallo tiden för den angivna filen.
Om det inte finns något värde eller angett till MaxValue upphör filen aldrig att gälla.

```yaml
Type: System.DateTimeOffset
Parameter Sets: SetAbsoluteNeverExpireExpiry
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Anger data Lake Store-sökvägen för det fil objekt för vilket du vill ange eller ta bort förfallo datum.

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RelativeFileExpiryOption
Relativa utgångs alternativ. RelativeToNow eller RelativeToCreationDate är aktuella alternativ

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions
Parameter Sets: SetRelativeExpiry
Aliases:
Accepted values: RelativeToNow, RelativeToCreationDate

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RelativeTime
Den relativa tiden i millisekunder för nu eller skapande tid

```yaml
Type: System.Int64
Parameter Sets: SetRelativeExpiry
Aliases:

Required: False
Position: 3
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

### Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance

### System. DateTimeOffset

### Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreEnums + PathRelativeExpiryOptions

### System. Int64

## VÄRDEN

### Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreItem

## ANMÄRKNINGAR
Alias: Set-AdlStoreItemExpiry

## RELATERADE LÄNKAR

[Get-AzDataLakeStoreItem](./Get-AzDataLakeStoreItem.md)

