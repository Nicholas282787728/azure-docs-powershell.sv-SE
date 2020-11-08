---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
ms.openlocfilehash: 6f9b08b59ff4b89243a26442b793bf2cf70f73d3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088962"
---
# <span data-ttu-id="b86c4-101">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="b86c4-101">Get-AzStorageBlobCopyState</span></span>

## <span data-ttu-id="b86c4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b86c4-102">SYNOPSIS</span></span>
<span data-ttu-id="b86c4-103">Hämtar kopierings statusen för en Azure Storage-blob.</span><span class="sxs-lookup"><span data-stu-id="b86c4-103">Gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="b86c4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b86c4-104">SYNTAX</span></span>

### <span data-ttu-id="b86c4-105">NamePipeline (standard)</span><span class="sxs-lookup"><span data-stu-id="b86c4-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b86c4-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="b86c4-106">BlobPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b86c4-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="b86c4-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="b86c4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b86c4-108">DESCRIPTION</span></span>
<span data-ttu-id="b86c4-109">Cmdleten **Get-AzStorageBlobCopyState** hämtar kopierings statusen för en Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="b86c4-109">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="b86c4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b86c4-110">EXAMPLES</span></span>

### <span data-ttu-id="b86c4-111">Exempel 1: få kopierings status för en BLOB</span><span class="sxs-lookup"><span data-stu-id="b86c4-111">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="b86c4-112">Det här kommandot får kopierings statusen för blobben som heter ContosoPlanning2015 i container-ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="b86c4-112">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="b86c4-113">Exempel 2: Hämta kopians status för en BLOB genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="b86c4-113">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzStorageBlobCopyState
```

<span data-ttu-id="b86c4-114">Det här kommandot hämtar blobben med namnet ContosoPlanning2015 i behållaren med namnet ContosoUploads med hjälp av cmdleten **Get-AzStorageBlob** och skickar sedan resultatet till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="b86c4-114">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b86c4-115">Cmdleten **Get-AzStorageBlobCopyState** får kopierings statusen för den blobben.</span><span class="sxs-lookup"><span data-stu-id="b86c4-115">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="b86c4-116">Exempel 3: Hämta kopierings status för en BLOB i en behållare med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="b86c4-116">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="b86c4-117">Det här kommandot hämtar behållaren med namnet **Get-AzStorageBlob** och skickar sedan resultatet till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b86c4-117">This command gets the container named by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="b86c4-118">Cmdleten **Get-AzStorageContainer** hämtar kopierings statusen för blobben som heter ContosoPlanning2015 i behållaren.</span><span class="sxs-lookup"><span data-stu-id="b86c4-118">The **Get-AzStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

## <span data-ttu-id="b86c4-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b86c4-119">PARAMETERS</span></span>

### <span data-ttu-id="b86c4-120">-BLOB</span><span class="sxs-lookup"><span data-stu-id="b86c4-120">-Blob</span></span>
<span data-ttu-id="b86c4-121">Anger namnet på en blob.</span><span class="sxs-lookup"><span data-stu-id="b86c4-121">Specifies the name of a blob.</span></span>
<span data-ttu-id="b86c4-122">Denna cmdlet får tillståndet för BLOB-filåtgärden för Azure Storage blob som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b86c4-122">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b86c4-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b86c4-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b86c4-124">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="b86c4-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b86c4-125">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="b86c4-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b86c4-126">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="b86c4-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b86c4-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b86c4-127">-CloudBlob</span></span>
<span data-ttu-id="b86c4-128">Anger ett **CloudBlob** -objekt från ett Azure Storage-bibliotek.</span><span class="sxs-lookup"><span data-stu-id="b86c4-128">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="b86c4-129">För att hämta ett **CloudBlob** -objekt, Använd cmdleten Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="b86c4-129">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b86c4-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b86c4-130">-CloudBlobContainer</span></span>
<span data-ttu-id="b86c4-131">Anger ett **CloudBlobContainer** -objekt från klient bibliotek för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="b86c4-131">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="b86c4-132">Denna cmdlet hämtar kopierings statusen för en BLOB i behållaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b86c4-132">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="b86c4-133">För att hämta ett **CloudBlobContainer** -objekt, Använd cmdleten Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="b86c4-133">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b86c4-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b86c4-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b86c4-135">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="b86c4-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b86c4-136">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="b86c4-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b86c4-137">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="b86c4-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b86c4-138">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="b86c4-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b86c4-139">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="b86c4-139">The default value is 10.</span></span>

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

### <span data-ttu-id="b86c4-140">-Container</span><span class="sxs-lookup"><span data-stu-id="b86c4-140">-Container</span></span>
<span data-ttu-id="b86c4-141">Anger namnet på en behållare.</span><span class="sxs-lookup"><span data-stu-id="b86c4-141">Specifies the name of a container.</span></span>
<span data-ttu-id="b86c4-142">Denna cmdlet hämtar kopierings statusen för en BLOB i behållaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b86c4-142">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b86c4-143">-Kontext</span><span class="sxs-lookup"><span data-stu-id="b86c4-143">-Context</span></span>
<span data-ttu-id="b86c4-144">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="b86c4-144">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b86c4-145">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="b86c4-145">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b86c4-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b86c4-146">-DefaultProfile</span></span>
<span data-ttu-id="b86c4-147">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b86c4-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b86c4-148">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b86c4-148">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b86c4-149">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="b86c4-149">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="b86c4-150">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="b86c4-150">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="b86c4-151">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="b86c4-151">-WaitForComplete</span></span>
<span data-ttu-id="b86c4-152">Anger att denna cmdlet väntar på att kopieringen ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="b86c4-152">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="b86c4-153">Om du inte anger den här parametern returnerar denna cmdlet ett resultat omedelbart.</span><span class="sxs-lookup"><span data-stu-id="b86c4-153">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="b86c4-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b86c4-154">CommonParameters</span></span>
<span data-ttu-id="b86c4-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b86c4-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b86c4-156">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b86c4-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b86c4-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b86c4-157">INPUTS</span></span>

### <span data-ttu-id="b86c4-158">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b86c4-158">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="b86c4-159">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b86c4-159">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="b86c4-160">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b86c4-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b86c4-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b86c4-161">OUTPUTS</span></span>

### <span data-ttu-id="b86c4-162">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b86c4-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="b86c4-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b86c4-163">NOTES</span></span>

## <span data-ttu-id="b86c4-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b86c4-164">RELATED LINKS</span></span>

[<span data-ttu-id="b86c4-165">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b86c4-165">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="b86c4-166">Stopp-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b86c4-166">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)


