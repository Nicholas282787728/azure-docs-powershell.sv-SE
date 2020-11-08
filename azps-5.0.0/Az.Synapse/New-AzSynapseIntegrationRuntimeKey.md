---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 836dcabaa190b66daf5a4f3f2fdaf300fe47ccdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271164"
---
# <span data-ttu-id="e906a-101">New-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="e906a-101">New-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="e906a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e906a-102">SYNOPSIS</span></span>
<span data-ttu-id="e906a-103">Återskapa den självvärdbaserade integrerings kör nyckeln.</span><span class="sxs-lookup"><span data-stu-id="e906a-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="e906a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e906a-104">SYNTAX</span></span>

### <span data-ttu-id="e906a-105">NewByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e906a-105">NewByNameParameterSet (Default)</span></span>
```
New-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -KeyName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e906a-106">NewByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e906a-106">NewByParentObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace> -KeyName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e906a-107">NewByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e906a-107">NewByResourceIdParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -ResourceId <String> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e906a-108">NewByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e906a-108">NewByInputObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e906a-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e906a-109">DESCRIPTION</span></span>
<span data-ttu-id="e906a-110">Cmdlet **New-AzSynapseIntegrationRuntimeKey** återskapar integrerings körnings nyckeln med det nycklar som anges med parametern "värde namn".</span><span class="sxs-lookup"><span data-stu-id="e906a-110">The cmdlet **New-AzSynapseIntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="e906a-111">Den föregående knappen är ogiltig.</span><span class="sxs-lookup"><span data-stu-id="e906a-111">The previous key will is invalid.</span></span>

## <span data-ttu-id="e906a-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e906a-112">EXAMPLES</span></span>

### <span data-ttu-id="e906a-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e906a-113">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -KeyName authKey2
```

<span data-ttu-id="e906a-114">Cmdleten återskapar nyckeln ' authKey2 ' för integration runtime "test-selfhost-IR".</span><span class="sxs-lookup"><span data-stu-id="e906a-114">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="e906a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e906a-115">PARAMETERS</span></span>

### <span data-ttu-id="e906a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e906a-116">-DefaultProfile</span></span>
<span data-ttu-id="e906a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e906a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e906a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e906a-118">-Force</span></span>
<span data-ttu-id="e906a-119">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e906a-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e906a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e906a-120">-InputObject</span></span>
<span data-ttu-id="e906a-121">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="e906a-121">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: NewByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e906a-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="e906a-122">-KeyName</span></span>
<span data-ttu-id="e906a-123">Namn på en autentiseringsnyckel för den självvärdbaserade integrerings körningen.</span><span class="sxs-lookup"><span data-stu-id="e906a-123">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e906a-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="e906a-124">-Name</span></span>
<span data-ttu-id="e906a-125">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="e906a-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet, NewByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e906a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e906a-126">-ResourceGroupName</span></span>
<span data-ttu-id="e906a-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="e906a-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e906a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e906a-128">-ResourceId</span></span>
<span data-ttu-id="e906a-129">Resurs-ID för Synapse.</span><span class="sxs-lookup"><span data-stu-id="e906a-129">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e906a-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e906a-130">-WorkspaceName</span></span>
<span data-ttu-id="e906a-131">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="e906a-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e906a-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e906a-132">-WorkspaceObject</span></span>
<span data-ttu-id="e906a-133">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="e906a-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e906a-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e906a-134">-Confirm</span></span>
<span data-ttu-id="e906a-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e906a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e906a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e906a-136">-WhatIf</span></span>
<span data-ttu-id="e906a-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e906a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e906a-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e906a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e906a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e906a-139">CommonParameters</span></span>
<span data-ttu-id="e906a-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e906a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e906a-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e906a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e906a-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e906a-142">INPUTS</span></span>

### <span data-ttu-id="e906a-143">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e906a-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e906a-144">Microsoft. Azure. commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e906a-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e906a-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e906a-145">OUTPUTS</span></span>

### <span data-ttu-id="e906a-146">Microsoft. Azure. commands. Synapse. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="e906a-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="e906a-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e906a-147">NOTES</span></span>

## <span data-ttu-id="e906a-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e906a-148">RELATED LINKS</span></span>
