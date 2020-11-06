---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 6289aa916b4d03559fccb11ea0a8897f4b506b53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578487"
---
# <span data-ttu-id="b427d-101">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="b427d-101">New-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="b427d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b427d-102">SYNOPSIS</span></span>
<span data-ttu-id="b427d-103">Skapar ett användar konto i en batch-datornod.</span><span class="sxs-lookup"><span data-stu-id="b427d-103">Creates a user account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b427d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b427d-104">SYNTAX</span></span>

### <span data-ttu-id="b427d-105">Et</span><span class="sxs-lookup"><span data-stu-id="b427d-105">Id</span></span>
```
New-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <String>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b427d-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="b427d-106">ParentObject</span></span>
```
New-AzureBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <String>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b427d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b427d-107">DESCRIPTION</span></span>
<span data-ttu-id="b427d-108">Cmdleten **New-AzureBatchComputeNodeUser** skapar ett användar konto på en Azure Batch-datornod.</span><span class="sxs-lookup"><span data-stu-id="b427d-108">The **New-AzureBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="b427d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b427d-109">EXAMPLES</span></span>

### <span data-ttu-id="b427d-110">Exempel 1: skapa ett användar konto med administratörs behörighet</span><span class="sxs-lookup"><span data-stu-id="b427d-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzureBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="b427d-111">Det här kommandot skapar ett användar konto på noden Compute som har ID-ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="b427d-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="b427d-112">Noden finns i poolen med ID-MyPool01.</span><span class="sxs-lookup"><span data-stu-id="b427d-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="b427d-113">Användar namnet är TestUser, lösen ordet är lösen ord, kontot upphör att gälla om sju dagar och kontot har administratörs behörighet.</span><span class="sxs-lookup"><span data-stu-id="b427d-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="b427d-114">Exempel 2: skapa ett användar konto på en datornod med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="b427d-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzureBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="b427d-115">Det här kommandot får Compute-noden med namnet ComputeNode01 med hjälp av cmdleten **Get-AzureBatchComputeNode** .</span><span class="sxs-lookup"><span data-stu-id="b427d-115">This command gets the compute node named ComputeNode01 by using the **Get-AzureBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="b427d-116">Noden finns i poolen med ID-MyPool01.</span><span class="sxs-lookup"><span data-stu-id="b427d-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="b427d-117">Kommandot skickar den beräknade noden till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="b427d-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b427d-118">Kommandot skapar ett användar konto med användar namnet TestUserand lösen ord.</span><span class="sxs-lookup"><span data-stu-id="b427d-118">The command creates a user account that has the user name TestUserand the password Password.</span></span>

## <span data-ttu-id="b427d-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b427d-119">PARAMETERS</span></span>

### <span data-ttu-id="b427d-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b427d-120">-BatchContext</span></span>
<span data-ttu-id="b427d-121">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b427d-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b427d-122">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="b427d-122">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="b427d-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="b427d-123">-ComputeNode</span></span>
<span data-ttu-id="b427d-124">Anger noden Compute, som ett **PSComputeNode** -objekt, där denna cmdlet skapar ett användar konto.</span><span class="sxs-lookup"><span data-stu-id="b427d-124">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="b427d-125">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="b427d-125">-ComputeNodeId</span></span>
<span data-ttu-id="b427d-126">Anger ID för den datornod där denna cmdlet skapar ett användar konto.</span><span class="sxs-lookup"><span data-stu-id="b427d-126">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="b427d-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b427d-127">-ExpiryTime</span></span>
<span data-ttu-id="b427d-128">Anger sista giltighets tiden för det nya kontot.</span><span class="sxs-lookup"><span data-stu-id="b427d-128">Specifies the expiry time for the new user account.</span></span>

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

### <span data-ttu-id="b427d-129">-IsAdmin</span><span class="sxs-lookup"><span data-stu-id="b427d-129">-IsAdmin</span></span>
<span data-ttu-id="b427d-130">Anger att cmdleten skapar ett användar konto som har administratörs behörighet.</span><span class="sxs-lookup"><span data-stu-id="b427d-130">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

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

### <span data-ttu-id="b427d-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="b427d-131">-Name</span></span>
<span data-ttu-id="b427d-132">Anger namnet på det nya lokala Windows-kontot.</span><span class="sxs-lookup"><span data-stu-id="b427d-132">Specifies the name of the new local Windows account.</span></span>

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

### <span data-ttu-id="b427d-133">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="b427d-133">-Password</span></span>
<span data-ttu-id="b427d-134">Anger lösen ordet för användar kontot.</span><span class="sxs-lookup"><span data-stu-id="b427d-134">Specifies the user account password.</span></span>

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

### <span data-ttu-id="b427d-135">-PoolId</span><span class="sxs-lookup"><span data-stu-id="b427d-135">-PoolId</span></span>
<span data-ttu-id="b427d-136">Anger ID: t för poolen som innehåller den datornod där användar kontot ska skapas.</span><span class="sxs-lookup"><span data-stu-id="b427d-136">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

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

### <span data-ttu-id="b427d-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b427d-137">-DefaultProfile</span></span>
<span data-ttu-id="b427d-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b427d-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b427d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b427d-139">CommonParameters</span></span>
<span data-ttu-id="b427d-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b427d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b427d-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b427d-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b427d-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b427d-142">INPUTS</span></span>

### <span data-ttu-id="b427d-143">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b427d-143">BatchAccountContext</span></span>
<span data-ttu-id="b427d-144">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="b427d-144">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="b427d-145">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="b427d-145">PSComputeNode</span></span>
<span data-ttu-id="b427d-146">Parametern ' ComputeNode ' godkänner värdet av typen ' PSComputeNode ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="b427d-146">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="b427d-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b427d-147">OUTPUTS</span></span>

## <span data-ttu-id="b427d-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b427d-148">NOTES</span></span>

## <span data-ttu-id="b427d-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b427d-149">RELATED LINKS</span></span>

[<span data-ttu-id="b427d-150">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b427d-150">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b427d-151">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="b427d-151">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="b427d-152">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="b427d-152">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="b427d-153">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="b427d-153">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


