---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvhd
schema: 2.0.0
ms.openlocfilehash: 3c8efdc640ec3cee4cd3d0a8eaf2a63f5832c918
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929525"
---
# <span data-ttu-id="a3503-101">Add-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="a3503-101">Add-AzureRmVhd</span></span>

## <span data-ttu-id="a3503-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a3503-102">SYNOPSIS</span></span>
<span data-ttu-id="a3503-103">Uppladdar en virtuell hård disk från en lokal virtuell dator till en BLOB i ett moln lagrings konto i Azure.</span><span class="sxs-lookup"><span data-stu-id="a3503-103">Uploads a virtual hard disk from an on-premises virtual machine to a blob in a cloud storage account in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3503-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a3503-104">SYNTAX</span></span>

```
Add-AzureRmVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3503-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a3503-105">DESCRIPTION</span></span>
<span data-ttu-id="a3503-106">Cmdleten **Add-AzureRmVhd** laddar upp lokala virtuella hård diskar i VHD-format till ett BLOB-lagringssystem som fasta virtuella hård diskar.</span><span class="sxs-lookup"><span data-stu-id="a3503-106">The **Add-AzureRmVhd** cmdlet uploads on-premises virtual hard disks, in .vhd file format, to a blob storage account as fixed virtual hard disks.</span></span>
<span data-ttu-id="a3503-107">Du kan konfigurera hur många överförings trådar som ska användas eller skriva över en befintlig BLOB i angiven mål-URI.</span><span class="sxs-lookup"><span data-stu-id="a3503-107">You can configure the number of uploader threads that will be used or overwrite an existing blob in the specified destination URI.</span></span>
<span data-ttu-id="a3503-108">Dessutom kan du ladda upp en uppdaterad version av en lokal. VHD-fil.</span><span class="sxs-lookup"><span data-stu-id="a3503-108">Also supported is the ability to upload a patched version of an on-premises .vhd file.</span></span>
<span data-ttu-id="a3503-109">När en virtuell hård disk har laddats upp kan du ladda upp differentierings diskar som använder bas bilden som överordnad.</span><span class="sxs-lookup"><span data-stu-id="a3503-109">When a base virtual hard disk has already been uploaded, you can upload differencing disks that use the base image as the parent.</span></span>
<span data-ttu-id="a3503-110">URL för delad åtkomst till en signatur (SAS) stöds också.</span><span class="sxs-lookup"><span data-stu-id="a3503-110">Shared access signature (SAS) URI is supported also.</span></span>

## <span data-ttu-id="a3503-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a3503-111">EXAMPLES</span></span>

### <span data-ttu-id="a3503-112">Exempel 1: lägga till en VHD-fil</span><span class="sxs-lookup"><span data-stu-id="a3503-112">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="a3503-113">Det här kommandot lägger till en VHD-fil till ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="a3503-113">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="a3503-114">Exempel 2: Lägg till en VHD-fil och skriv över mål platsen</span><span class="sxs-lookup"><span data-stu-id="a3503-114">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="a3503-115">Det här kommandot lägger till en VHD-fil till ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="a3503-115">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="a3503-116">Kommandot skriver över en befintlig fil.</span><span class="sxs-lookup"><span data-stu-id="a3503-116">The command overwrites an existing file.</span></span>

### <span data-ttu-id="a3503-117">Exempel 3: lägga till en VHD-fil och ange antalet trådar</span><span class="sxs-lookup"><span data-stu-id="a3503-117">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

<span data-ttu-id="a3503-118">Det här kommandot lägger till en VHD-fil till ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="a3503-118">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="a3503-119">Kommandot anger antalet trådar som ska användas för att överföra filen.</span><span class="sxs-lookup"><span data-stu-id="a3503-119">The command specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="a3503-120">Exempel 4: Lägg till en VHD-fil och ange SAS URI</span><span class="sxs-lookup"><span data-stu-id="a3503-120">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="a3503-121">Det här kommandot lägger till en. VHD-fil till ett lagrings konto och anger SAS URI.</span><span class="sxs-lookup"><span data-stu-id="a3503-121">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="a3503-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a3503-122">PARAMETERS</span></span>

### <span data-ttu-id="a3503-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3503-123">-AsJob</span></span>
<span data-ttu-id="a3503-124">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="a3503-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a3503-125">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="a3503-125">-BaseImageUriToPatch</span></span>
<span data-ttu-id="a3503-126">Anger URI till en bas avbildnings-BLOB i Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="a3503-126">Specifies the URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="a3503-127">En SAS-säkerhetsassociationer kan anges som värde för den här parametern.</span><span class="sxs-lookup"><span data-stu-id="a3503-127">An SAS can be specified as the value for this parameter.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3503-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3503-128">-DefaultProfile</span></span>
<span data-ttu-id="a3503-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a3503-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3503-130">-Mål</span><span class="sxs-lookup"><span data-stu-id="a3503-130">-Destination</span></span>
<span data-ttu-id="a3503-131">Anger URI för en BLOB i Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="a3503-131">Specifies the URI of a blob in Blob Storage.</span></span>
<span data-ttu-id="a3503-132">Parametern har stöd för SAS URI, men mål för korrigerings scenarier kan inte vara en SAS URI.</span><span class="sxs-lookup"><span data-stu-id="a3503-132">The parameter supports SAS URI, although patching scenarios destination cannot be an SAS URI.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3503-133">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="a3503-133">-LocalFilePath</span></span>
<span data-ttu-id="a3503-134">Anger sökvägen till den lokala VHD-filen.</span><span class="sxs-lookup"><span data-stu-id="a3503-134">Specifies the path of the local .vhd file.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3503-135">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="a3503-135">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="a3503-136">Anger antalet överförings trådar som ska användas när VHD-filen överförs.</span><span class="sxs-lookup"><span data-stu-id="a3503-136">Specifies the number of uploader threads to be used when uploading the .vhd file.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3503-137">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="a3503-137">-OverWrite</span></span>
<span data-ttu-id="a3503-138">Anger att denna cmdlet skriver över en befintlig BLOB i angiven mål-URI, om en sådan finns.</span><span class="sxs-lookup"><span data-stu-id="a3503-138">Indicates that this cmdlet overwrites an existing blob in the specified destination URI, if one exists.</span></span>

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

### <span data-ttu-id="a3503-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3503-139">-ResourceGroupName</span></span>
<span data-ttu-id="a3503-140">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a3503-140">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3503-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3503-141">CommonParameters</span></span>
<span data-ttu-id="a3503-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3503-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3503-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3503-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3503-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a3503-144">INPUTS</span></span>

### <span data-ttu-id="a3503-145">Ingen</span><span class="sxs-lookup"><span data-stu-id="a3503-145">None</span></span>
<span data-ttu-id="a3503-146">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="a3503-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a3503-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a3503-147">OUTPUTS</span></span>

### <span data-ttu-id="a3503-148">Microsoft. Azure. commands. Compute. Models. VhdUploadContext</span><span class="sxs-lookup"><span data-stu-id="a3503-148">Microsoft.Azure.Commands.Compute.Models.VhdUploadContext</span></span>

## <span data-ttu-id="a3503-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a3503-149">NOTES</span></span>

## <span data-ttu-id="a3503-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a3503-150">RELATED LINKS</span></span>

[<span data-ttu-id="a3503-151">Spara – AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="a3503-151">Save-AzureRmVhd</span></span>](./Save-AzureRmVhd.md)


