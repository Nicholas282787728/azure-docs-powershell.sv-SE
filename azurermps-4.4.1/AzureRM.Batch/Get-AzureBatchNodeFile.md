---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 38ED2854-23D0-400E-A5C8-239346B2AF99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFile.md
ms.openlocfilehash: 0a027bd15d4b207baf9c69fcb9104428c2881872
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757317"
---
# <span data-ttu-id="14b1a-101">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="14b1a-101">Get-AzureBatchNodeFile</span></span>

## <span data-ttu-id="14b1a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="14b1a-102">SYNOPSIS</span></span>
<span data-ttu-id="14b1a-103">Hämtar egenskaperna för kommandofiler.</span><span class="sxs-lookup"><span data-stu-id="14b1a-103">Gets the properties of Batch node files.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14b1a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="14b1a-104">SYNTAX</span></span>

### <span data-ttu-id="14b1a-105">ComputeNode_Id (standard)</span><span class="sxs-lookup"><span data-stu-id="14b1a-105">ComputeNode_Id (Default)</span></span>
```
Get-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [[-Name] <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14b1a-106">Task_Id</span><span class="sxs-lookup"><span data-stu-id="14b1a-106">Task_Id</span></span>
```
Get-AzureBatchNodeFile -JobId <String> -TaskId <String> [[-Name] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14b1a-107">Task_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="14b1a-107">Task_ODataFilter</span></span>
```
Get-AzureBatchNodeFile -JobId <String> -TaskId <String> [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14b1a-108">ParentTask</span><span class="sxs-lookup"><span data-stu-id="14b1a-108">ParentTask</span></span>
```
Get-AzureBatchNodeFile [[-Task] <PSCloudTask>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14b1a-109">ComputeNode_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="14b1a-109">ComputeNode_ODataFilter</span></span>
```
Get-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Recursive] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="14b1a-110">ParentComputeNode</span><span class="sxs-lookup"><span data-stu-id="14b1a-110">ParentComputeNode</span></span>
```
Get-AzureBatchNodeFile [[-ComputeNode] <PSComputeNode>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14b1a-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="14b1a-111">DESCRIPTION</span></span>
<span data-ttu-id="14b1a-112">Cmdleten **Get-AzureBatchNodeFile** hämtar egenskaperna för Azure-gruppnoden för en aktivitet eller en datornod.</span><span class="sxs-lookup"><span data-stu-id="14b1a-112">The **Get-AzureBatchNodeFile** cmdlet gets the properties of the Azure Batch node files of a task or compute node.</span></span>
<span data-ttu-id="14b1a-113">Du kan begränsa resultaten genom att ange ett filter för Open data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="14b1a-113">To narrow your results, you can specify an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="14b1a-114">Om du anger en aktivitet men inte ett filter returnerar denna cmdlet egenskaper för den aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="14b1a-114">If you specify a task, but not a filter, this cmdlet returns properties for all node files for that task.</span></span>
<span data-ttu-id="14b1a-115">Om du anger en datornod men inte ett filter returnerar denna cmdlet egenskaper för alla filer för den beräknade noden.</span><span class="sxs-lookup"><span data-stu-id="14b1a-115">If you specify a compute node, but not a filter, this cmdlet returns properties for all node files for that compute node.</span></span>

## <span data-ttu-id="14b1a-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="14b1a-116">EXAMPLES</span></span>

### <span data-ttu-id="14b1a-117">Exempel 1: Hämta egenskaperna för en datornod som är kopplad till en aktivitet</span><span class="sxs-lookup"><span data-stu-id="14b1a-117">Example 1: Get the properties of a node file associated with a task</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Name "Stdout.txt" -BatchContext $Context
IsDirectory Name          Properties                                      Url

----------- ----          ----------                                      ---

False       StdOut.txt    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="14b1a-118">Det här kommandot får egenskaperna för StdOut.txt-nodadressen som är kopplad till den aktivitet som har ID-Task26 i jobbet som har ID-000001.</span><span class="sxs-lookup"><span data-stu-id="14b1a-118">This command gets the properties of the StdOut.txt node file associated with the task that has the ID Task26 in the job that has the ID Job-000001.</span></span>
<span data-ttu-id="14b1a-119">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="14b1a-119">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="14b1a-120">Exempel 2: Hämta egenskaperna för Node-filer som associeras med en aktivitet med hjälp av ett filter</span><span class="sxs-lookup"><span data-stu-id="14b1a-120">Example 2: Get the properties of node files associated with a task by using a filter</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-00002" -TaskId "Task26" -Filter "startswith(name,'St')" -BatchContext $Context
IsDirectory Name        Properties                                      Url

----------- ----        ----------                                      ---

False       StdErr.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="14b1a-121">Det här kommandot får egenskaperna för de nodnamn vars namn börjar med St och är associerade med en aktivitet som har ID-Task26 under jobb med ID-00002.</span><span class="sxs-lookup"><span data-stu-id="14b1a-121">This command gets the properties of the node files whose names start with st and are associated with task that has the ID Task26 under job that has the ID Job-00002.</span></span>

### <span data-ttu-id="14b1a-122">Exempel 3: Hämta egenskaperna för nodnamn rekursivt för en aktivitet</span><span class="sxs-lookup"><span data-stu-id="14b1a-122">Example 3: Recursively get the properties of node files associated with a task</span></span>
```
PS C:\>Get-AzureBatchTask "Job-00003" "Task31" -BatchContext $Context | Get-AzureBatchNodeFile -Recursive -BatchContext $Context
IsDirectory Name             Properties                                      Url

----------- ----             ----------                                      ---

False       ProcessEnv.cmd   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdErr.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
True        wd                                                               https://cmdletexample.westus.Batch.contoso... 
False       wd\newFile.txt   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="14b1a-123">Det här kommandot får egenskaperna för alla filer som är kopplade till aktiviteten som har ID-Task31 i jobbet jobb-00003.</span><span class="sxs-lookup"><span data-stu-id="14b1a-123">This command gets the properties of all files associated with the task that has the ID Task31 in job Job-00003.</span></span>
<span data-ttu-id="14b1a-124">Det här kommandot anger den *rekursiva* parametern.</span><span class="sxs-lookup"><span data-stu-id="14b1a-124">This command specifies the *Recursive* parameter.</span></span>
<span data-ttu-id="14b1a-125">Därför utförs en rekursiv fil ökning och returnerar wd\newFile.txt-filen.</span><span class="sxs-lookup"><span data-stu-id="14b1a-125">Therefore, the cmdlet performs a recursive file search is performed, and returns the wd\newFile.txt node file.</span></span>

### <span data-ttu-id="14b1a-126">Exempel 4: Hämta en fil från en datornod</span><span class="sxs-lookup"><span data-stu-id="14b1a-126">Example 4: Get a single file from a compute node</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Name "Startup\StdOut.txt" -BatchContext $Context
IsDirectory Name                    Properties                                      Url
----------- ----                    ----------                                      ---
False       startup\stdout.txt      Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="14b1a-127">Det här kommandot hämtar filen som heter Startup\StdOut.txt från noden Compute och som har ID-ComputeNode01 i poolen som har ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="14b1a-127">This command gets the file that is named Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

### <span data-ttu-id="14b1a-128">Exempel 5: Hämta alla filer under en mapp från en datornod</span><span class="sxs-lookup"><span data-stu-id="14b1a-128">Example 5: Get all files under a folder from a compute node</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Filter "startswith(name,'startup')" -Recursive -BatchContext $Context
IsDirectory Name                      Properties                                      Url
----------- ----                      ----------                                      ---
True        startup                                                                   https://cmdletexample.westus.Batch.contoso... 
False       startup\ProcessEnv.cmd    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       startup\stderr.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       startup\stdout.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
True        startup\wd                                                                https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="14b1a-129">Det här kommandot får alla filer under startmappen från Compute-noden som har ID-ComputeNode01 i poolen som har ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="14b1a-129">This command gets all the files under the startup folder from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>
<span data-ttu-id="14b1a-130">Denna cmdlet anger den *rekursiva* parametern.</span><span class="sxs-lookup"><span data-stu-id="14b1a-130">This cmdlet specifies the *Recursive* parameter.</span></span>

### <span data-ttu-id="14b1a-131">Exempel 6: Hämta filer från rotmappen för en datornod</span><span class="sxs-lookup"><span data-stu-id="14b1a-131">Example 6: Get files from the root folder of a compute node</span></span>
```
PS C:\>Get-AzureBatchComputeNode "Pool22" -Id "ComputeNode01" -BatchContext $Context | Get-AzureBatchNodeFile -BatchContext $Context
IsDirectory Name           Properties       Url
----------- ----           ----------       ---
True        shared                          https://cmdletexample.westus.Batch.contoso... 
True        startup                         https://cmdletexample.westus.Batch.contoso... 
True        workitems                       https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="14b1a-132">Det här kommandot får alla filer i rotmappen för Compute-noden som har ID-ComputeNode01 i poolen som har ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="14b1a-132">This command gets all the files at the root folder of the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

## <span data-ttu-id="14b1a-133">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="14b1a-133">PARAMETERS</span></span>

### <span data-ttu-id="14b1a-134">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="14b1a-134">-BatchContext</span></span>
<span data-ttu-id="14b1a-135">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="14b1a-135">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="14b1a-136">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="14b1a-136">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="14b1a-137">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="14b1a-137">-ComputeNode</span></span>
<span data-ttu-id="14b1a-138">Anger noden Compute, som ett **PSComputeNode** -objekt, som innehåller batchattributet-filerna.</span><span class="sxs-lookup"><span data-stu-id="14b1a-138">Specifies the compute node, as a **PSComputeNode** object, that contains the Batch node files.</span></span>
<span data-ttu-id="14b1a-139">Använd cmdleten Get-AzureBatchComputeNode för att hämta ett Compute Node-objekt.</span><span class="sxs-lookup"><span data-stu-id="14b1a-139">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="14b1a-140">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="14b1a-140">-ComputeNodeId</span></span>
<span data-ttu-id="14b1a-141">Anger ID för den datornod som innehåller batchattributet-filerna.</span><span class="sxs-lookup"><span data-stu-id="14b1a-141">Specifies the ID of the compute node that contains the Batch node files.</span></span>

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

### <span data-ttu-id="14b1a-142">-Filter</span><span class="sxs-lookup"><span data-stu-id="14b1a-142">-Filter</span></span>
<span data-ttu-id="14b1a-143">Anger en OData filter-sats.</span><span class="sxs-lookup"><span data-stu-id="14b1a-143">Specifies an OData filter clause.</span></span>
<span data-ttu-id="14b1a-144">Denna cmdlet returnerar egenskaper för de zonfiler som matchar det filter som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="14b1a-144">This cmdlet returns properties for node files that match the filter that this parameter specifies.</span></span>

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

### <span data-ttu-id="14b1a-145">-JobId</span><span class="sxs-lookup"><span data-stu-id="14b1a-145">-JobId</span></span>
<span data-ttu-id="14b1a-146">Anger ID för jobbet som innehåller mål uppgiften.</span><span class="sxs-lookup"><span data-stu-id="14b1a-146">Specifies the ID of the job that contains the target task.</span></span>

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

### <span data-ttu-id="14b1a-147">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="14b1a-147">-MaxCount</span></span>
<span data-ttu-id="14b1a-148">Anger det maximala antalet nodtyper som denna cmdlet returnerar egenskaper för.</span><span class="sxs-lookup"><span data-stu-id="14b1a-148">Specifies the maximum number of node files for which this cmdlet returns properties.</span></span>
<span data-ttu-id="14b1a-149">Om du anger ett värde som är noll (0) eller mindre används ingen övre gräns av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="14b1a-149">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="14b1a-150">Standardvärdet är 1000.</span><span class="sxs-lookup"><span data-stu-id="14b1a-150">The default value is 1000.</span></span>

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

### <span data-ttu-id="14b1a-151">-Namn</span><span class="sxs-lookup"><span data-stu-id="14b1a-151">-Name</span></span>
<span data-ttu-id="14b1a-152">Anger namnet på den nod som den här cmdleten hämtar egenskaper för.</span><span class="sxs-lookup"><span data-stu-id="14b1a-152">Specifies the name of the node file for which this cmdlet retrieves properties.</span></span>
<span data-ttu-id="14b1a-153">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="14b1a-153">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, Task_Id
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b1a-154">-PoolId</span><span class="sxs-lookup"><span data-stu-id="14b1a-154">-PoolId</span></span>
<span data-ttu-id="14b1a-155">Anger ID för poolen som innehåller den datornod från vilken du vill hämta egenskaper för Node-filer.</span><span class="sxs-lookup"><span data-stu-id="14b1a-155">Specifies the ID of the pool that contains the compute node from which to get properties of node files.</span></span>

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

### <span data-ttu-id="14b1a-156">-Rekursivt</span><span class="sxs-lookup"><span data-stu-id="14b1a-156">-Recursive</span></span>
<span data-ttu-id="14b1a-157">Anger att denna cmdlet returnerar en rekursiv lista över filer.</span><span class="sxs-lookup"><span data-stu-id="14b1a-157">Indicates that this cmdlet returns a recursive list of files.</span></span>
<span data-ttu-id="14b1a-158">Annars returneras bara filerna i rotmappen.</span><span class="sxs-lookup"><span data-stu-id="14b1a-158">Otherwise, it returns only the files in the root folder.</span></span>

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

### <span data-ttu-id="14b1a-159">-Aktivitets</span><span class="sxs-lookup"><span data-stu-id="14b1a-159">-Task</span></span>
<span data-ttu-id="14b1a-160">Anger aktiviteten, som ett **PSCloudTask** -objekt, som Node-filerna är associerade med.</span><span class="sxs-lookup"><span data-stu-id="14b1a-160">Specifies the task, as a **PSCloudTask** object, with which the node files are associated.</span></span>
<span data-ttu-id="14b1a-161">Använd cmdleten Get-AzureBatchTask för att få ett aktivitets objekt.</span><span class="sxs-lookup"><span data-stu-id="14b1a-161">To obtain a task object, use the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="14b1a-162">-TaskId</span><span class="sxs-lookup"><span data-stu-id="14b1a-162">-TaskId</span></span>
<span data-ttu-id="14b1a-163">Anger ID för den aktivitet som den här cmdleten får egenskaper för.</span><span class="sxs-lookup"><span data-stu-id="14b1a-163">Specifies the ID of the task for which this cmdlet gets properties of node files.</span></span>

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

### <span data-ttu-id="14b1a-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14b1a-164">-DefaultProfile</span></span>
<span data-ttu-id="14b1a-165">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="14b1a-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14b1a-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14b1a-166">CommonParameters</span></span>
<span data-ttu-id="14b1a-167">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14b1a-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14b1a-168">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14b1a-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14b1a-169">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="14b1a-169">INPUTS</span></span>

### <span data-ttu-id="14b1a-170">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="14b1a-170">BatchAccountContext</span></span>
<span data-ttu-id="14b1a-171">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="14b1a-171">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="14b1a-172">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="14b1a-172">PSComputeNode</span></span>
<span data-ttu-id="14b1a-173">Parametern ' ComputeNode ' godkänner värdet av typen ' PSComputeNode ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="14b1a-173">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

### <span data-ttu-id="14b1a-174">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="14b1a-174">PSCloudTask</span></span>
<span data-ttu-id="14b1a-175">Parametern ' Task ' godkänner värdet av typen ' PSCloudTask ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="14b1a-175">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="14b1a-176">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="14b1a-176">OUTPUTS</span></span>

### <span data-ttu-id="14b1a-177">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="14b1a-177">PSNodeFile</span></span>

## <span data-ttu-id="14b1a-178">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="14b1a-178">NOTES</span></span>

## <span data-ttu-id="14b1a-179">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="14b1a-179">RELATED LINKS</span></span>

[<span data-ttu-id="14b1a-180">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="14b1a-180">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="14b1a-181">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="14b1a-181">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="14b1a-182">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="14b1a-182">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)

[<span data-ttu-id="14b1a-183">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="14b1a-183">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="14b1a-184">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="14b1a-184">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


