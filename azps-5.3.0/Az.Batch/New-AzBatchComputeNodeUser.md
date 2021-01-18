---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
ms.openlocfilehash: 5695f0bf0a7cc65b1eb032be33116cc40ec0618e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524759"
---
# <span data-ttu-id="7e88f-101">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="7e88f-101">New-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="7e88f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e88f-102">SYNOPSIS</span></span>
<span data-ttu-id="7e88f-103">Skapar ett användar konto i en batch-datornod.</span><span class="sxs-lookup"><span data-stu-id="7e88f-103">Creates a user account on a Batch compute node.</span></span>

## <span data-ttu-id="7e88f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e88f-104">SYNTAX</span></span>

### <span data-ttu-id="7e88f-105">Et</span><span class="sxs-lookup"><span data-stu-id="7e88f-105">Id</span></span>
```
New-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e88f-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="7e88f-106">ParentObject</span></span>
```
New-AzBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e88f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e88f-107">DESCRIPTION</span></span>
<span data-ttu-id="7e88f-108">Cmdleten **New-AzBatchComputeNodeUser** skapar ett användar konto på en Azure Batch-datornod.</span><span class="sxs-lookup"><span data-stu-id="7e88f-108">The **New-AzBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="7e88f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e88f-109">EXAMPLES</span></span>

### <span data-ttu-id="7e88f-110">Exempel 1: skapa ett användar konto med administratörs behörighet</span><span class="sxs-lookup"><span data-stu-id="7e88f-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="7e88f-111">Det här kommandot skapar ett användar konto på noden Compute som har ID-ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="7e88f-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="7e88f-112">Noden finns i poolen med ID-MyPool01.</span><span class="sxs-lookup"><span data-stu-id="7e88f-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="7e88f-113">Användar namnet är TestUser, lösen ordet är lösen ord, kontot upphör att gälla om sju dagar och kontot har administratörs behörighet.</span><span class="sxs-lookup"><span data-stu-id="7e88f-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="7e88f-114">Exempel 2: skapa ett användar konto på en datornod med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="7e88f-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="7e88f-115">Det här kommandot får Compute-noden med namnet ComputeNode01 med hjälp av cmdleten **Get-AzBatchComputeNode** .</span><span class="sxs-lookup"><span data-stu-id="7e88f-115">This command gets the compute node named ComputeNode01 by using the **Get-AzBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="7e88f-116">Noden finns i poolen med ID-MyPool01.</span><span class="sxs-lookup"><span data-stu-id="7e88f-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="7e88f-117">Kommandot skickar den beräknade noden till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="7e88f-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7e88f-118">Kommandot skapar ett användar konto som har användar namnet TestUser och lösen ordet.</span><span class="sxs-lookup"><span data-stu-id="7e88f-118">The command creates a user account that has the user name TestUser and the password Password.</span></span>

## <span data-ttu-id="7e88f-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e88f-119">PARAMETERS</span></span>

### <span data-ttu-id="7e88f-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7e88f-120">-BatchContext</span></span>
<span data-ttu-id="7e88f-121">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7e88f-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7e88f-122">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7e88f-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7e88f-123">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="7e88f-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7e88f-124">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="7e88f-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7e88f-125">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="7e88f-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7e88f-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="7e88f-126">-ComputeNode</span></span>
<span data-ttu-id="7e88f-127">Anger noden Compute, som ett **PSComputeNode** -objekt, där denna cmdlet skapar ett användar konto.</span><span class="sxs-lookup"><span data-stu-id="7e88f-127">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="7e88f-128">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="7e88f-128">-ComputeNodeId</span></span>
<span data-ttu-id="7e88f-129">Anger ID för den datornod där denna cmdlet skapar ett användar konto.</span><span class="sxs-lookup"><span data-stu-id="7e88f-129">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="7e88f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e88f-130">-DefaultProfile</span></span>
<span data-ttu-id="7e88f-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7e88f-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e88f-132">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="7e88f-132">-ExpiryTime</span></span>
<span data-ttu-id="7e88f-133">Anger sista giltighets tiden för det nya kontot.</span><span class="sxs-lookup"><span data-stu-id="7e88f-133">Specifies the expiry time for the new user account.</span></span>

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

### <span data-ttu-id="7e88f-134">-IsAdmin</span><span class="sxs-lookup"><span data-stu-id="7e88f-134">-IsAdmin</span></span>
<span data-ttu-id="7e88f-135">Anger att cmdleten skapar ett användar konto som har administratörs behörighet.</span><span class="sxs-lookup"><span data-stu-id="7e88f-135">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

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

### <span data-ttu-id="7e88f-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="7e88f-136">-Name</span></span>
<span data-ttu-id="7e88f-137">Anger namnet på det nya lokala Windows-kontot.</span><span class="sxs-lookup"><span data-stu-id="7e88f-137">Specifies the name of the new local Windows account.</span></span>

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

### <span data-ttu-id="7e88f-138">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="7e88f-138">-Password</span></span>
<span data-ttu-id="7e88f-139">Anger lösen ordet för användar kontot.</span><span class="sxs-lookup"><span data-stu-id="7e88f-139">Specifies the user account password.</span></span>

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

### <span data-ttu-id="7e88f-140">-PoolId</span><span class="sxs-lookup"><span data-stu-id="7e88f-140">-PoolId</span></span>
<span data-ttu-id="7e88f-141">Anger ID: t för poolen som innehåller den datornod där användar kontot ska skapas.</span><span class="sxs-lookup"><span data-stu-id="7e88f-141">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

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

### <span data-ttu-id="7e88f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e88f-142">CommonParameters</span></span>
<span data-ttu-id="7e88f-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e88f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e88f-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e88f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e88f-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e88f-145">INPUTS</span></span>

### <span data-ttu-id="7e88f-146">Microsoft.Azure.Commands.BatCH. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="7e88f-146">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="7e88f-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7e88f-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7e88f-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e88f-148">OUTPUTS</span></span>

### <span data-ttu-id="7e88f-149">System. Void</span><span class="sxs-lookup"><span data-stu-id="7e88f-149">System.Void</span></span>

## <span data-ttu-id="7e88f-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e88f-150">NOTES</span></span>

## <span data-ttu-id="7e88f-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e88f-151">RELATED LINKS</span></span>

[<span data-ttu-id="7e88f-152">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="7e88f-152">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="7e88f-153">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="7e88f-153">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="7e88f-154">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="7e88f-154">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="7e88f-155">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="7e88f-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
