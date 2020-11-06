---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
ms.openlocfilehash: 7795182ff1594c098a2afd778c137c48dc74c955
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579636"
---
# <span data-ttu-id="f6c32-101">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="f6c32-101">Get-AzureBatchNodeFileContent</span></span>

## <span data-ttu-id="f6c32-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6c32-102">SYNOPSIS</span></span>
<span data-ttu-id="f6c32-103">Hämtar en batchfil.</span><span class="sxs-lookup"><span data-stu-id="f6c32-103">Gets a Batch node file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6c32-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6c32-104">SYNTAX</span></span>

### <span data-ttu-id="f6c32-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="f6c32-105">Task_Id_Path</span></span>
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6c32-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="f6c32-106">Task_Id_Stream</span></span>
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6c32-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="f6c32-107">ComputeNode_Id_Path</span></span>
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6c32-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="f6c32-108">ComputeNode_Id_Stream</span></span>
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6c32-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="f6c32-109">InputObject_Path</span></span>
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f6c32-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="f6c32-110">InputObject_Stream</span></span>
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6c32-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6c32-111">DESCRIPTION</span></span>
<span data-ttu-id="f6c32-112">Cmdleten **Get-AzureBatchNodeFileContent** hämtar en Azure-batchfil och sparar den som en fil eller en ström.</span><span class="sxs-lookup"><span data-stu-id="f6c32-112">The **Get-AzureBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="f6c32-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6c32-113">EXAMPLES</span></span>

### <span data-ttu-id="f6c32-114">Exempel 1: Hämta en zonfil som är kopplad till en aktivitet och spara filen</span><span class="sxs-lookup"><span data-stu-id="f6c32-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzureBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="f6c32-115">Det här kommandot får den zonfil som heter StdOut.txt och sparar den i E:\PowerShell\StdOut.txt fil Sök vägen på den lokala datorn.</span><span class="sxs-lookup"><span data-stu-id="f6c32-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="f6c32-116">StdOut.txt-nodadressen är kopplad till en aktivitet som har ID-Task01 för jobbet som har ID-Job01.</span><span class="sxs-lookup"><span data-stu-id="f6c32-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="f6c32-117">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="f6c32-117">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="f6c32-118">Exempel 2: Hämta en batchfil och spara den på en angiven fil Sök väg med förloppet</span><span class="sxs-lookup"><span data-stu-id="f6c32-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="f6c32-119">Det här kommandot får den zonfil som heter StdErr.txt genom att använda Get-AzureBatchNodeFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6c32-119">This command gets the node file that is named StdErr.txt by using the Get-AzureBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="f6c32-120">Kommandot skickar filen till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="f6c32-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f6c32-121">Den aktuella cmdleten sparar filen i E:\PowerShell\StdOut.txt fil Sök väg på den lokala datorn.</span><span class="sxs-lookup"><span data-stu-id="f6c32-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="f6c32-122">StdOut.txt-nodadressen är kopplad till aktiviteten som har ID-Task02 för jobbet som har ID Job02.</span><span class="sxs-lookup"><span data-stu-id="f6c32-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="f6c32-123">Exempel 3: Hämta en batchjournal som är kopplad till en aktivitet och dirigera den till en ström</span><span class="sxs-lookup"><span data-stu-id="f6c32-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="f6c32-124">Det första kommandot skapar en ström genom att använda New-Object cmdlet och lagrar den i $Stream-variabeln.</span><span class="sxs-lookup"><span data-stu-id="f6c32-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="f6c32-125">Det andra kommandot får den zonfil som heter StdOut.txt från aktiviteten som har ID-Task11 för jobbet som har ID-Job03.</span><span class="sxs-lookup"><span data-stu-id="f6c32-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="f6c32-126">Kommandot dirigerar fil innehåll till strömmen i $Stream.</span><span class="sxs-lookup"><span data-stu-id="f6c32-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="f6c32-127">Exempel 4: Hämta en zonfil från en datornod och spara den</span><span class="sxs-lookup"><span data-stu-id="f6c32-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="f6c32-128">Med det här kommandot får du Startup\StdOut.txt Node-noden som innehåller ID-ComputeNode01 i poolen som har ID Pool01.</span><span class="sxs-lookup"><span data-stu-id="f6c32-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="f6c32-129">Kommandot sparar filen i E:\PowerShell\StdOut.txt fil Sök väg på den lokala datorn.</span><span class="sxs-lookup"><span data-stu-id="f6c32-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="f6c32-130">Exempel 5: Hämta en zonfil från en datornod och spara den med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="f6c32-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="f6c32-131">Det här kommandot får Startup\StdOut.txt med den här noden genom att använda Get-AzureBatchNodeFile från noden Compute som har ID-ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="f6c32-131">This command gets the node file Startup\StdOut.txt by using Get-AzureBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="f6c32-132">Noden Compute finns i poolen med ID-Pool01.</span><span class="sxs-lookup"><span data-stu-id="f6c32-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="f6c32-133">Kommandot skickar den noden till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f6c32-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="f6c32-134">Denna cmdlet sparar filen i E:\PowerShell\StdOut.txt fil Sök väg på den lokala datorn.</span><span class="sxs-lookup"><span data-stu-id="f6c32-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="f6c32-135">Exempel 6: Hämta en zonfil från en datornod och dirigera den till en ström</span><span class="sxs-lookup"><span data-stu-id="f6c32-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="f6c32-136">Det första kommandot skapar en ström genom att använda New-Object cmdlet och lagrar den i $Stream-variabeln.</span><span class="sxs-lookup"><span data-stu-id="f6c32-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="f6c32-137">Det andra kommandot får den nod som heter StdOut.txt från noden Compute och som har ID-ComputeNode01 i poolen som har ID Pool01.</span><span class="sxs-lookup"><span data-stu-id="f6c32-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="f6c32-138">Kommandot dirigerar fil innehåll till strömmen i $Stream.</span><span class="sxs-lookup"><span data-stu-id="f6c32-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="f6c32-139">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6c32-139">PARAMETERS</span></span>

