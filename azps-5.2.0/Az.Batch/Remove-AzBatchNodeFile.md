---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
ms.openlocfilehash: 7e9aeebebfc5720ab006d43071eadeabe6bcf655
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401531"
---
# <span data-ttu-id="310dd-101">Remove-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="310dd-101">Remove-AzBatchNodeFile</span></span>

## <span data-ttu-id="310dd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="310dd-102">SYNOPSIS</span></span>
<span data-ttu-id="310dd-103">Tar bort en nodadress för en aktivitet eller en datornod.</span><span class="sxs-lookup"><span data-stu-id="310dd-103">Deletes a node file for a task or compute node.</span></span>

## <span data-ttu-id="310dd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="310dd-104">SYNTAX</span></span>

### <span data-ttu-id="310dd-105">Projektaktivitetsnr</span><span class="sxs-lookup"><span data-stu-id="310dd-105">Task</span></span>
```
Remove-AzBatchNodeFile -JobId <String> -TaskId <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="310dd-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="310dd-106">ComputeNode</span></span>
```
Remove-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="310dd-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="310dd-107">InputObject</span></span>
```
Remove-AzBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="310dd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="310dd-108">DESCRIPTION</span></span>
<span data-ttu-id="310dd-109">Cmdleten **Remove-AzBatchNodeFile** tar bort en Azure-batchjournal för en aktivitet eller en datornod.</span><span class="sxs-lookup"><span data-stu-id="310dd-109">The **Remove-AzBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="310dd-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="310dd-110">EXAMPLES</span></span>

### <span data-ttu-id="310dd-111">Exempel 1: ta bort en fil som är kopplad till en aktivitet</span><span class="sxs-lookup"><span data-stu-id="310dd-111">Example 1: Delete a file associated with a task</span></span>
```
PS C:\>Remove-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="310dd-112">Det här kommandot tar bort den zonfil som heter wd\testFile.txt.</span><span class="sxs-lookup"><span data-stu-id="310dd-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="310dd-113">Filen är kopplad till uppgiften som har ID-Task26 under jobbet jobb-000001.</span><span class="sxs-lookup"><span data-stu-id="310dd-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="310dd-114">Exempel 2: ta bort en fil från en datornod</span><span class="sxs-lookup"><span data-stu-id="310dd-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Path "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="310dd-115">Det här kommandot tar bort den zonfil som heter startup\testFile.txt från angiven datornod i poolen med ID-Pool07.</span><span class="sxs-lookup"><span data-stu-id="310dd-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="310dd-116">Exempel 3: ta bort en fil med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="310dd-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile2.txt" -BatchContext $Context | Remove-AzBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="310dd-117">Det här kommandot får Node-filen genom att använda **Get-AzBatchNodeFile**.</span><span class="sxs-lookup"><span data-stu-id="310dd-117">This command gets the node file by using **Get-AzBatchNodeFile**.</span></span>
<span data-ttu-id="310dd-118">Filen är kopplad till uppgiften som har ID-Task26 under jobbet jobb-000001.</span><span class="sxs-lookup"><span data-stu-id="310dd-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="310dd-119">Kommandot skickar filen till den aktuella cmdleten med hjälp av pipeline.</span><span class="sxs-lookup"><span data-stu-id="310dd-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="310dd-120">Den aktuella cmdleten tar bort filen.</span><span class="sxs-lookup"><span data-stu-id="310dd-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="310dd-121">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="310dd-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="310dd-122">Därför uppmanas du inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="310dd-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="310dd-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="310dd-123">PARAMETERS</span></span>

### <span data-ttu-id="310dd-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="310dd-124">-BatchContext</span></span>
<span data-ttu-id="310dd-125">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="310dd-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="310dd-126">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="310dd-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="310dd-127">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="310dd-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="310dd-128">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="310dd-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="310dd-129">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="310dd-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="310dd-130">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="310dd-130">-ComputeNodeId</span></span>
<span data-ttu-id="310dd-131">Anger ID för den datornod som innehåller batchfilen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="310dd-131">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="310dd-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="310dd-132">-DefaultProfile</span></span>
<span data-ttu-id="310dd-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="310dd-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="310dd-134">-Force</span><span class="sxs-lookup"><span data-stu-id="310dd-134">-Force</span></span>
<span data-ttu-id="310dd-135">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="310dd-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="310dd-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="310dd-136">-InputObject</span></span>
<span data-ttu-id="310dd-137">Anger **PSNodeFile** -objekt som representerar den nod som tas bort med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="310dd-137">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="310dd-138">För att få en **PSNodeFile**, Använd cmdleten Get-AzBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="310dd-138">To obtain a **PSNodeFile**, use the Get-AzBatchNodeFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="310dd-139">-JobId</span><span class="sxs-lookup"><span data-stu-id="310dd-139">-JobId</span></span>
<span data-ttu-id="310dd-140">Anger ID för jobbet som innehåller uppgiften.</span><span class="sxs-lookup"><span data-stu-id="310dd-140">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="310dd-141">-Path</span><span class="sxs-lookup"><span data-stu-id="310dd-141">-Path</span></span>
<span data-ttu-id="310dd-142">Sökvägen till den nod som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="310dd-142">The file path of the node file to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: Task, ComputeNode
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="310dd-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="310dd-143">-PoolId</span></span>
<span data-ttu-id="310dd-144">Anger ID för poolen som innehåller de datornoder för vilka denna cmdlet tar bort en fil.</span><span class="sxs-lookup"><span data-stu-id="310dd-144">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="310dd-145">-Rekursivt</span><span class="sxs-lookup"><span data-stu-id="310dd-145">-Recursive</span></span>
<span data-ttu-id="310dd-146">Anger att denna cmdlet tar bort mappen och alla undermappar och filer under den angivna sökvägen.</span><span class="sxs-lookup"><span data-stu-id="310dd-146">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="310dd-147">Denna cmdlet är bara relevant om sökvägen är en mapp.</span><span class="sxs-lookup"><span data-stu-id="310dd-147">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="310dd-148">-TaskId</span><span class="sxs-lookup"><span data-stu-id="310dd-148">-TaskId</span></span>
<span data-ttu-id="310dd-149">Anger aktivitetens ID.</span><span class="sxs-lookup"><span data-stu-id="310dd-149">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="310dd-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="310dd-150">-Confirm</span></span>
<span data-ttu-id="310dd-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="310dd-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="310dd-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="310dd-152">-WhatIf</span></span>
<span data-ttu-id="310dd-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="310dd-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="310dd-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="310dd-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="310dd-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="310dd-155">CommonParameters</span></span>
<span data-ttu-id="310dd-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="310dd-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="310dd-157">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="310dd-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="310dd-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="310dd-158">INPUTS</span></span>

### <span data-ttu-id="310dd-159">System. String</span><span class="sxs-lookup"><span data-stu-id="310dd-159">System.String</span></span>

### <span data-ttu-id="310dd-160">Microsoft.Azure.Commands.BatCH. Modeller. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="310dd-160">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="310dd-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="310dd-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="310dd-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="310dd-162">OUTPUTS</span></span>

### <span data-ttu-id="310dd-163">System. Void</span><span class="sxs-lookup"><span data-stu-id="310dd-163">System.Void</span></span>

## <span data-ttu-id="310dd-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="310dd-164">NOTES</span></span>

## <span data-ttu-id="310dd-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="310dd-165">RELATED LINKS</span></span>

[<span data-ttu-id="310dd-166">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="310dd-166">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="310dd-167">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="310dd-167">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="310dd-168">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="310dd-168">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)


