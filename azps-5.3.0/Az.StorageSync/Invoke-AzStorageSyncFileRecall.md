---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: fb053da61aabd9328f4ff3d848243ff9b84d6d09
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521955"
---
# <span data-ttu-id="229bc-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="229bc-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="229bc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="229bc-102">SYNOPSIS</span></span>
<span data-ttu-id="229bc-103">Det här kommandot återställer alla nivåbaserade filer tillbaka till lokala diskar.</span><span class="sxs-lookup"><span data-stu-id="229bc-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="229bc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="229bc-104">SYNTAX</span></span>

### <span data-ttu-id="229bc-105">StringParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="229bc-105">StringParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="229bc-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="229bc-106">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="229bc-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="229bc-107">ObjectParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="229bc-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="229bc-108">DESCRIPTION</span></span>
<span data-ttu-id="229bc-109">När moln lager är aktiverat på en server slut punkt (en specifik plats på en registrerad Server) kan det här kommandot användas för att återkalla alla nivåbaserade filer till lokala diskar.</span><span class="sxs-lookup"><span data-stu-id="229bc-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="229bc-110">Vi rekommenderar starkt att du inaktiverar moln skiktning på den här server slut punkten innan du påbörjar återställningen.</span><span class="sxs-lookup"><span data-stu-id="229bc-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="229bc-111">Om du fortfarande har en lager nivå kan du komma ihåg att återkalla andra filer som missar för att uppfylla allt innehåll som finns på lokala diskar.</span><span class="sxs-lookup"><span data-stu-id="229bc-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="229bc-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="229bc-112">EXAMPLES</span></span>

### <span data-ttu-id="229bc-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="229bc-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="229bc-114">Detta kommando återkallar rekursivt alla skiktade filer under rot Sök vägen för den angivna Server slut punkten.</span><span class="sxs-lookup"><span data-stu-id="229bc-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="229bc-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="229bc-115">PARAMETERS</span></span>

### <span data-ttu-id="229bc-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="229bc-116">-AsJob</span></span>
<span data-ttu-id="229bc-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="229bc-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="229bc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="229bc-118">-DefaultProfile</span></span>
<span data-ttu-id="229bc-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="229bc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="229bc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="229bc-120">-InputObject</span></span>
<span data-ttu-id="229bc-121">SyncGroup-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="229bc-121">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer, ServerEndpoint

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="229bc-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="229bc-122">-Name</span></span>
<span data-ttu-id="229bc-123">Namn på ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="229bc-123">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ServerEndpointName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="229bc-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="229bc-124">-PassThru</span></span>
<span data-ttu-id="229bc-125">I normal körning returnerar denna cmdlet inget värde vid framgång.</span><span class="sxs-lookup"><span data-stu-id="229bc-125">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="229bc-126">Om du anger parametern PassThru, skriver cmdleten ett värde till pipeline efter att körningen lyckats.</span><span class="sxs-lookup"><span data-stu-id="229bc-126">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="229bc-127">-Mönster</span><span class="sxs-lookup"><span data-stu-id="229bc-127">-Pattern</span></span>
<span data-ttu-id="229bc-128">Mönster för fil namnet</span><span class="sxs-lookup"><span data-stu-id="229bc-128">Pattern of the file name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="229bc-129">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="229bc-129">-RecallPath</span></span>
<span data-ttu-id="229bc-130">Sökväg som måste återkallas.</span><span class="sxs-lookup"><span data-stu-id="229bc-130">Recall path which need to be recalled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="229bc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="229bc-131">-ResourceGroupName</span></span>
<span data-ttu-id="229bc-132">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="229bc-132">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="229bc-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="229bc-133">-ResourceId</span></span>
<span data-ttu-id="229bc-134">Resurs-ID för ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="229bc-134">ServerEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="229bc-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="229bc-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="229bc-136">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="229bc-136">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="229bc-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="229bc-137">-SyncGroupName</span></span>
<span data-ttu-id="229bc-138">Namn på SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="229bc-138">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="229bc-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="229bc-139">-Confirm</span></span>
<span data-ttu-id="229bc-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="229bc-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="229bc-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="229bc-141">-WhatIf</span></span>
<span data-ttu-id="229bc-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="229bc-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="229bc-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="229bc-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="229bc-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="229bc-144">CommonParameters</span></span>
<span data-ttu-id="229bc-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="229bc-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="229bc-146">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="229bc-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="229bc-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="229bc-147">INPUTS</span></span>

### <span data-ttu-id="229bc-148">System. String</span><span class="sxs-lookup"><span data-stu-id="229bc-148">System.String</span></span>

### <span data-ttu-id="229bc-149">Microsoft. Azure. commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="229bc-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="229bc-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="229bc-150">OUTPUTS</span></span>

### <span data-ttu-id="229bc-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="229bc-151">System.Boolean</span></span>

## <span data-ttu-id="229bc-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="229bc-152">NOTES</span></span>

## <span data-ttu-id="229bc-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="229bc-153">RELATED LINKS</span></span>
