---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
ms.openlocfilehash: e6d5bcad88e50fcd166e2d7a8c37ca948ae355f8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923677"
---
# <span data-ttu-id="a6d23-101">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="a6d23-101">Get-AzStorageBlobCopyState</span></span>

## <span data-ttu-id="a6d23-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a6d23-102">SYNOPSIS</span></span>
<span data-ttu-id="a6d23-103">Hämtar kopierings statusen för en Azure Storage-blob.</span><span class="sxs-lookup"><span data-stu-id="a6d23-103">Gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="a6d23-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a6d23-104">SYNTAX</span></span>

### <span data-ttu-id="a6d23-105">NamePipeline (standard)</span><span class="sxs-lookup"><span data-stu-id="a6d23-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a6d23-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="a6d23-106">BlobPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a6d23-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="a6d23-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a6d23-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a6d23-108">DESCRIPTION</span></span>
<span data-ttu-id="a6d23-109">Cmdleten **Get-AzStorageBlobCopyState** hämtar kopierings statusen för en Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="a6d23-109">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="a6d23-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a6d23-110">EXAMPLES</span></span>

### <span data-ttu-id="a6d23-111">Exempel 1: få kopierings status för en BLOB</span><span class="sxs-lookup"><span data-stu-id="a6d23-111">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="a6d23-112">Det här kommandot får kopierings statusen för blobben som heter ContosoPlanning2015 i container-ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="a6d23-112">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="a6d23-113">Exempel 2: Hämta kopians status för en BLOB genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="a6d23-113">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzStorageBlobCopyState
```

<span data-ttu-id="a6d23-114">Det här kommandot hämtar blobben med namnet ContosoPlanning2015 i behållaren med namnet ContosoUploads med hjälp av cmdleten **Get-AzStorageBlob** och skickar sedan resultatet till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="a6d23-114">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a6d23-115">Cmdleten **Get-AzStorageBlobCopyState** får kopierings statusen för den blobben.</span><span class="sxs-lookup"><span data-stu-id="a6d23-115">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="a6d23-116">Exempel 3: Hämta kopierings status för en BLOB i en behållare med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="a6d23-116">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="a6d23-117">Det här kommandot hämtar behållaren med namnet **Get-AzStorageBlob** och skickar sedan resultatet till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a6d23-117">This command gets the container named by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="a6d23-118">Cmdleten **Get-AzStorageContainer** hämtar kopierings statusen för blobben som heter ContosoPlanning2015 i behållaren.</span><span class="sxs-lookup"><span data-stu-id="a6d23-118">The **Get-AzStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

## <span data-ttu-id="a6d23-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a6d23-119">PARAMETERS</span></span>

### <span data-ttu-id="a6d23-120">-BLOB</span><span class="sxs-lookup"><span data-stu-id="a6d23-120">-Blob</span></span>
<span data-ttu-id="a6d23-121">Anger namnet på en blob.</span><span class="sxs-lookup"><span data-stu-id="a6d23-121">Specifies the name of a blob.</span></span>
<span data-ttu-id="a6d23-122">Denna cmdlet får tillståndet för BLOB-filåtgärden för Azure Storage blob som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="a6d23-122">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="a6d23-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a6d23-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a6d23-124">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="a6d23-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a6d23-125">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="a6d23-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a6d23-126">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="a6d23-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a6d23-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a6d23-127">-CloudBlob</span></span>
<span data-ttu-id="a6d23-128">Anger ett **CloudBlob** -objekt från ett Azure Storage-bibliotek.</span><span class="sxs-lookup"><span data-stu-id="a6d23-128">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="a6d23-129">För att hämta ett **CloudBlob** -objekt, Använd cmdleten Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="a6d23-129">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6d23-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="a6d23-130">-CloudBlobContainer</span></span>
<span data-ttu-id="a6d23-131">Anger ett **CloudBlobContainer** -objekt från klient bibliotek för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="a6d23-131">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="a6d23-132">Denna cmdlet hämtar kopierings statusen för en BLOB i behållaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="a6d23-132">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="a6d23-133">För att hämta ett **CloudBlobContainer** -objekt, Använd cmdleten Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="a6d23-133">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6d23-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a6d23-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a6d23-135">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="a6d23-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a6d23-136">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="a6d23-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a6d23-137">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="a6d23-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a6d23-138">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="a6d23-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a6d23-139">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="a6d23-139">The default value is 10.</span></span>

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

### <span data-ttu-id="a6d23-140">-Container</span><span class="sxs-lookup"><span data-stu-id="a6d23-140">-Container</span></span>
<span data-ttu-id="a6d23-141">Anger namnet på en behållare.</span><span class="sxs-lookup"><span data-stu-id="a6d23-141">Specifies the name of a container.</span></span>
<span data-ttu-id="a6d23-142">Denna cmdlet hämtar kopierings statusen för en BLOB i behållaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="a6d23-142">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="a6d23-143">-Kontext</span><span class="sxs-lookup"><span data-stu-id="a6d23-143">-Context</span></span>
<span data-ttu-id="a6d23-144">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="a6d23-144">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a6d23-145">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="a6d23-145">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a6d23-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6d23-146">-DefaultProfile</span></span>
<span data-ttu-id="a6d23-147">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a6d23-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6d23-148">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a6d23-148">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a6d23-149">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="a6d23-149">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="a6d23-150">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="a6d23-150">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="a6d23-151">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="a6d23-151">-WaitForComplete</span></span>
<span data-ttu-id="a6d23-152">Anger att denna cmdlet väntar på att kopieringen ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="a6d23-152">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="a6d23-153">Om du inte anger den här parametern returnerar denna cmdlet ett resultat omedelbart.</span><span class="sxs-lookup"><span data-stu-id="a6d23-153">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="a6d23-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6d23-154">CommonParameters</span></span>
<span data-ttu-id="a6d23-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6d23-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6d23-156">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6d23-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6d23-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a6d23-157">INPUTS</span></span>

### <span data-ttu-id="a6d23-158">Microsoft. WindowsAz. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a6d23-158">Microsoft.WindowsAz.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="a6d23-159">Microsoft. WindowsAz. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="a6d23-159">Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="a6d23-160">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a6d23-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a6d23-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a6d23-161">OUTPUTS</span></span>

### <span data-ttu-id="a6d23-162">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a6d23-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="a6d23-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a6d23-163">NOTES</span></span>

## <span data-ttu-id="a6d23-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a6d23-164">RELATED LINKS</span></span>

[<span data-ttu-id="a6d23-165">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a6d23-165">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="a6d23-166">Stopp-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a6d23-166">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)


