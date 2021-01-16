---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 3c90e02194fa761bbb0fc00e11ea09d03ca00c1c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404211"
---
# <span data-ttu-id="bef35-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bef35-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="bef35-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bef35-102">SYNOPSIS</span></span>
<span data-ttu-id="bef35-103">Laddar ned innehållet i en fil.</span><span class="sxs-lookup"><span data-stu-id="bef35-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="bef35-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bef35-104">SYNTAX</span></span>

### <span data-ttu-id="bef35-105">Resurs namn (standard)</span><span class="sxs-lookup"><span data-stu-id="bef35-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="bef35-106">Resurserna</span><span class="sxs-lookup"><span data-stu-id="bef35-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="bef35-107">Katalogen</span><span class="sxs-lookup"><span data-stu-id="bef35-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="bef35-108">Fil</span><span class="sxs-lookup"><span data-stu-id="bef35-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="bef35-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bef35-109">DESCRIPTION</span></span>
<span data-ttu-id="bef35-110">Cmdleten **Get-AzStorageFileContent** laddar ned innehållet i en fil och sparar den sedan på en destination som du anger.</span><span class="sxs-lookup"><span data-stu-id="bef35-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="bef35-111">Denna cmdlet returnerar inte innehållet i filen.</span><span class="sxs-lookup"><span data-stu-id="bef35-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="bef35-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bef35-112">EXAMPLES</span></span>

### <span data-ttu-id="bef35-113">Exempel 1: Ladda ned en fil från en mapp</span><span class="sxs-lookup"><span data-stu-id="bef35-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="bef35-114">Det här kommandot laddar ned en fil med namnet CurrentDataFile i mappen ContosoWorkingFolder från fil resursen ContosoShare06 till den aktuella mappen.</span><span class="sxs-lookup"><span data-stu-id="bef35-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="bef35-115">Exempel 2: laddar ned filer under exempel fil resurs</span><span class="sxs-lookup"><span data-stu-id="bef35-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="bef35-116">I det här exemplet hämtas filerna under exempel fil resurs</span><span class="sxs-lookup"><span data-stu-id="bef35-116">This example downloads the files under sample file share</span></span>

