---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
ms.openlocfilehash: b04461caa9b3f10438706a5a2a2017eef3e71cb3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93755108"
---
# <span data-ttu-id="51feb-101">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="51feb-101">Get-AzBatchNodeFileContent</span></span>

## <span data-ttu-id="51feb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51feb-102">SYNOPSIS</span></span>
<span data-ttu-id="51feb-103">Hämtar en batchfil.</span><span class="sxs-lookup"><span data-stu-id="51feb-103">Gets a Batch node file.</span></span>

## <span data-ttu-id="51feb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51feb-104">SYNTAX</span></span>

### <span data-ttu-id="51feb-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="51feb-105">Task_Id_Path</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51feb-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="51feb-106">Task_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51feb-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="51feb-107">ComputeNode_Id_Path</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51feb-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="51feb-108">ComputeNode_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51feb-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="51feb-109">InputObject_Path</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="51feb-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="51feb-110">InputObject_Stream</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="51feb-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51feb-111">DESCRIPTION</span></span>
<span data-ttu-id="51feb-112">Cmdleten **Get-AzBatchNodeFileContent** hämtar en Azure-batchfil och sparar den som en fil eller en ström.</span><span class="sxs-lookup"><span data-stu-id="51feb-112">The **Get-AzBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="51feb-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51feb-113">EXAMPLES</span></span>

### <span data-ttu-id="51feb-114">Exempel 1: Hämta en zonfil som är kopplad till en aktivitet och spara filen</span><span class="sxs-lookup"><span data-stu-id="51feb-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="51feb-115">Det här kommandot får den zonfil som heter StdOut.txt och sparar den i E:\PowerShell\StdOut.txt fil Sök vägen på den lokala datorn.</span><span class="sxs-lookup"><span data-stu-id="51feb-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="51feb-116">StdOut.txt-nodadressen är kopplad till en aktivitet som har ID-Task01 för jobbet som har ID-Job01.</span><span class="sxs-lookup"><span data-stu-id="51feb-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="51feb-117">Använd Get-AzBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="51feb-117">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="51feb-118">Exempel 2: Hämta en batchfil och spara den på en angiven fil Sök väg med förloppet</span><span class="sxs-lookup"><span data-stu-id="51feb-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="51feb-119">Det här kommandot får den zonfil som heter StdErr.txt genom att använda Get-AzBatchNodeFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51feb-119">This command gets the node file that is named StdErr.txt by using the Get-AzBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="51feb-120">Kommandot skickar filen till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="51feb-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="51feb-121">Den aktuella cmdleten sparar filen i E:\PowerShell\StdOut.txt fil Sök väg på den lokala datorn.</span><span class="sxs-lookup"><span data-stu-id="51feb-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="51feb-122">StdOut.txt-nodadressen är kopplad till aktiviteten som har ID-Task02 för jobbet som har ID Job02.</span><span class="sxs-lookup"><span data-stu-id="51feb-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="51feb-123">Exempel 3: Hämta en batchjournal som är kopplad till en aktivitet och dirigera den till en ström</span><span class="sxs-lookup"><span data-stu-id="51feb-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="51feb-124">Det första kommandot skapar en ström genom att använda New-Object cmdlet och lagrar den i $Stream-variabeln.</span><span class="sxs-lookup"><span data-stu-id="51feb-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="51feb-125">Det andra kommandot får den zonfil som heter StdOut.txt från aktiviteten som har ID-Task11 för jobbet som har ID-Job03.</span><span class="sxs-lookup"><span data-stu-id="51feb-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="51feb-126">Kommandot dirigerar fil innehåll till strömmen i $Stream.</span><span class="sxs-lookup"><span data-stu-id="51feb-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="51feb-127">Exempel 4: Hämta en zonfil från en datornod och spara den</span><span class="sxs-lookup"><span data-stu-id="51feb-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="51feb-128">Med det här kommandot får du Startup\StdOut.txt Node-noden som innehåller ID-ComputeNode01 i poolen som har ID Pool01.</span><span class="sxs-lookup"><span data-stu-id="51feb-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="51feb-129">Kommandot sparar filen i E:\PowerShell\StdOut.txt fil Sök väg på den lokala datorn.</span><span class="sxs-lookup"><span data-stu-id="51feb-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="51feb-130">Exempel 5: Hämta en zonfil från en datornod och spara den med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="51feb-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="51feb-131">Det här kommandot får Startup\StdOut.txt med den här noden genom att använda Get-AzBatchNodeFile från noden Compute som har ID-ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="51feb-131">This command gets the node file Startup\StdOut.txt by using Get-AzBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="51feb-132">Noden Compute finns i poolen med ID-Pool01.</span><span class="sxs-lookup"><span data-stu-id="51feb-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="51feb-133">Kommandot skickar den noden till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="51feb-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="51feb-134">Denna cmdlet sparar filen i E:\PowerShell\StdOut.txt fil Sök väg på den lokala datorn.</span><span class="sxs-lookup"><span data-stu-id="51feb-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="51feb-135">Exempel 6: Hämta en zonfil från en datornod och dirigera den till en ström</span><span class="sxs-lookup"><span data-stu-id="51feb-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="51feb-136">Det första kommandot skapar en ström genom att använda New-Object cmdlet och lagrar den i $Stream-variabeln.</span><span class="sxs-lookup"><span data-stu-id="51feb-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="51feb-137">Det andra kommandot får den nod som heter StdOut.txt från noden Compute och som har ID-ComputeNode01 i poolen som har ID Pool01.</span><span class="sxs-lookup"><span data-stu-id="51feb-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="51feb-138">Kommandot dirigerar fil innehåll till strömmen i $Stream.</span><span class="sxs-lookup"><span data-stu-id="51feb-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="51feb-139">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51feb-139">PARAMETERS</span></span>

