---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 6fb398e44b2e6de8a0d00e9a8d737916fafa2472
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757951"
---
# <span data-ttu-id="90f2d-101">Set-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="90f2d-101">Set-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="90f2d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90f2d-102">SYNOPSIS</span></span>
<span data-ttu-id="90f2d-103">Ändrar egenskaper för ett konto i en batch-datornod.</span><span class="sxs-lookup"><span data-stu-id="90f2d-103">Modifies properties of an account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90f2d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90f2d-104">SYNTAX</span></span>

```
Set-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90f2d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90f2d-105">DESCRIPTION</span></span>
<span data-ttu-id="90f2d-106">Cmdleten **set-AzureBatchComputeNodeUser** ändrar egenskaperna för ett användar konto i en Azure Batch-datornod.</span><span class="sxs-lookup"><span data-stu-id="90f2d-106">The **Set-AzureBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="90f2d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90f2d-107">EXAMPLES</span></span>

### <span data-ttu-id="90f2d-108">Exempel 1: uppdatera ett användar konto</span><span class="sxs-lookup"><span data-stu-id="90f2d-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzureBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="90f2d-109">Det här kommandot ändrar användar kontot som heter PFuller på noden Compute och som har angivet ID i poolen med namnet ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="90f2d-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="90f2d-110">Kommandot ändrar lösen ordet för kontot och förfallo tiden.</span><span class="sxs-lookup"><span data-stu-id="90f2d-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="90f2d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90f2d-111">PARAMETERS</span></span>

### <span data-ttu-id="90f2d-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="90f2d-112">-BatchContext</span></span>
<span data-ttu-id="90f2d-113">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="90f2d-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="90f2d-114">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="90f2d-114">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="90f2d-115">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="90f2d-115">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="90f2d-116">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="90f2d-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="90f2d-117">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="90f2d-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="90f2d-118">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="90f2d-118">-ComputeNodeId</span></span>
<span data-ttu-id="90f2d-119">Anger ID för den datornod som denna cmdlet körs på.</span><span class="sxs-lookup"><span data-stu-id="90f2d-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90f2d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90f2d-120">-DefaultProfile</span></span>
<span data-ttu-id="90f2d-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="90f2d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90f2d-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="90f2d-122">-ExpiryTime</span></span>
<span data-ttu-id="90f2d-123">Anger förfallo tiden för användar kontot.</span><span class="sxs-lookup"><span data-stu-id="90f2d-123">Specifies the expiry time for the user account.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90f2d-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="90f2d-124">-Name</span></span>
<span data-ttu-id="90f2d-125">Anger namnet på det användar konto som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="90f2d-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90f2d-126">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="90f2d-126">-Password</span></span>
<span data-ttu-id="90f2d-127">Anger lösen ordet för användar kontot.</span><span class="sxs-lookup"><span data-stu-id="90f2d-127">Specifies the password for the user account.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90f2d-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="90f2d-128">-PoolId</span></span>
<span data-ttu-id="90f2d-129">Anger ID för poolen som innehåller den datornod som denna cmdlet körs på.</span><span class="sxs-lookup"><span data-stu-id="90f2d-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90f2d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90f2d-130">CommonParameters</span></span>
<span data-ttu-id="90f2d-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90f2d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90f2d-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90f2d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90f2d-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90f2d-133">INPUTS</span></span>

### <span data-ttu-id="90f2d-134">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="90f2d-134">BatchAccountContext</span></span>
<span data-ttu-id="90f2d-135">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="90f2d-135">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="90f2d-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90f2d-136">OUTPUTS</span></span>

## <span data-ttu-id="90f2d-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90f2d-137">NOTES</span></span>

## <span data-ttu-id="90f2d-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90f2d-138">RELATED LINKS</span></span>

[<span data-ttu-id="90f2d-139">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="90f2d-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="90f2d-140">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="90f2d-140">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="90f2d-141">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="90f2d-141">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="90f2d-142">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="90f2d-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


