---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
ms.openlocfilehash: bdd92d01c7b2a69f588b54504f014ea6b17d0aff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920787"
---
# <span data-ttu-id="ee976-101">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ee976-101">Start-AzStorageFileCopy</span></span>

## <span data-ttu-id="ee976-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ee976-102">SYNOPSIS</span></span>
<span data-ttu-id="ee976-103">Kopierar en källfil.</span><span class="sxs-lookup"><span data-stu-id="ee976-103">Starts to copy a source file.</span></span>

## <span data-ttu-id="ee976-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ee976-104">SYNTAX</span></span>

### <span data-ttu-id="ee976-105">Hålla</span><span class="sxs-lookup"><span data-stu-id="ee976-105">ContainerName</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee976-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ee976-106">ContainerInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee976-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="ee976-107">BlobInstanceFilePath</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee976-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="ee976-108">BlobInstanceFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee976-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="ee976-109">ShareName</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee976-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="ee976-110">ShareInstance</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee976-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="ee976-111">FileInstanceToFilePath</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee976-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="ee976-112">FileInstanceToFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee976-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="ee976-113">UriToFilePath</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee976-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="ee976-114">UriToFileInstance</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee976-115">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ee976-115">DESCRIPTION</span></span>
<span data-ttu-id="ee976-116">Cmdleten **Start-AzStorageFileCopy** börjar kopiera en källfil till en målfil.</span><span class="sxs-lookup"><span data-stu-id="ee976-116">The **Start-AzStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="ee976-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ee976-117">EXAMPLES</span></span>

### <span data-ttu-id="ee976-118">Exempel 1: Starta kopiering från fil till fil med hjälp av resurs namn och fil namn</span><span class="sxs-lookup"><span data-stu-id="ee976-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="ee976-119">Det här kommandot startar en kopierings åtgärd från en fil till en fil.</span><span class="sxs-lookup"><span data-stu-id="ee976-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="ee976-120">Kommandot anger resurs namn och fil namn</span><span class="sxs-lookup"><span data-stu-id="ee976-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="ee976-121">Exempel 2: starta kopierings åtgärd från blob till fil genom att använda container namn och blob-namn</span><span class="sxs-lookup"><span data-stu-id="ee976-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="ee976-122">Det här kommandot startar en kopierings åtgärd från blobben till fil.</span><span class="sxs-lookup"><span data-stu-id="ee976-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="ee976-123">Kommandot anger namn på behållare och blob-namn</span><span class="sxs-lookup"><span data-stu-id="ee976-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="ee976-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ee976-124">PARAMETERS</span></span>

### <span data-ttu-id="ee976-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="ee976-125">-AbsoluteUri</span></span>
<span data-ttu-id="ee976-126">Anger käll filens URI.</span><span class="sxs-lookup"><span data-stu-id="ee976-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="ee976-127">Om käll platsen kräver en autentiseringsuppgift måste du ange en.</span><span class="sxs-lookup"><span data-stu-id="ee976-127">If the source location requires a credential, you must provide one.</span></span>

