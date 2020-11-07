---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: aa1c7cebbcb6fe24b06638644d19b07c83c2ff04
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923661"
---
# Get-AzStorageFileContent

## Sammanfattning
Laddar ned innehållet i en fil.

## FRÅGESYNTAXEN

### Resurs namn (standard)
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Resurserna
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Katalogen
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Fil
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzStorageFileContent** laddar ned innehållet i en fil och sparar den sedan på en destination som du anger.
Denna cmdlet returnerar inte innehållet i filen.

## BESKRIVS

### Exempel 1: Ladda ned en fil från en mapp
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

Det här kommandot laddar ned en fil med namnet CurrentDataFile i mappen ContosoWorkingFolder från fil resursen ContosoShare06 till den aktuella mappen.

### Exempel 2: laddar ned filer under exempel fil resurs
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

I det här exemplet hämtas filerna under exempel fil resurs

## MALLPARAMETRAR

### -CheckMd5
Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.
Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.
Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.
Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.

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
Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.
Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.
Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.
Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.

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
Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.
Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.
Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.
Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.

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
Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.
Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.
Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.
Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.

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

### -Mål
Anger mål Sök vägen.
Denna cmdlet laddar ner fil innehållet till den plats som den här parametern anger.
Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.
Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.
Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.
Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.

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

### -Katalog
Anger en mapp som ett **CloudFileDirectory** -objekt.
Denna cmdlet hämtar innehåll från en fil i den mapp som anges i den här parametern.
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

### -Fil
Anger en fil som ett **CloudFile** -objekt.
Denna cmdlet hämtar filen som parametern anger.
För att hämta ett **CloudFile** -objekt, Använd cmdleten Get-AzStorageFile.

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
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
Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.
Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.
Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.
Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.

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
Denna cmdlet hämtar innehållet som den här parametern anger.
Om filen inte finns returnerar denna cmdlet ett fel.

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

### -ServerTimeoutPerRequest
Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.
Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.
Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.
Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.

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
Denna cmdlet laddar ner innehållet i filen i avsnittet Dela den här parametern anger.
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
Denna cmdlet laddar ner innehållet i filen i avsnittet Dela den här parametern anger.

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

### Microsoft. WindowsAz. Storage. File. CloudFile
Parametrar: fil (ByValue)

### Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext

## VÄRDEN

### Microsoft. WindowsAz. Storage. File. CloudFile

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzStorageFile](./Get-AzStorageFile.md)

[Set-AzStorageFileContent](./Set-AzStorageFileContent.md)


