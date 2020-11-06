---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/Start-AzureBatchComputeNodeServiceLogUpload
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchComputeNodeServiceLogUpload.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchComputeNodeServiceLogUpload.md
ms.openlocfilehash: 8f171b42e3f1e1f087890ec451d5a3ff13cb8c57
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578984"
---
# <span data-ttu-id="ef7b3-101">Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="ef7b3-101">Start-AzureBatchComputeNodeServiceLogUpload</span></span>

## <span data-ttu-id="ef7b3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef7b3-102">SYNOPSIS</span></span>
<span data-ttu-id="ef7b3-103">Ladda upp loggfiler för datornoder till en Azure-lagringsenhet.</span><span class="sxs-lookup"><span data-stu-id="ef7b3-103">Upload compute node service log files to an Azure Storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef7b3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef7b3-104">SYNTAX</span></span>

### <span data-ttu-id="ef7b3-105">AzureBatchComputeNodeServiceLogUpload (standard)</span><span class="sxs-lookup"><span data-stu-id="ef7b3-105">AzureBatchComputeNodeServiceLogUpload (Default)</span></span>
```
Start-AzureBatchComputeNodeServiceLogUpload [-ContainerUrl] <String> [-StartTime] <DateTime>
 [-EndTime <DateTime>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef7b3-106">Et</span><span class="sxs-lookup"><span data-stu-id="ef7b3-106">Id</span></span>
```
Start-AzureBatchComputeNodeServiceLogUpload [-PoolId] <String> [-ComputeNodeId] <String>
 [-ContainerUrl] <String> [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef7b3-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="ef7b3-107">ParentObject</span></span>
```
Start-AzureBatchComputeNodeServiceLogUpload [-ComputeNode] <PSComputeNode> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef7b3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef7b3-108">DESCRIPTION</span></span>
<span data-ttu-id="ef7b3-109">Denna cmdlet samlar in loggfiler för Azure Batch-tjänsten från Compute-noder om du råkar ut för ett fel och vill eskalera till Azure-support.</span><span class="sxs-lookup"><span data-stu-id="ef7b3-109">This cmdlet gathers Azure Batch service log files from compute nodes if you are experiencing an error and wish to escalate to Azure support.</span></span> <span data-ttu-id="ef7b3-110">Loggfilerna för Azure Batch-tjänsten bör delas med Azure-Support för att felsöka problem med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ef7b3-110">The Azure Batch service log files should be shared with Azure support to aid in debugging issues with the Batch service.</span></span> 

## <span data-ttu-id="ef7b3-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef7b3-111">EXAMPLES</span></span>

### <span data-ttu-id="ef7b3-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ef7b3-112">Example 1</span></span>

```powershell
PS C:\> $storageContext = New-AzureStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzureStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzureRmBatchAccountKeys -AccountName "contosobatch"
PS C:\> Start-AzureBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    4 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="ef7b3-113">Ladda upp Compute Node service-loggar skrivna den 1 januari 2018 midnatt, som har hämtats från noden Compute, angivet pool-ID för poolen där noden Compute finns och Compute Node ID.</span><span class="sxs-lookup"><span data-stu-id="ef7b3-113">Upload compute node service logs written on or after January 1, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="ef7b3-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ef7b3-114">Example 2</span></span>

```powershell
PS C:\> $storageContext = New-AzureStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzureStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzureRmBatchAccountKeys -AccountName "contosobatch"
PS C:\> Start-AzureBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="ef7b3-115">Ladda upp Compute Node service-loggar som skrivits den 1 januari 2018 midnatt och före den 10 januari 2018 midnatt, som har hämtats från noden Compute, angivet pool-ID för poolen där noden befinner sig och Compute Node ID.</span><span class="sxs-lookup"><span data-stu-id="ef7b3-115">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="ef7b3-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="ef7b3-116">Example 3</span></span>

```powershell
PS C:\> $storageContext = New-AzureStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzureStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzureRmBatchAccountKeys -AccountName "contosobatch"
PS C:\> Get-AzureBatchComputeNode -BatchContext $batchContext -Id "tvm-1612030122_1-20180405t234700z" -PoolId "contosopool" | Start-AzureBatchComputeNodeServiceLogUpload -BatchContext $batchContext -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="ef7b3-117">Ladda upp Compute Node service-loggar som skrivits den 1 januari 2018 midnatt och före den 10 januari 2018 midnatt, som erhålls från noden Compute Node.</span><span class="sxs-lookup"><span data-stu-id="ef7b3-117">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node object.</span></span>

## <span data-ttu-id="ef7b3-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef7b3-118">PARAMETERS</span></span>

### <span data-ttu-id="ef7b3-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ef7b3-119">-BatchContext</span></span>
<span data-ttu-id="ef7b3-120">Den BatchAccountContext-instans som ska användas vid interaktion med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ef7b3-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="ef7b3-121">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ef7b3-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="ef7b3-122">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="ef7b3-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="ef7b3-123">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="ef7b3-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="ef7b3-124">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ef7b3-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef7b3-125">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="ef7b3-125">-ComputeNode</span></span>
<span data-ttu-id="ef7b3-126">Anger det **PSComputeNode** -objekt som tjänst loggar hämtas från.</span><span class="sxs-lookup"><span data-stu-id="ef7b3-126">Specifies the **PSComputeNode** object from which service logs are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef7b3-127">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="ef7b3-127">-ComputeNodeId</span></span>
<span data-ttu-id="ef7b3-128">ID för Compute-noden.</span><span class="sxs-lookup"><span data-stu-id="ef7b3-128">The id of the compute node.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef7b3-129">-ContainerUrl</span><span class="sxs-lookup"><span data-stu-id="ef7b3-129">-ContainerUrl</span></span>
<span data-ttu-id="ef7b3-130">URL-adressen till en Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="ef7b3-130">The container url to Azure Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef7b3-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef7b3-131">-DefaultProfile</span></span>
<span data-ttu-id="ef7b3-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ef7b3-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef7b3-133">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="ef7b3-133">-EndTime</span></span>
<span data-ttu-id="ef7b3-134">Slut tiden för tjänst loggen laddas upp (valfritt).</span><span class="sxs-lookup"><span data-stu-id="ef7b3-134">The end time of service log to be uploaded (optional).</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef7b3-135">-PoolId</span><span class="sxs-lookup"><span data-stu-id="ef7b3-135">-PoolId</span></span>
<span data-ttu-id="ef7b3-136">ID för poolen som innehåller noden Compute.</span><span class="sxs-lookup"><span data-stu-id="ef7b3-136">The id of the pool that contains the compute node.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef7b3-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ef7b3-137">-StartTime</span></span>
<span data-ttu-id="ef7b3-138">Start tiden för tjänst loggen laddas upp.</span><span class="sxs-lookup"><span data-stu-id="ef7b3-138">The start time of service log to be uploaded.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef7b3-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ef7b3-139">-Confirm</span></span>
<span data-ttu-id="ef7b3-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ef7b3-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef7b3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef7b3-141">-WhatIf</span></span>
<span data-ttu-id="ef7b3-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ef7b3-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef7b3-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ef7b3-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef7b3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef7b3-144">CommonParameters</span></span>
<span data-ttu-id="ef7b3-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef7b3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef7b3-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef7b3-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef7b3-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef7b3-147">INPUTS</span></span>

### <span data-ttu-id="ef7b3-148">Microsoft.Azure.Commands.BatCH. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="ef7b3-148">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="ef7b3-149">Parametrar: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ef7b3-149">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="ef7b3-150">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ef7b3-150">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="ef7b3-151">Parametrar: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ef7b3-151">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="ef7b3-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef7b3-152">OUTPUTS</span></span>

### <span data-ttu-id="ef7b3-153">Microsoft.Azure.Commands.BatCH. Modeller. PSStartComputeNodeServiceLogUploadResult</span><span class="sxs-lookup"><span data-stu-id="ef7b3-153">Microsoft.Azure.Commands.Batch.Models.PSStartComputeNodeServiceLogUploadResult</span></span>

## <span data-ttu-id="ef7b3-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef7b3-154">NOTES</span></span>

## <span data-ttu-id="ef7b3-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef7b3-155">RELATED LINKS</span></span>
