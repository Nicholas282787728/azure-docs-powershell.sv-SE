---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 5df58da7ef5fa0829da27f4d6a46372f42bc9dc5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397256"
---
# <span data-ttu-id="58eb4-101">Get-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="58eb4-101">Get-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="58eb4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="58eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="58eb4-103">Hämtar information om en körnings tids nod.</span><span class="sxs-lookup"><span data-stu-id="58eb4-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="58eb4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="58eb4-104">SYNTAX</span></span>

### <span data-ttu-id="58eb4-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="58eb4-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="58eb4-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58eb4-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58eb4-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58eb4-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58eb4-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58eb4-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58eb4-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="58eb4-109">DESCRIPTION</span></span>
<span data-ttu-id="58eb4-110">Cmdleten **Get-AzSynapseIntegrationRuntimeNode** hämtar detalj informationen för en integrations körnings nod.</span><span class="sxs-lookup"><span data-stu-id="58eb4-110">The **Get-AzSynapseIntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="58eb4-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="58eb4-111">EXAMPLES</span></span>

### <span data-ttu-id="58eb4-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="58eb4-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'
```

<span data-ttu-id="58eb4-113">Cmdleten hämtar information om noden "Node_1" i den självvärdbaserade integrerings körningens "test-selfhost-IR" i arbets ytans ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="58eb4-113">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="58eb4-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="58eb4-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress
```

<span data-ttu-id="58eb4-115">Cmdleten får information om noden "Node_1" i integrerings programmet test-selfhost-IR i arbets ytan test-DF-EU2, inklusive IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="58eb4-115">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="58eb4-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="58eb4-116">PARAMETERS</span></span>

### <span data-ttu-id="58eb4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58eb4-117">-DefaultProfile</span></span>
<span data-ttu-id="58eb4-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="58eb4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58eb4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58eb4-119">-InputObject</span></span>
<span data-ttu-id="58eb4-120">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="58eb4-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58eb4-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="58eb4-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="58eb4-122">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="58eb4-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58eb4-123">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="58eb4-123">-IpAddress</span></span>
<span data-ttu-id="58eb4-124">IP-adressen för integration runtime-noden.</span><span class="sxs-lookup"><span data-stu-id="58eb4-124">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="58eb4-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="58eb4-125">-Name</span></span>
<span data-ttu-id="58eb4-126">Integration runtime-nodnamnet.</span><span class="sxs-lookup"><span data-stu-id="58eb4-126">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58eb4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58eb4-127">-ResourceGroupName</span></span>
<span data-ttu-id="58eb4-128">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="58eb4-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58eb4-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58eb4-129">-ResourceId</span></span>
<span data-ttu-id="58eb4-130">Resurs-ID för Synapse.</span><span class="sxs-lookup"><span data-stu-id="58eb4-130">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58eb4-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="58eb4-131">-WorkspaceName</span></span>
<span data-ttu-id="58eb4-132">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="58eb4-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58eb4-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="58eb4-133">-WorkspaceObject</span></span>
<span data-ttu-id="58eb4-134">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="58eb4-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58eb4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58eb4-135">CommonParameters</span></span>
<span data-ttu-id="58eb4-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58eb4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58eb4-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58eb4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58eb4-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="58eb4-138">INPUTS</span></span>

### <span data-ttu-id="58eb4-139">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="58eb4-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="58eb4-140">Microsoft. Azure. commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="58eb4-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="58eb4-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="58eb4-141">OUTPUTS</span></span>

### <span data-ttu-id="58eb4-142">Microsoft. Azure. commands. Synapse. Models. PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="58eb4-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="58eb4-143">Microsoft. Azure. commands. Synapse. Models. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="58eb4-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="58eb4-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="58eb4-144">NOTES</span></span>

## <span data-ttu-id="58eb4-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="58eb4-145">RELATED LINKS</span></span>
