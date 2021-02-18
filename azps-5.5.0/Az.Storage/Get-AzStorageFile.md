---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: 8251c18acad2da881c3215df6a2e743b6804af6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231631"
---
# Get-AzStorageFile

## SYNOPSIS
Listar kataloger och filer för en sökväg.

## SYNTAX

### ShareName (standard)
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### Dela
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### Katalog
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzStorageFile** visar kataloger och filer för den delning eller katalog du anger.
Ange *sökvägsparametern* för att få en instans av en katalog eller fil i den angivna sökvägen.
Den här cmdleten **returnerar AzureStorageFile-** **och AzureStorageDirectory-objekt.**
Du kan använda egenskapen **IsDirectory** till att skilja mellan mappar och filer.

## EXEMPEL

### Exempel 1: Lista kataloger i en resurs
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "AzureStorageFileDirectory"}
```

Det här kommandot listar bara kataloger i dela ContosoShare06.
Först hämtas både filer och kataloger, skickar  dem till var-operatorn med hjälp av rörledningsoperatorn och tar sedan bort objekt vars typ inte är "AzureStorageFileDirectory".

### Exempel 2: Lista en filkatalog
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

Det här kommandot visar filerna och mapparna i katalogen ContosoWorkingFolder under resursen ContosoShare06.
Den hämtar först kataloginstansen och förs sedan till cmdleten **Get-AzStorageFile** för att lista katalogen.

## PARAMETERS

### -ClientTimeoutPerRequest
Anger klientsidans time out-intervall i sekunder för en tjänstbegäran.
Om det föregående samtalet misslyckas inom det angivna intervallet försöker den här cmdleten att begära en gång till.
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
Den här parametern kan hjälpa till att minska problem med nätverksanslutningen i miljöer med låg bandbredd, till exempel 100 kilobit per sekund.
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
Anger ett Azure Storage-sammanhang.
För att få ett Storage-sammanhang använder du New-AzStorageContext-cmdleten.

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

### -Directory
Anger en mapp som ett **CloudFileDirectory-objekt.**
Den här cmdleten hämtar mappen som parametern anger.
Om du vill hämta en katalog använder du New-AzStorageDirectory-cmdleten.
Du kan också använda **cmdleten Get-AzStorageFile** för att hämta en katalog.

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
Om du utelämnar *sökvägsparametern* visar **Get-AzStorageFile** kataloger och filer i den angivna filresursen eller katalogen.
Om du tar med *sökvägsparametern* **returnerar Get-AzStorageFile** en instans av en katalog eller fil i den angivna sökvägen.

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
Anger tidsgränsintervallet på tjänstsidan i sekunder för en begäran.
Om det angivna intervallet gått innan tjänsten bearbetar begäran returnerar lagringstjänsten ett fel.

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
Anger ett **CloudFileShare-objekt.**
Den här cmdleten hämtar en fil eller katalog från filresursen som parametern anger.
Om du vill **hämta ett CloudFileShare-objekt** använder du Get-AzStorageShare cmdleten.
Det här objektet innehåller storage-kontexten.
Om du anger den här parametern ska du inte ange *kontextparametern.*

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
Anger namnet på filresursen.
Den här cmdleten hämtar en fil eller katalog från filresursen som parametern anger.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.Azure.Storage.File.CloudFileShare

### Microsoft.Azure.Storage.File.CloudFileDirectory

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.iStorageContext

## UTDATA

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzStorageFileContent](./Get-AzStorageFileContent.md)

[New-AzStorageDirectory](./New-AzStorageDirectory.md)

[Remove-AzStorageDirectory](./Remove-AzStorageDirectory.md)

[Remove-AzStorageFile](./Remove-AzStorageFile.md)

[Set-AzStorageFileContent](./Set-AzStorageFileContent.md)


