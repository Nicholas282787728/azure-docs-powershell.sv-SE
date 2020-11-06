---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
ms.openlocfilehash: 0641fdf635bce2bbb545e50ecc99a39329fabc9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576369"
---
# <span data-ttu-id="b21cd-101">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b21cd-101">Get-AzureStorageFileContent</span></span>

## <span data-ttu-id="b21cd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b21cd-102">SYNOPSIS</span></span>
<span data-ttu-id="b21cd-103">Laddar ned innehållet i en fil.</span><span class="sxs-lookup"><span data-stu-id="b21cd-103">Downloads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b21cd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b21cd-104">SYNTAX</span></span>

### <span data-ttu-id="b21cd-105">Resurs namn (standard)</span><span class="sxs-lookup"><span data-stu-id="b21cd-105">ShareName (Default)</span></span>
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b21cd-106">Resurserna</span><span class="sxs-lookup"><span data-stu-id="b21cd-106">Share</span></span>
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b21cd-107">Katalogen</span><span class="sxs-lookup"><span data-stu-id="b21cd-107">Directory</span></span>
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b21cd-108">Fil</span><span class="sxs-lookup"><span data-stu-id="b21cd-108">File</span></span>
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b21cd-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b21cd-109">DESCRIPTION</span></span>
<span data-ttu-id="b21cd-110">Cmdleten **Get-AzureStorageFileContent** laddar ned innehållet i en fil och sparar den sedan på en destination som du anger.</span><span class="sxs-lookup"><span data-stu-id="b21cd-110">The **Get-AzureStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="b21cd-111">Denna cmdlet returnerar inte innehållet i filen.</span><span class="sxs-lookup"><span data-stu-id="b21cd-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="b21cd-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b21cd-112">EXAMPLES</span></span>