### <span data-ttu-id="51feb-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="51feb-140">-BatchContext</span></span>
<span data-ttu-id="51feb-141">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="51feb-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="51feb-142">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="51feb-142">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="51feb-143">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="51feb-143">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="51feb-144">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="51feb-144">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="51feb-145">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="51feb-145">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="51feb-146">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="51feb-146">-ByteRangeEnd</span></span>
<span data-ttu-id="51feb-147">Slutet på byte-området som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="51feb-147">The end of the byte range to be downloaded.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51feb-148">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="51feb-148">-ByteRangeStart</span></span>
<span data-ttu-id="51feb-149">Början på byte-området som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="51feb-149">The start of the byte range to be downloaded.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51feb-150">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="51feb-150">-ComputeNodeId</span></span>
<span data-ttu-id="51feb-151">Anger ID för den datornod som innehåller den zonfil som cmdleten returnerar.</span><span class="sxs-lookup"><span data-stu-id="51feb-151">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51feb-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51feb-152">-DefaultProfile</span></span>
<span data-ttu-id="51feb-153">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="51feb-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51feb-154">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="51feb-154">-DestinationPath</span></span>
<span data-ttu-id="51feb-155">Anger sökvägen till den plats där denna cmdlet sparar zonfilen.</span><span class="sxs-lookup"><span data-stu-id="51feb-155">Specifies the file path where this cmdlet saves the node file.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, ComputeNode_Id_Path, InputObject_Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51feb-156">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="51feb-156">-DestinationStream</span></span>
<span data-ttu-id="51feb-157">Anger i vilken ström den här cmdleten skriver fil innehållet.</span><span class="sxs-lookup"><span data-stu-id="51feb-157">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="51feb-158">Denna cmdlet stänger inte eller spolar inte tillbaka strömmen.</span><span class="sxs-lookup"><span data-stu-id="51feb-158">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: System.IO.Stream
Parameter Sets: Task_Id_Stream, ComputeNode_Id_Stream, InputObject_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51feb-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51feb-159">-InputObject</span></span>
<span data-ttu-id="51feb-160">Anger filen som den här cmdleten får, som ett **PSNodeFile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="51feb-160">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="51feb-161">Använd Get-AzBatchNodeFile cmdlet för att hämta ett nod fil objekt.</span><span class="sxs-lookup"><span data-stu-id="51feb-161">To obtain a node file object, use the Get-AzBatchNodeFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51feb-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="51feb-162">-JobId</span></span>
<span data-ttu-id="51feb-163">Anger ID för jobbet som innehåller mål uppgiften.</span><span class="sxs-lookup"><span data-stu-id="51feb-163">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51feb-164">-Path</span><span class="sxs-lookup"><span data-stu-id="51feb-164">-Path</span></span>
<span data-ttu-id="51feb-165">Sökvägen till den nod som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="51feb-165">The path of the node file to download.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51feb-166">-PoolId</span><span class="sxs-lookup"><span data-stu-id="51feb-166">-PoolId</span></span>
<span data-ttu-id="51feb-167">Anger ID för den pool som innehåller den datornod som innehåller den zonfil som cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="51feb-167">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51feb-168">-TaskId</span><span class="sxs-lookup"><span data-stu-id="51feb-168">-TaskId</span></span>
<span data-ttu-id="51feb-169">Anger aktivitetens ID.</span><span class="sxs-lookup"><span data-stu-id="51feb-169">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51feb-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51feb-170">CommonParameters</span></span>
<span data-ttu-id="51feb-171">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51feb-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51feb-172">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51feb-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51feb-173">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51feb-173">INPUTS</span></span>

### <span data-ttu-id="51feb-174">System. String</span><span class="sxs-lookup"><span data-stu-id="51feb-174">System.String</span></span>

### <span data-ttu-id="51feb-175">Microsoft.Azure.Commands.BatCH. Modeller. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="51feb-175">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="51feb-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="51feb-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="51feb-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51feb-177">OUTPUTS</span></span>

### <span data-ttu-id="51feb-178">System. Void</span><span class="sxs-lookup"><span data-stu-id="51feb-178">System.Void</span></span>

## <span data-ttu-id="51feb-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51feb-179">NOTES</span></span>

## <span data-ttu-id="51feb-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51feb-180">RELATED LINKS</span></span>

[<span data-ttu-id="51feb-181">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="51feb-181">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="51feb-182">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="51feb-182">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="51feb-183">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="51feb-183">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


