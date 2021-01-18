---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: 8251c18acad2da881c3215df6a2e743b6804af6e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520303"
---
# Get-AzStorageFile

## Sammanfattning
Visar en lista över kataloger och filer för en sökväg.

## FRÅGESYNTAXEN

### Resurs namn (standard)
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### Resurserna
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### Katalogen
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzStorageFile** innehåller en lista över kataloger och filer för den delning eller katalog som du anger.
Ange parametern *Path* för att få en instans av en katalog eller fil på den angivna sökvägen.
Denna cmdlet returnerar **AzureStorageFile** -och **AzureStorageDirectory** -objekt.
Du kan använda egenskapen **IsDirectory** för att skilja mellan mappar och filer.

## BESKRIVS

### Exempel 1: lista kataloger i en resurs
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "AzureStorageFileDirectory"}
```

Det här kommandot listar bara katalogerna i avsnittet Dela ContosoShare06.
Den hämtar först både filer och kataloger, skickar dem till operatorn **WHERE** genom att använda pipeline-operatorn och ignorera sedan alla objekt vars typ inte är "AzureStorageFileDirectory".

### Exempel 2: lista en fil katalog
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

Det här kommandot listar filerna och mapparna i katalogen ContosoWorkingFolder under fliken Dela ContosoShare06.
Den först får katalog instansen och går sedan till cmdleten **Get-AzStorageFile** för att lista katalogen.

## MALLPARAMETRAR

### -ClientTimeoutPerRequest
Anger tids gräns för klient sidan i sekunder för en tjänst förfrågan.
Om det föregående samtalet inte fungerar inom det angivna intervallet, försöker den här cmdleten igen.
Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.

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
Anger maximalt antal samtidiga nätverks samtal.
Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.
Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.
Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.
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

### -Kontext
Anger en Azure Storage-kontext.
Använd New-AzStorageContext cmdlet för att få en lagrings kontext.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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

### -Katalog
Anger en mapp som ett **CloudFileDirectory** -objekt.
Denna cmdlet tar fram den mapp som den här parametern anger.
Använd New-AzStorageDirectory cmdlet för att få en katalog.
Du kan också använda cmdleten **Get-AzStorageFile** för att få en katalog.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Path
Anger sökvägen till en mapp.
Om du utelämnar parametern *Path* visas **katalogerna** och filerna i den angivna fil resursen eller katalogen.
Om du inkluderar parametern *Path* returnerar **Get-AzStorageFile** en instans av en katalog eller fil i den angivna sökvägen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Anger timeout-intervallet i sekunder för en begäran.
Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.

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

### -Dela
Anger ett **CloudFileShare** -objekt.
Denna cmdlet hämtar en fil eller katalog från fil resursen som den här parametern anger.
För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzStorageShare.
Det här objektet innehåller lagrings kontexten.
Om du anger den här parametern ska du inte ange en *kontext* parameter.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ShareName
Anger namnet på fil resursen.
Denna cmdlet hämtar en fil eller katalog från fil resursen som den här parametern anger.

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. Storage. File. CloudFileShare

### Microsoft. Azure. Storage. File. CloudFileDirectory

### Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext

## VÄRDEN

### Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageFile

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzStorageFileContent](./Get-AzStorageFileContent.md)

[New-AzStorageDirectory](./New-AzStorageDirectory.md)

[Remove-AzStorageDirectory](./Remove-AzStorageDirectory.md)

[Remove-AzStorageFile](./Remove-AzStorageFile.md)

[Set-AzStorageFileContent](./Set-AzStorageFileContent.md)


