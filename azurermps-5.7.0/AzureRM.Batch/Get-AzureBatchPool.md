---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
ms.openlocfilehash: 2bd84d8e5d0f48c5b9a3af65944ece99369270c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574433"
---
# <span data-ttu-id="97427-101">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="97427-101">Get-AzureBatchPool</span></span>

## <span data-ttu-id="97427-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="97427-102">SYNOPSIS</span></span>
<span data-ttu-id="97427-103">Hämtar batchattribut under det angivna batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="97427-103">Gets Batch pools under the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97427-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="97427-104">SYNTAX</span></span>

### <span data-ttu-id="97427-105">ODataFilter (standard)</span><span class="sxs-lookup"><span data-stu-id="97427-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97427-106">Et</span><span class="sxs-lookup"><span data-stu-id="97427-106">Id</span></span>
```
Get-AzureBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97427-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="97427-107">DESCRIPTION</span></span>
<span data-ttu-id="97427-108">Cmdleten **Get-AzureBatchPool** hämtar Azure Batch-pooler under batch-kontot som anges med parametern *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="97427-108">The **Get-AzureBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="97427-109">Du kan använda *ID-* parametern för att få en enda pool, eller så kan du använda parametern *filter* om du vill hämta de pooler som matchar ett open data Protocol (OData)-filter.</span><span class="sxs-lookup"><span data-stu-id="97427-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="97427-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="97427-110">EXAMPLES</span></span>

### <span data-ttu-id="97427-111">Exempel 1: Hämta en pool utifrån ID</span><span class="sxs-lookup"><span data-stu-id="97427-111">Example 1: Get a pool by ID</span></span>
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

<span data-ttu-id="97427-112">Med det här kommandot hämtas poolen med ID-nummer.</span><span class="sxs-lookup"><span data-stu-id="97427-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="97427-113">Exempel 2: Hämta alla pooler med ett OData-filter</span><span class="sxs-lookup"><span data-stu-id="97427-113">Example 2: Get all pools using an OData filter</span></span>
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

<span data-ttu-id="97427-114">Det här kommandot får de pooler vars ID: n börjar med att använda parametern *filter* .</span><span class="sxs-lookup"><span data-stu-id="97427-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="97427-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="97427-115">PARAMETERS</span></span>

### <span data-ttu-id="97427-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="97427-116">-BatchContext</span></span>
<span data-ttu-id="97427-117">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="97427-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="97427-118">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="97427-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="97427-119">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="97427-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="97427-120">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="97427-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="97427-121">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="97427-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97427-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97427-122">-DefaultProfile</span></span>
<span data-ttu-id="97427-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="97427-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97427-124">-Expandera</span><span class="sxs-lookup"><span data-stu-id="97427-124">-Expand</span></span>
<span data-ttu-id="97427-125">Anger en Open data Protocol (OData) Expand-sats.</span><span class="sxs-lookup"><span data-stu-id="97427-125">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="97427-126">Ange ett värde för den här parametern för att hämta associerade enheter för huvud enheten som du får.</span><span class="sxs-lookup"><span data-stu-id="97427-126">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97427-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="97427-127">-Filter</span></span>
<span data-ttu-id="97427-128">Anger den OData filter-sats som ska användas för att fråga efter pooler.</span><span class="sxs-lookup"><span data-stu-id="97427-128">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="97427-129">Om du inte anger något filter returneras alla pooler under batch-konto som anges med parametern *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="97427-129">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97427-130">-ID</span><span class="sxs-lookup"><span data-stu-id="97427-130">-Id</span></span>
<span data-ttu-id="97427-131">Anger ID för den pool som ska visas.</span><span class="sxs-lookup"><span data-stu-id="97427-131">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="97427-132">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="97427-132">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97427-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="97427-133">-MaxCount</span></span>
<span data-ttu-id="97427-134">Anger det maximala antalet pooler som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="97427-134">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="97427-135">Om du anger ett värde som är noll (0) eller mindre används ingen övre gräns av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="97427-135">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="97427-136">Standardvärdet är 1000.</span><span class="sxs-lookup"><span data-stu-id="97427-136">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97427-137">-Välj</span><span class="sxs-lookup"><span data-stu-id="97427-137">-Select</span></span>
<span data-ttu-id="97427-138">Anger en OData SELECT-sats.</span><span class="sxs-lookup"><span data-stu-id="97427-138">Specifies an OData select clause.</span></span>
<span data-ttu-id="97427-139">Ange ett värde för den här parametern för att få specifika egenskaper i stället för alla objekt egenskaper.</span><span class="sxs-lookup"><span data-stu-id="97427-139">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97427-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97427-140">CommonParameters</span></span>
<span data-ttu-id="97427-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97427-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97427-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97427-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97427-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="97427-143">INPUTS</span></span>

### <span data-ttu-id="97427-144">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="97427-144">BatchAccountContext</span></span>
<span data-ttu-id="97427-145">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="97427-145">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="97427-146">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="97427-146">String</span></span>
<span data-ttu-id="97427-147">Parametern ' ID ' godkänner värdet för typen ' String ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="97427-147">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="97427-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="97427-148">OUTPUTS</span></span>

### <span data-ttu-id="97427-149">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="97427-149">PSCloudPool</span></span>

## <span data-ttu-id="97427-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="97427-150">NOTES</span></span>

## <span data-ttu-id="97427-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="97427-151">RELATED LINKS</span></span>

[<span data-ttu-id="97427-152">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="97427-152">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="97427-153">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="97427-153">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="97427-154">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="97427-154">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="97427-155">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="97427-155">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


