---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 3c90e02194fa761bbb0fc00e11ea09d03ca00c1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210726"
---
# Get-AzStorageFileContent

## SYNOPSIS
Laddar ned innehållet i en fil.

## SYNTAX

### ShareName (standard)
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### Dela
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### Katalog
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### Fil
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzStorageFileContent** laddar ned innehållet i en fil och sparar den sedan till en destination som du anger.
Den här cmdleten returnerar inte innehållet i filen.

## EXEMPEL

### Exempel 1: Ladda ned en fil från en mapp
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

Med det här kommandot hämtas en fil som heter CurrentDataFile i mappen ContosoWorkingFolder från filresursen ContosoShare06 till den aktuella mappen.

### Exempel 2: Laddar ned filerna under exempelresursen
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

I det här exemplet laddas filerna ned under exempelresursen

### Exempel 3: Ladda ned en Azure-fil till en lokal fil och spara Azure File SMB-egenskaperna (File Attributtes, File Creation Time, File Last Write Time) i den lokala filen.
```
PS C:\>Get-AzStorageFileContent -ShareName sample -Path "dir1/file1" -Destination $localFilePath -PreserveSMBAttribute
```

Det här exemplet laddar ned en Azure-fil till en lokal fil och sparar Azure File SMB-egenskaperna (File Attributtes, File Creation Time, File Last Write Time) i den lokala filen.

## PARAMETERS

### -As Ent
Kör cmdleten i bakgrunden.

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

### -CheckMd5
Anger om Md5-summan ska kontrolleras för den hämtade filen.

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

### -ClientTimeoutPerRequest
Anger klienttidens time out-intervall i sekunder för en tjänstbegäran. Om det föregående samtalet misslyckas i det angivna intervallet försöker den här cmdleten att skicka begäran på ny plats. Om denna cmdlet inte får ett lyckat svar innan intervallet gått returnerar denna cmdlet ett fel.

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
Anger maximalt antal samtidiga nätverkssamtal. Du kan använda den här parametern för att begränsa samtidigheten för att begränsa den lokala CPU-belastningen och bandbreddsanvändningen genom att ange maximalt antal samtidiga nätverkssamtal. Det angivna värdet är ett absolut antal och multipliceras inte med basantalet. Den här parametern kan minska problem med nätverksanslutningen i miljöer med låg bandbredd, till exempel 100 kilobit per sekund. Standardvärdet är 10.

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
Anger ett Azure Storage-sammanhang. Om du vill skapa ett sammanhang använder New-AzStorageContext-cmdleten.

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

### -Destination
Anger målsökvägen.
Den här cmdleten laddar ned filinnehållet till den plats som parametern anger.
Om du anger sökvägen till en fil som inte finns skapar cmdleten filen och sparar innehållet i den nya filen.
Om du anger en sökväg till en fil  som redan finns och du anger force-parametern skriver cmdleten över filen.
Om du anger en sökväg till en befintlig fil och du inte anger Force uppmanas du av cmdleten innan den fortsätter.
Om du anger sökvägen till en mapp försöker den här cmdleten skapa en fil som har namnet på Azure-lagringsfilen.

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

### -Directory
Anger en mapp som ett **CloudFileDirectory-objekt.**
Den här cmdleten hämtar innehåll för en fil i den mapp som parametern anger.
Om du vill hämta en katalog använder du New-AzStorageDirectory-cmdleten.
Du kan också använda cmdlet Get-AzStorageFile för att hämta en katalog.

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

### -Arkiv
Anger en fil som ett **CloudFile-objekt.**
Den här cmdleten hämtar filen som parametern anger.
Om du vill **hämta ett CloudFile-objekt** använder du Get-AzStorageFile-cmdleten.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Force
Om du anger sökvägen till en fil som inte finns skapar cmdleten filen och sparar innehållet i den nya filen.
Om du anger en sökväg till en fil  som redan finns och du anger force-parametern skriver cmdleten över filen.
Om du anger en sökväg till en befintlig fil och du inte anger Force uppmanas du av cmdleten innan den fortsätter.
Om du anger sökvägen till en mapp försöker den här cmdleten skapa en fil som har namnet på Azure-lagringsfilen.

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
Anger att denna cmdlet returnerar **AzureStorageFile-objektet** som den laddar ned.

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
Anger sökvägen till en fil.
Den här cmdleten hämtar innehållet i filen som parametern anger.
Om filen inte finns returnerar cmdleten ett fel.

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreserveSMBAttribute
Behåll källegenskaperna för filen SMB (Filattributtes, tid då filen skapades, Filtid för senaste skrivning) i målfilen. Den här parametern är bara tillgänglig i Windows.

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

### -ServerTimeoutPerRequest
Anger time out-intervallet för tjänstsidan i sekunder för en begäran. Om det angivna intervallet gått innan tjänsten bearbetar begäran returnerar lagringstjänsten ett fel.

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
Den här cmdleten laddar ned innehållet i filen i parametern Dela den här parametern.
Om du vill **hämta ett CloudFileShare-objekt** använder du Get-AzStorageShare cmdleten.
Det här objektet innehåller lagringskontexten.
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
Den här cmdleten laddar ned innehållet i filen i parametern Dela den här parametern.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.Azure.Storage.File.CloudFileShare

### Microsoft.Azure.Storage.File.CloudFileDirectory

### Microsoft.Azure.Storage.File.CloudFile

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.iStorageContext

## UTDATA

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzStorageFile](./Get-AzStorageFile.md)

[Set-AzStorageFileContent](./Set-AzStorageFileContent.md)


