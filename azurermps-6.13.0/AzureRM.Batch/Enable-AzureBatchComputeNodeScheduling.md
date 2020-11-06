---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: e00a1a923afdd8a851416e872028a30ce1e04a55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579028"
---
# <span data-ttu-id="95aa8-101">Enable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="95aa8-101">Enable-AzureBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="95aa8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="95aa8-102">SYNOPSIS</span></span>
<span data-ttu-id="95aa8-103">Aktiverar schemaläggning av aktiviteter på angiven datornod.</span><span class="sxs-lookup"><span data-stu-id="95aa8-103">Enables task scheduling on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95aa8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="95aa8-104">SYNTAX</span></span>

### <span data-ttu-id="95aa8-105">ID (standard)</span><span class="sxs-lookup"><span data-stu-id="95aa8-105">Id (Default)</span></span>
```
Enable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95aa8-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="95aa8-106">InputObject</span></span>
```
Enable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95aa8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="95aa8-107">DESCRIPTION</span></span>
<span data-ttu-id="95aa8-108">Cmdleten **Enable-AzureBatchComputeNodeScheduling** aktiverar aktivitets schemaläggning på den angivna noden för beräkning.</span><span class="sxs-lookup"><span data-stu-id="95aa8-108">The **Enable-AzureBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="95aa8-109">En datornod är en virtuell Azure-dator avsedd för en viss program belastning.</span><span class="sxs-lookup"><span data-stu-id="95aa8-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="95aa8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="95aa8-110">EXAMPLES</span></span>

### <span data-ttu-id="95aa8-111">Exempel 1: Aktivera schemaläggning av en datornod</span><span class="sxs-lookup"><span data-stu-id="95aa8-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Enable-AzureBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="95aa8-112">De här kommandona aktiverar schemaläggning av aktivitet på TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="95aa8-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="95aa8-113">Det första kommandot i exemplet skapar en objekt referens som innehåller konto nycklarna för batch-contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="95aa8-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="95aa8-114">Denna objekt referens lagras i en variabel som heter $context.</span><span class="sxs-lookup"><span data-stu-id="95aa8-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="95aa8-115">Det andra kommandot använder då den här objekt referensen och cmdleten **Enable-AzureBatchComputeNodeScheduling** för att ansluta till poolen för pool och aktivera schemaläggning för TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="95aa8-115">The second command then uses this object reference and the **Enable-AzureBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="95aa8-116">Exempel 2: Aktivera schemaläggning av aktiviteter på datornoder i en pool</span><span class="sxs-lookup"><span data-stu-id="95aa8-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzureBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="95aa8-117">De här kommandona aktiverar schemaläggning av aktiviteter på alla datornoder som finns i poolens Pool06.</span><span class="sxs-lookup"><span data-stu-id="95aa8-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="95aa8-118">För att utföra den här åtgärden skapar det första kommandot i exemplet en objekt referens som innehåller konto nycklarna för batch-contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="95aa8-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="95aa8-119">Denna objekt referens lagras i en variabel som heter $context.</span><span class="sxs-lookup"><span data-stu-id="95aa8-119">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="95aa8-120">Med det andra kommandot i exemplet används den här objekt referensen och **Get-AzureBatchComputeNode** för att returnera en samling av alla datornoder som finns i Pool06.</span><span class="sxs-lookup"><span data-stu-id="95aa8-120">The second command in the example then uses this object reference and **Get-AzureBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="95aa8-121">Samlingen är då piped till cmdleten **Enable-AzureBatchComputeNodeScheduling** , som aktiverar schemaläggning av aktiviteter på varje datornod i samlingen.</span><span class="sxs-lookup"><span data-stu-id="95aa8-121">That collection is then piped to the **Enable-AzureBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="95aa8-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="95aa8-122">PARAMETERS</span></span>

### <span data-ttu-id="95aa8-123">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="95aa8-123">-BatchContext</span></span>
<span data-ttu-id="95aa8-124">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="95aa8-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="95aa8-125">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="95aa8-125">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="95aa8-126">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="95aa8-126">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="95aa8-127">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="95aa8-127">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="95aa8-128">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="95aa8-128">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="95aa8-129">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="95aa8-129">-ComputeNode</span></span>
<span data-ttu-id="95aa8-130">Anger en objekt referens till noden Compute där schemaläggning av aktiviteter är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="95aa8-130">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="95aa8-131">Den här objekt referensen skapas med Get-AzureBatchComputeNode cmdlet och det returnerade datornoder-objektet sparas i en variabel.</span><span class="sxs-lookup"><span data-stu-id="95aa8-131">This object reference is created by using the Get-AzureBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95aa8-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95aa8-132">-DefaultProfile</span></span>
<span data-ttu-id="95aa8-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="95aa8-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95aa8-134">-ID</span><span class="sxs-lookup"><span data-stu-id="95aa8-134">-Id</span></span>
<span data-ttu-id="95aa8-135">Anger ID för den datornod där aktivitets schemaläggningen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="95aa8-135">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="95aa8-136">-PoolId</span><span class="sxs-lookup"><span data-stu-id="95aa8-136">-PoolId</span></span>
<span data-ttu-id="95aa8-137">Anger ID för den gruppbearbetningssekvens som innehåller den datornod där aktivitets schemaläggningen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="95aa8-137">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="95aa8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95aa8-138">CommonParameters</span></span>
<span data-ttu-id="95aa8-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95aa8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95aa8-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95aa8-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95aa8-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="95aa8-141">INPUTS</span></span>

### <span data-ttu-id="95aa8-142">Microsoft.Azure.Commands.BatCH. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="95aa8-142">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="95aa8-143">Parametrar: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="95aa8-143">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="95aa8-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="95aa8-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="95aa8-145">Parametrar: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="95aa8-145">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="95aa8-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="95aa8-146">OUTPUTS</span></span>

### <span data-ttu-id="95aa8-147">System. Void</span><span class="sxs-lookup"><span data-stu-id="95aa8-147">System.Void</span></span>

## <span data-ttu-id="95aa8-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="95aa8-148">NOTES</span></span>

## <span data-ttu-id="95aa8-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="95aa8-149">RELATED LINKS</span></span>

[<span data-ttu-id="95aa8-150">Disable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="95aa8-150">Disable-AzureBatchComputeNodeScheduling</span></span>](./Disable-AzureBatchComputeNodeScheduling.md)


