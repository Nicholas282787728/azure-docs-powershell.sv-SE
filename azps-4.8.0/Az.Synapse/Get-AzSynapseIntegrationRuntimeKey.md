---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 08ce91d6d9a942dd20078e0c3b5b537360aac9fc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100721"
---
# <span data-ttu-id="6fb87-101">Get-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="6fb87-101">Get-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="6fb87-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6fb87-102">SYNOPSIS</span></span>
<span data-ttu-id="6fb87-103">Hämtar nycklar för en självvärds integrerings körning.</span><span class="sxs-lookup"><span data-stu-id="6fb87-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="6fb87-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6fb87-104">SYNTAX</span></span>

### <span data-ttu-id="6fb87-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6fb87-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fb87-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fb87-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fb87-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fb87-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6fb87-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fb87-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fb87-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6fb87-109">DESCRIPTION</span></span>
<span data-ttu-id="6fb87-110">Cmdleten **Get-AzSynapseIntegrationRuntimeKey** hämtar nycklar för en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="6fb87-110">The **Get-AzSynapseIntegrationRuntimeKey** cmdlet gets keys for an integration runtime.</span></span> <span data-ttu-id="6fb87-111">Nycklarna används för att registrera en nod för integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="6fb87-111">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="6fb87-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6fb87-112">EXAMPLES</span></span>

### <span data-ttu-id="6fb87-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6fb87-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="6fb87-114">Cmdleten hämtar nycklar för en integrations körning med namnet ' test-selfhost-IR '.</span><span class="sxs-lookup"><span data-stu-id="6fb87-114">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="6fb87-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6fb87-115">PARAMETERS</span></span>

### <span data-ttu-id="6fb87-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fb87-116">-DefaultProfile</span></span>
<span data-ttu-id="6fb87-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6fb87-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fb87-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fb87-118">-InputObject</span></span>
<span data-ttu-id="6fb87-119">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="6fb87-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="6fb87-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="6fb87-120">-Name</span></span>
<span data-ttu-id="6fb87-121">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="6fb87-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="6fb87-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fb87-122">-ResourceGroupName</span></span>
<span data-ttu-id="6fb87-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="6fb87-123">Resource group name.</span></span>

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

### <span data-ttu-id="6fb87-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fb87-124">-ResourceId</span></span>
<span data-ttu-id="6fb87-125">Resurs-ID för Synapse.</span><span class="sxs-lookup"><span data-stu-id="6fb87-125">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="6fb87-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6fb87-126">-WorkspaceName</span></span>
<span data-ttu-id="6fb87-127">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="6fb87-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6fb87-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6fb87-128">-WorkspaceObject</span></span>
<span data-ttu-id="6fb87-129">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="6fb87-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6fb87-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fb87-130">CommonParameters</span></span>
<span data-ttu-id="6fb87-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fb87-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fb87-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6fb87-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fb87-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6fb87-133">INPUTS</span></span>

### <span data-ttu-id="6fb87-134">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6fb87-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6fb87-135">Microsoft. Azure. commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6fb87-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6fb87-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6fb87-136">OUTPUTS</span></span>

### <span data-ttu-id="6fb87-137">Microsoft. Azure. commands. Synapse. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="6fb87-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="6fb87-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6fb87-138">NOTES</span></span>

## <span data-ttu-id="6fb87-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6fb87-139">RELATED LINKS</span></span>
