---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
ms.openlocfilehash: 3d40a74af8b1f7b3dbb44a53d08b169501af704d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583668"
---
# <span data-ttu-id="ed274-101">Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="ed274-101">Remove-AzureBatchNodeFile</span></span>

## <span data-ttu-id="ed274-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed274-102">SYNOPSIS</span></span>
<span data-ttu-id="ed274-103">Tar bort en nodadress för en aktivitet eller en datornod.</span><span class="sxs-lookup"><span data-stu-id="ed274-103">Deletes a node file for a task or compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed274-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed274-104">SYNTAX</span></span>

### <span data-ttu-id="ed274-105">Projektaktivitetsnr</span><span class="sxs-lookup"><span data-stu-id="ed274-105">Task</span></span>
```
Remove-AzureBatchNodeFile -JobId <String> -TaskId <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed274-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="ed274-106">ComputeNode</span></span>
```
Remove-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed274-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ed274-107">InputObject</span></span>
```
Remove-AzureBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed274-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed274-108">DESCRIPTION</span></span>
<span data-ttu-id="ed274-109">Cmdleten **Remove-AzureBatchNodeFile** tar bort en Azure-batchjournal för en aktivitet eller en datornod.</span><span class="sxs-lookup"><span data-stu-id="ed274-109">The **Remove-AzureBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="ed274-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed274-110">EXAMPLES</span></span>

### <span data-ttu-id="ed274-111">Exempel 1: ta bort en fil assocated med en uppgift</span><span class="sxs-lookup"><span data-stu-id="ed274-111">Example 1: Delete a file assocated with a task</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="ed274-112">Det här kommandot tar bort den zonfil som heter wd\testFile.txt.</span><span class="sxs-lookup"><span data-stu-id="ed274-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="ed274-113">Filen är kopplad till uppgiften som har ID-Task26 under jobbet jobb-000001.</span><span class="sxs-lookup"><span data-stu-id="ed274-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="ed274-114">Exempel 2: ta bort en fil från en datornod</span><span class="sxs-lookup"><span data-stu-id="ed274-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Path "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="ed274-115">Det här kommandot tar bort den zonfil som heter startup\testFile.txt från angiven datornod i poolen med ID-Pool07.</span><span class="sxs-lookup"><span data-stu-id="ed274-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="ed274-116">Exempel 3: ta bort en fil med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="ed274-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile2.txt" -BatchContext $Context | Remove-AzureBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="ed274-117">Det här kommandot får Node-filen genom att använda **Get-AzureBatchNodeFile**.</span><span class="sxs-lookup"><span data-stu-id="ed274-117">This command gets the node file by using **Get-AzureBatchNodeFile**.</span></span>
<span data-ttu-id="ed274-118">Filen är kopplad till uppgiften som har ID-Task26 under jobbet jobb-000001.</span><span class="sxs-lookup"><span data-stu-id="ed274-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="ed274-119">Kommandot skickar filen till den aktuella cmdleten med hjälp av pipeline.</span><span class="sxs-lookup"><span data-stu-id="ed274-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="ed274-120">Den aktuella cmdleten tar bort filen.</span><span class="sxs-lookup"><span data-stu-id="ed274-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="ed274-121">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="ed274-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="ed274-122">Därför uppmanas du inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="ed274-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ed274-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed274-123">PARAMETERS</span></span>

### <span data-ttu-id="ed274-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ed274-124">-BatchContext</span></span>
<span data-ttu-id="ed274-125">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ed274-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ed274-126">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ed274-126">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ed274-127">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="ed274-127">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ed274-128">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="ed274-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ed274-129">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ed274-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ed274-130">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="ed274-130">-ComputeNodeId</span></span>
<span data-ttu-id="ed274-131">Anger ID för den datornod som innehåller batchfilen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="ed274-131">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: ComputeNode
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed274-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed274-132">-DefaultProfile</span></span>
<span data-ttu-id="ed274-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ed274-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed274-134">-Force</span><span class="sxs-lookup"><span data-stu-id="ed274-134">-Force</span></span>
<span data-ttu-id="ed274-135">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ed274-135">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed274-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed274-136">-InputObject</span></span>
<span data-ttu-id="ed274-137">Anger **PSNodeFile** -objekt som representerar den nod som tas bort med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ed274-137">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="ed274-138">För att få en **PSNodeFile** , Använd cmdleten Get-AzureBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="ed274-138">To obtain a **PSNodeFile** , use the Get-AzureBatchNodeFile cmdlet.</span></span>

```yaml
Type: PSNodeFile
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed274-139">-JobId</span><span class="sxs-lookup"><span data-stu-id="ed274-139">-JobId</span></span>
<span data-ttu-id="ed274-140">Anger ID för jobbet som innehåller uppgiften.</span><span class="sxs-lookup"><span data-stu-id="ed274-140">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: String
Parameter Sets: Task
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed274-141">-Path</span><span class="sxs-lookup"><span data-stu-id="ed274-141">-Path</span></span>
<span data-ttu-id="ed274-142">Sökvägen till den nod som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ed274-142">The file path of the node file to delete.</span></span>

```yaml
Type: String
Parameter Sets: Task, ComputeNode
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed274-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="ed274-143">-PoolId</span></span>
<span data-ttu-id="ed274-144">Anger ID för poolen som innehåller de datornoder för vilka denna cmdlet tar bort en fil.</span><span class="sxs-lookup"><span data-stu-id="ed274-144">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

```yaml
Type: String
Parameter Sets: ComputeNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed274-145">-Rekursivt</span><span class="sxs-lookup"><span data-stu-id="ed274-145">-Recursive</span></span>
<span data-ttu-id="ed274-146">Anger att denna cmdlet tar bort mappen och alla undermappar och filer under den angivna sökvägen.</span><span class="sxs-lookup"><span data-stu-id="ed274-146">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="ed274-147">Denna cmdlet är bara relevant om sökvägen är en mapp.</span><span class="sxs-lookup"><span data-stu-id="ed274-147">This cmdlet is relevant only if the path is a folder.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed274-148">-TaskId</span><span class="sxs-lookup"><span data-stu-id="ed274-148">-TaskId</span></span>
<span data-ttu-id="ed274-149">Anger aktivitetens ID.</span><span class="sxs-lookup"><span data-stu-id="ed274-149">Specifies the ID of the task.</span></span>

```yaml
Type: String
Parameter Sets: Task
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed274-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ed274-150">-Confirm</span></span>
<span data-ttu-id="ed274-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ed274-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed274-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed274-152">-WhatIf</span></span>
<span data-ttu-id="ed274-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ed274-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed274-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ed274-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed274-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed274-155">CommonParameters</span></span>
<span data-ttu-id="ed274-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed274-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed274-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed274-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed274-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed274-158">INPUTS</span></span>

### <span data-ttu-id="ed274-159">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ed274-159">BatchAccountContext</span></span>
<span data-ttu-id="ed274-160">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="ed274-160">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="ed274-161">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="ed274-161">PSNodeFile</span></span>
<span data-ttu-id="ed274-162">Parametern ' InputObject ' godkänner värdet av typen ' PSNodeFile ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="ed274-162">Parameter 'InputObject' accepts value of type 'PSNodeFile' from the pipeline</span></span>

## <span data-ttu-id="ed274-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed274-163">OUTPUTS</span></span>

## <span data-ttu-id="ed274-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed274-164">NOTES</span></span>

## <span data-ttu-id="ed274-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed274-165">RELATED LINKS</span></span>

[<span data-ttu-id="ed274-166">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ed274-166">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ed274-167">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="ed274-167">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="ed274-168">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="ed274-168">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)


