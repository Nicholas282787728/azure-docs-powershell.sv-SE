---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
ms.openlocfilehash: 636ceb216c7bb6aec2016bdd047a26f707108c9b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103293"
---
# <span data-ttu-id="87644-101">Set-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="87644-101">Set-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="87644-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="87644-102">SYNOPSIS</span></span>
<span data-ttu-id="87644-103">Ändrar egenskaper för ett konto i en batch-datornod.</span><span class="sxs-lookup"><span data-stu-id="87644-103">Modifies properties of an account on a Batch compute node.</span></span>

## <span data-ttu-id="87644-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="87644-104">SYNTAX</span></span>

```
Set-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87644-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="87644-105">DESCRIPTION</span></span>
<span data-ttu-id="87644-106">Cmdleten **set-AzBatchComputeNodeUser** ändrar egenskaperna för ett användar konto i en Azure Batch-datornod.</span><span class="sxs-lookup"><span data-stu-id="87644-106">The **Set-AzBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="87644-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="87644-107">EXAMPLES</span></span>

### <span data-ttu-id="87644-108">Exempel 1: uppdatera ett användar konto</span><span class="sxs-lookup"><span data-stu-id="87644-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="87644-109">Det här kommandot ändrar användar kontot som heter PFuller på noden Compute och som har angivet ID i poolen med namnet ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="87644-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="87644-110">Kommandot ändrar lösen ordet för kontot och förfallo tiden.</span><span class="sxs-lookup"><span data-stu-id="87644-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="87644-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="87644-111">PARAMETERS</span></span>

### <span data-ttu-id="87644-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="87644-112">-BatchContext</span></span>
<span data-ttu-id="87644-113">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="87644-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="87644-114">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="87644-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="87644-115">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="87644-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="87644-116">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="87644-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="87644-117">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="87644-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="87644-118">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="87644-118">-ComputeNodeId</span></span>
<span data-ttu-id="87644-119">Anger ID för den datornod som denna cmdlet körs på.</span><span class="sxs-lookup"><span data-stu-id="87644-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="87644-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87644-120">-DefaultProfile</span></span>
<span data-ttu-id="87644-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="87644-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87644-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="87644-122">-ExpiryTime</span></span>
<span data-ttu-id="87644-123">Anger förfallo tiden för användar kontot.</span><span class="sxs-lookup"><span data-stu-id="87644-123">Specifies the expiry time for the user account.</span></span>

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

### <span data-ttu-id="87644-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="87644-124">-Name</span></span>
<span data-ttu-id="87644-125">Anger namnet på det användar konto som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="87644-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="87644-126">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="87644-126">-Password</span></span>
<span data-ttu-id="87644-127">Anger lösen ordet för användar kontot.</span><span class="sxs-lookup"><span data-stu-id="87644-127">Specifies the password for the user account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87644-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="87644-128">-PoolId</span></span>
<span data-ttu-id="87644-129">Anger ID för poolen som innehåller den datornod som denna cmdlet körs på.</span><span class="sxs-lookup"><span data-stu-id="87644-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="87644-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87644-130">CommonParameters</span></span>
<span data-ttu-id="87644-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87644-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87644-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87644-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87644-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="87644-133">INPUTS</span></span>

### <span data-ttu-id="87644-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="87644-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="87644-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="87644-135">OUTPUTS</span></span>

### <span data-ttu-id="87644-136">System. Void</span><span class="sxs-lookup"><span data-stu-id="87644-136">System.Void</span></span>

## <span data-ttu-id="87644-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="87644-137">NOTES</span></span>

## <span data-ttu-id="87644-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="87644-138">RELATED LINKS</span></span>

[<span data-ttu-id="87644-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="87644-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="87644-140">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="87644-140">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="87644-141">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="87644-141">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="87644-142">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="87644-142">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
