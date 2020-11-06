---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: febcec4d309e849e3b259fc2d80b3129ca7b65f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582487"
---
# Export-AzureRmDataLakeStoreItem

## Sammanfattning
Laddar ned en fil från data Lake Store.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### Ingen diagnostikloggning (standard)
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Inkludera diagnostikloggning
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **export-AzureRmDataLakeStoreItem** laddar ned en fil från data Lake Store.

## BESKRIVS

### Exempel 1: Hämta ett objekt från data Lake Store
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv"
```

Det här kommandot laddar ned filen TestSource.csv från data Lake Store till C:\Test.csv.

## MALLPARAMETRAR

### -Konto
Anger namnet på data Lake Store-kontot.

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

### -ConcurrentFileCount
Anger det högsta antalet filer som laddas ned parallellt för en mapp nedladdning.
Standardvärdet är fem (5).

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Mål
Anger den lokala fil Sök vägen som filen ska hämtas till.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiagnosticLogLevel
Anger om den diagnostiska loggnings nivå som ska användas för att registrera händelser under fil-eller mapp-importen. Standard är ett fel.

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel
Parameter Sets: Include diagnostic logging
Aliases: 
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiagnosticLogPath
Anger sökvägen till Diagnostikrapporten för att spela in händelser för fil-eller mapp.

```yaml
Type: System.String
Parameter Sets: Include diagnostic logging
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Anger att den här åtgärden kan skriva över målfilen om den redan finns.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Anger sökvägen för det objekt som ska hämtas från data Lake Store från rot katalogen (/).

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

### -PerFileThreadCount
Anger maximalt antal trådar som ska användas per fil.
Standardvärdet är tio (10).

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Recurse
Anger att en mapp som laddas ned är rekursiv.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Fortsätt
Anger att filen eller filerna som kopieras är en fortsättning på en tidigare nedladdning.
Nedladdningen fortsätter från den senaste filen som inte laddats ned helt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### strängvärdet
Sökvägen till filen eller mappen laddades ner till.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmDataLakeStoreItem](./Get-AzureRmDataLakeStoreItem.md)

[Import-AzureRmDataLakeStoreItem](./Import-AzureRmDataLakeStoreItem.md)

[Anslut-AzureRmDataLakeStoreItem](./Join-AzureRmDataLakeStoreItem.md)

[Move-AzureRmDataLakeStoreItem](./Move-AzureRmDataLakeStoreItem.md)

[New-AzureRmDataLakeStoreItem](./New-AzureRmDataLakeStoreItem.md)

[Remove-AzureRmDataLakeStoreItem](./Remove-AzureRmDataLakeStoreItem.md)

[Test-AzureRmDataLakeStoreItem](./Test-AzureRmDataLakeStoreItem.md)


