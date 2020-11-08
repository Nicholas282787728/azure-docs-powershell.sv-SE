---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/sync-azsynapseintegrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
ms.openlocfilehash: feb9d74cf49dfa8ae5455b303ee78f443a08e942
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100692"
---
# <span data-ttu-id="acc5c-101">Sync-AzSynapseIntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="acc5c-101">Sync-AzSynapseIntegrationRuntimeCredential</span></span>

## <span data-ttu-id="acc5c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="acc5c-102">SYNOPSIS</span></span>
<span data-ttu-id="acc5c-103">Synkroniserar uppgifter med kör tids noder för integration.</span><span class="sxs-lookup"><span data-stu-id="acc5c-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="acc5c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="acc5c-104">SYNTAX</span></span>

### <span data-ttu-id="acc5c-105">StopByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="acc5c-105">StopByNameParameterSet (Default)</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="acc5c-106">StopByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="acc5c-106">StopByParentObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -IntegrationRuntimeName <String>
 -WorkspaceObject <PSSynapseWorkspace> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="acc5c-107">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="acc5c-107">StopByResourceIdParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -ResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acc5c-108">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="acc5c-108">StopByInputObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acc5c-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="acc5c-109">DESCRIPTION</span></span>
<span data-ttu-id="acc5c-110">**Sync-AzSynapseIntegrationRuntimeCredential** -cmdleten synkroniserar lokala autentiseringsuppgifter bland integrations körnings noder, vilket innebär att autentiseringsuppgifterna är identiska på alla noder.</span><span class="sxs-lookup"><span data-stu-id="acc5c-110">The **Sync-AzSynapseIntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="acc5c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="acc5c-111">EXAMPLES</span></span>

### <span data-ttu-id="acc5c-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="acc5c-112">Example 1</span></span>
```powershell
PS C:\> Sync-AzSynapseIntegrationRuntimeCredential -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir'
```

<span data-ttu-id="acc5c-113">Synkroniserar uppgifter med kör tids noder för integration.</span><span class="sxs-lookup"><span data-stu-id="acc5c-113">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="acc5c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="acc5c-114">PARAMETERS</span></span>

### <span data-ttu-id="acc5c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc5c-115">-DefaultProfile</span></span>
<span data-ttu-id="acc5c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="acc5c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acc5c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="acc5c-117">-Force</span></span>
<span data-ttu-id="acc5c-118">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="acc5c-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="acc5c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acc5c-119">-InputObject</span></span>
<span data-ttu-id="acc5c-120">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="acc5c-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="acc5c-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="acc5c-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="acc5c-122">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="acc5c-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="acc5c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acc5c-123">-ResourceGroupName</span></span>
<span data-ttu-id="acc5c-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="acc5c-124">Resource group name.</span></span>

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

### <span data-ttu-id="acc5c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acc5c-125">-ResourceId</span></span>
<span data-ttu-id="acc5c-126">Resurs-ID för Synapse.</span><span class="sxs-lookup"><span data-stu-id="acc5c-126">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="acc5c-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="acc5c-127">-WorkspaceName</span></span>
<span data-ttu-id="acc5c-128">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="acc5c-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="acc5c-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="acc5c-129">-WorkspaceObject</span></span>
<span data-ttu-id="acc5c-130">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="acc5c-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="acc5c-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="acc5c-131">-Confirm</span></span>
<span data-ttu-id="acc5c-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="acc5c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acc5c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acc5c-133">-WhatIf</span></span>
<span data-ttu-id="acc5c-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="acc5c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acc5c-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="acc5c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acc5c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc5c-136">CommonParameters</span></span>
<span data-ttu-id="acc5c-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acc5c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc5c-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="acc5c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc5c-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="acc5c-139">INPUTS</span></span>

### <span data-ttu-id="acc5c-140">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="acc5c-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="acc5c-141">Microsoft. Azure. commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="acc5c-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="acc5c-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="acc5c-142">OUTPUTS</span></span>

### <span data-ttu-id="acc5c-143">System. Void</span><span class="sxs-lookup"><span data-stu-id="acc5c-143">System.Void</span></span>

## <span data-ttu-id="acc5c-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="acc5c-144">NOTES</span></span>

## <span data-ttu-id="acc5c-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="acc5c-145">RELATED LINKS</span></span>
