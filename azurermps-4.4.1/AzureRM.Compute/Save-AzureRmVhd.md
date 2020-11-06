---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVhd.md
ms.openlocfilehash: cc43308f0e0051a050b3983968d9c86f67ec66b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585720"
---
# <span data-ttu-id="cc49c-101">Save-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="cc49c-101">Save-AzureRmVhd</span></span>

## <span data-ttu-id="cc49c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cc49c-102">SYNOPSIS</span></span>
<span data-ttu-id="cc49c-103">Sparar hämtade VHD-bilder lokalt.</span><span class="sxs-lookup"><span data-stu-id="cc49c-103">Saves downloaded .vhd images locally.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc49c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cc49c-104">SYNTAX</span></span>

### <span data-ttu-id="cc49c-105">ResourceGroupParameterSetName</span><span class="sxs-lookup"><span data-stu-id="cc49c-105">ResourceGroupParameterSetName</span></span>
```
Save-AzureRmVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc49c-106">StorageKeyParameterSetName</span><span class="sxs-lookup"><span data-stu-id="cc49c-106">StorageKeyParameterSetName</span></span>
```
Save-AzureRmVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc49c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cc49c-107">DESCRIPTION</span></span>
<span data-ttu-id="cc49c-108">Cmdleten **Save-AzureRmVhd** sparar. VHD-bilder från en BLOB där de lagras i en fil.</span><span class="sxs-lookup"><span data-stu-id="cc49c-108">The **Save-AzureRmVhd** cmdlet saves .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="cc49c-109">Du kan ange hur många par trådar som processen använder och om du vill ersätta en fil som redan finns.</span><span class="sxs-lookup"><span data-stu-id="cc49c-109">You can specify the number of downloader threads that the process uses and whether to replace a file that already exists.</span></span>

<span data-ttu-id="cc49c-110">Denna cmdlet laddar ner innehållet som det är.</span><span class="sxs-lookup"><span data-stu-id="cc49c-110">This cmdlet downloads content as it is.</span></span>
<span data-ttu-id="cc49c-111">Den tillämpar ingen konvertering från virtuell hård disk (VHD).</span><span class="sxs-lookup"><span data-stu-id="cc49c-111">It does not apply any Virtual Hard Disk (VHD) format conversion.</span></span>

## <span data-ttu-id="cc49c-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cc49c-112">EXAMPLES</span></span>

### <span data-ttu-id="cc49c-113">Exempel 1: Ladda ned en bild</span><span class="sxs-lookup"><span data-stu-id="cc49c-113">Example 1: Download an image</span></span>
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="cc49c-114">Det här kommandot laddar ned en VHD-fil och lagrar den i den lokala sökvägen C:\vhd\Win7Image.vhd.</span><span class="sxs-lookup"><span data-stu-id="cc49c-114">This command downloads a .vhd file, and stores it in the local path C:\vhd\Win7Image.vhd.</span></span>

### <span data-ttu-id="cc49c-115">Exempel 2: Ladda ned en bild och skriv över den lokala filen</span><span class="sxs-lookup"><span data-stu-id="cc49c-115">Example 2: Download an image and overwrite the local file</span></span>
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="cc49c-116">Det här kommandot laddar ned en VHD-fil och lagrar den i den lokala sökvägen.</span><span class="sxs-lookup"><span data-stu-id="cc49c-116">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="cc49c-117">Kommandot innehåller parametern *Overwrite* .</span><span class="sxs-lookup"><span data-stu-id="cc49c-117">The command includes the *Overwrite* parameter.</span></span>
<span data-ttu-id="cc49c-118">Om C:\vhd\Win7Image.vhd redan finns ersätter det här kommandot det.</span><span class="sxs-lookup"><span data-stu-id="cc49c-118">Therefore, if C:\vhd\Win7Image.vhd already exists, this command replaces it.</span></span>

