---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 38ED2854-23D0-400E-A5C8-239346B2AF99
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
ms.openlocfilehash: 3337cfa2423d6bc3a26c96ea734ce517f2707a04
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93755109"
---
# <span data-ttu-id="61a2b-101">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="61a2b-101">Get-AzBatchNodeFile</span></span>

## <span data-ttu-id="61a2b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="61a2b-102">SYNOPSIS</span></span>
<span data-ttu-id="61a2b-103">Hämtar egenskaperna för kommandofiler.</span><span class="sxs-lookup"><span data-stu-id="61a2b-103">Gets the properties of Batch node files.</span></span>

## <span data-ttu-id="61a2b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="61a2b-104">SYNTAX</span></span>

### <span data-ttu-id="61a2b-105">ComputeNode_Id (standard)</span><span class="sxs-lookup"><span data-stu-id="61a2b-105">ComputeNode_Id (Default)</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [[-Path] <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61a2b-106">Task_Id</span><span class="sxs-lookup"><span data-stu-id="61a2b-106">Task_Id</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [[-Path] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61a2b-107">Task_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="61a2b-107">Task_ODataFilter</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61a2b-108">ParentTask</span><span class="sxs-lookup"><span data-stu-id="61a2b-108">ParentTask</span></span>
```
Get-AzBatchNodeFile [[-Task] <PSCloudTask>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61a2b-109">ComputeNode_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="61a2b-109">ComputeNode_ODataFilter</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Recursive] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="61a2b-110">ParentComputeNode</span><span class="sxs-lookup"><span data-stu-id="61a2b-110">ParentComputeNode</span></span>
```
Get-AzBatchNodeFile [[-ComputeNode] <PSComputeNode>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61a2b-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="61a2b-111">DESCRIPTION</span></span>
<span data-ttu-id="61a2b-112">Cmdleten **Get-AzBatchNodeFile** hämtar egenskaperna för Azure-gruppnoden för en aktivitet eller en datornod.</span><span class="sxs-lookup"><span data-stu-id="61a2b-112">The **Get-AzBatchNodeFile** cmdlet gets the properties of the Azure Batch node files of a task or compute node.</span></span>
<span data-ttu-id="61a2b-113">Du kan begränsa resultaten genom att ange ett filter för Open data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="61a2b-113">To narrow your results, you can specify an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="61a2b-114">Om du anger en aktivitet men inte ett filter returnerar denna cmdlet egenskaper för den aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="61a2b-114">If you specify a task, but not a filter, this cmdlet returns properties for all node files for that task.</span></span>
<span data-ttu-id="61a2b-115">Om du anger en datornod men inte ett filter returnerar denna cmdlet egenskaper för alla filer för den beräknade noden.</span><span class="sxs-lookup"><span data-stu-id="61a2b-115">If you specify a compute node, but not a filter, this cmdlet returns properties for all node files for that compute node.</span></span>

## <span data-ttu-id="61a2b-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="61a2b-116">EXAMPLES</span></span>

### <span data-ttu-id="61a2b-117">Exempel 1: Hämta egenskaperna för en datornod som är kopplad till en aktivitet</span><span class="sxs-lookup"><span data-stu-id="61a2b-117">Example 1: Get the properties of a node file associated with a task</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "Stdout.txt" -BatchContext $Context
IsDirectory Name          Properties                                      Url

----------- ----          ----------                                      ---

False       StdOut.txt    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="61a2b-118">Det här kommandot får egenskaperna för StdOut.txt-nodadressen som är kopplad till den aktivitet som har ID-Task26 i jobbet som har ID-000001.</span><span class="sxs-lookup"><span data-stu-id="61a2b-118">This command gets the properties of the StdOut.txt node file associated with the task that has the ID Task26 in the job that has the ID Job-000001.</span></span>
<span data-ttu-id="61a2b-119">Använd Get-AzBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="61a2b-119">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="61a2b-120">Exempel 2: Hämta egenskaperna för Node-filer som associeras med en aktivitet med hjälp av ett filter</span><span class="sxs-lookup"><span data-stu-id="61a2b-120">Example 2: Get the properties of node files associated with a task by using a filter</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-00002" -TaskId "Task26" -Filter "startswith(name,'St')" -BatchContext $Context
IsDirectory Name        Properties                                      Url

----------- ----        ----------                                      ---

False       StdErr.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="61a2b-121">Det här kommandot får egenskaperna för de nodnamn vars namn börjar med St och är associerade med en aktivitet som har ID-Task26 under jobb med ID-00002.</span><span class="sxs-lookup"><span data-stu-id="61a2b-121">This command gets the properties of the node files whose names start with st and are associated with task that has the ID Task26 under job that has the ID Job-00002.</span></span>

### <span data-ttu-id="61a2b-122">Exempel 3: Hämta egenskaperna för nodnamn rekursivt för en aktivitet</span><span class="sxs-lookup"><span data-stu-id="61a2b-122">Example 3: Recursively get the properties of node files associated with a task</span></span>
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

<span data-ttu-id="61a2b-123">Det här kommandot får egenskaperna för alla filer som är kopplade till aktiviteten som har ID-Task31 i jobbet jobb-00003.</span><span class="sxs-lookup"><span data-stu-id="61a2b-123">This command gets the properties of all files associated with the task that has the ID Task31 in job Job-00003.</span></span>
<span data-ttu-id="61a2b-124">Det här kommandot anger den *rekursiva* parametern.</span><span class="sxs-lookup"><span data-stu-id="61a2b-124">This command specifies the *Recursive* parameter.</span></span>
<span data-ttu-id="61a2b-125">Därför utförs en rekursiv fil ökning och returnerar wd\newFile.txt-filen.</span><span class="sxs-lookup"><span data-stu-id="61a2b-125">Therefore, the cmdlet performs a recursive file search is performed, and returns the wd\newFile.txt node file.</span></span>

### <span data-ttu-id="61a2b-126">Exempel 4: Hämta en fil från en datornod</span><span class="sxs-lookup"><span data-stu-id="61a2b-126">Example 4: Get a single file from a compute node</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context
IsDirectory Name                    Properties                                      Url
----------- ----                    ----------                                      ---
False       startup\stdout.txt      Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="61a2b-127">Det här kommandot hämtar filen som heter Startup\StdOut.txt från noden Compute och som har ID-ComputeNode01 i poolen som har ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="61a2b-127">This command gets the file that is named Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

### <span data-ttu-id="61a2b-128">Exempel 5: Hämta alla filer under en mapp från en datornod</span><span class="sxs-lookup"><span data-stu-id="61a2b-128">Example 5: Get all files under a folder from a compute node</span></span>
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

<span data-ttu-id="61a2b-129">Det här kommandot får alla filer under startmappen från Compute-noden som har ID-ComputeNode01 i poolen som har ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="61a2b-129">This command gets all the files under the startup folder from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>
<span data-ttu-id="61a2b-130">Denna cmdlet anger den *rekursiva* parametern.</span><span class="sxs-lookup"><span data-stu-id="61a2b-130">This cmdlet specifies the *Recursive* parameter.</span></span>

### <span data-ttu-id="61a2b-131">Exempel 6: Hämta filer från rotmappen för en datornod</span><span class="sxs-lookup"><span data-stu-id="61a2b-131">Example 6: Get files from the root folder of a compute node</span></span>
```
PS C:\>Get-AzBatchComputeNode "Pool22" -Id "ComputeNode01" -BatchContext $Context | Get-AzBatchNodeFile -BatchContext $Context
IsDirectory Name           Properties       Url
----------- ----           ----------       ---
True        shared                          https://cmdletexample.westus.Batch.contoso... 
True        startup                         https://cmdletexample.westus.Batch.contoso... 
True        workitems                       https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="61a2b-132">Det här kommandot får alla filer i rotmappen för Compute-noden som har ID-ComputeNode01 i poolen som har ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="61a2b-132">This command gets all the files at the root folder of the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

## <span data-ttu-id="61a2b-133">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="61a2b-133">PARAMETERS</span></span>

### <span data-ttu-id="61a2b-134">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="61a2b-134">-BatchContext</span></span>
<span data-ttu-id="61a2b-135">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="61a2b-135">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="61a2b-136">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="61a2b-136">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="61a2b-137">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="61a2b-137">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="61a2b-138">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="61a2b-138">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="61a2b-139">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="61a2b-139">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="61a2b-140">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="61a2b-140">-ComputeNode</span></span>
<span data-ttu-id="61a2b-141">Anger noden Compute, som ett **PSComputeNode** -objekt, som innehåller batchattributet-filerna.</span><span class="sxs-lookup"><span data-stu-id="61a2b-141">Specifies the compute node, as a **PSComputeNode** object, that contains the Batch node files.</span></span>
<span data-ttu-id="61a2b-142">Använd cmdleten Get-AzBatchComputeNode för att hämta ett Compute Node-objekt.</span><span class="sxs-lookup"><span data-stu-id="61a2b-142">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="61a2b-143">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="61a2b-143">-ComputeNodeId</span></span>
<span data-ttu-id="61a2b-144">Anger ID för den datornod som innehåller batchattributet-filerna.</span><span class="sxs-lookup"><span data-stu-id="61a2b-144">Specifies the ID of the compute node that contains the Batch node files.</span></span>

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

### <span data-ttu-id="61a2b-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61a2b-145">-DefaultProfile</span></span>
<span data-ttu-id="61a2b-146">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="61a2b-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61a2b-147">-Filter</span><span class="sxs-lookup"><span data-stu-id="61a2b-147">-Filter</span></span>
<span data-ttu-id="61a2b-148">Anger en OData filter-sats.</span><span class="sxs-lookup"><span data-stu-id="61a2b-148">Specifies an OData filter clause.</span></span>
<span data-ttu-id="61a2b-149">Denna cmdlet returnerar egenskaper för de zonfiler som matchar det filter som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="61a2b-149">This cmdlet returns properties for node files that match the filter that this parameter specifies.</span></span>

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

### <span data-ttu-id="61a2b-150">-JobId</span><span class="sxs-lookup"><span data-stu-id="61a2b-150">-JobId</span></span>
<span data-ttu-id="61a2b-151">Anger ID för jobbet som innehåller mål uppgiften.</span><span class="sxs-lookup"><span data-stu-id="61a2b-151">Specifies the ID of the job that contains the target task.</span></span>

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

### <span data-ttu-id="61a2b-152">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="61a2b-152">-MaxCount</span></span>
<span data-ttu-id="61a2b-153">Anger det maximala antalet nodtyper som denna cmdlet returnerar egenskaper för.</span><span class="sxs-lookup"><span data-stu-id="61a2b-153">Specifies the maximum number of node files for which this cmdlet returns properties.</span></span>
<span data-ttu-id="61a2b-154">Om du anger ett värde som är noll (0) eller mindre används ingen övre gräns av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="61a2b-154">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="61a2b-155">Standardvärdet är 1000.</span><span class="sxs-lookup"><span data-stu-id="61a2b-155">The default value is 1000.</span></span>

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

### <span data-ttu-id="61a2b-156">-Path</span><span class="sxs-lookup"><span data-stu-id="61a2b-156">-Path</span></span>
<span data-ttu-id="61a2b-157">Anger sökvägen till den nod som den här cmdleten hämtar egenskaper för.</span><span class="sxs-lookup"><span data-stu-id="61a2b-157">Specifies the path of the node file for which this cmdlet retrieves properties.</span></span>
<span data-ttu-id="61a2b-158">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="61a2b-158">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="61a2b-159">-PoolId</span><span class="sxs-lookup"><span data-stu-id="61a2b-159">-PoolId</span></span>
<span data-ttu-id="61a2b-160">Anger ID för poolen som innehåller den datornod från vilken du vill hämta egenskaper för Node-filer.</span><span class="sxs-lookup"><span data-stu-id="61a2b-160">Specifies the ID of the pool that contains the compute node from which to get properties of node files.</span></span>

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

### <span data-ttu-id="61a2b-161">-Rekursivt</span><span class="sxs-lookup"><span data-stu-id="61a2b-161">-Recursive</span></span>
<span data-ttu-id="61a2b-162">Anger att denna cmdlet returnerar en rekursiv lista över filer.</span><span class="sxs-lookup"><span data-stu-id="61a2b-162">Indicates that this cmdlet returns a recursive list of files.</span></span>
<span data-ttu-id="61a2b-163">Annars returneras bara filerna i rotmappen.</span><span class="sxs-lookup"><span data-stu-id="61a2b-163">Otherwise, it returns only the files in the root folder.</span></span>

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

### <span data-ttu-id="61a2b-164">-Aktivitets</span><span class="sxs-lookup"><span data-stu-id="61a2b-164">-Task</span></span>
<span data-ttu-id="61a2b-165">Anger aktiviteten, som ett **PSCloudTask** -objekt, som Node-filerna är associerade med.</span><span class="sxs-lookup"><span data-stu-id="61a2b-165">Specifies the task, as a **PSCloudTask** object, with which the node files are associated.</span></span>
<span data-ttu-id="61a2b-166">Använd cmdleten Get-AzBatchTask för att få ett aktivitets objekt.</span><span class="sxs-lookup"><span data-stu-id="61a2b-166">To obtain a task object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="61a2b-167">-TaskId</span><span class="sxs-lookup"><span data-stu-id="61a2b-167">-TaskId</span></span>
<span data-ttu-id="61a2b-168">Anger ID för den aktivitet som den här cmdleten får egenskaper för.</span><span class="sxs-lookup"><span data-stu-id="61a2b-168">Specifies the ID of the task for which this cmdlet gets properties of node files.</span></span>

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

### <span data-ttu-id="61a2b-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61a2b-169">CommonParameters</span></span>
<span data-ttu-id="61a2b-170">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61a2b-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61a2b-171">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61a2b-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61a2b-172">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="61a2b-172">INPUTS</span></span>

### <span data-ttu-id="61a2b-173">System. String</span><span class="sxs-lookup"><span data-stu-id="61a2b-173">System.String</span></span>

### <span data-ttu-id="61a2b-174">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="61a2b-174">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="61a2b-175">Microsoft.Azure.Commands.BatCH. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="61a2b-175">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="61a2b-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="61a2b-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="61a2b-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="61a2b-177">OUTPUTS</span></span>

### <span data-ttu-id="61a2b-178">Microsoft.Azure.Commands.BatCH. Modeller. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="61a2b-178">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

## <span data-ttu-id="61a2b-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="61a2b-179">NOTES</span></span>

## <span data-ttu-id="61a2b-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="61a2b-180">RELATED LINKS</span></span>

[<span data-ttu-id="61a2b-181">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="61a2b-181">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="61a2b-182">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="61a2b-182">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="61a2b-183">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="61a2b-183">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="61a2b-184">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="61a2b-184">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="61a2b-185">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="61a2b-185">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


