---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E4660D0A-26CB-488C-9A29-3ED94A0DCDA2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e62cb7ed272a5c0d5ff4ff0ecbafe30a0c5ee9e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093187"
---
# <span data-ttu-id="f33f9-101">Save-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="f33f9-101">Save-AzureVhd</span></span>

## <span data-ttu-id="f33f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f33f9-102">SYNOPSIS</span></span>
<span data-ttu-id="f33f9-103">Aktiverar nedladdning av. VHD-bilder.</span><span class="sxs-lookup"><span data-stu-id="f33f9-103">Enables download of .vhd images.</span></span>

## <span data-ttu-id="f33f9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f33f9-104">SYNTAX</span></span>

```
Save-AzureVhd [-Source] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfThreads] <Int32>] [[-StorageKey] <String>]
 [-OverWrite] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f33f9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f33f9-105">DESCRIPTION</span></span>
<span data-ttu-id="f33f9-106">Med cmdleten **Save-AzureVhd** kan du ladda ned en VHD-avbildning från en BLOB där de lagras till en fil.</span><span class="sxs-lookup"><span data-stu-id="f33f9-106">The **Save-AzureVhd** cmdlet enables download of .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="f33f9-107">Den har parametrar för att konfigurera nedladdningen genom att ange antalet Hämta trådar som används eller skriva över filen som redan finns i den angivna sökvägen.</span><span class="sxs-lookup"><span data-stu-id="f33f9-107">It has parameters to configure the download process by specifying the number of downloader threads that are used or overwriting the file which already exists in the specified file path.</span></span>

<span data-ttu-id="f33f9-108">**Save-AzureVhd** gör inte något format konvertering för VHD och blobben laddas ner.</span><span class="sxs-lookup"><span data-stu-id="f33f9-108">**Save-AzureVhd** does not do any VHD format conversion and the blob is downloaded as it is.</span></span>

## <span data-ttu-id="f33f9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f33f9-109">EXAMPLES</span></span>

### <span data-ttu-id="f33f9-110">Exempel 1: Ladda ned en VHD-fil</span><span class="sxs-lookup"><span data-stu-id="f33f9-110">Example 1: Download a VHD file</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="f33f9-111">Det här kommandot laddar ned en VHD-fil.</span><span class="sxs-lookup"><span data-stu-id="f33f9-111">This command downloads a .vhd file.</span></span>

### <span data-ttu-id="f33f9-112">Exempel 2: Ladda ned en VHD-fil och skriv över den lokala filen</span><span class="sxs-lookup"><span data-stu-id="f33f9-112">Example 2: Download a VHD file and overwrite the local file</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="f33f9-113">Det här kommandot laddar ned en VHD-fil och skriver över en fil i mål Sök vägen.</span><span class="sxs-lookup"><span data-stu-id="f33f9-113">This command downloads a .vhd file and overwrites any file in the destination path.</span></span>

### <span data-ttu-id="f33f9-114">Exempel 3: Ladda ned en VHD-fil och ange antalet trådar</span><span class="sxs-lookup"><span data-stu-id="f33f9-114">Example 3: Download a VHD file and specify the number of threads</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="f33f9-115">Det här kommandot laddar ned en VHD-fil och anger antalet trådar.</span><span class="sxs-lookup"><span data-stu-id="f33f9-115">This command downloads a .vhd file and specifies the number of threads.</span></span>

### <span data-ttu-id="f33f9-116">Exempel 4: Ladda ned en VHD-fil och ange lagrings plats</span><span class="sxs-lookup"><span data-stu-id="f33f9-116">Example 4: Download a VHD file and specify the storage key</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw=="
```

<span data-ttu-id="f33f9-117">Det här kommandot laddar ned en VHD-fil och anger lagrings utrymmet.</span><span class="sxs-lookup"><span data-stu-id="f33f9-117">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="f33f9-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f33f9-118">PARAMETERS</span></span>

### <span data-ttu-id="f33f9-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f33f9-119">-InformationAction</span></span>
<span data-ttu-id="f33f9-120">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="f33f9-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f33f9-121">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f33f9-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f33f9-122">Vidare</span><span class="sxs-lookup"><span data-stu-id="f33f9-122">Continue</span></span>
- <span data-ttu-id="f33f9-123">Över</span><span class="sxs-lookup"><span data-stu-id="f33f9-123">Ignore</span></span>
- <span data-ttu-id="f33f9-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="f33f9-124">Inquire</span></span>
- <span data-ttu-id="f33f9-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f33f9-125">SilentlyContinue</span></span>
- <span data-ttu-id="f33f9-126">Stanna</span><span class="sxs-lookup"><span data-stu-id="f33f9-126">Stop</span></span>
- <span data-ttu-id="f33f9-127">Avbryt</span><span class="sxs-lookup"><span data-stu-id="f33f9-127">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f33f9-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f33f9-128">-InformationVariable</span></span>
<span data-ttu-id="f33f9-129">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="f33f9-129">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f33f9-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="f33f9-130">-LocalFilePath</span></span>
<span data-ttu-id="f33f9-131">Anger lokal fil Sök väg.</span><span class="sxs-lookup"><span data-stu-id="f33f9-131">Specifies the local file path.</span></span>

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

### <span data-ttu-id="f33f9-132">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="f33f9-132">-NumberOfThreads</span></span>
<span data-ttu-id="f33f9-133">Anger hur många nedladdnings trådar som denna cmdlet använder under nedladdningen.</span><span class="sxs-lookup"><span data-stu-id="f33f9-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

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

### <span data-ttu-id="f33f9-134">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="f33f9-134">-OverWrite</span></span>
<span data-ttu-id="f33f9-135">Anger att denna cmdlet tar bort filen som anges av *LocalFilePath* -filen om den finns.</span><span class="sxs-lookup"><span data-stu-id="f33f9-135">Specifies that this cmdlet deletes the file specified by *LocalFilePath* file if it exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f33f9-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="f33f9-136">-Profile</span></span>
<span data-ttu-id="f33f9-137">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="f33f9-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f33f9-138">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="f33f9-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f33f9-139">-Källa</span><span class="sxs-lookup"><span data-stu-id="f33f9-139">-Source</span></span>
<span data-ttu-id="f33f9-140">Anger URI (Uniform Resource Identifier) för blobben i `Azure` .</span><span class="sxs-lookup"><span data-stu-id="f33f9-140">Specifies the Uniform Resource Identifier (URI) to the blob in `Azure`.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: src

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f33f9-141">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="f33f9-141">-StorageKey</span></span>
<span data-ttu-id="f33f9-142">Anger lagrings Key för Blob Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="f33f9-142">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="f33f9-143">Om det inte anges försöker **Spara-AzureVhd** att bestämma lagrings namnet på kontot i *SourceUri* från Azure.</span><span class="sxs-lookup"><span data-stu-id="f33f9-143">If it is not provided, **Save-AzureVhd** attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: sk

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f33f9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f33f9-144">CommonParameters</span></span>
<span data-ttu-id="f33f9-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f33f9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f33f9-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f33f9-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f33f9-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f33f9-147">INPUTS</span></span>

## <span data-ttu-id="f33f9-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f33f9-148">OUTPUTS</span></span>

## <span data-ttu-id="f33f9-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f33f9-149">NOTES</span></span>

## <span data-ttu-id="f33f9-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f33f9-150">RELATED LINKS</span></span>

[<span data-ttu-id="f33f9-151">Add-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="f33f9-151">Add-AzureVhd</span></span>](./Add-AzureVhd.md)


