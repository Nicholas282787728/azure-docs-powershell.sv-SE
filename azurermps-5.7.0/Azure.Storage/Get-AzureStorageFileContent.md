---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
ms.openlocfilehash: 1dc1e95e2ecf085faad664f624e7595acd9ab607
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577356"
---
# <span data-ttu-id="51d4b-101">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="51d4b-101">Get-AzureStorageFileContent</span></span>

## <span data-ttu-id="51d4b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51d4b-102">SYNOPSIS</span></span>
<span data-ttu-id="51d4b-103">Laddar ned innehållet i en fil.</span><span class="sxs-lookup"><span data-stu-id="51d4b-103">Downloads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51d4b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51d4b-104">SYNTAX</span></span>

### <span data-ttu-id="51d4b-105">Resurs namn (standard)</span><span class="sxs-lookup"><span data-stu-id="51d4b-105">ShareName (Default)</span></span>
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51d4b-106">Resurserna</span><span class="sxs-lookup"><span data-stu-id="51d4b-106">Share</span></span>
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51d4b-107">Katalogen</span><span class="sxs-lookup"><span data-stu-id="51d4b-107">Directory</span></span>
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51d4b-108">Fil</span><span class="sxs-lookup"><span data-stu-id="51d4b-108">File</span></span>
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51d4b-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51d4b-109">DESCRIPTION</span></span>
<span data-ttu-id="51d4b-110">Cmdleten **Get-AzureStorageFileContent** laddar ned innehållet i en fil och sparar den sedan på en destination som du anger.</span><span class="sxs-lookup"><span data-stu-id="51d4b-110">The **Get-AzureStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="51d4b-111">Denna cmdlet returnerar inte innehållet i filen.</span><span class="sxs-lookup"><span data-stu-id="51d4b-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="51d4b-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51d4b-112">EXAMPLES</span></span>