### <span data-ttu-id="f6c32-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f6c32-140">-BatchContext</span></span>
<span data-ttu-id="f6c32-141">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f6c32-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f6c32-142">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f6c32-142">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f6c32-143">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="f6c32-143">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f6c32-144">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="f6c32-144">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f6c32-145">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f6c32-145">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f6c32-146">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="f6c32-146">-ByteRangeEnd</span></span>
<span data-ttu-id="f6c32-147">Slutet på byte-området som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="f6c32-147">The end of the byte range to be downloaded.</span></span>
```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6c32-148">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="f6c32-148">-ByteRangeStart</span></span>
<span data-ttu-id="f6c32-149">Början på byte-området som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="f6c32-149">The start of the byte range to be downloaded.</span></span>
```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6c32-150">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="f6c32-150">-ComputeNodeId</span></span>
<span data-ttu-id="f6c32-151">Anger ID för den datornod som innehåller den zonfil som cmdleten returnerar.</span><span class="sxs-lookup"><span data-stu-id="f6c32-151">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

```yaml
Type: String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6c32-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6c32-152">-DefaultProfile</span></span>
<span data-ttu-id="f6c32-153">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f6c32-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6c32-154">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="f6c32-154">-DestinationPath</span></span>
<span data-ttu-id="f6c32-155">Anger sökvägen till den plats där denna cmdlet sparar zonfilen.</span><span class="sxs-lookup"><span data-stu-id="f6c32-155">Specifies the file path where this cmdlet saves the node file.</span></span>

```yaml
Type: String
Parameter Sets: Task_Id_Path, ComputeNode_Id_Path, InputObject_Path
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6c32-156">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="f6c32-156">-DestinationStream</span></span>
<span data-ttu-id="f6c32-157">Anger i vilken ström den här cmdleten skriver fil innehållet.</span><span class="sxs-lookup"><span data-stu-id="f6c32-157">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="f6c32-158">Denna cmdlet stänger inte eller spolar inte tillbaka strömmen.</span><span class="sxs-lookup"><span data-stu-id="f6c32-158">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: Stream
Parameter Sets: Task_Id_Stream, ComputeNode_Id_Stream, InputObject_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6c32-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6c32-159">-InputObject</span></span>
<span data-ttu-id="f6c32-160">Anger filen som den här cmdleten får, som ett **PSNodeFile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f6c32-160">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="f6c32-161">Använd Get-AzureBatchNodeFile cmdlet för att hämta ett nod fil objekt.</span><span class="sxs-lookup"><span data-stu-id="f6c32-161">To obtain a node file object, use the Get-AzureBatchNodeFile cmdlet.</span></span>

```yaml
Type: PSNodeFile
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6c32-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="f6c32-162">-JobId</span></span>
<span data-ttu-id="f6c32-163">Anger ID för jobbet som innehåller mål uppgiften.</span><span class="sxs-lookup"><span data-stu-id="f6c32-163">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6c32-164">-Path</span><span class="sxs-lookup"><span data-stu-id="f6c32-164">-Path</span></span>
<span data-ttu-id="f6c32-165">Sökvägen till den nod som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="f6c32-165">The path of the node file to download.</span></span>

```yaml
Type: String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6c32-166">-PoolId</span><span class="sxs-lookup"><span data-stu-id="f6c32-166">-PoolId</span></span>
<span data-ttu-id="f6c32-167">Anger ID för den pool som innehåller den datornod som innehåller den zonfil som cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="f6c32-167">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6c32-168">-TaskId</span><span class="sxs-lookup"><span data-stu-id="f6c32-168">-TaskId</span></span>
<span data-ttu-id="f6c32-169">Anger aktivitetens ID.</span><span class="sxs-lookup"><span data-stu-id="f6c32-169">Specifies the ID of the task.</span></span>

```yaml
Type: String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6c32-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6c32-170">CommonParameters</span></span>
<span data-ttu-id="f6c32-171">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6c32-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6c32-172">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6c32-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6c32-173">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6c32-173">INPUTS</span></span>

### <span data-ttu-id="f6c32-174">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f6c32-174">BatchAccountContext</span></span>
<span data-ttu-id="f6c32-175">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f6c32-175">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="f6c32-176">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="f6c32-176">PSNodeFile</span></span>
<span data-ttu-id="f6c32-177">Parametern ' InputObject ' godkänner värdet av typen ' PSNodeFile ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f6c32-177">Parameter 'InputObject' accepts value of type 'PSNodeFile' from the pipeline</span></span>

## <span data-ttu-id="f6c32-178">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6c32-178">OUTPUTS</span></span>

## <span data-ttu-id="f6c32-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6c32-179">NOTES</span></span>

## <span data-ttu-id="f6c32-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6c32-180">RELATED LINKS</span></span>

[<span data-ttu-id="f6c32-181">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f6c32-181">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="f6c32-182">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="f6c32-182">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="f6c32-183">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="f6c32-183">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


