---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobCopyState.md
ms.openlocfilehash: 619f909ab794b5531d15d89343ea6263bea7ce03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573124"
---
# <span data-ttu-id="33ddf-101">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="33ddf-101">Get-AzureStorageBlobCopyState</span></span>

## <span data-ttu-id="33ddf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="33ddf-102">SYNOPSIS</span></span>
<span data-ttu-id="33ddf-103">Hämtar kopierings statusen för en Azure Storage-blob.</span><span class="sxs-lookup"><span data-stu-id="33ddf-103">Gets the copy status of an Azure Storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33ddf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="33ddf-104">SYNTAX</span></span>

### <span data-ttu-id="33ddf-105">NamePipeline (standard)</span><span class="sxs-lookup"><span data-stu-id="33ddf-105">NamePipeline (Default)</span></span>
```
Get-AzureStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="33ddf-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="33ddf-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="33ddf-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="33ddf-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="33ddf-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="33ddf-108">DESCRIPTION</span></span>
<span data-ttu-id="33ddf-109">Cmdleten **Get-AzureStorageBlobCopyState** hämtar kopierings statusen för en Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="33ddf-109">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="33ddf-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="33ddf-110">EXAMPLES</span></span>

### <span data-ttu-id="33ddf-111">Exempel 1: få kopierings status för en BLOB</span><span class="sxs-lookup"><span data-stu-id="33ddf-111">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="33ddf-112">Det här kommandot får kopierings statusen för blobben som heter ContosoPlanning2015 i container-ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="33ddf-112">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="33ddf-113">Exempel 2: Hämta kopians status för en BLOB genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="33ddf-113">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzureStorageBlobCopyState
```

<span data-ttu-id="33ddf-114">Det här kommandot hämtar blobben med namnet ContosoPlanning2015 i behållaren med namnet ContosoUploads med hjälp av cmdleten **Get-AzureStorageBlob** och skickar sedan resultatet till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="33ddf-114">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="33ddf-115">Cmdleten **Get-AzureStorageBlobCopyState** får kopierings statusen för den blobben.</span><span class="sxs-lookup"><span data-stu-id="33ddf-115">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="33ddf-116">Exempel 3: Hämta kopierings status för en BLOB i en behållare med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="33ddf-116">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="33ddf-117">Det här kommandot hämtar behållaren med namnet **Get-AzureStorageBlob** och skickar sedan resultatet till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="33ddf-117">This command gets the container named by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="33ddf-118">Cmdleten **Get-AzureStorageContainer** hämtar kopierings statusen för blobben som heter ContosoPlanning2015 i behållaren.</span><span class="sxs-lookup"><span data-stu-id="33ddf-118">The **Get-AzureStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

## <span data-ttu-id="33ddf-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="33ddf-119">PARAMETERS</span></span>

### <span data-ttu-id="33ddf-120">-BLOB</span><span class="sxs-lookup"><span data-stu-id="33ddf-120">-Blob</span></span>
<span data-ttu-id="33ddf-121">Anger namnet på en blob.</span><span class="sxs-lookup"><span data-stu-id="33ddf-121">Specifies the name of a blob.</span></span>
<span data-ttu-id="33ddf-122">Denna cmdlet får tillståndet för BLOB-filåtgärden för Azure Storage blob som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="33ddf-122">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="33ddf-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="33ddf-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="33ddf-124">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="33ddf-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="33ddf-125">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="33ddf-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="33ddf-126">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="33ddf-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="33ddf-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="33ddf-127">-CloudBlob</span></span>
<span data-ttu-id="33ddf-128">Anger ett **CloudBlob** -objekt från ett Azure Storage-bibliotek.</span><span class="sxs-lookup"><span data-stu-id="33ddf-128">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="33ddf-129">För att hämta ett **CloudBlob** -objekt, Använd cmdleten Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="33ddf-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33ddf-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="33ddf-130">-CloudBlobContainer</span></span>
<span data-ttu-id="33ddf-131">Anger ett **CloudBlobContainer** -objekt från klient bibliotek för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="33ddf-131">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="33ddf-132">Denna cmdlet hämtar kopierings statusen för en BLOB i behållaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="33ddf-132">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="33ddf-133">För att hämta ett **CloudBlobContainer** -objekt, Använd cmdleten Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="33ddf-133">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33ddf-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="33ddf-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="33ddf-135">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="33ddf-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="33ddf-136">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="33ddf-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="33ddf-137">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="33ddf-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="33ddf-138">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="33ddf-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="33ddf-139">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="33ddf-139">The default value is 10.</span></span>

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

### <span data-ttu-id="33ddf-140">-Container</span><span class="sxs-lookup"><span data-stu-id="33ddf-140">-Container</span></span>
<span data-ttu-id="33ddf-141">Anger namnet på en behållare.</span><span class="sxs-lookup"><span data-stu-id="33ddf-141">Specifies the name of a container.</span></span>
<span data-ttu-id="33ddf-142">Denna cmdlet hämtar kopierings statusen för en BLOB i behållaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="33ddf-142">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="33ddf-143">-Kontext</span><span class="sxs-lookup"><span data-stu-id="33ddf-143">-Context</span></span>
<span data-ttu-id="33ddf-144">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="33ddf-144">Specifies an Azure storage context.</span></span>
<span data-ttu-id="33ddf-145">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="33ddf-145">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="33ddf-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33ddf-146">-DefaultProfile</span></span>
<span data-ttu-id="33ddf-147">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="33ddf-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33ddf-148">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="33ddf-148">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="33ddf-149">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="33ddf-149">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="33ddf-150">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="33ddf-150">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="33ddf-151">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="33ddf-151">-WaitForComplete</span></span>
<span data-ttu-id="33ddf-152">Anger att denna cmdlet väntar på att kopieringen ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="33ddf-152">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="33ddf-153">Om du inte anger den här parametern returnerar denna cmdlet ett resultat omedelbart.</span><span class="sxs-lookup"><span data-stu-id="33ddf-153">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="33ddf-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33ddf-154">CommonParameters</span></span>
<span data-ttu-id="33ddf-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33ddf-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33ddf-156">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33ddf-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33ddf-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="33ddf-157">INPUTS</span></span>

### <span data-ttu-id="33ddf-158">Microsoft. WindowsAzure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="33ddf-158">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="33ddf-159">Microsoft. WindowsAzure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="33ddf-159">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="33ddf-160">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="33ddf-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="33ddf-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="33ddf-161">OUTPUTS</span></span>

### <span data-ttu-id="33ddf-162">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="33ddf-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="33ddf-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="33ddf-163">NOTES</span></span>

## <span data-ttu-id="33ddf-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="33ddf-164">RELATED LINKS</span></span>

[<span data-ttu-id="33ddf-165">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="33ddf-165">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="33ddf-166">Stopp-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="33ddf-166">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)


