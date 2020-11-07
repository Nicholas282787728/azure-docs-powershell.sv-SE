---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
ms.openlocfilehash: 35a4ebeeb456b9234ed61b8010dd66bffd89165b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923453"
---
# Set-AzStorageFileContent

## Sammanfattning
Överför innehållet i en fil.

## FRÅGESYNTAXEN

### Resurs namn (standard)
```
Set-AzStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Resurserna
```
Set-AzStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Katalogen
```
Set-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzStorageFileContent** laddar upp innehållet i en fil till en fil på en angiven resurs.

## BESKRIVS

### Exempel 1: Ladda upp en fil i den aktuella mappen
```
PS C:\>Set-AzStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

Det här kommandot laddar upp en fil med namnet DataFile37 i den aktuella mappen som en fil med namnet CurrentDataFile i mappen som heter ContosoWorkingFolder.

### Exempel 2: Ladda upp alla filer i den aktuella mappen
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

I det här exemplet används flera vanliga Windows PowerShell-cmdlets och den aktuella cmdleten för att ladda upp alla filer från den aktuella mappen till rotmappen med ContosoShare06.
Det första kommandot får namnet på den aktuella mappen och lagrar det i $CurrentFolder variabeln.
Det andra kommandot använder cmdleten **Get-AzStorageShare** för att hämta fil resursen med namnet ContosoShare06 och lagrar den sedan i $container variabel.
Det sista kommandot får innehållet i den aktuella mappen och skickar dem till Where-Object cmdlet genom att använda pipeline-operatorn.
Denna cmdlet filtrerar bort objekt som inte är filer och överför sedan filerna till ForEach-Object cmdlet.
Denna cmdlet kör ett skript block för varje fil som skapar en lämplig sökväg för den och använder sedan den aktuella cmdleten för att ladda upp filen.
Resultatet har samma namn och samma relativa position som de andra filerna som det här exemplet laddar upp.
Om du vill ha mer information om skript block skriver du `Get-Help about_Script_Blocks` .

## MALLPARAMETRAR

### -ClientTimeoutPerRequest
Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.
Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.
Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.

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
Använd cmdleten [New-AzStorageContext](./New-AzStorageContext.md) för att få en lagrings kontext.

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
Denna cmdlet laddar upp filen till mappen som den här parametern anger.
Använd New-AzStorageDirectory cmdlet för att få en katalog.
Du kan också använda Get-AzStorageFile cmdlet för att få en katalog.

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Force
Anger att denna cmdlet skriver över en befintlig Azure-lagringsenhet.

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

### -PassThru
Anger att den här cmdleten returnerar **AzureStorageFile** -objektet som skapas eller upprättas.

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

### -Path
Anger sökvägen till en fil eller mapp.
Denna cmdlet laddar upp innehåll till filen som den här parametern anger, eller till en fil i mappen som den här parametern anger.
Om du anger en mapp skapar denna cmdlet en fil med samma namn som käll filen.
Om du anger en sökväg till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i filen.
Om du anger en fil som redan finns och du anger parametern _Force_ skriver denna cmdlet över innehållet i filen.
Om du anger en fil som redan finns och du inte anger _Force_ , gör denna cmdlet ingen ändring och returnerar ett fel.
Om du anger en sökväg till en mapp som inte finns görs ingen ändring av denna cmdlet och ett fel returneras.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Anger längden på tids gränsen för en server del av en begäran.

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

### -Dela
Anger ett **CloudFileShare** -objekt.
Denna cmdlet laddas upp till en fil i fil resursen den här parametern anger.
För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzStorageShare.
Det här objektet innehåller lagrings kontexten.
Om du anger den här parametern ska du inte ange en *kontext* parameter.

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
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
Denna cmdlet laddas upp till en fil i fil resursen den här parametern anger.

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

### -Källa
Anger den källfil som denna cmdlet laddar upp.
Om du anger en fil som inte finns returnerar denna cmdlet ett fel.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### Microsoft. WindowsAz. Storage. File. CloudFileShare
Parametrar: dela (ByValue)

### Microsoft. WindowsAz. Storage. File. CloudFileDirectory
Parametrar: katalog (ByValue)

### System. String

### Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext

## VÄRDEN

### Microsoft. WindowsAz. Storage. File. CloudFile

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Remove-AzStorageDirectory](./Remove-AzStorageDirectory.md)

[New-AzStorageDirectory](./New-AzStorageDirectory.md)

[Get-AzStorageFileContent](./Get-AzStorageFileContent.md)
