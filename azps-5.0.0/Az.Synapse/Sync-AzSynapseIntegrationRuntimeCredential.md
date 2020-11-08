---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/sync-azsynapseintegrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
ms.openlocfilehash: feb9d74cf49dfa8ae5455b303ee78f443a08e942
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94262886"
---
# <span data-ttu-id="d8057-101">Sync-AzSynapseIntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="d8057-101">Sync-AzSynapseIntegrationRuntimeCredential</span></span>

## <span data-ttu-id="d8057-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8057-102">SYNOPSIS</span></span>
<span data-ttu-id="d8057-103">Synkroniserar uppgifter med kör tids noder för integration.</span><span class="sxs-lookup"><span data-stu-id="d8057-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="d8057-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8057-104">SYNTAX</span></span>

### <span data-ttu-id="d8057-105">StopByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d8057-105">StopByNameParameterSet (Default)</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8057-106">StopByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8057-106">StopByParentObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -IntegrationRuntimeName <String>
 -WorkspaceObject <PSSynapseWorkspace> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8057-107">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8057-107">StopByResourceIdParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -ResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8057-108">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8057-108">StopByInputObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8057-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8057-109">DESCRIPTION</span></span>
<span data-ttu-id="d8057-110">**Sync-AzSynapseIntegrationRuntimeCredential** -cmdleten synkroniserar lokala autentiseringsuppgifter bland integrations körnings noder, vilket innebär att autentiseringsuppgifterna är identiska på alla noder.</span><span class="sxs-lookup"><span data-stu-id="d8057-110">The **Sync-AzSynapseIntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="d8057-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8057-111">EXAMPLES</span></span>

### <span data-ttu-id="d8057-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d8057-112">Example 1</span></span>
```powershell
PS C:\> Sync-AzSynapseIntegrationRuntimeCredential -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir'
```

<span data-ttu-id="d8057-113">Synkroniserar uppgifter med kör tids noder för integration.</span><span class="sxs-lookup"><span data-stu-id="d8057-113">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="d8057-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8057-114">PARAMETERS</span></span>

### <span data-ttu-id="d8057-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8057-115">-DefaultProfile</span></span>
<span data-ttu-id="d8057-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d8057-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8057-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d8057-117">-Force</span></span>
<span data-ttu-id="d8057-118">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d8057-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d8057-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8057-119">-InputObject</span></span>
<span data-ttu-id="d8057-120">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="d8057-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: StopByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8057-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="d8057-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="d8057-122">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="d8057-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet, StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8057-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8057-123">-ResourceGroupName</span></span>
<span data-ttu-id="d8057-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="d8057-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8057-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8057-125">-ResourceId</span></span>
<span data-ttu-id="d8057-126">Resurs-ID för Synapse.</span><span class="sxs-lookup"><span data-stu-id="d8057-126">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8057-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d8057-127">-WorkspaceName</span></span>
<span data-ttu-id="d8057-128">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="d8057-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8057-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d8057-129">-WorkspaceObject</span></span>
<span data-ttu-id="d8057-130">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="d8057-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8057-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d8057-131">-Confirm</span></span>
<span data-ttu-id="d8057-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d8057-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8057-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8057-133">-WhatIf</span></span>
<span data-ttu-id="d8057-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d8057-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8057-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d8057-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8057-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8057-136">CommonParameters</span></span>
<span data-ttu-id="d8057-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8057-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8057-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8057-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8057-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8057-139">INPUTS</span></span>

### <span data-ttu-id="d8057-140">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d8057-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d8057-141">Microsoft. Azure. commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d8057-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="d8057-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8057-142">OUTPUTS</span></span>

### <span data-ttu-id="d8057-143">System. Void</span><span class="sxs-lookup"><span data-stu-id="d8057-143">System.Void</span></span>

## <span data-ttu-id="d8057-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8057-144">NOTES</span></span>

## <span data-ttu-id="d8057-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8057-145">RELATED LINKS</span></span>
