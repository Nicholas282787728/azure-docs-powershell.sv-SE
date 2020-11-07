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
# <span data-ttu-id="7892a-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7892a-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="7892a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7892a-102">SYNOPSIS</span></span>
<span data-ttu-id="7892a-103">Laddar ned innehållet i en fil.</span><span class="sxs-lookup"><span data-stu-id="7892a-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="7892a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7892a-104">SYNTAX</span></span>

### <span data-ttu-id="7892a-105">Resurs namn (standard)</span><span class="sxs-lookup"><span data-stu-id="7892a-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7892a-106">Resurserna</span><span class="sxs-lookup"><span data-stu-id="7892a-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7892a-107">Katalogen</span><span class="sxs-lookup"><span data-stu-id="7892a-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7892a-108">Fil</span><span class="sxs-lookup"><span data-stu-id="7892a-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7892a-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7892a-109">DESCRIPTION</span></span>
<span data-ttu-id="7892a-110">Cmdleten **Get-AzStorageFileContent** laddar ned innehållet i en fil och sparar den sedan på en destination som du anger.</span><span class="sxs-lookup"><span data-stu-id="7892a-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="7892a-111">Denna cmdlet returnerar inte innehållet i filen.</span><span class="sxs-lookup"><span data-stu-id="7892a-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="7892a-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7892a-112">EXAMPLES</span></span>

### <span data-ttu-id="7892a-113">Exempel 1: Ladda ned en fil från en mapp</span><span class="sxs-lookup"><span data-stu-id="7892a-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="7892a-114">Det här kommandot laddar ned en fil med namnet CurrentDataFile i mappen ContosoWorkingFolder från fil resursen ContosoShare06 till den aktuella mappen.</span><span class="sxs-lookup"><span data-stu-id="7892a-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="7892a-115">Exempel 2: laddar ned filer under exempel fil resurs</span><span class="sxs-lookup"><span data-stu-id="7892a-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="7892a-116">I det här exemplet hämtas filerna under exempel fil resurs</span><span class="sxs-lookup"><span data-stu-id="7892a-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="7892a-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7892a-117">PARAMETERS</span></span>

