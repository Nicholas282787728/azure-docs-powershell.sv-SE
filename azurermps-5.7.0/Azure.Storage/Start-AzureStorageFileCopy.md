---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/start-azurestoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageFileCopy.md
ms.openlocfilehash: 47129dfd409ad72aa250ed78ce4b61d1463b9390
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586452"
---
# <span data-ttu-id="2206d-101">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2206d-101">Start-AzureStorageFileCopy</span></span>

## <span data-ttu-id="2206d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2206d-102">SYNOPSIS</span></span>
<span data-ttu-id="2206d-103">Kopierar en källfil.</span><span class="sxs-lookup"><span data-stu-id="2206d-103">Starts to copy a source file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2206d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2206d-104">SYNTAX</span></span>

### <span data-ttu-id="2206d-105">Hålla</span><span class="sxs-lookup"><span data-stu-id="2206d-105">ContainerName</span></span>
```
Start-AzureStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2206d-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2206d-106">ContainerInstance</span></span>
```
Start-AzureStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2206d-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="2206d-107">BlobInstanceFilePath</span></span>
```
Start-AzureStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2206d-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="2206d-108">BlobInstanceFileInstance</span></span>
```
Start-AzureStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2206d-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="2206d-109">ShareName</span></span>
```
Start-AzureStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2206d-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="2206d-110">ShareInstance</span></span>
```
Start-AzureStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2206d-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="2206d-111">FileInstanceToFilePath</span></span>
```
Start-AzureStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2206d-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="2206d-112">FileInstanceToFileInstance</span></span>
```
Start-AzureStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2206d-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="2206d-113">UriToFilePath</span></span>
```
Start-AzureStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2206d-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="2206d-114">UriToFileInstance</span></span>
```
Start-AzureStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2206d-115">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2206d-115">DESCRIPTION</span></span>
<span data-ttu-id="2206d-116">Cmdleten **Start-AzureStorageFileCopy** börjar kopiera en källfil till en målfil.</span><span class="sxs-lookup"><span data-stu-id="2206d-116">The **Start-AzureStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="2206d-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2206d-117">EXAMPLES</span></span>

### <span data-ttu-id="2206d-118">Exempel 1: Starta kopiering från fil till fil med hjälp av resurs namn och fil namn</span><span class="sxs-lookup"><span data-stu-id="2206d-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzureStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="2206d-119">Det här kommandot startar en kopierings åtgärd från en fil till en fil.</span><span class="sxs-lookup"><span data-stu-id="2206d-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="2206d-120">Kommandot anger resurs namn och fil namn</span><span class="sxs-lookup"><span data-stu-id="2206d-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="2206d-121">Exempel 2: starta kopierings åtgärd från blob till fil genom att använda container namn och blob-namn</span><span class="sxs-lookup"><span data-stu-id="2206d-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzureStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="2206d-122">Det här kommandot startar en kopierings åtgärd från blobben till fil.</span><span class="sxs-lookup"><span data-stu-id="2206d-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="2206d-123">Kommandot anger namn på behållare och blob-namn</span><span class="sxs-lookup"><span data-stu-id="2206d-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="2206d-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2206d-124">PARAMETERS</span></span>

### <span data-ttu-id="2206d-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="2206d-125">-AbsoluteUri</span></span>
<span data-ttu-id="2206d-126">Anger käll filens URI.</span><span class="sxs-lookup"><span data-stu-id="2206d-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="2206d-127">Om käll platsen kräver en autentiseringsuppgift måste du ange en.</span><span class="sxs-lookup"><span data-stu-id="2206d-127">If the source location requires a credential, you must provide one.</span></span>

