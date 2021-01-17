---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
ms.openlocfilehash: c70cc0f8659a04e8a10a4fbd2b776d22fca6a616
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424192"
---
# <span data-ttu-id="14e50-101">Remove-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="14e50-101">Remove-AzSynapseLinkedService</span></span>

## <span data-ttu-id="14e50-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="14e50-102">SYNOPSIS</span></span>
<span data-ttu-id="14e50-103">Tar bort en länkad tjänst från arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="14e50-103">Removes a linked service from workspace.</span></span>

## <span data-ttu-id="14e50-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="14e50-104">SYNTAX</span></span>

### <span data-ttu-id="14e50-105">RemoveByName (standard)</span><span class="sxs-lookup"><span data-stu-id="14e50-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14e50-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="14e50-106">RemoveByObject</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14e50-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="14e50-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseLinkedService -InputObject <PSLinkedServiceResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14e50-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="14e50-108">DESCRIPTION</span></span>
<span data-ttu-id="14e50-109">Cmdleten **Remove-AzSynapseLinkedService** tar bort en länkad tjänst från arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="14e50-109">The **Remove-AzSynapseLinkedService** cmdlet removes a linked service from workspace.</span></span>

## <span data-ttu-id="14e50-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="14e50-110">EXAMPLES</span></span>

### <span data-ttu-id="14e50-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="14e50-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="14e50-112">Det här kommandot tar bort den länkade tjänsten som heter ContosoLinkedService från arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="14e50-112">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="14e50-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="14e50-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="14e50-114">Det här kommandot tar bort den länkade tjänsten som heter ContosoLinkedService från arbets ytan som heter ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="14e50-114">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="14e50-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="14e50-115">Example 3</span></span>
```powershell
PS C:\> $linkedService = Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
PS C:\> $linkedService | Remove-AzSynapseLinkedService
```

<span data-ttu-id="14e50-116">Det här kommandot tar bort den länkade tjänsten som heter ContosoLinkedService från arbets ytan som heter ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="14e50-116">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="14e50-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="14e50-117">PARAMETERS</span></span>

### <span data-ttu-id="14e50-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14e50-118">-AsJob</span></span>
<span data-ttu-id="14e50-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="14e50-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14e50-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14e50-120">-DefaultProfile</span></span>
<span data-ttu-id="14e50-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="14e50-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14e50-122">-Force</span><span class="sxs-lookup"><span data-stu-id="14e50-122">-Force</span></span>
<span data-ttu-id="14e50-123">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="14e50-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="14e50-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14e50-124">-InputObject</span></span>
<span data-ttu-id="14e50-125">Det länkade serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="14e50-125">The linked service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14e50-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="14e50-126">-Name</span></span>
<span data-ttu-id="14e50-127">Namnet på den länkade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="14e50-127">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e50-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14e50-128">-PassThru</span></span>
<span data-ttu-id="14e50-129">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="14e50-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="14e50-130">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="14e50-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="14e50-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="14e50-131">-WorkspaceName</span></span>
<span data-ttu-id="14e50-132">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="14e50-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e50-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="14e50-133">-WorkspaceObject</span></span>
<span data-ttu-id="14e50-134">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="14e50-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14e50-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="14e50-135">-Confirm</span></span>
<span data-ttu-id="14e50-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="14e50-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14e50-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14e50-137">-WhatIf</span></span>
<span data-ttu-id="14e50-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="14e50-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14e50-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="14e50-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14e50-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14e50-140">CommonParameters</span></span>
<span data-ttu-id="14e50-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14e50-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14e50-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14e50-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14e50-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="14e50-143">INPUTS</span></span>

### <span data-ttu-id="14e50-144">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="14e50-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="14e50-145">Microsoft. Azure. commands. Synapse. Models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="14e50-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="14e50-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="14e50-146">OUTPUTS</span></span>

### <span data-ttu-id="14e50-147">Microsoft. Azure. commands. Synapse. Models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="14e50-147">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="14e50-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="14e50-148">NOTES</span></span>

## <span data-ttu-id="14e50-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="14e50-149">RELATED LINKS</span></span>