### <span data-ttu-id="cc49c-119">Exempel 3: Ladda ned en bild genom att använda ett angivet antal trådar</span><span class="sxs-lookup"><span data-stu-id="cc49c-119">Example 3: Download an image by using a specified number of threads</span></span>
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="cc49c-120">Det här kommandot laddar ned en VHD-fil och lagrar den i den lokala sökvägen.</span><span class="sxs-lookup"><span data-stu-id="cc49c-120">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="cc49c-121">Kommandot anger ett värde för 32 för parametern *NumberOfThreads* .</span><span class="sxs-lookup"><span data-stu-id="cc49c-121">The command specifies a value of 32 for the *NumberOfThreads* parameter.</span></span>
<span data-ttu-id="cc49c-122">Därför använder cmdleten 32 trådar för den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="cc49c-122">Therefore, the cmdlet uses 32 threads for this action.</span></span>

### <span data-ttu-id="cc49c-123">Exempel 4: Ladda ned en bild och ange lagrings plats</span><span class="sxs-lookup"><span data-stu-id="cc49c-123">Example 4: Download an image and specify the storage key</span></span>
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw=="
```

<span data-ttu-id="cc49c-124">Det här kommandot laddar ned en VHD-fil och anger lagrings utrymmet.</span><span class="sxs-lookup"><span data-stu-id="cc49c-124">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="cc49c-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cc49c-125">PARAMETERS</span></span>

### <span data-ttu-id="cc49c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc49c-126">-DefaultProfile</span></span>
<span data-ttu-id="cc49c-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cc49c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc49c-128">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="cc49c-128">-LocalFilePath</span></span>
<span data-ttu-id="cc49c-129">Anger den lokala sökvägen till den sparade bilden.</span><span class="sxs-lookup"><span data-stu-id="cc49c-129">Specifies the local file path of the saved image.</span></span>

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

### <span data-ttu-id="cc49c-130">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="cc49c-130">-NumberOfThreads</span></span>
<span data-ttu-id="cc49c-131">Anger hur många nedladdnings trådar som denna cmdlet använder under nedladdningen.</span><span class="sxs-lookup"><span data-stu-id="cc49c-131">Specifies the number of download threads that this cmdlet uses during download.</span></span>

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

### <span data-ttu-id="cc49c-132">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="cc49c-132">-OverWrite</span></span>
<span data-ttu-id="cc49c-133">Anger att denna cmdlet ersätter filen som anges i *LocalFilePath* -filen om den finns.</span><span class="sxs-lookup"><span data-stu-id="cc49c-133">Indicates that this cmdlet replaces the file specified by *LocalFilePath* file if it exists.</span></span>

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

### <span data-ttu-id="cc49c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc49c-134">-ResourceGroupName</span></span>
<span data-ttu-id="cc49c-135">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="cc49c-135">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="cc49c-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="cc49c-136">-SourceUri</span></span>
<span data-ttu-id="cc49c-137">Anger URI (Uniform Resource Identifier) för blobben i `Azure` .</span><span class="sxs-lookup"><span data-stu-id="cc49c-137">Specifies the Uniform Resource Identifier (URI) of the blob in `Azure`.</span></span>

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

### <span data-ttu-id="cc49c-138">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="cc49c-138">-StorageKey</span></span>
<span data-ttu-id="cc49c-139">Anger lagrings Key för Blob Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="cc49c-139">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="cc49c-140">Om du inte anger en profil försöker den här cmdleten avgöra lagrings plats för kontot i *SourceUri* från Azure.</span><span class="sxs-lookup"><span data-stu-id="cc49c-140">If you do not specify a key, this cmdlet attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

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

### <span data-ttu-id="cc49c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc49c-141">CommonParameters</span></span>
<span data-ttu-id="cc49c-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc49c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc49c-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc49c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc49c-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cc49c-144">INPUTS</span></span>

## <span data-ttu-id="cc49c-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cc49c-145">OUTPUTS</span></span>

## <span data-ttu-id="cc49c-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cc49c-146">NOTES</span></span>

## <span data-ttu-id="cc49c-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cc49c-147">RELATED LINKS</span></span>

[<span data-ttu-id="cc49c-148">Add-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="cc49c-148">Add-AzureRmVhd</span></span>](./Add-AzureRMVhd.md)