```yaml
Type: String
Parameter Sets: UriToFilePath, UriToFileInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2206d-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2206d-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2206d-129">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="2206d-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2206d-130">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="2206d-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2206d-131">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="2206d-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2206d-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2206d-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2206d-133">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="2206d-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2206d-134">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="2206d-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2206d-135">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="2206d-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2206d-136">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="2206d-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2206d-137">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="2206d-137">The default value is 10.</span></span>

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

### <span data-ttu-id="2206d-138">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2206d-138">-Context</span></span>
<span data-ttu-id="2206d-139">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="2206d-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="2206d-140">Använd New-AzureStorageContext cmdlet för att få en kontext.</span><span class="sxs-lookup"><span data-stu-id="2206d-140">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerName, ShareName
Aliases: SrcContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2206d-141">-DestContext</span><span class="sxs-lookup"><span data-stu-id="2206d-141">-DestContext</span></span>
<span data-ttu-id="2206d-142">Anger målets Azure-lagringsenhet.</span><span class="sxs-lookup"><span data-stu-id="2206d-142">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="2206d-143">Använd **New-AzureStorageContext** för att få en kontext.</span><span class="sxs-lookup"><span data-stu-id="2206d-143">To obtain a context, use **New-AzureStorageContext**.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2206d-144">-DestFile</span><span class="sxs-lookup"><span data-stu-id="2206d-144">-DestFile</span></span>
<span data-ttu-id="2206d-145">Anger ett **CloudFile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2206d-145">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="2206d-146">Du kan skapa en moln fil eller skaffa en genom att använda Get-AzureStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2206d-146">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: BlobInstanceFileInstance, FileInstanceToFileInstance, UriToFileInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2206d-147">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="2206d-147">-DestFilePath</span></span>
<span data-ttu-id="2206d-148">Anger sökvägen till målfilen relativt mål resursen.</span><span class="sxs-lookup"><span data-stu-id="2206d-148">Specifies the path of the destination file relative to the destination share.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2206d-149">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="2206d-149">-DestShareName</span></span>
<span data-ttu-id="2206d-150">Anger namnet på mål resursen.</span><span class="sxs-lookup"><span data-stu-id="2206d-150">Specifies the name of the destination share.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2206d-151">-Force</span><span class="sxs-lookup"><span data-stu-id="2206d-151">-Force</span></span>
<span data-ttu-id="2206d-152">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="2206d-152">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2206d-153">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2206d-153">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2206d-154">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="2206d-154">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="2206d-155">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="2206d-155">-SrcBlob</span></span>
<span data-ttu-id="2206d-156">Anger ett **CloudBlob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2206d-156">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="2206d-157">Du kan skapa en moln-BLOB eller skaffa en genom att använda Get-AzureStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2206d-157">You can create a cloud blob or obtain one by using the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobInstanceFilePath, BlobInstanceFileInstance
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2206d-158">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="2206d-158">-SrcBlobName</span></span>
<span data-ttu-id="2206d-159">Anger namnet på käll-blob.</span><span class="sxs-lookup"><span data-stu-id="2206d-159">Specifies the name of the source blob.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, ContainerInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2206d-160">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="2206d-160">-SrcContainer</span></span>
<span data-ttu-id="2206d-161">Anger ett Cloud BLOB Container-objekt.</span><span class="sxs-lookup"><span data-stu-id="2206d-161">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="2206d-162">Du kan skapa Cloud BLOB Container-objekt eller använda Get-AzureStorageContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2206d-162">You can create cloud blob container object or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2206d-163">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="2206d-163">-SrcContainerName</span></span>
<span data-ttu-id="2206d-164">Anger namnet på käll behållaren.</span><span class="sxs-lookup"><span data-stu-id="2206d-164">Specifies the name of the source container.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2206d-165">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="2206d-165">-SrcFile</span></span>
<span data-ttu-id="2206d-166">Anger ett **CloudFile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2206d-166">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="2206d-167">Du kan skapa en moln fil eller skaffa en genom att använda **Get-AzureStorageFile**.</span><span class="sxs-lookup"><span data-stu-id="2206d-167">You can create a cloud file or obtain one by using **Get-AzureStorageFile**.</span></span>

```yaml
Type: CloudFile
Parameter Sets: FileInstanceToFilePath, FileInstanceToFileInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2206d-168">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="2206d-168">-SrcFilePath</span></span>
<span data-ttu-id="2206d-169">Anger sökvägen till käll filen i förhållande till käll katalogen eller käll resursen.</span><span class="sxs-lookup"><span data-stu-id="2206d-169">Specifies the path of the source file relative to the source directory or source share.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, ShareInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2206d-170">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="2206d-170">-SrcShare</span></span>
<span data-ttu-id="2206d-171">Anger ett moln fil objekt.</span><span class="sxs-lookup"><span data-stu-id="2206d-171">Specifies a cloud file share object.</span></span>
<span data-ttu-id="2206d-172">Du kan skapa en moln fil resurs eller skaffa en genom att använda Get-AzureStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2206d-172">You can create a cloud file share or obtain one by using the Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: ShareInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2206d-173">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="2206d-173">-SrcShareName</span></span>
<span data-ttu-id="2206d-174">Anger namnet på käll delningen.</span><span class="sxs-lookup"><span data-stu-id="2206d-174">Specifies the name of the source share.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2206d-175">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2206d-175">-Confirm</span></span>
<span data-ttu-id="2206d-176">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2206d-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2206d-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2206d-177">-WhatIf</span></span>
<span data-ttu-id="2206d-178">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2206d-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2206d-179">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2206d-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2206d-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2206d-180">CommonParameters</span></span>
<span data-ttu-id="2206d-181">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2206d-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2206d-182">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2206d-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2206d-183">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2206d-183">INPUTS</span></span>

### <span data-ttu-id="2206d-184">CloudBlob</span><span class="sxs-lookup"><span data-stu-id="2206d-184">CloudBlob</span></span>

<span data-ttu-id="2206d-185">Parametern ' SrcBlob ' godkänner värdet av typen ' CloudBlob ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="2206d-185">Parameter 'SrcBlob' accepts value of type 'CloudBlob' from the pipeline</span></span>

### <span data-ttu-id="2206d-186">CloudFile</span><span class="sxs-lookup"><span data-stu-id="2206d-186">CloudFile</span></span>

<span data-ttu-id="2206d-187">Parametern ' SrcFile ' godkänner värdet av typen ' CloudFile ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="2206d-187">Parameter 'SrcFile' accepts value of type 'CloudFile' from the pipeline</span></span>

## <span data-ttu-id="2206d-188">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2206d-188">OUTPUTS</span></span>

## <span data-ttu-id="2206d-189">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2206d-189">NOTES</span></span>

## <span data-ttu-id="2206d-190">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2206d-190">RELATED LINKS</span></span>

[<span data-ttu-id="2206d-191">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2206d-191">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="2206d-192">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2206d-192">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="2206d-193">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="2206d-193">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="2206d-194">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="2206d-194">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="2206d-195">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="2206d-195">Get-AzureStorageFileCopyState</span></span>](./Get-AzureStorageFileCopyState.md)

[<span data-ttu-id="2206d-196">Stopp-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2206d-196">Stop-AzureStorageFileCopy</span></span>](./Stop-AzureStorageFileCopy.md)
