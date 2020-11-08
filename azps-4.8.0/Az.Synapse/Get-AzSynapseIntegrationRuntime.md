---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 285c0877441cabf51c723a472208cc002867fa7a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261502"
---
# <span data-ttu-id="89f45-101">Get-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="89f45-101">Get-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="89f45-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="89f45-102">SYNOPSIS</span></span>
<span data-ttu-id="89f45-103">Hämtar information om integrerings körnas resurser.</span><span class="sxs-lookup"><span data-stu-id="89f45-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="89f45-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="89f45-104">SYNTAX</span></span>

### <span data-ttu-id="89f45-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="89f45-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89f45-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89f45-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime [-Name <String>] -WorkspaceObject <PSSynapseWorkspace> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89f45-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="89f45-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -ResourceId <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="89f45-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89f45-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89f45-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="89f45-109">DESCRIPTION</span></span>
<span data-ttu-id="89f45-110">Cmdleten **Get-AzSynapseIntegrationRuntime** hämtar information om integrerings körningar på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="89f45-110">The **Get-AzSynapseIntegrationRuntime** cmdlet gets information about integration runtimes in a workspace.</span></span>
<span data-ttu-id="89f45-111">Om du anger namnet på en integrations körning får denna cmdlet information om integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="89f45-111">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="89f45-112">Om du inte anger ett namn hämtas den här cmdleten information om alla integrerings körningar på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="89f45-112">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a workspace.</span></span>

## <span data-ttu-id="89f45-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="89f45-113">EXAMPLES</span></span>

### <span data-ttu-id="89f45-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="89f45-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="89f45-115">Visa alla integrerings körningar i arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="89f45-115">List all integration runtimes in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="89f45-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="89f45-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="89f45-117">Det här kommandot visar information om integrations körningen med namnet ' test-selfhost-IR ' i arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="89f45-117">This command displays information about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="89f45-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="89f45-118">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Status
```

<span data-ttu-id="89f45-119">Det här kommandot visar detalj status för integrations körningen med namnet ' test-selfhost-IR ' i arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="89f45-119">This command displays detail status about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="89f45-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="89f45-120">PARAMETERS</span></span>

### <span data-ttu-id="89f45-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89f45-121">-DefaultProfile</span></span>
<span data-ttu-id="89f45-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="89f45-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89f45-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89f45-123">-InputObject</span></span>
<span data-ttu-id="89f45-124">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="89f45-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="89f45-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="89f45-125">-Name</span></span>
<span data-ttu-id="89f45-126">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="89f45-126">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89f45-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89f45-127">-ResourceGroupName</span></span>
<span data-ttu-id="89f45-128">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="89f45-128">Resource group name.</span></span>

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

### <span data-ttu-id="89f45-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89f45-129">-ResourceId</span></span>
<span data-ttu-id="89f45-130">Resurs-ID för Synapse.</span><span class="sxs-lookup"><span data-stu-id="89f45-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="89f45-131">-Status</span><span class="sxs-lookup"><span data-stu-id="89f45-131">-Status</span></span>
<span data-ttu-id="89f45-132">Information om integreringens detalj status.</span><span class="sxs-lookup"><span data-stu-id="89f45-132">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="89f45-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="89f45-133">-WorkspaceName</span></span>
<span data-ttu-id="89f45-134">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="89f45-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="89f45-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="89f45-135">-WorkspaceObject</span></span>
<span data-ttu-id="89f45-136">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="89f45-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="89f45-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89f45-137">CommonParameters</span></span>
<span data-ttu-id="89f45-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89f45-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89f45-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89f45-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89f45-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="89f45-140">INPUTS</span></span>

### <span data-ttu-id="89f45-141">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="89f45-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="89f45-142">Microsoft. Azure. commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="89f45-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="89f45-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="89f45-143">OUTPUTS</span></span>

### <span data-ttu-id="89f45-144">Microsoft. Azure. commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="89f45-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="89f45-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="89f45-145">NOTES</span></span>

## <span data-ttu-id="89f45-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="89f45-146">RELATED LINKS</span></span>
