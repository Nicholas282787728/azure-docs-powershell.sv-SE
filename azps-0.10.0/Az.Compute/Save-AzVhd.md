---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Save-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Save-AzVhd.md
ms.openlocfilehash: f178b6aca1cf3747bc53807290585c01b91f3c2e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924897"
---
# Save-AzVhd

## Sammanfattning
Sparar hämtade VHD-bilder lokalt.

## FRÅGESYNTAXEN

### ResourceGroupParameterSetName
```
Save-AzVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### StorageKeyParameterSetName
```
Save-AzVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Save-AzVhd** sparar. VHD-bilder från en BLOB där de lagras i en fil.
Du kan ange hur många par trådar som processen använder och om du vill ersätta en fil som redan finns.

Denna cmdlet laddar ner innehållet som det är.
Den tillämpar ingen konvertering från virtuell hård disk (VHD).

## BESKRIVS

### Exempel 1: Ladda ned en bild
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

Det här kommandot laddar ned en VHD-fil och lagrar den i den lokala sökvägen C:\vhd\Win7Image.vhd.

### Exempel 2: Ladda ned en bild och skriv över den lokala filen
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

Det här kommandot laddar ned en VHD-fil och lagrar den i den lokala sökvägen.
Kommandot innehåller parametern *Overwrite* .
Om C:\vhd\Win7Image.vhd redan finns ersätter det här kommandot det.

### Exempel 3: Ladda ned en bild genom att använda ett angivet antal trådar
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

Det här kommandot laddar ned en VHD-fil och lagrar den i den lokala sökvägen.
Kommandot anger ett värde för 32 för parametern *NumberOfThreads* .
Därför använder cmdleten 32 trådar för den här åtgärden.

### Exempel 4: Ladda ned en bild och ange lagrings plats
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

Det här kommandot laddar ned en VHD-fil och anger lagrings utrymmet.

## MALLPARAMETRAR

### -AsJob
Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.

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

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalFilePath
Anger den lokala sökvägen till den sparade bilden.

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NumberOfThreads
Anger hur många nedladdnings trådar som denna cmdlet använder under nedladdningen.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Skriver över
Anger att denna cmdlet ersätter filen som anges i *LocalFilePath* -filen om den finns.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på resurs gruppen för lagrings kontot.

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SourceUri
Anger URI (Uniform Resource Identifier) för blobben i `Azure` .

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: src, Source

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageKey
Anger lagrings Key för Blob Storage-kontot.
Om du inte anger en profil försöker den här cmdleten avgöra lagrings plats för kontot i *SourceUri* från Azure.

```yaml
Type: String
Parameter Sets: StorageKeyParameterSetName
Aliases: sk

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### Microsoft. Azure. commands. Compute. Models. VhdDownloadContext

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzVhd](./Add-AzVhd.md)


