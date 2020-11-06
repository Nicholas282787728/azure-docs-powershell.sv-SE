---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: a04a035e0fedfa4bca00eceda1dcf8dba0680c0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581583"
---
# Get-AzureStorageFileContent

## Sammanfattning
Laddar ned innehållet i en fil.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### Resurs namn (standard)
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Resurserna
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Katalogen
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Fil
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureStorageFileContent** laddar ned innehållet i en fil och sparar den sedan på en destination som du anger.
Denna cmdlet returnerar inte innehållet i filen.

## BESKRIVS

### Exempel 1: Ladda ned en fil från en mapp
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

Det här kommandot laddar ned en fil med namnet CurrentDataFile i mappen ContosoWorkingFolder från fil resursen ContosoShare06 till den aktuella mappen.

### Exempel 2: laddar ned filer under exempel fil resurs
```
PS C:\>Get-AzureStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzureStorageFileContent
```

I det här exemplet hämtas filerna under exempel fil resurs

## MALLPARAMETRAR

### -CheckMd5
Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.
Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.
Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.

Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientTimeoutPerRequest
Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.
Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.
Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.

Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.
Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.
Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.

Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kontext
Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.
Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.
Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.

Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Mål
Anger mål Sök vägen.
Denna cmdlet laddar ner fil innehållet till den plats som den här parametern anger.

Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.
Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.
Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.

Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Katalog
Anger en mapp som ett **CloudFileDirectory** -objekt.
Denna cmdlet hämtar innehåll från en fil i den mapp som anges i den här parametern.
Använd New-AzureStorageDirectory cmdlet för att få en katalog.
Du kan också använda Get-AzureStorageFile cmdlet för att få en katalog.

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Fil
Anger en fil som ett **CloudFile** -objekt.
Denna cmdlet hämtar filen som parametern anger.
För att hämta ett **CloudFile** -objekt, Använd cmdleten Get-AzureStorageFile.

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Force
Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.
Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.
Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.

Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.
Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.
Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.

Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Anger sökvägen till en fil.
Denna cmdlet hämtar innehållet som den här parametern anger.
Om filen inte finns returnerar denna cmdlet ett fel.

```yaml
Type: String
Parameter Sets: ShareName, Share, Directory
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.
Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.
Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.

Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Dela
Anger ett **CloudFileShare** -objekt.
Denna cmdlet laddar ner innehållet i filen i avsnittet Dela den här parametern anger.
För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzureStorageShare.
Det här objektet innehåller lagrings kontexten.
Om du anger den här parametern ska du inte ange en *kontext* parameter.

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ShareName
Anger namnet på fil resursen.
Denna cmdlet laddar ner innehållet i filen i avsnittet Dela den här parametern anger.

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### IStorageContext

Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline

### CloudFileDirectory

Parametern ' Directory ' godkänner värdet av typen ' CloudFileDirectory ' från pipeline

### CloudFile

Parametern ' File ' godkänner värdet för typen ' CloudFile ' från pipeline

### CloudFileShare

Parametern ' Share ' godkänner värdet av typen ' CloudFileShare ' från pipeline

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureStorageFile](./Get-AzureStorageFile.md)

[Set-AzureStorageFileContent](./Set-AzureStorageFileContent.md)