### <span data-ttu-id="51d4b-113">Exempel 1: Ladda ned en fil från en mapp</span><span class="sxs-lookup"><span data-stu-id="51d4b-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="51d4b-114">Det här kommandot laddar ned en fil med namnet CurrentDataFile i mappen ContosoWorkingFolder från fil resursen ContosoShare06 till den aktuella mappen.</span><span class="sxs-lookup"><span data-stu-id="51d4b-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="51d4b-115">Exempel 2: laddar ned filer under exempel fil resurs</span><span class="sxs-lookup"><span data-stu-id="51d4b-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzureStorageFileContent
```

<span data-ttu-id="51d4b-116">I det här exemplet hämtas filerna under exempel fil resurs</span><span class="sxs-lookup"><span data-stu-id="51d4b-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="51d4b-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51d4b-117">PARAMETERS</span></span>

### <span data-ttu-id="51d4b-118">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="51d4b-118">-CheckMd5</span></span>
<span data-ttu-id="51d4b-119">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="51d4b-119">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="51d4b-120">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="51d4b-120">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="51d4b-121">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="51d4b-121">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="51d4b-122">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="51d4b-122">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="51d4b-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="51d4b-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="51d4b-124">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="51d4b-124">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="51d4b-125">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="51d4b-125">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="51d4b-126">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="51d4b-126">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="51d4b-127">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="51d4b-127">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51d4b-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="51d4b-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="51d4b-129">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="51d4b-129">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="51d4b-130">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="51d4b-130">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="51d4b-131">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="51d4b-131">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="51d4b-132">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="51d4b-132">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51d4b-133">-Kontext</span><span class="sxs-lookup"><span data-stu-id="51d4b-133">-Context</span></span>
<span data-ttu-id="51d4b-134">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="51d4b-134">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="51d4b-135">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="51d4b-135">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="51d4b-136">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="51d4b-136">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="51d4b-137">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="51d4b-137">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51d4b-138">-Mål</span><span class="sxs-lookup"><span data-stu-id="51d4b-138">-Destination</span></span>
<span data-ttu-id="51d4b-139">Anger mål Sök vägen.</span><span class="sxs-lookup"><span data-stu-id="51d4b-139">Specifies the destination path.</span></span>
<span data-ttu-id="51d4b-140">Denna cmdlet laddar ner fil innehållet till den plats som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="51d4b-140">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>

<span data-ttu-id="51d4b-141">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="51d4b-141">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="51d4b-142">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="51d4b-142">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="51d4b-143">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="51d4b-143">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="51d4b-144">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="51d4b-144">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51d4b-145">-Katalog</span><span class="sxs-lookup"><span data-stu-id="51d4b-145">-Directory</span></span>
<span data-ttu-id="51d4b-146">Anger en mapp som ett **CloudFileDirectory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="51d4b-146">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="51d4b-147">Denna cmdlet hämtar innehåll från en fil i den mapp som anges i den här parametern.</span><span class="sxs-lookup"><span data-stu-id="51d4b-147">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="51d4b-148">Använd New-AzureStorageDirectory cmdlet för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="51d4b-148">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="51d4b-149">Du kan också använda Get-AzureStorageFile cmdlet för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="51d4b-149">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51d4b-150">-Fil</span><span class="sxs-lookup"><span data-stu-id="51d4b-150">-File</span></span>
<span data-ttu-id="51d4b-151">Anger en fil som ett **CloudFile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="51d4b-151">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="51d4b-152">Denna cmdlet hämtar filen som parametern anger.</span><span class="sxs-lookup"><span data-stu-id="51d4b-152">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="51d4b-153">För att hämta ett **CloudFile** -objekt, Använd cmdleten Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="51d4b-153">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51d4b-154">-Force</span><span class="sxs-lookup"><span data-stu-id="51d4b-154">-Force</span></span>
<span data-ttu-id="51d4b-155">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="51d4b-155">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="51d4b-156">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="51d4b-156">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="51d4b-157">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="51d4b-157">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="51d4b-158">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="51d4b-158">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="51d4b-159">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51d4b-159">-PassThru</span></span>
<span data-ttu-id="51d4b-160">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="51d4b-160">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="51d4b-161">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="51d4b-161">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="51d4b-162">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="51d4b-162">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="51d4b-163">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="51d4b-163">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="51d4b-164">-Path</span><span class="sxs-lookup"><span data-stu-id="51d4b-164">-Path</span></span>
<span data-ttu-id="51d4b-165">Anger sökvägen till en fil.</span><span class="sxs-lookup"><span data-stu-id="51d4b-165">Specifies the path of a file.</span></span>
<span data-ttu-id="51d4b-166">Denna cmdlet hämtar innehållet som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="51d4b-166">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="51d4b-167">Om filen inte finns returnerar denna cmdlet ett fel.</span><span class="sxs-lookup"><span data-stu-id="51d4b-167">If the file does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share, Directory
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51d4b-168">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="51d4b-168">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="51d4b-169">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="51d4b-169">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="51d4b-170">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="51d4b-170">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="51d4b-171">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="51d4b-171">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="51d4b-172">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="51d4b-172">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51d4b-173">-Dela</span><span class="sxs-lookup"><span data-stu-id="51d4b-173">-Share</span></span>
<span data-ttu-id="51d4b-174">Anger ett **CloudFileShare** -objekt.</span><span class="sxs-lookup"><span data-stu-id="51d4b-174">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="51d4b-175">Denna cmdlet laddar ner innehållet i filen i avsnittet Dela den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="51d4b-175">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="51d4b-176">För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="51d4b-176">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="51d4b-177">Det här objektet innehåller lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="51d4b-177">This object contains the storage context.</span></span>
<span data-ttu-id="51d4b-178">Om du anger den här parametern ska du inte ange en *kontext* parameter.</span><span class="sxs-lookup"><span data-stu-id="51d4b-178">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51d4b-179">-ShareName</span><span class="sxs-lookup"><span data-stu-id="51d4b-179">-ShareName</span></span>
<span data-ttu-id="51d4b-180">Anger namnet på fil resursen.</span><span class="sxs-lookup"><span data-stu-id="51d4b-180">Specifies the name of the file share.</span></span>
<span data-ttu-id="51d4b-181">Denna cmdlet laddar ner innehållet i filen i avsnittet Dela den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="51d4b-181">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51d4b-182">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="51d4b-182">-Confirm</span></span>
<span data-ttu-id="51d4b-183">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="51d4b-183">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51d4b-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51d4b-184">-WhatIf</span></span>
<span data-ttu-id="51d4b-185">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="51d4b-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51d4b-186">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="51d4b-186">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51d4b-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51d4b-187">CommonParameters</span></span>
<span data-ttu-id="51d4b-188">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51d4b-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51d4b-189">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51d4b-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51d4b-190">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51d4b-190">INPUTS</span></span>

### <span data-ttu-id="51d4b-191">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="51d4b-191">IStorageContext</span></span>

<span data-ttu-id="51d4b-192">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="51d4b-192">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="51d4b-193">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="51d4b-193">CloudFileDirectory</span></span>

<span data-ttu-id="51d4b-194">Parametern ' Directory ' godkänner värdet av typen ' CloudFileDirectory ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="51d4b-194">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="51d4b-195">CloudFile</span><span class="sxs-lookup"><span data-stu-id="51d4b-195">CloudFile</span></span>

<span data-ttu-id="51d4b-196">Parametern ' File ' godkänner värdet för typen ' CloudFile ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="51d4b-196">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

### <span data-ttu-id="51d4b-197">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="51d4b-197">CloudFileShare</span></span>

<span data-ttu-id="51d4b-198">Parametern ' Share ' godkänner värdet av typen ' CloudFileShare ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="51d4b-198">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="51d4b-199">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51d4b-199">OUTPUTS</span></span>

## <span data-ttu-id="51d4b-200">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51d4b-200">NOTES</span></span>

## <span data-ttu-id="51d4b-201">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51d4b-201">RELATED LINKS</span></span>

[<span data-ttu-id="51d4b-202">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="51d4b-202">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="51d4b-203">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="51d4b-203">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