### <span data-ttu-id="b21cd-113">Exempel 1: Ladda ned en fil från en mapp</span><span class="sxs-lookup"><span data-stu-id="b21cd-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="b21cd-114">Det här kommandot laddar ned en fil med namnet CurrentDataFile i mappen ContosoWorkingFolder från fil resursen ContosoShare06 till den aktuella mappen.</span><span class="sxs-lookup"><span data-stu-id="b21cd-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="b21cd-115">Exempel 2: laddar ned filer under exempel fil resurs</span><span class="sxs-lookup"><span data-stu-id="b21cd-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzureStorageFileContent
```

<span data-ttu-id="b21cd-116">I det här exemplet hämtas filerna under exempel fil resurs</span><span class="sxs-lookup"><span data-stu-id="b21cd-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="b21cd-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b21cd-117">PARAMETERS</span></span>

### <span data-ttu-id="b21cd-118">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="b21cd-118">-CheckMd5</span></span>
<span data-ttu-id="b21cd-119">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="b21cd-119">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="b21cd-120">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="b21cd-120">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="b21cd-121">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="b21cd-121">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="b21cd-122">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="b21cd-122">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="b21cd-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b21cd-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b21cd-124">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="b21cd-124">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="b21cd-125">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="b21cd-125">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="b21cd-126">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="b21cd-126">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="b21cd-127">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="b21cd-127">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="b21cd-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b21cd-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b21cd-129">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="b21cd-129">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="b21cd-130">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="b21cd-130">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="b21cd-131">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="b21cd-131">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="b21cd-132">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="b21cd-132">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="b21cd-133">-Kontext</span><span class="sxs-lookup"><span data-stu-id="b21cd-133">-Context</span></span>
<span data-ttu-id="b21cd-134">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="b21cd-134">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="b21cd-135">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="b21cd-135">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="b21cd-136">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="b21cd-136">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="b21cd-137">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="b21cd-137">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="b21cd-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b21cd-138">-DefaultProfile</span></span>
<span data-ttu-id="b21cd-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b21cd-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b21cd-140">-Mål</span><span class="sxs-lookup"><span data-stu-id="b21cd-140">-Destination</span></span>
<span data-ttu-id="b21cd-141">Anger mål Sök vägen.</span><span class="sxs-lookup"><span data-stu-id="b21cd-141">Specifies the destination path.</span></span>
<span data-ttu-id="b21cd-142">Denna cmdlet laddar ner fil innehållet till den plats som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b21cd-142">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="b21cd-143">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="b21cd-143">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="b21cd-144">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="b21cd-144">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="b21cd-145">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="b21cd-145">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="b21cd-146">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="b21cd-146">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="b21cd-147">-Katalog</span><span class="sxs-lookup"><span data-stu-id="b21cd-147">-Directory</span></span>
<span data-ttu-id="b21cd-148">Anger en mapp som ett **CloudFileDirectory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b21cd-148">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="b21cd-149">Denna cmdlet hämtar innehåll från en fil i den mapp som anges i den här parametern.</span><span class="sxs-lookup"><span data-stu-id="b21cd-149">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="b21cd-150">Använd New-AzureStorageDirectory cmdlet för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="b21cd-150">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="b21cd-151">Du kan också använda Get-AzureStorageFile cmdlet för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="b21cd-151">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="b21cd-152">-Fil</span><span class="sxs-lookup"><span data-stu-id="b21cd-152">-File</span></span>
<span data-ttu-id="b21cd-153">Anger en fil som ett **CloudFile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b21cd-153">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="b21cd-154">Denna cmdlet hämtar filen som parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b21cd-154">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="b21cd-155">För att hämta ett **CloudFile** -objekt, Använd cmdleten Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="b21cd-155">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="b21cd-156">-Force</span><span class="sxs-lookup"><span data-stu-id="b21cd-156">-Force</span></span>
<span data-ttu-id="b21cd-157">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="b21cd-157">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="b21cd-158">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="b21cd-158">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="b21cd-159">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="b21cd-159">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="b21cd-160">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="b21cd-160">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="b21cd-161">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b21cd-161">-PassThru</span></span>
<span data-ttu-id="b21cd-162">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="b21cd-162">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="b21cd-163">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="b21cd-163">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="b21cd-164">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="b21cd-164">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="b21cd-165">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="b21cd-165">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="b21cd-166">-Path</span><span class="sxs-lookup"><span data-stu-id="b21cd-166">-Path</span></span>
<span data-ttu-id="b21cd-167">Anger sökvägen till en fil.</span><span class="sxs-lookup"><span data-stu-id="b21cd-167">Specifies the path of a file.</span></span>
<span data-ttu-id="b21cd-168">Denna cmdlet hämtar innehållet som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b21cd-168">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="b21cd-169">Om filen inte finns returnerar denna cmdlet ett fel.</span><span class="sxs-lookup"><span data-stu-id="b21cd-169">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b21cd-170">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b21cd-170">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b21cd-171">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="b21cd-171">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="b21cd-172">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="b21cd-172">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="b21cd-173">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="b21cd-173">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="b21cd-174">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="b21cd-174">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="b21cd-175">-Dela</span><span class="sxs-lookup"><span data-stu-id="b21cd-175">-Share</span></span>
<span data-ttu-id="b21cd-176">Anger ett **CloudFileShare** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b21cd-176">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="b21cd-177">Denna cmdlet laddar ner innehållet i filen i avsnittet Dela den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b21cd-177">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="b21cd-178">För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="b21cd-178">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="b21cd-179">Det här objektet innehåller lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="b21cd-179">This object contains the storage context.</span></span>
<span data-ttu-id="b21cd-180">Om du anger den här parametern ska du inte ange en *kontext* parameter.</span><span class="sxs-lookup"><span data-stu-id="b21cd-180">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="b21cd-181">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b21cd-181">-ShareName</span></span>
<span data-ttu-id="b21cd-182">Anger namnet på fil resursen.</span><span class="sxs-lookup"><span data-stu-id="b21cd-182">Specifies the name of the file share.</span></span>
<span data-ttu-id="b21cd-183">Denna cmdlet laddar ner innehållet i filen i avsnittet Dela den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b21cd-183">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="b21cd-184">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b21cd-184">-Confirm</span></span>
<span data-ttu-id="b21cd-185">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b21cd-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b21cd-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b21cd-186">-WhatIf</span></span>
<span data-ttu-id="b21cd-187">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b21cd-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b21cd-188">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b21cd-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b21cd-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b21cd-189">CommonParameters</span></span>
<span data-ttu-id="b21cd-190">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b21cd-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b21cd-191">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b21cd-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b21cd-192">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b21cd-192">INPUTS</span></span>

### <span data-ttu-id="b21cd-193">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="b21cd-193">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="b21cd-194">Parametrar: dela (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b21cd-194">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="b21cd-195">Microsoft. WindowsAzure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="b21cd-195">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="b21cd-196">Parametrar: katalog (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b21cd-196">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="b21cd-197">Microsoft. WindowsAzure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="b21cd-197">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="b21cd-198">Parametrar: fil (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b21cd-198">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="b21cd-199">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b21cd-199">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b21cd-200">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b21cd-200">OUTPUTS</span></span>

### <span data-ttu-id="b21cd-201">Microsoft. WindowsAzure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="b21cd-201">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="b21cd-202">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b21cd-202">NOTES</span></span>

## <span data-ttu-id="b21cd-203">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b21cd-203">RELATED LINKS</span></span>

[<span data-ttu-id="b21cd-204">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="b21cd-204">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="b21cd-205">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b21cd-205">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