```yaml
Type: System.String
Parameter Sets: UriToFilePath, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee976-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ee976-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ee976-129">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="ee976-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ee976-130">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="ee976-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ee976-131">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="ee976-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ee976-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ee976-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ee976-133">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="ee976-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ee976-134">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="ee976-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ee976-135">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="ee976-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ee976-136">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="ee976-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ee976-137">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="ee976-137">The default value is 10.</span></span>

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

### <span data-ttu-id="ee976-138">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ee976-138">-Context</span></span>
<span data-ttu-id="ee976-139">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="ee976-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="ee976-140">Använd New-AzStorageContext cmdlet för att få en kontext.</span><span class="sxs-lookup"><span data-stu-id="ee976-140">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, ShareName
Aliases: SrcContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee976-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee976-141">-DefaultProfile</span></span>
<span data-ttu-id="ee976-142">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ee976-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee976-143">-DestContext</span><span class="sxs-lookup"><span data-stu-id="ee976-143">-DestContext</span></span>
<span data-ttu-id="ee976-144">Anger målets Azure-lagringsenhet.</span><span class="sxs-lookup"><span data-stu-id="ee976-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="ee976-145">Använd **New-AzStorageContext** för att få en kontext.</span><span class="sxs-lookup"><span data-stu-id="ee976-145">To obtain a context, use **New-AzStorageContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee976-146">-DestFile</span><span class="sxs-lookup"><span data-stu-id="ee976-146">-DestFile</span></span>
<span data-ttu-id="ee976-147">Anger ett **CloudFile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ee976-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="ee976-148">Du kan skapa en moln fil eller skaffa en genom att använda Get-AzStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee976-148">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: BlobInstanceFileInstance, FileInstanceToFileInstance, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee976-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="ee976-149">-DestFilePath</span></span>
<span data-ttu-id="ee976-150">Anger sökvägen till målfilen relativt mål resursen.</span><span class="sxs-lookup"><span data-stu-id="ee976-150">Specifies the path of the destination file relative to the destination share.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee976-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="ee976-151">-DestShareName</span></span>
<span data-ttu-id="ee976-152">Anger namnet på mål resursen.</span><span class="sxs-lookup"><span data-stu-id="ee976-152">Specifies the name of the destination share.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee976-153">-Force</span><span class="sxs-lookup"><span data-stu-id="ee976-153">-Force</span></span>
<span data-ttu-id="ee976-154">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ee976-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ee976-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ee976-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ee976-156">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="ee976-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="ee976-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="ee976-157">-SrcBlob</span></span>
<span data-ttu-id="ee976-158">Anger ett **CloudBlob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ee976-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="ee976-159">Du kan skapa en moln-BLOB eller skaffa en genom att använda Get-AzStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee976-159">You can create a cloud blob or obtain one by using the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceFilePath, BlobInstanceFileInstance
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee976-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="ee976-160">-SrcBlobName</span></span>
<span data-ttu-id="ee976-161">Anger namnet på käll-blob.</span><span class="sxs-lookup"><span data-stu-id="ee976-161">Specifies the name of the source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee976-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="ee976-162">-SrcContainer</span></span>
<span data-ttu-id="ee976-163">Anger ett Cloud BLOB Container-objekt.</span><span class="sxs-lookup"><span data-stu-id="ee976-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="ee976-164">Du kan skapa Cloud BLOB Container-objekt eller använda Get-AzStorageContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee976-164">You can create cloud blob container object or use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee976-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="ee976-165">-SrcContainerName</span></span>
<span data-ttu-id="ee976-166">Anger namnet på käll behållaren.</span><span class="sxs-lookup"><span data-stu-id="ee976-166">Specifies the name of the source container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee976-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="ee976-167">-SrcFile</span></span>
<span data-ttu-id="ee976-168">Anger ett **CloudFile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ee976-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="ee976-169">Du kan skapa en moln fil eller skaffa en genom att använda **Get-AzStorageFile**.</span><span class="sxs-lookup"><span data-stu-id="ee976-169">You can create a cloud file or obtain one by using **Get-AzStorageFile**.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstanceToFilePath, FileInstanceToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee976-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="ee976-170">-SrcFilePath</span></span>
<span data-ttu-id="ee976-171">Anger sökvägen till käll filen i förhållande till käll katalogen eller käll resursen.</span><span class="sxs-lookup"><span data-stu-id="ee976-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, ShareInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee976-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="ee976-172">-SrcShare</span></span>
<span data-ttu-id="ee976-173">Anger ett moln fil objekt.</span><span class="sxs-lookup"><span data-stu-id="ee976-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="ee976-174">Du kan skapa en moln fil resurs eller skaffa en genom att använda Get-AzStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee976-174">You can create a cloud file share or obtain one by using the Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee976-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="ee976-175">-SrcShareName</span></span>
<span data-ttu-id="ee976-176">Anger namnet på käll delningen.</span><span class="sxs-lookup"><span data-stu-id="ee976-176">Specifies the name of the source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee976-177">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ee976-177">-Confirm</span></span>
<span data-ttu-id="ee976-178">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ee976-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee976-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee976-179">-WhatIf</span></span>
<span data-ttu-id="ee976-180">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ee976-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee976-181">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ee976-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee976-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee976-182">CommonParameters</span></span>
<span data-ttu-id="ee976-183">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee976-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee976-184">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee976-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee976-185">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ee976-185">INPUTS</span></span>

### <span data-ttu-id="ee976-186">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ee976-186">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="ee976-187">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="ee976-187">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="ee976-188">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ee976-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ee976-189">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ee976-189">OUTPUTS</span></span>

### <span data-ttu-id="ee976-190">System. Void</span><span class="sxs-lookup"><span data-stu-id="ee976-190">System.Void</span></span>

## <span data-ttu-id="ee976-191">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ee976-191">NOTES</span></span>

## <span data-ttu-id="ee976-192">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ee976-192">RELATED LINKS</span></span>

[<span data-ttu-id="ee976-193">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ee976-193">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="ee976-194">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ee976-194">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="ee976-195">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="ee976-195">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="ee976-196">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="ee976-196">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="ee976-197">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="ee976-197">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="ee976-198">Stopp-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ee976-198">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)