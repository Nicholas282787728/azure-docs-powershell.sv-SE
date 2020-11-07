---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
ms.openlocfilehash: 6f89e7db5d2df2c475be1ac9875fd1e87217db77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758298"
---
# <span data-ttu-id="6b8a6-101">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="6b8a6-101">Get-AzureBatchPool</span></span>

## <span data-ttu-id="6b8a6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6b8a6-102">SYNOPSIS</span></span>
<span data-ttu-id="6b8a6-103">Hämtar batchattribut under det angivna batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="6b8a6-103">Gets Batch pools under the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b8a6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6b8a6-104">SYNTAX</span></span>

### <span data-ttu-id="6b8a6-105">ODataFilter (standard)</span><span class="sxs-lookup"><span data-stu-id="6b8a6-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b8a6-106">Et</span><span class="sxs-lookup"><span data-stu-id="6b8a6-106">Id</span></span>
```
Get-AzureBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b8a6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6b8a6-107">DESCRIPTION</span></span>
<span data-ttu-id="6b8a6-108">Cmdleten **Get-AzureBatchPool** hämtar Azure Batch-pooler under batch-kontot som anges med parametern *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="6b8a6-108">The **Get-AzureBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="6b8a6-109">Du kan använda *ID-* parametern för att få en enda pool, eller så kan du använda parametern *filter* om du vill hämta de pooler som matchar ett open data Protocol (OData)-filter.</span><span class="sxs-lookup"><span data-stu-id="6b8a6-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="6b8a6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6b8a6-110">EXAMPLES</span></span>

### <span data-ttu-id="6b8a6-111">Exempel 1: Hämta en pool utifrån ID</span><span class="sxs-lookup"><span data-stu-id="6b8a6-111">Example 1: Get a pool by ID</span></span>
```
PS C:\>Get-AzureBatchPool -Id "MyPool" -BatchContext $Context
AllocationState                      : Resizing
AllocationStateTransitionTime        : 7/25/2015 9:30:28 PM
AutoScaleEnabled                     : False
AutoScaleFormula                     : 
AutoScaleRun                         : 
CertificateReferences                : 
CreationTime                         : 7/25/2015 9:30:28 PM
CurrentDedicated                     : 0
CurrentOSVersion                     : *
DisplayName                          : 
ETag                                 : 0x8D29538429CF04C
Id                                   : MyPool
InterComputeNodeCommunicationEnabled : False
LastModified                         : 7/25/2015 9:30:28 PM
MaxTasksPerComputeNode               : 1
Metadata                             : 
OSFamily                             : 4
ResizeError                          : 
ResizeTimeout                        : 00:05:00
TaskSchedulingPolicy                 : Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
StartTask                            : 
State                                : Active
StateTransitionTime                  : 7/25/2015 9:30:28 PM
Statistics                           : 
TargetDedicated                      : 1
TargetOSVersion                      : *
Url                                  : https://cmdletexample.westus.batch.azure.com/pools/MyPool
VirtualMachineSize                   : small
```

<span data-ttu-id="6b8a6-112">Med det här kommandot hämtas poolen med ID-nummer.</span><span class="sxs-lookup"><span data-stu-id="6b8a6-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="6b8a6-113">Exempel 2: Hämta alla pooler med ett OData-filter</span><span class="sxs-lookup"><span data-stu-id="6b8a6-113">Example 2: Get all pools using an OData filter</span></span>
```
PS C:\>Get-AzureBatchPool -Filter "startswith(id,'My')" -BatchContext $Context
AllocationState                      : Resizing
AllocationStateTransitionTime        : 7/25/2015 9:30:28 PM
AutoScaleEnabled                     : False
AutoScaleFormula                     : 
AutoScaleRun                         : 
CertificateReferences                : 
CreationTime                         : 7/25/2015 9:30:28 PM
CurrentDedicated                     : 0
CurrentOSVersion                     : *
DisplayName                          : 
ETag                                 : 0x8D29538429CF04C
Id                                   : MyPool
InterComputeNodeCommunicationEnabled : False
LastModified                         : 7/25/2015 9:30:28 PM
MaxTasksPerComputeNode               : 1
Metadata                             : 
OSFamily                             : 4
ResizeError                          : 
ResizeTimeout                        : 00:05:00
TaskSchedulingPolicy                 : Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
StartTask                            : 
State                                : Active
StateTransitionTime                  : 7/25/2015 9:30:28 PM
Statistics                           : 
TargetDedicated                      : 1
TargetOSVersion                      : *
Url                                  : https://cmdletexample.westus.batch.azure.com/pools/MyPool
VirtualMachineSize                   : small
```

<span data-ttu-id="6b8a6-114">Det här kommandot får de pooler vars ID: n börjar med att använda parametern *filter* .</span><span class="sxs-lookup"><span data-stu-id="6b8a6-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="6b8a6-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6b8a6-115">PARAMETERS</span></span>

### <span data-ttu-id="6b8a6-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6b8a6-116">-BatchContext</span></span>
<span data-ttu-id="6b8a6-117">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6b8a6-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6b8a6-118">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="6b8a6-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="6b8a6-119">-Expandera</span><span class="sxs-lookup"><span data-stu-id="6b8a6-119">-Expand</span></span>
<span data-ttu-id="6b8a6-120">Anger en Open data Protocol (OData) Expand-sats.</span><span class="sxs-lookup"><span data-stu-id="6b8a6-120">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="6b8a6-121">Ange ett värde för den här parametern för att hämta associerade enheter för huvud enheten som du får.</span><span class="sxs-lookup"><span data-stu-id="6b8a6-121">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b8a6-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="6b8a6-122">-Filter</span></span>
<span data-ttu-id="6b8a6-123">Anger den OData filter-sats som ska användas för att fråga efter pooler.</span><span class="sxs-lookup"><span data-stu-id="6b8a6-123">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="6b8a6-124">Om du inte anger något filter returneras alla pooler under batch-konto som anges med parametern *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="6b8a6-124">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b8a6-125">-ID</span><span class="sxs-lookup"><span data-stu-id="6b8a6-125">-Id</span></span>
<span data-ttu-id="6b8a6-126">Anger ID för den pool som ska visas.</span><span class="sxs-lookup"><span data-stu-id="6b8a6-126">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="6b8a6-127">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="6b8a6-127">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b8a6-128">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="6b8a6-128">-MaxCount</span></span>
<span data-ttu-id="6b8a6-129">Anger det maximala antalet pooler som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="6b8a6-129">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="6b8a6-130">Om du anger ett värde som är noll (0) eller mindre används ingen övre gräns av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6b8a6-130">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="6b8a6-131">Standardvärdet är 1000.</span><span class="sxs-lookup"><span data-stu-id="6b8a6-131">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b8a6-132">-Välj</span><span class="sxs-lookup"><span data-stu-id="6b8a6-132">-Select</span></span>
<span data-ttu-id="6b8a6-133">Anger en OData SELECT-sats.</span><span class="sxs-lookup"><span data-stu-id="6b8a6-133">Specifies an OData select clause.</span></span>
<span data-ttu-id="6b8a6-134">Ange ett värde för den här parametern för att få specifika egenskaper i stället för alla objekt egenskaper.</span><span class="sxs-lookup"><span data-stu-id="6b8a6-134">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b8a6-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b8a6-135">-DefaultProfile</span></span>
<span data-ttu-id="6b8a6-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6b8a6-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b8a6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b8a6-137">CommonParameters</span></span>
<span data-ttu-id="6b8a6-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b8a6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b8a6-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b8a6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b8a6-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6b8a6-140">INPUTS</span></span>

### <span data-ttu-id="6b8a6-141">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6b8a6-141">BatchAccountContext</span></span>
<span data-ttu-id="6b8a6-142">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="6b8a6-142">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="6b8a6-143">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="6b8a6-143">String</span></span>
<span data-ttu-id="6b8a6-144">Parametern ' ID ' godkänner värdet för typen ' String ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="6b8a6-144">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="6b8a6-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6b8a6-145">OUTPUTS</span></span>

### <span data-ttu-id="6b8a6-146">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="6b8a6-146">PSCloudPool</span></span>

## <span data-ttu-id="6b8a6-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6b8a6-147">NOTES</span></span>

## <span data-ttu-id="6b8a6-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6b8a6-148">RELATED LINKS</span></span>

[<span data-ttu-id="6b8a6-149">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6b8a6-149">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="6b8a6-150">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="6b8a6-150">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="6b8a6-151">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="6b8a6-151">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="6b8a6-152">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="6b8a6-152">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


