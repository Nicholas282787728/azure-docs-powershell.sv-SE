---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
ms.openlocfilehash: 3fed30a260532378274e2df815d6e4b252c018f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100252853"
---
# Set-AzStorageFileContent

## SYNOPSIS
Laddar upp innehållet i en fil.

## SYNTAX

### ShareName (standard)
```
Set-AzStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### Dela
```
Set-AzStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### Katalog
```
Set-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Set-AzStorageFileContent** laddar upp innehållet i en fil till en fil på en viss resurs.

## EXEMPEL

### Exempel 1: Ladda upp en fil i den aktuella mappen
```
PS C:\>Set-AzStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

Med det här kommandot överförs en fil med namnet DataFile37 i den aktuella mappen som en fil med namnet CurrentDataFile i mappen ContosoWorkingFolder.

### Exempel 2: Ladda upp alla filer i den aktuella mappen
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

Det här exemplet använder flera vanliga Windows PowerShell-cmdlets och den aktuella cmdleten för att ladda upp alla filer från den aktuella mappen till rotmappen för behållaren ContosoShare06.
Det första kommandot får namnet på den aktuella mappen och lagrar den i $CurrentFolder variabeln.
Det andra kommandot använder cmdleten **Get-AzStorageShare** för att hämta filresursen ContosoShare06 och lagrar den sedan i $Container variabeln.
Det slutliga kommandot får innehållet i den aktuella mappen och skickar vart och ett till cmdleten Where-Object med hjälp av rörledningsoperatorn.
Den cmdleten filtrerar bort objekt som inte är filer och skickar sedan filerna ForEach-Object cmdleten.
Den cmdleten kör ett skriptblock för varje fil som skapar rätt sökväg för den och använder sedan den aktuella cmdleten för att ladda upp filen.
Resultatet har samma namn och samma relativa position när det gäller andra filer som det här exemplet laddar upp.
Mer information om skriptblock hittar du om du `Get-Help about_Script_Blocks` skriver.

### Exempel 3: Ladda upp en lokal fil till en Azure-fil och spara de lokala fil-SMB-egenskaperna (File Attributtes, File Creation Time, File Last Write Time) i Azure-filen.
```
PS C:\>Get-AzStorageFileContent -source $localFilePath -ShareName sample -Path "dir1/file1" -PreserveSMBAttribute
```

Det här exemplet laddar upp en lokal fil till en Azure-fil och sparar de lokala fil-SMB-egenskaperna (File Attributtes, File Creation Time, File Last Write Time) i Azure-filen.

## PARAMETERS

### -As Ent fån
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
Anger ett Azure-lagringssammanhang.
Om du vill skapa ett lagringssammanhang använder du cmdleten [New-AzStorageContext.](./New-AzStorageContext.md)

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
Den här cmdleten laddar upp filen till mappen som parametern anger.
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

### -Force
Anger att den här cmdleten skriver över en befintlig Azure-lagringsfil.

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
Anger att denna cmdlet returnerar **AzureStorageFile-objektet** som skapas eller överförs.

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
Den här cmdleten laddar upp innehållet till filen som parametern anger, eller till en fil i mappen som parametern anger.
Om du anger en mapp skapar den här cmdleten en fil med samma namn som källfilen.
Om du anger en sökväg till en fil som inte finns skapar cmdleten filen och sparar innehållet i den filen.
Om du anger en fil som redan  finns och du anger force-parametern skriver den här cmdleten över innehållet i filen.
Om du anger en fil som redan finns och du inte anger Force gör den här cmdleten ingen ändring och returnerar ett fel.
Om du anger en sökväg till en mapp som inte finns gör den här cmdleten ingen ändring och returnerar ett fel.

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

### -Dela
Anger ett **CloudFileShare-objekt.**
Den här cmdleten laddas upp till en fil i filresursen som den här parametern anger.
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
Den här cmdleten laddas upp till en fil i filresursen som den här parametern anger.

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
Anger källfilen som cmdleten laddar upp.
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

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.iStorageContext

## UTDATA

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Remove-AzStorageDirectory](./Remove-AzStorageDirectory.md)

[New-AzStorageDirectory](./New-AzStorageDirectory.md)

[Get-AzStorageFileContent](./Get-AzStorageFileContent.md)
