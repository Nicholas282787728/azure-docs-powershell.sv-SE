---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 99DC239C-EA68-4830-9345-762CD6A3F68C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 320b95add2806f48121151a71bdf36a572fa05a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093444"
---
# <span data-ttu-id="69a47-101">Add-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="69a47-101">Add-AzureVhd</span></span>

## <span data-ttu-id="69a47-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="69a47-102">SYNOPSIS</span></span>
<span data-ttu-id="69a47-103">Laddar upp en VHD-fil från en lokal dator till en BLOB i ett moln lagrings konto i Azure.</span><span class="sxs-lookup"><span data-stu-id="69a47-103">Uploads a VHD file from an on-premise computer to a blob in a cloud storage account in Azure.</span></span>

## <span data-ttu-id="69a47-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="69a47-104">SYNTAX</span></span>

```
Add-AzureVhd [-Destination] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfUploaderThreads] <Int32>]
 [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="69a47-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="69a47-105">DESCRIPTION</span></span>
<span data-ttu-id="69a47-106">Cmdleten **Add-AzureVhd** för den lokala VHD-avbildningen till ett Blob Storage-konto som åtgärdade VHD-bilder.</span><span class="sxs-lookup"><span data-stu-id="69a47-106">The **Add-AzureVhd** cmdlet uploads on premise Virtual hard disk (VHD) images to a blob storage account as fixed .vhd images.</span></span>
<span data-ttu-id="69a47-107">Den har parametrar för att konfigurera uppladdnings processen, till exempel hur många överförings trådar som ska användas eller för att skriva över en blob som redan finns i angiven mål-URI.</span><span class="sxs-lookup"><span data-stu-id="69a47-107">It has parameters to configure the upload process such as specifying the number of uploader threads that will be used or overwriting a blob which already exists in the specified destination URI.</span></span>
<span data-ttu-id="69a47-108">För lokala VHD-avbildningar stöds också korrigerings scenario så att differentiering av disk bilder kan laddas upp utan att du behöver ladda upp dem som redan har laddats upp.</span><span class="sxs-lookup"><span data-stu-id="69a47-108">For on premise VHD images, patching scenario is also supported so that diff disk images can be uploaded without having to upload the already uploaded base images.</span></span> <span data-ttu-id="69a47-109">Signaturen för delad åtkomst (SAS) stöds också.</span><span class="sxs-lookup"><span data-stu-id="69a47-109">Shared Access Signature (SAS) URI is also supported.</span></span>

## <span data-ttu-id="69a47-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="69a47-110">EXAMPLES</span></span>

### <span data-ttu-id="69a47-111">Exempel 1: lägga till en VHD-fil</span><span class="sxs-lookup"><span data-stu-id="69a47-111">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="69a47-112">Det här kommandot lägger till en VHD-fil till ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="69a47-112">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="69a47-113">Exempel 2: Lägg till en VHD-fil och skriv över mål platsen</span><span class="sxs-lookup"><span data-stu-id="69a47-113">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="69a47-114">Det här kommandot lägger till en VHD-fil till ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="69a47-114">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="69a47-115">Exempel 3: lägga till en VHD-fil och ange antalet trådar</span><span class="sxs-lookup"><span data-stu-id="69a47-115">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="69a47-116">Det här kommandot lägger till en. VHD-fil till ett lagrings konto och anger antalet trådar som ska användas för att överföra filen.</span><span class="sxs-lookup"><span data-stu-id="69a47-116">This command adds a .vhd file to a storage account and specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="69a47-117">Exempel 4: Lägg till en VHD-fil och ange SAS URI</span><span class="sxs-lookup"><span data-stu-id="69a47-117">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01-09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveOSIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="69a47-118">Det här kommandot lägger till en. VHD-fil till ett lagrings konto och anger SAS URI.</span><span class="sxs-lookup"><span data-stu-id="69a47-118">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="69a47-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="69a47-119">PARAMETERS</span></span>

### <span data-ttu-id="69a47-120">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="69a47-120">-BaseImageUriToPatch</span></span>
<span data-ttu-id="69a47-121">Anger en URI till en bas avbildnings-BLOB i Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="69a47-121">Specifies an URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="69a47-122">SAS i URI-inmatning stöds också.</span><span class="sxs-lookup"><span data-stu-id="69a47-122">SAS in URI input is supported as well.</span></span>

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

### <span data-ttu-id="69a47-123">-Mål</span><span class="sxs-lookup"><span data-stu-id="69a47-123">-Destination</span></span>
<span data-ttu-id="69a47-124">Anger en URI till en BLOB i Microsoft Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="69a47-124">Specifies a URI to a blob in Microsoft Azure Blob Storage.</span></span>
<span data-ttu-id="69a47-125">SAS i URI-indata stöds.</span><span class="sxs-lookup"><span data-stu-id="69a47-125">SAS in URI input is supported.</span></span>
<span data-ttu-id="69a47-126">I korrigerings scenarier kan destinationen emellertid inte vara en SAS URI.</span><span class="sxs-lookup"><span data-stu-id="69a47-126">However, in patching scenarios the destination cannot be a SAS URI.</span></span>

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

### <span data-ttu-id="69a47-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="69a47-127">-InformationAction</span></span>
<span data-ttu-id="69a47-128">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="69a47-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="69a47-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="69a47-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="69a47-130">Vidare</span><span class="sxs-lookup"><span data-stu-id="69a47-130">Continue</span></span>
- <span data-ttu-id="69a47-131">Över</span><span class="sxs-lookup"><span data-stu-id="69a47-131">Ignore</span></span>
- <span data-ttu-id="69a47-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="69a47-132">Inquire</span></span>
- <span data-ttu-id="69a47-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="69a47-133">SilentlyContinue</span></span>
- <span data-ttu-id="69a47-134">Stanna</span><span class="sxs-lookup"><span data-stu-id="69a47-134">Stop</span></span>
- <span data-ttu-id="69a47-135">Avbryt</span><span class="sxs-lookup"><span data-stu-id="69a47-135">Suspend</span></span>

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

### <span data-ttu-id="69a47-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="69a47-136">-InformationVariable</span></span>
<span data-ttu-id="69a47-137">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="69a47-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="69a47-138">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="69a47-138">-LocalFilePath</span></span>
<span data-ttu-id="69a47-139">Den lokala VHD-filens fil Sök väg.</span><span class="sxs-lookup"><span data-stu-id="69a47-139">Species the file path of the local .vhd file.</span></span>

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

### <span data-ttu-id="69a47-140">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="69a47-140">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="69a47-141">Anger antalet trådar som ska laddas upp.</span><span class="sxs-lookup"><span data-stu-id="69a47-141">Specifies the number of threads to use for upload.</span></span>

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

### <span data-ttu-id="69a47-142">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="69a47-142">-OverWrite</span></span>
<span data-ttu-id="69a47-143">Anger att den här cmdleten tar bort den befintliga blobben i angiven mål-URI om den finns.</span><span class="sxs-lookup"><span data-stu-id="69a47-143">Specifies that this cmdlet deletes the existing blob in the specified destination URI if it exists.</span></span>

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

### <span data-ttu-id="69a47-144">-Profil</span><span class="sxs-lookup"><span data-stu-id="69a47-144">-Profile</span></span>
<span data-ttu-id="69a47-145">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="69a47-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="69a47-146">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="69a47-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="69a47-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69a47-147">CommonParameters</span></span>
<span data-ttu-id="69a47-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69a47-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69a47-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69a47-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69a47-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="69a47-150">INPUTS</span></span>

## <span data-ttu-id="69a47-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="69a47-151">OUTPUTS</span></span>

## <span data-ttu-id="69a47-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="69a47-152">NOTES</span></span>

## <span data-ttu-id="69a47-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="69a47-153">RELATED LINKS</span></span>

[<span data-ttu-id="69a47-154">Spara – AzureVhd</span><span class="sxs-lookup"><span data-stu-id="69a47-154">Save-AzureVhd</span></span>](./Save-AzureVhd.md)


