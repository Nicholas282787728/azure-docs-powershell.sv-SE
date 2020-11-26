---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
ms.openlocfilehash: ca493914cc91d16566fddcebed5367fa81be1d2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271143"
---
# <span data-ttu-id="1de6d-101">Remove-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="1de6d-101">Remove-AzSynapseLinkedService</span></span>

## <span data-ttu-id="1de6d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1de6d-102">SYNOPSIS</span></span>
<span data-ttu-id="1de6d-103">Tar bort en länkad tjänst från arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="1de6d-103">Removes a linked service from workspace.</span></span>

## <span data-ttu-id="1de6d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1de6d-104">SYNTAX</span></span>

### <span data-ttu-id="1de6d-105">RemoveByName (standard)</span><span class="sxs-lookup"><span data-stu-id="1de6d-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1de6d-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="1de6d-106">RemoveByObject</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1de6d-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="1de6d-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseLinkedService -InputObject <PSLinkedServiceResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1de6d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1de6d-108">DESCRIPTION</span></span>
<span data-ttu-id="1de6d-109">Cmdleten **Remove-AzSynapseLinkedService** tar bort en länkad tjänst från arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="1de6d-109">The **Remove-AzSynapseLinkedService** cmdlet removes a linked service from workspace.</span></span>

## <span data-ttu-id="1de6d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1de6d-110">EXAMPLES</span></span>

### <span data-ttu-id="1de6d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1de6d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="1de6d-112">Det här kommandot tar bort den länkade tjänsten som heter ContosoLinkedService från arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="1de6d-112">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="1de6d-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1de6d-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="1de6d-114">Det här kommandot tar bort den länkade tjänsten som heter ContosoLinkedService från arbets ytan som heter ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="1de6d-114">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="1de6d-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="1de6d-115">Example 3</span></span>
```powershell
PS C:\> $linkedService = Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
PS C:\> $linkedService | Remove-AzSynapseLinkedService
```

<span data-ttu-id="1de6d-116">Det här kommandot tar bort den länkade tjänsten som heter ContosoLinkedService från arbets ytan som heter ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="1de6d-116">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="1de6d-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1de6d-117">PARAMETERS</span></span>

### <span data-ttu-id="1de6d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1de6d-118">-AsJob</span></span>
<span data-ttu-id="1de6d-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1de6d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1de6d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1de6d-120">-DefaultProfile</span></span>
<span data-ttu-id="1de6d-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1de6d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1de6d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1de6d-122">-InputObject</span></span>
<span data-ttu-id="1de6d-123">Det länkade serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="1de6d-123">The linked service object.</span></span>

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

### <span data-ttu-id="1de6d-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="1de6d-124">-Name</span></span>
<span data-ttu-id="1de6d-125">Namnet på den länkade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1de6d-125">The linked service name.</span></span>

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

### <span data-ttu-id="1de6d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1de6d-126">-PassThru</span></span>
<span data-ttu-id="1de6d-127">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="1de6d-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1de6d-128">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="1de6d-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1de6d-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1de6d-129">-WorkspaceName</span></span>
<span data-ttu-id="1de6d-130">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="1de6d-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1de6d-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1de6d-131">-WorkspaceObject</span></span>
<span data-ttu-id="1de6d-132">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="1de6d-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1de6d-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1de6d-133">-Confirm</span></span>
<span data-ttu-id="1de6d-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1de6d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1de6d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1de6d-135">-WhatIf</span></span>
<span data-ttu-id="1de6d-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1de6d-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1de6d-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1de6d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1de6d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1de6d-138">CommonParameters</span></span>
<span data-ttu-id="1de6d-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1de6d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1de6d-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1de6d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1de6d-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1de6d-141">INPUTS</span></span>

### <span data-ttu-id="1de6d-142">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1de6d-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="1de6d-143">Microsoft. Azure. commands. Synapse. Models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="1de6d-143">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="1de6d-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1de6d-144">OUTPUTS</span></span>

### <span data-ttu-id="1de6d-145">Microsoft. Azure. commands. Synapse. Models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="1de6d-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="1de6d-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1de6d-146">NOTES</span></span>

## <span data-ttu-id="1de6d-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1de6d-147">RELATED LINKS</span></span>