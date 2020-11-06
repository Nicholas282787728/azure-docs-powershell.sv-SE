---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
ms.openlocfilehash: a5e8fd6e6cfba8832365f385cc90357bac59efb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578452"
---
# <span data-ttu-id="c81d4-101">Set-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="c81d4-101">Set-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="c81d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c81d4-102">SYNOPSIS</span></span>
<span data-ttu-id="c81d4-103">Ändrar egenskaper för ett konto i en batch-datornod.</span><span class="sxs-lookup"><span data-stu-id="c81d4-103">Modifies properties of an account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c81d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c81d4-104">SYNTAX</span></span>

```
Set-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <String> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c81d4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c81d4-105">DESCRIPTION</span></span>
<span data-ttu-id="c81d4-106">Cmdleten **set-AzureBatchComputeNodeUser** ändrar egenskaperna för ett användar konto i en Azure Batch-datornod.</span><span class="sxs-lookup"><span data-stu-id="c81d4-106">The **Set-AzureBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="c81d4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c81d4-107">EXAMPLES</span></span>

### <span data-ttu-id="c81d4-108">Exempel 1: uppdatera ett användar konto</span><span class="sxs-lookup"><span data-stu-id="c81d4-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzureBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="c81d4-109">Det här kommandot ändrar användar kontot som heter PFuller på noden Compute och som har angivet ID i poolen med namnet ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="c81d4-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="c81d4-110">Kommandot ändrar lösen ordet för kontot och förfallo tiden.</span><span class="sxs-lookup"><span data-stu-id="c81d4-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="c81d4-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c81d4-111">PARAMETERS</span></span>

### <span data-ttu-id="c81d4-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c81d4-112">-BatchContext</span></span>
<span data-ttu-id="c81d4-113">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c81d4-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c81d4-114">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c81d4-114">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="c81d4-115">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="c81d4-115">-ComputeNodeId</span></span>
<span data-ttu-id="c81d4-116">Anger ID för den datornod som denna cmdlet körs på.</span><span class="sxs-lookup"><span data-stu-id="c81d4-116">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c81d4-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c81d4-117">-ExpiryTime</span></span>
<span data-ttu-id="c81d4-118">Anger förfallo tiden för användar kontot.</span><span class="sxs-lookup"><span data-stu-id="c81d4-118">Specifies the expiry time for the user account.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c81d4-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="c81d4-119">-Name</span></span>
<span data-ttu-id="c81d4-120">Anger namnet på det användar konto som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="c81d4-120">Specifies the name of the user account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c81d4-121">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="c81d4-121">-Password</span></span>
<span data-ttu-id="c81d4-122">Anger lösen ordet för användar kontot.</span><span class="sxs-lookup"><span data-stu-id="c81d4-122">Specifies the password for the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c81d4-123">-PoolId</span><span class="sxs-lookup"><span data-stu-id="c81d4-123">-PoolId</span></span>
<span data-ttu-id="c81d4-124">Anger ID för poolen som innehåller den datornod som denna cmdlet körs på.</span><span class="sxs-lookup"><span data-stu-id="c81d4-124">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c81d4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c81d4-125">-DefaultProfile</span></span>
<span data-ttu-id="c81d4-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c81d4-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c81d4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c81d4-127">CommonParameters</span></span>
<span data-ttu-id="c81d4-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c81d4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c81d4-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c81d4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c81d4-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c81d4-130">INPUTS</span></span>

### <span data-ttu-id="c81d4-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c81d4-131">BatchAccountContext</span></span>
<span data-ttu-id="c81d4-132">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c81d4-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="c81d4-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c81d4-133">OUTPUTS</span></span>

## <span data-ttu-id="c81d4-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c81d4-134">NOTES</span></span>

## <span data-ttu-id="c81d4-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c81d4-135">RELATED LINKS</span></span>

[<span data-ttu-id="c81d4-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c81d4-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c81d4-137">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="c81d4-137">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="c81d4-138">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="c81d4-138">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="c81d4-139">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="c81d4-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


