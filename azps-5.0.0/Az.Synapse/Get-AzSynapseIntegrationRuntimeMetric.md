---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
ms.openlocfilehash: 0b6700d11b017f00f10328afae2cc6638087f216
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324203"
---
# <span data-ttu-id="e229a-101">Get-AzSynapseIntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="e229a-101">Get-AzSynapseIntegrationRuntimeMetric</span></span>

## <span data-ttu-id="e229a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e229a-102">SYNOPSIS</span></span>
<span data-ttu-id="e229a-103">Hämtar Metric-data för en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="e229a-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="e229a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e229a-104">SYNTAX</span></span>

### <span data-ttu-id="e229a-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e229a-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e229a-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e229a-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e229a-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e229a-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e229a-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e229a-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e229a-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e229a-109">DESCRIPTION</span></span>
<span data-ttu-id="e229a-110">Cmdleten **Get-AzSynapseIntegrationRuntimeMetric** hämtar mått data om integrerings körningen på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="e229a-110">The **Get-AzSynapseIntegrationRuntimeMetric** cmdlet gets metric data about integration runtime in a workspace.</span></span>

## <span data-ttu-id="e229a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e229a-111">EXAMPLES</span></span>

### <span data-ttu-id="e229a-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e229a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeMetric -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="e229a-113">Det här kommandot visar Metric-uppgifter om integrations körningen med namnet ' test-selfhost-IR ' i arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e229a-113">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="e229a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e229a-114">PARAMETERS</span></span>

### <span data-ttu-id="e229a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e229a-115">-DefaultProfile</span></span>
<span data-ttu-id="e229a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e229a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e229a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e229a-117">-InputObject</span></span>
<span data-ttu-id="e229a-118">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="e229a-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="e229a-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="e229a-119">-Name</span></span>
<span data-ttu-id="e229a-120">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="e229a-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e229a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e229a-121">-ResourceGroupName</span></span>
<span data-ttu-id="e229a-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="e229a-122">Resource group name.</span></span>

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

### <span data-ttu-id="e229a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e229a-123">-ResourceId</span></span>
<span data-ttu-id="e229a-124">Resurs-ID för Synapse.</span><span class="sxs-lookup"><span data-stu-id="e229a-124">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="e229a-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e229a-125">-WorkspaceName</span></span>
<span data-ttu-id="e229a-126">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="e229a-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e229a-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e229a-127">-WorkspaceObject</span></span>
<span data-ttu-id="e229a-128">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="e229a-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e229a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e229a-129">CommonParameters</span></span>
<span data-ttu-id="e229a-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e229a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e229a-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e229a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e229a-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e229a-132">INPUTS</span></span>

### <span data-ttu-id="e229a-133">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e229a-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e229a-134">Microsoft. Azure. commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e229a-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e229a-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e229a-135">OUTPUTS</span></span>

### <span data-ttu-id="e229a-136">Microsoft. Azure. commands. Synapse. Models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="e229a-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="e229a-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e229a-137">NOTES</span></span>

## <span data-ttu-id="e229a-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e229a-138">RELATED LINKS</span></span>
