---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 38ED2854-23D0-400E-A5C8-239346B2AF99
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
ms.openlocfilehash: db8ef62a158edaa3a697af9f77e7932dfa18c096
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325356"
---
# <span data-ttu-id="ce8e0-101">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="ce8e0-101">Get-AzBatchNodeFile</span></span>

## <span data-ttu-id="ce8e0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce8e0-102">SYNOPSIS</span></span>
<span data-ttu-id="ce8e0-103">Hämtar egenskaperna för kommandofiler.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-103">Gets the properties of Batch node files.</span></span>

## <span data-ttu-id="ce8e0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce8e0-104">SYNTAX</span></span>

### <span data-ttu-id="ce8e0-105">ComputeNode_Id (standard)</span><span class="sxs-lookup"><span data-stu-id="ce8e0-105">ComputeNode_Id (Default)</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [[-Path] <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce8e0-106">Task_Id</span><span class="sxs-lookup"><span data-stu-id="ce8e0-106">Task_Id</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [[-Path] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce8e0-107">Task_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="ce8e0-107">Task_ODataFilter</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce8e0-108">ParentTask</span><span class="sxs-lookup"><span data-stu-id="ce8e0-108">ParentTask</span></span>
```
Get-AzBatchNodeFile [[-Task] <PSCloudTask>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce8e0-109">ComputeNode_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="ce8e0-109">ComputeNode_ODataFilter</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Recursive] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ce8e0-110">ParentComputeNode</span><span class="sxs-lookup"><span data-stu-id="ce8e0-110">ParentComputeNode</span></span>
```
Get-AzBatchNodeFile [[-ComputeNode] <PSComputeNode>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce8e0-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce8e0-111">DESCRIPTION</span></span>
<span data-ttu-id="ce8e0-112">Cmdleten **Get-AzBatchNodeFile** hämtar egenskaperna för Azure-gruppnoden för en aktivitet eller en datornod.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-112">The **Get-AzBatchNodeFile** cmdlet gets the properties of the Azure Batch node files of a task or compute node.</span></span>
<span data-ttu-id="ce8e0-113">Du kan begränsa resultaten genom att ange ett filter för Open data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="ce8e0-113">To narrow your results, you can specify an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="ce8e0-114">Om du anger en aktivitet men inte ett filter returnerar denna cmdlet egenskaper för den aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-114">If you specify a task, but not a filter, this cmdlet returns properties for all node files for that task.</span></span>
<span data-ttu-id="ce8e0-115">Om du anger en datornod men inte ett filter returnerar denna cmdlet egenskaper för alla filer för den beräknade noden.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-115">If you specify a compute node, but not a filter, this cmdlet returns properties for all node files for that compute node.</span></span>

## <span data-ttu-id="ce8e0-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce8e0-116">EXAMPLES</span></span>

### <span data-ttu-id="ce8e0-117">Exempel 1: Hämta egenskaperna för en datornod som är kopplad till en aktivitet</span><span class="sxs-lookup"><span data-stu-id="ce8e0-117">Example 1: Get the properties of a node file associated with a task</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "Stdout.txt" -BatchContext $Context
IsDirectory Name          Properties                                      Url

----------- ----          ----------                                      ---

False       StdOut.txt    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="ce8e0-118">Det här kommandot får egenskaperna för StdOut.txt-nodadressen som är kopplad till den aktivitet som har ID-Task26 i jobbet som har ID-000001.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-118">This command gets the properties of the StdOut.txt node file associated with the task that has the ID Task26 in the job that has the ID Job-000001.</span></span>
<span data-ttu-id="ce8e0-119">Använd Get-AzBatchAccountKey cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-119">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="ce8e0-120">Exempel 2: Hämta egenskaperna för Node-filer som associeras med en aktivitet med hjälp av ett filter</span><span class="sxs-lookup"><span data-stu-id="ce8e0-120">Example 2: Get the properties of node files associated with a task by using a filter</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-00002" -TaskId "Task26" -Filter "startswith(name,'St')" -BatchContext $Context
IsDirectory Name        Properties                                      Url

----------- ----        ----------                                      ---

False       StdErr.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       StdOut.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="ce8e0-121">Det här kommandot får egenskaperna för de nodnamn vars namn börjar med St och är associerade med en aktivitet som har ID-Task26 under jobb med ID-00002.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-121">This command gets the properties of the node files whose names start with st and are associated with task that has the ID Task26 under job that has the ID Job-00002.</span></span>

### <span data-ttu-id="ce8e0-122">Exempel 3: Hämta egenskaperna för nodnamn rekursivt för en aktivitet</span><span class="sxs-lookup"><span data-stu-id="ce8e0-122">Example 3: Recursively get the properties of node files associated with a task</span></span>
```
PS C:\>Get-AzBatchTask "Job-00003" "Task31" -BatchContext $Context | Get-AzBatchNodeFile -Recursive -BatchContext $Context
IsDirectory Name             Properties                                      Url

----------- ----             ----------                                      ---

False       ProcessEnv.cmd   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       StdErr.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       StdOut.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
True        wd                                                               https://cmdletexample.westus.Batch.contoso...
False       wd\newFile.txt   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="ce8e0-123">Det här kommandot får egenskaperna för alla filer som är kopplade till aktiviteten som har ID-Task31 i jobbet jobb-00003.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-123">This command gets the properties of all files associated with the task that has the ID Task31 in job Job-00003.</span></span>
<span data-ttu-id="ce8e0-124">Det här kommandot anger den *rekursiva* parametern.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-124">This command specifies the *Recursive* parameter.</span></span>
<span data-ttu-id="ce8e0-125">Därför utförs en rekursiv fil ökning och returnerar wd\newFile.txt-filen.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-125">Therefore, the cmdlet performs a recursive file search is performed, and returns the wd\newFile.txt node file.</span></span>

### <span data-ttu-id="ce8e0-126">Exempel 4: Hämta en fil från en datornod</span><span class="sxs-lookup"><span data-stu-id="ce8e0-126">Example 4: Get a single file from a compute node</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context
IsDirectory Name                    Properties                                      Url
----------- ----                    ----------                                      ---
False       startup\stdout.txt      Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="ce8e0-127">Det här kommandot hämtar filen som heter Startup\StdOut.txt från noden Compute och som har ID-ComputeNode01 i poolen som har ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-127">This command gets the file that is named Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

### <span data-ttu-id="ce8e0-128">Exempel 5: Hämta alla filer under en mapp från en datornod</span><span class="sxs-lookup"><span data-stu-id="ce8e0-128">Example 5: Get all files under a folder from a compute node</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Filter "startswith(name,'startup')" -Recursive -BatchContext $Context
IsDirectory Name                      Properties                                      Url
----------- ----                      ----------                                      ---
True        startup                                                                   https://cmdletexample.westus.Batch.contoso...
False       startup\ProcessEnv.cmd    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       startup\stderr.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       startup\stdout.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
True        startup\wd                                                                https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="ce8e0-129">Det här kommandot får alla filer under startmappen från Compute-noden som har ID-ComputeNode01 i poolen som har ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-129">This command gets all the files under the startup folder from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>
<span data-ttu-id="ce8e0-130">Denna cmdlet anger den *rekursiva* parametern.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-130">This cmdlet specifies the *Recursive* parameter.</span></span>

### <span data-ttu-id="ce8e0-131">Exempel 6: Hämta filer från rotmappen för en datornod</span><span class="sxs-lookup"><span data-stu-id="ce8e0-131">Example 6: Get files from the root folder of a compute node</span></span>
```
PS C:\>Get-AzBatchComputeNode "Pool22" -Id "ComputeNode01" -BatchContext $Context | Get-AzBatchNodeFile -BatchContext $Context
IsDirectory Name           Properties       Url
----------- ----           ----------       ---
True        shared                          https://cmdletexample.westus.Batch.contoso...
True        startup                         https://cmdletexample.westus.Batch.contoso...
True        workitems                       https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="ce8e0-132">Det här kommandot får alla filer i rotmappen för Compute-noden som har ID-ComputeNode01 i poolen som har ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-132">This command gets all the files at the root folder of the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

## <span data-ttu-id="ce8e0-133">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce8e0-133">PARAMETERS</span></span>

### <span data-ttu-id="ce8e0-134">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ce8e0-134">-BatchContext</span></span>
<span data-ttu-id="ce8e0-135">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-135">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ce8e0-136">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-136">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ce8e0-137">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-137">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ce8e0-138">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-138">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ce8e0-139">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-139">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ce8e0-140">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="ce8e0-140">-ComputeNode</span></span>
<span data-ttu-id="ce8e0-141">Anger noden Compute, som ett **PSComputeNode** -objekt, som innehåller batchattributet-filerna.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-141">Specifies the compute node, as a **PSComputeNode** object, that contains the Batch node files.</span></span>
<span data-ttu-id="ce8e0-142">Använd cmdleten Get-AzBatchComputeNode för att hämta ett Compute Node-objekt.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-142">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentComputeNode
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce8e0-143">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="ce8e0-143">-ComputeNodeId</span></span>
<span data-ttu-id="ce8e0-144">Anger ID för den datornod som innehåller batchattributet-filerna.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-144">Specifies the ID of the compute node that contains the Batch node files.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce8e0-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce8e0-145">-DefaultProfile</span></span>
<span data-ttu-id="ce8e0-146">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce8e0-147">-Filter</span><span class="sxs-lookup"><span data-stu-id="ce8e0-147">-Filter</span></span>
<span data-ttu-id="ce8e0-148">Anger en OData filter-sats.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-148">Specifies an OData filter clause.</span></span>
<span data-ttu-id="ce8e0-149">Denna cmdlet returnerar egenskaper för de zonfiler som matchar det filter som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-149">This cmdlet returns properties for node files that match the filter that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce8e0-150">-JobId</span><span class="sxs-lookup"><span data-stu-id="ce8e0-150">-JobId</span></span>
<span data-ttu-id="ce8e0-151">Anger ID för jobbet som innehåller mål uppgiften.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-151">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce8e0-152">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ce8e0-152">-MaxCount</span></span>
<span data-ttu-id="ce8e0-153">Anger det maximala antalet nodtyper som denna cmdlet returnerar egenskaper för.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-153">Specifies the maximum number of node files for which this cmdlet returns properties.</span></span>
<span data-ttu-id="ce8e0-154">Om du anger ett värde som är noll (0) eller mindre används ingen övre gräns av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-154">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="ce8e0-155">Standardvärdet är 1000.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-155">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce8e0-156">-Path</span><span class="sxs-lookup"><span data-stu-id="ce8e0-156">-Path</span></span>
<span data-ttu-id="ce8e0-157">Anger sökvägen till den nod som den här cmdleten hämtar egenskaper för.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-157">Specifies the path of the node file for which this cmdlet retrieves properties.</span></span>
<span data-ttu-id="ce8e0-158">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-158">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, Task_Id
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce8e0-159">-PoolId</span><span class="sxs-lookup"><span data-stu-id="ce8e0-159">-PoolId</span></span>
<span data-ttu-id="ce8e0-160">Anger ID för poolen som innehåller den datornod från vilken du vill hämta egenskaper för Node-filer.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-160">Specifies the ID of the pool that contains the compute node from which to get properties of node files.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce8e0-161">-Rekursivt</span><span class="sxs-lookup"><span data-stu-id="ce8e0-161">-Recursive</span></span>
<span data-ttu-id="ce8e0-162">Anger att denna cmdlet returnerar en rekursiv lista över filer.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-162">Indicates that this cmdlet returns a recursive list of files.</span></span>
<span data-ttu-id="ce8e0-163">Annars returneras bara filerna i rotmappen.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-163">Otherwise, it returns only the files in the root folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce8e0-164">-Aktivitets</span><span class="sxs-lookup"><span data-stu-id="ce8e0-164">-Task</span></span>
<span data-ttu-id="ce8e0-165">Anger aktiviteten, som ett **PSCloudTask** -objekt, som Node-filerna är associerade med.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-165">Specifies the task, as a **PSCloudTask** object, with which the node files are associated.</span></span>
<span data-ttu-id="ce8e0-166">Använd cmdleten Get-AzBatchTask för att få ett aktivitets objekt.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-166">To obtain a task object, use the Get-AzBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentTask
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce8e0-167">-TaskId</span><span class="sxs-lookup"><span data-stu-id="ce8e0-167">-TaskId</span></span>
<span data-ttu-id="ce8e0-168">Anger ID för den aktivitet som den här cmdleten får egenskaper för.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-168">Specifies the ID of the task for which this cmdlet gets properties of node files.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce8e0-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce8e0-169">CommonParameters</span></span>
<span data-ttu-id="ce8e0-170">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce8e0-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce8e0-171">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce8e0-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce8e0-172">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce8e0-172">INPUTS</span></span>

### <span data-ttu-id="ce8e0-173">System. String</span><span class="sxs-lookup"><span data-stu-id="ce8e0-173">System.String</span></span>

### <span data-ttu-id="ce8e0-174">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="ce8e0-174">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="ce8e0-175">Microsoft.Azure.Commands.BatCH. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="ce8e0-175">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="ce8e0-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ce8e0-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ce8e0-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce8e0-177">OUTPUTS</span></span>

### <span data-ttu-id="ce8e0-178">Microsoft.Azure.Commands.BatCH. Modeller. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="ce8e0-178">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

## <span data-ttu-id="ce8e0-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce8e0-179">NOTES</span></span>

## <span data-ttu-id="ce8e0-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce8e0-180">RELATED LINKS</span></span>

[<span data-ttu-id="ce8e0-181">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ce8e0-181">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ce8e0-182">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ce8e0-182">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="ce8e0-183">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="ce8e0-183">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="ce8e0-184">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="ce8e0-184">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="ce8e0-185">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="ce8e0-185">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
