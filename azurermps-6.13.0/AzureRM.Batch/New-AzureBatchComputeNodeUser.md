---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 1e95eff4e93b1b7d55a099ad188fc196025cd06f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574034"
---
# <span data-ttu-id="7d7b5-101">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="7d7b5-101">New-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="7d7b5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d7b5-102">SYNOPSIS</span></span>
<span data-ttu-id="7d7b5-103">Skapar ett användar konto i en batch-datornod.</span><span class="sxs-lookup"><span data-stu-id="7d7b5-103">Creates a user account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d7b5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d7b5-104">SYNTAX</span></span>

### <span data-ttu-id="7d7b5-105">Et</span><span class="sxs-lookup"><span data-stu-id="7d7b5-105">Id</span></span>
```
New-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String>
 -Password <SecureString> [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d7b5-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="7d7b5-106">ParentObject</span></span>
```
New-AzureBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d7b5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d7b5-107">DESCRIPTION</span></span>
<span data-ttu-id="7d7b5-108">Cmdleten **New-AzureBatchComputeNodeUser** skapar ett användar konto på en Azure Batch-datornod.</span><span class="sxs-lookup"><span data-stu-id="7d7b5-108">The **New-AzureBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="7d7b5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d7b5-109">EXAMPLES</span></span>

### <span data-ttu-id="7d7b5-110">Exempel 1: skapa ett användar konto med administratörs behörighet</span><span class="sxs-lookup"><span data-stu-id="7d7b5-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzureBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="7d7b5-111">Det här kommandot skapar ett användar konto på noden Compute som har ID-ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="7d7b5-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="7d7b5-112">Noden finns i poolen med ID-MyPool01.</span><span class="sxs-lookup"><span data-stu-id="7d7b5-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="7d7b5-113">Användar namnet är TestUser, lösen ordet är lösen ord, kontot upphör att gälla om sju dagar och kontot har administratörs behörighet.</span><span class="sxs-lookup"><span data-stu-id="7d7b5-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="7d7b5-114">Exempel 2: skapa ett användar konto på en datornod med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="7d7b5-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzureBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="7d7b5-115">Det här kommandot får Compute-noden med namnet ComputeNode01 med hjälp av cmdleten **Get-AzureBatchComputeNode** .</span><span class="sxs-lookup"><span data-stu-id="7d7b5-115">This command gets the compute node named ComputeNode01 by using the **Get-AzureBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="7d7b5-116">Noden finns i poolen med ID-MyPool01.</span><span class="sxs-lookup"><span data-stu-id="7d7b5-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="7d7b5-117">Kommandot skickar den beräknade noden till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="7d7b5-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7d7b5-118">Kommandot skapar ett användar konto med användar namnet TestUserand lösen ord.</span><span class="sxs-lookup"><span data-stu-id="7d7b5-118">The command creates a user account that has the user name TestUserand the password Password.</span></span>

## <span data-ttu-id="7d7b5-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d7b5-119">PARAMETERS</span></span>

### <span data-ttu-id="7d7b5-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7d7b5-120">-BatchContext</span></span>
<span data-ttu-id="7d7b5-121">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7d7b5-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7d7b5-122">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7d7b5-122">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7d7b5-123">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="7d7b5-123">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7d7b5-124">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="7d7b5-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7d7b5-125">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="7d7b5-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7d7b5-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="7d7b5-126">-ComputeNode</span></span>
<span data-ttu-id="7d7b5-127">Anger noden Compute, som ett **PSComputeNode** -objekt, där denna cmdlet skapar ett användar konto.</span><span class="sxs-lookup"><span data-stu-id="7d7b5-127">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d7b5-128">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="7d7b5-128">-ComputeNodeId</span></span>
<span data-ttu-id="7d7b5-129">Anger ID för den datornod där denna cmdlet skapar ett användar konto.</span><span class="sxs-lookup"><span data-stu-id="7d7b5-129">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="7d7b5-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d7b5-130">-DefaultProfile</span></span>
<span data-ttu-id="7d7b5-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7d7b5-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d7b5-132">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="7d7b5-132">-ExpiryTime</span></span>
<span data-ttu-id="7d7b5-133">Anger sista giltighets tiden för det nya kontot.</span><span class="sxs-lookup"><span data-stu-id="7d7b5-133">Specifies the expiry time for the new user account.</span></span>

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

### <span data-ttu-id="7d7b5-134">-IsAdmin</span><span class="sxs-lookup"><span data-stu-id="7d7b5-134">-IsAdmin</span></span>
<span data-ttu-id="7d7b5-135">Anger att cmdleten skapar ett användar konto som har administratörs behörighet.</span><span class="sxs-lookup"><span data-stu-id="7d7b5-135">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

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

### <span data-ttu-id="7d7b5-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="7d7b5-136">-Name</span></span>
<span data-ttu-id="7d7b5-137">Anger namnet på det nya lokala Windows-kontot.</span><span class="sxs-lookup"><span data-stu-id="7d7b5-137">Specifies the name of the new local Windows account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d7b5-138">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="7d7b5-138">-Password</span></span>
<span data-ttu-id="7d7b5-139">Anger lösen ordet för användar kontot.</span><span class="sxs-lookup"><span data-stu-id="7d7b5-139">Specifies the user account password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d7b5-140">-PoolId</span><span class="sxs-lookup"><span data-stu-id="7d7b5-140">-PoolId</span></span>
<span data-ttu-id="7d7b5-141">Anger ID: t för poolen som innehåller den datornod där användar kontot ska skapas.</span><span class="sxs-lookup"><span data-stu-id="7d7b5-141">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

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

### <span data-ttu-id="7d7b5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d7b5-142">CommonParameters</span></span>
<span data-ttu-id="7d7b5-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d7b5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d7b5-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d7b5-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d7b5-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d7b5-145">INPUTS</span></span>

### <span data-ttu-id="7d7b5-146">Microsoft.Azure.Commands.BatCH. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="7d7b5-146">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="7d7b5-147">Parametrar: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7d7b5-147">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="7d7b5-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7d7b5-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="7d7b5-149">Parametrar: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7d7b5-149">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="7d7b5-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d7b5-150">OUTPUTS</span></span>

### <span data-ttu-id="7d7b5-151">System. Void</span><span class="sxs-lookup"><span data-stu-id="7d7b5-151">System.Void</span></span>

## <span data-ttu-id="7d7b5-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d7b5-152">NOTES</span></span>

## <span data-ttu-id="7d7b5-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d7b5-153">RELATED LINKS</span></span>

[<span data-ttu-id="7d7b5-154">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7d7b5-154">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="7d7b5-155">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="7d7b5-155">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="7d7b5-156">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="7d7b5-156">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="7d7b5-157">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="7d7b5-157">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


