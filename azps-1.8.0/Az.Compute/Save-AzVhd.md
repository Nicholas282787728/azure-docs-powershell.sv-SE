---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVhd.md
ms.openlocfilehash: 7fccc80dcd882253a656e403109d43da07ab111d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754489"
---
# <span data-ttu-id="ad837-101">Save-AzVhd</span><span class="sxs-lookup"><span data-stu-id="ad837-101">Save-AzVhd</span></span>

## <span data-ttu-id="ad837-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad837-102">SYNOPSIS</span></span>
<span data-ttu-id="ad837-103">Sparar hämtade VHD-bilder lokalt.</span><span class="sxs-lookup"><span data-stu-id="ad837-103">Saves downloaded .vhd images locally.</span></span>

## <span data-ttu-id="ad837-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad837-104">SYNTAX</span></span>

### <span data-ttu-id="ad837-105">ResourceGroupParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ad837-105">ResourceGroupParameterSetName</span></span>
```
Save-AzVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad837-106">StorageKeyParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ad837-106">StorageKeyParameterSetName</span></span>
```
Save-AzVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfThreads] <Int32>]
 [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad837-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad837-107">DESCRIPTION</span></span>
<span data-ttu-id="ad837-108">Cmdleten **Save-AzVhd** sparar. VHD-bilder från en BLOB där de lagras i en fil.</span><span class="sxs-lookup"><span data-stu-id="ad837-108">The **Save-AzVhd** cmdlet saves .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="ad837-109">Du kan ange hur många par trådar som processen använder och om du vill ersätta en fil som redan finns.</span><span class="sxs-lookup"><span data-stu-id="ad837-109">You can specify the number of downloader threads that the process uses and whether to replace a file that already exists.</span></span>
<span data-ttu-id="ad837-110">Denna cmdlet laddar ner innehållet som det är.</span><span class="sxs-lookup"><span data-stu-id="ad837-110">This cmdlet downloads content as it is.</span></span>
<span data-ttu-id="ad837-111">Den tillämpar ingen konvertering från virtuell hård disk (VHD).</span><span class="sxs-lookup"><span data-stu-id="ad837-111">It does not apply any Virtual Hard Disk (VHD) format conversion.</span></span>

## <span data-ttu-id="ad837-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad837-112">EXAMPLES</span></span>

### <span data-ttu-id="ad837-113">Exempel 1: Ladda ned en bild</span><span class="sxs-lookup"><span data-stu-id="ad837-113">Example 1: Download an image</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

<span data-ttu-id="ad837-114">Det här kommandot laddar ned en VHD-fil och lagrar den i den lokala sökvägen C:\vhd\Win7Image.vhd.</span><span class="sxs-lookup"><span data-stu-id="ad837-114">This command downloads a .vhd file, and stores it in the local path C:\vhd\Win7Image.vhd.</span></span>

### <span data-ttu-id="ad837-115">Exempel 2: Ladda ned en bild och skriv över den lokala filen</span><span class="sxs-lookup"><span data-stu-id="ad837-115">Example 2: Download an image and overwrite the local file</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

<span data-ttu-id="ad837-116">Det här kommandot laddar ned en VHD-fil och lagrar den i den lokala sökvägen.</span><span class="sxs-lookup"><span data-stu-id="ad837-116">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="ad837-117">Kommandot innehåller parametern *Overwrite* .</span><span class="sxs-lookup"><span data-stu-id="ad837-117">The command includes the *Overwrite* parameter.</span></span>
<span data-ttu-id="ad837-118">Om C:\vhd\Win7Image.vhd redan finns ersätter det här kommandot det.</span><span class="sxs-lookup"><span data-stu-id="ad837-118">Therefore, if C:\vhd\Win7Image.vhd already exists, this command replaces it.</span></span>

### <span data-ttu-id="ad837-119">Exempel 3: Ladda ned en bild genom att använda ett angivet antal trådar</span><span class="sxs-lookup"><span data-stu-id="ad837-119">Example 3: Download an image by using a specified number of threads</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

<span data-ttu-id="ad837-120">Det här kommandot laddar ned en VHD-fil och lagrar den i den lokala sökvägen.</span><span class="sxs-lookup"><span data-stu-id="ad837-120">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="ad837-121">Kommandot anger ett värde för 32 för parametern *NumberOfThreads* .</span><span class="sxs-lookup"><span data-stu-id="ad837-121">The command specifies a value of 32 for the *NumberOfThreads* parameter.</span></span>
<span data-ttu-id="ad837-122">Därför använder cmdleten 32 trådar för den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="ad837-122">Therefore, the cmdlet uses 32 threads for this action.</span></span>

### <span data-ttu-id="ad837-123">Exempel 4: Ladda ned en bild och ange lagrings plats</span><span class="sxs-lookup"><span data-stu-id="ad837-123">Example 4: Download an image and specify the storage key</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

<span data-ttu-id="ad837-124">Det här kommandot laddar ned en VHD-fil och anger lagrings utrymmet.</span><span class="sxs-lookup"><span data-stu-id="ad837-124">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="ad837-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad837-125">PARAMETERS</span></span>

### <span data-ttu-id="ad837-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad837-126">-AsJob</span></span>
<span data-ttu-id="ad837-127">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="ad837-127">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ad837-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad837-128">-DefaultProfile</span></span>
<span data-ttu-id="ad837-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ad837-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad837-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="ad837-130">-LocalFilePath</span></span>
<span data-ttu-id="ad837-131">Anger den lokala sökvägen till den sparade bilden.</span><span class="sxs-lookup"><span data-stu-id="ad837-131">Specifies the local file path of the saved image.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad837-132">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="ad837-132">-NumberOfThreads</span></span>
<span data-ttu-id="ad837-133">Anger hur många nedladdnings trådar som denna cmdlet använder under nedladdningen.</span><span class="sxs-lookup"><span data-stu-id="ad837-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad837-134">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="ad837-134">-OverWrite</span></span>
<span data-ttu-id="ad837-135">Anger att denna cmdlet ersätter filen som anges i *LocalFilePath* -filen om den finns.</span><span class="sxs-lookup"><span data-stu-id="ad837-135">Indicates that this cmdlet replaces the file specified by *LocalFilePath* file if it exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad837-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad837-136">-ResourceGroupName</span></span>
<span data-ttu-id="ad837-137">Anger namnet på resurs gruppen för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="ad837-137">Specifies the name of the resource group of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad837-138">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="ad837-138">-SourceUri</span></span>
<span data-ttu-id="ad837-139">Anger URI (Uniform Resource Identifier) för blobben i `Azure` .</span><span class="sxs-lookup"><span data-stu-id="ad837-139">Specifies the Uniform Resource Identifier (URI) of the blob in `Azure`.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: src, Source

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad837-140">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="ad837-140">-StorageKey</span></span>
<span data-ttu-id="ad837-141">Anger lagrings Key för Blob Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="ad837-141">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="ad837-142">Om du inte anger en profil försöker den här cmdleten avgöra lagrings plats för kontot i *SourceUri* från Azure.</span><span class="sxs-lookup"><span data-stu-id="ad837-142">If you do not specify a key, this cmdlet attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageKeyParameterSetName
Aliases: sk

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad837-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad837-143">CommonParameters</span></span>
<span data-ttu-id="ad837-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad837-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad837-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad837-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad837-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad837-146">INPUTS</span></span>

### <span data-ttu-id="ad837-147">System. String</span><span class="sxs-lookup"><span data-stu-id="ad837-147">System.String</span></span>

### <span data-ttu-id="ad837-148">System. URI</span><span class="sxs-lookup"><span data-stu-id="ad837-148">System.Uri</span></span>

## <span data-ttu-id="ad837-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad837-149">OUTPUTS</span></span>

### <span data-ttu-id="ad837-150">Microsoft. Azure. commands. Compute. Models. VhdDownloadContext</span><span class="sxs-lookup"><span data-stu-id="ad837-150">Microsoft.Azure.Commands.Compute.Models.VhdDownloadContext</span></span>

## <span data-ttu-id="ad837-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad837-151">NOTES</span></span>

## <span data-ttu-id="ad837-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad837-152">RELATED LINKS</span></span>

[<span data-ttu-id="ad837-153">Add-AzVhd</span><span class="sxs-lookup"><span data-stu-id="ad837-153">Add-AzVhd</span></span>](./Add-AzVhd.md)


