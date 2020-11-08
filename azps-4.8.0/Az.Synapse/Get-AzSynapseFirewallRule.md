---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
ms.openlocfilehash: 22a7bb4c135a4424aa27a76f9e13ba14f21ca572
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100712"
---
# <span data-ttu-id="96640-101">Get-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="96640-101">Get-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="96640-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96640-102">SYNOPSIS</span></span>
<span data-ttu-id="96640-103">Hämtar en Synapse för analys brand vägg.</span><span class="sxs-lookup"><span data-stu-id="96640-103">Gets a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="96640-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96640-104">SYNTAX</span></span>

### <span data-ttu-id="96640-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="96640-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96640-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96640-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseFirewallRule -WorkSpaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96640-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96640-107">DESCRIPTION</span></span>
<span data-ttu-id="96640-108">Cmdleten **Get-AzSynapseFirewallRule** har en Azure Synapse Analytics Firewall-regel.</span><span class="sxs-lookup"><span data-stu-id="96640-108">The **Get-AzSynapseFirewallRule** cmdlet gets a Azure Synapse Analytics Firewall Rule.</span></span>
<span data-ttu-id="96640-109">Om du inte anger ett regel namn hämtas den här cmdleten alla regler.</span><span class="sxs-lookup"><span data-stu-id="96640-109">If you do not specify a rule name, this cmdlet gets all rules.</span></span>

## <span data-ttu-id="96640-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96640-110">EXAMPLES</span></span>

### <span data-ttu-id="96640-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="96640-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="96640-112">Det här kommandot får alla brand Väggs regler under en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="96640-112">This command gets all firewall rules under a workspace.</span></span>

### <span data-ttu-id="96640-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="96640-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="96640-114">Det här kommandot får brand Väggs regeln under arbets ytan ContosoWorkspace med namnet ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="96640-114">This command gets the firewall rule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="96640-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="96640-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseFirewallRule
```

<span data-ttu-id="96640-116">Det här kommandot får alla brand Väggs regler under en arbets yta genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="96640-116">This command gets all firewall rules under a workspace through pipeline.</span></span>

## <span data-ttu-id="96640-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96640-117">PARAMETERS</span></span>

### <span data-ttu-id="96640-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96640-118">-DefaultProfile</span></span>
<span data-ttu-id="96640-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="96640-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96640-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="96640-120">-Name</span></span>
<span data-ttu-id="96640-121">Firerwall regel namn för arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="96640-121">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96640-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96640-122">-ResourceGroupName</span></span>
<span data-ttu-id="96640-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="96640-123">Resource group name.</span></span>

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

### <span data-ttu-id="96640-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="96640-124">-WorkspaceName</span></span>
<span data-ttu-id="96640-125">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="96640-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="96640-126">-WorkSpaceObject</span><span class="sxs-lookup"><span data-stu-id="96640-126">-WorkSpaceObject</span></span>
<span data-ttu-id="96640-127">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="96640-127">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="96640-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96640-128">CommonParameters</span></span>
<span data-ttu-id="96640-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96640-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96640-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96640-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96640-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96640-131">INPUTS</span></span>

### <span data-ttu-id="96640-132">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="96640-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="96640-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96640-133">OUTPUTS</span></span>

### <span data-ttu-id="96640-134">Microsoft. Azure. commands. Synapse. Models. PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="96640-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="96640-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96640-135">NOTES</span></span>

## <span data-ttu-id="96640-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96640-136">RELATED LINKS</span></span>