### <span data-ttu-id="bef35-117">Exempel 3: Ladda ned en Azure-fil till en lokal fil och perserve Azure-filen SMB-egenskaper (fil Attributtes, fil skapande tid, senaste skrivnings tid) i den lokala filen.</span><span class="sxs-lookup"><span data-stu-id="bef35-117">Example 3: Download an Azure file to a local file, and perserve the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName sample -Path "dir1/file1" -Destination $localFilePath -PreserveSMBAttribute
```

<span data-ttu-id="bef35-118">I det här exemplet hämtas en Azure-fil till en lokal fil och perserves Azure-filens SMB-egenskaper (fil Attributtes, fil skapande tid, senaste skrivnings tid) i den lokala filen.</span><span class="sxs-lookup"><span data-stu-id="bef35-118">This example downloads an Azure file to a local file, and perserves the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>

## <span data-ttu-id="bef35-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bef35-119">PARAMETERS</span></span>

### <span data-ttu-id="bef35-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bef35-120">-AsJob</span></span>
<span data-ttu-id="bef35-121">Kör cmdleten i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="bef35-121">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="bef35-122">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="bef35-122">-CheckMd5</span></span>
<span data-ttu-id="bef35-123">Anger om Md5-summan för den hämtade filen ska kontrol leras.</span><span class="sxs-lookup"><span data-stu-id="bef35-123">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="bef35-124">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bef35-124">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bef35-125">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="bef35-125">Specifies the client-side time-out interval, in seconds, for one service request.</span></span> <span data-ttu-id="bef35-126">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="bef35-126">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span> <span data-ttu-id="bef35-127">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="bef35-127">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bef35-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bef35-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bef35-129">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="bef35-129">Specifies the maximum concurrent network calls.</span></span> <span data-ttu-id="bef35-130">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="bef35-130">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span> <span data-ttu-id="bef35-131">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="bef35-131">The specified value is an absolute count and is not multiplied by the core count.</span></span> <span data-ttu-id="bef35-132">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="bef35-132">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span> <span data-ttu-id="bef35-133">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="bef35-133">The default value is 10.</span></span>

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

### <span data-ttu-id="bef35-134">-Kontext</span><span class="sxs-lookup"><span data-stu-id="bef35-134">-Context</span></span>
<span data-ttu-id="bef35-135">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="bef35-135">Specifies an Azure Storage context.</span></span> <span data-ttu-id="bef35-136">Använd New-AzStorageContext cmdlet för att få en kontext.</span><span class="sxs-lookup"><span data-stu-id="bef35-136">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="bef35-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bef35-137">-DefaultProfile</span></span>
<span data-ttu-id="bef35-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bef35-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bef35-139">-Mål</span><span class="sxs-lookup"><span data-stu-id="bef35-139">-Destination</span></span>
<span data-ttu-id="bef35-140">Anger mål Sök vägen.</span><span class="sxs-lookup"><span data-stu-id="bef35-140">Specifies the destination path.</span></span>
<span data-ttu-id="bef35-141">Denna cmdlet laddar ner fil innehållet till den plats som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="bef35-141">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="bef35-142">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="bef35-142">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="bef35-143">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="bef35-143">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="bef35-144">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="bef35-144">If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="bef35-145">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="bef35-145">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="bef35-146">-Katalog</span><span class="sxs-lookup"><span data-stu-id="bef35-146">-Directory</span></span>
<span data-ttu-id="bef35-147">Anger en mapp som ett **CloudFileDirectory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="bef35-147">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="bef35-148">Denna cmdlet hämtar innehåll från en fil i den mapp som anges i den här parametern.</span><span class="sxs-lookup"><span data-stu-id="bef35-148">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="bef35-149">Använd New-AzStorageDirectory cmdlet för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="bef35-149">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="bef35-150">Du kan också använda Get-AzStorageFile cmdlet för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="bef35-150">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bef35-151">-Fil</span><span class="sxs-lookup"><span data-stu-id="bef35-151">-File</span></span>
<span data-ttu-id="bef35-152">Anger en fil som ett **CloudFile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="bef35-152">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="bef35-153">Denna cmdlet hämtar filen som parametern anger.</span><span class="sxs-lookup"><span data-stu-id="bef35-153">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="bef35-154">För att hämta ett **CloudFile** -objekt, Använd cmdleten Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="bef35-154">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bef35-155">-Force</span><span class="sxs-lookup"><span data-stu-id="bef35-155">-Force</span></span>
<span data-ttu-id="bef35-156">Om du anger sökvägen till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i den nya filen.</span><span class="sxs-lookup"><span data-stu-id="bef35-156">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="bef35-157">Om du anger en sökväg till en fil som redan finns och du anger parametern *Force* skrivs filen över.</span><span class="sxs-lookup"><span data-stu-id="bef35-157">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="bef35-158">Om du anger en sökväg till en befintlig fil och inte anger *tvinga* visas en uppmaning innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="bef35-158">If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="bef35-159">Om du anger sökvägen till en mapp försöker denna cmdlet att skapa en fil med namnet på Azure Storage-filen.</span><span class="sxs-lookup"><span data-stu-id="bef35-159">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="bef35-160">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bef35-160">-PassThru</span></span>
<span data-ttu-id="bef35-161">Anger att den här cmdleten returnerar **AzureStorageFile** -objektet som hämtas.</span><span class="sxs-lookup"><span data-stu-id="bef35-161">Indicates that this cmdlet returns the **AzureStorageFile** object that it downloads.</span></span>

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

### <span data-ttu-id="bef35-162">-Path</span><span class="sxs-lookup"><span data-stu-id="bef35-162">-Path</span></span>
<span data-ttu-id="bef35-163">Anger sökvägen till en fil.</span><span class="sxs-lookup"><span data-stu-id="bef35-163">Specifies the path of a file.</span></span>
<span data-ttu-id="bef35-164">Denna cmdlet hämtar innehållet som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="bef35-164">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="bef35-165">Om filen inte finns returnerar denna cmdlet ett fel.</span><span class="sxs-lookup"><span data-stu-id="bef35-165">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="bef35-166">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="bef35-166">-PreserveSMBAttribute</span></span>
<span data-ttu-id="bef35-167">Behåll käll filens SMB-egenskaper (fil Attributtes, fil skapande tid, senaste skrivnings tid) i målfil.</span><span class="sxs-lookup"><span data-stu-id="bef35-167">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="bef35-168">Denna parameter är endast tillgänglig i Windows.</span><span class="sxs-lookup"><span data-stu-id="bef35-168">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="bef35-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bef35-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bef35-170">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="bef35-170">Specifies the service side time-out interval, in seconds, for a request.</span></span> <span data-ttu-id="bef35-171">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="bef35-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bef35-172">-Dela</span><span class="sxs-lookup"><span data-stu-id="bef35-172">-Share</span></span>
<span data-ttu-id="bef35-173">Anger ett **CloudFileShare** -objekt.</span><span class="sxs-lookup"><span data-stu-id="bef35-173">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="bef35-174">Denna cmdlet laddar ner innehållet i filen i avsnittet Dela den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="bef35-174">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="bef35-175">För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="bef35-175">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="bef35-176">Det här objektet innehåller lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="bef35-176">This object contains the storage context.</span></span>
<span data-ttu-id="bef35-177">Om du anger den här parametern ska du inte ange en *kontext* parameter.</span><span class="sxs-lookup"><span data-stu-id="bef35-177">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bef35-178">-ShareName</span><span class="sxs-lookup"><span data-stu-id="bef35-178">-ShareName</span></span>
<span data-ttu-id="bef35-179">Anger namnet på fil resursen.</span><span class="sxs-lookup"><span data-stu-id="bef35-179">Specifies the name of the file share.</span></span>
<span data-ttu-id="bef35-180">Denna cmdlet laddar ner innehållet i filen i avsnittet Dela den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="bef35-180">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="bef35-181">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bef35-181">-Confirm</span></span>
<span data-ttu-id="bef35-182">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bef35-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bef35-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bef35-183">-WhatIf</span></span>
<span data-ttu-id="bef35-184">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bef35-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bef35-185">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bef35-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bef35-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bef35-186">CommonParameters</span></span>
<span data-ttu-id="bef35-187">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bef35-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bef35-188">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bef35-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bef35-189">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bef35-189">INPUTS</span></span>

### <span data-ttu-id="bef35-190">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="bef35-190">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="bef35-191">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="bef35-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="bef35-192">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="bef35-192">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="bef35-193">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bef35-193">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bef35-194">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bef35-194">OUTPUTS</span></span>

### <span data-ttu-id="bef35-195">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="bef35-195">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="bef35-196">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bef35-196">NOTES</span></span>

## <span data-ttu-id="bef35-197">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bef35-197">RELATED LINKS</span></span>

[<span data-ttu-id="bef35-198">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="bef35-198">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="bef35-199">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bef35-199">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