### <span data-ttu-id="7892a-118">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="7892a-118">-CheckMd5</span></span>
<span data-ttu-id="7892a-119">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="7892a-119">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="7892a-120">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="7892a-120">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="7892a-121">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="7892a-121">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="7892a-122">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="7892a-122">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="7892a-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7892a-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7892a-124">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="7892a-124">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="7892a-125">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="7892a-125">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="7892a-126">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="7892a-126">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="7892a-127">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="7892a-127">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="7892a-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7892a-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7892a-129">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="7892a-129">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="7892a-130">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="7892a-130">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="7892a-131">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="7892a-131">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="7892a-132">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="7892a-132">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="7892a-133">-Kontext</span><span class="sxs-lookup"><span data-stu-id="7892a-133">-Context</span></span>
<span data-ttu-id="7892a-134">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="7892a-134">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="7892a-135">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="7892a-135">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="7892a-136">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="7892a-136">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="7892a-137">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="7892a-137">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="7892a-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7892a-138">-DefaultProfile</span></span>
<span data-ttu-id="7892a-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7892a-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7892a-140">-Mål</span><span class="sxs-lookup"><span data-stu-id="7892a-140">-Destination</span></span>
<span data-ttu-id="7892a-141">Anger mål Sök vägen.</span><span class="sxs-lookup"><span data-stu-id="7892a-141">Specifies the destination path.</span></span>
<span data-ttu-id="7892a-142">Denna cmdlet laddar ner fil innehållet till den plats som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="7892a-142">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="7892a-143">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="7892a-143">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="7892a-144">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="7892a-144">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="7892a-145">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="7892a-145">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="7892a-146">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="7892a-146">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="7892a-147">-Katalog</span><span class="sxs-lookup"><span data-stu-id="7892a-147">-Directory</span></span>
<span data-ttu-id="7892a-148">Anger en mapp som ett **CloudFileDirectory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="7892a-148">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="7892a-149">Denna cmdlet hämtar innehåll från en fil i den mapp som anges i den här parametern.</span><span class="sxs-lookup"><span data-stu-id="7892a-149">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="7892a-150">Använd New-AzStorageDirectory cmdlet för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="7892a-150">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="7892a-151">Du kan också använda Get-AzStorageFile cmdlet för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="7892a-151">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="7892a-152">-Fil</span><span class="sxs-lookup"><span data-stu-id="7892a-152">-File</span></span>
<span data-ttu-id="7892a-153">Anger en fil som ett **CloudFile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="7892a-153">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="7892a-154">Denna cmdlet hämtar filen som parametern anger.</span><span class="sxs-lookup"><span data-stu-id="7892a-154">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="7892a-155">För att hämta ett **CloudFile** -objekt, Använd cmdleten Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="7892a-155">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="7892a-156">-Force</span><span class="sxs-lookup"><span data-stu-id="7892a-156">-Force</span></span>
<span data-ttu-id="7892a-157">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="7892a-157">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="7892a-158">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="7892a-158">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="7892a-159">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="7892a-159">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="7892a-160">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="7892a-160">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="7892a-161">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7892a-161">-PassThru</span></span>
<span data-ttu-id="7892a-162">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="7892a-162">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="7892a-163">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="7892a-163">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="7892a-164">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="7892a-164">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="7892a-165">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="7892a-165">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="7892a-166">-Path</span><span class="sxs-lookup"><span data-stu-id="7892a-166">-Path</span></span>
<span data-ttu-id="7892a-167">Anger sökvägen till en fil.</span><span class="sxs-lookup"><span data-stu-id="7892a-167">Specifies the path of a file.</span></span>
<span data-ttu-id="7892a-168">Denna cmdlet hämtar innehållet som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="7892a-168">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="7892a-169">Om filen inte finns returnerar denna cmdlet ett fel.</span><span class="sxs-lookup"><span data-stu-id="7892a-169">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7892a-170">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7892a-170">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7892a-171">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="7892a-171">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="7892a-172">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="7892a-172">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="7892a-173">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="7892a-173">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="7892a-174">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="7892a-174">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="7892a-175">-Dela</span><span class="sxs-lookup"><span data-stu-id="7892a-175">-Share</span></span>
<span data-ttu-id="7892a-176">Anger ett **CloudFileShare** -objekt.</span><span class="sxs-lookup"><span data-stu-id="7892a-176">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="7892a-177">Denna cmdlet laddar ner innehållet i filen i avsnittet Dela den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="7892a-177">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="7892a-178">För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="7892a-178">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="7892a-179">Det här objektet innehåller lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="7892a-179">This object contains the storage context.</span></span>
<span data-ttu-id="7892a-180">Om du anger den här parametern ska du inte ange en *kontext* parameter.</span><span class="sxs-lookup"><span data-stu-id="7892a-180">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="7892a-181">-ShareName</span><span class="sxs-lookup"><span data-stu-id="7892a-181">-ShareName</span></span>
<span data-ttu-id="7892a-182">Anger namnet på fil resursen.</span><span class="sxs-lookup"><span data-stu-id="7892a-182">Specifies the name of the file share.</span></span>
<span data-ttu-id="7892a-183">Denna cmdlet laddar ner innehållet i filen i avsnittet Dela den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="7892a-183">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="7892a-184">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7892a-184">-Confirm</span></span>
<span data-ttu-id="7892a-185">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7892a-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7892a-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7892a-186">-WhatIf</span></span>
<span data-ttu-id="7892a-187">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7892a-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7892a-188">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7892a-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7892a-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7892a-189">CommonParameters</span></span>
<span data-ttu-id="7892a-190">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7892a-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7892a-191">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7892a-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7892a-192">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7892a-192">INPUTS</span></span>

### <span data-ttu-id="7892a-193">Microsoft. WindowsAz. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="7892a-193">Microsoft.WindowsAz.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="7892a-194">Parametrar: dela (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7892a-194">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="7892a-195">Microsoft. WindowsAz. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="7892a-195">Microsoft.WindowsAz.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="7892a-196">Parametrar: katalog (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7892a-196">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="7892a-197">Microsoft. WindowsAz. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="7892a-197">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>
<span data-ttu-id="7892a-198">Parametrar: fil (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7892a-198">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="7892a-199">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7892a-199">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7892a-200">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7892a-200">OUTPUTS</span></span>

### <span data-ttu-id="7892a-201">Microsoft. WindowsAz. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="7892a-201">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>

## <span data-ttu-id="7892a-202">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7892a-202">NOTES</span></span>

## <span data-ttu-id="7892a-203">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7892a-203">RELATED LINKS</span></span>

[<span data-ttu-id="7892a-204">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="7892a-204">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="7892a-205">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7892a-205">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


