---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
ms.openlocfilehash: d95892068b92745fa09419d83d3bdb001f0bdead
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393808"
---
# <span data-ttu-id="61122-101">Get-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="61122-101">Get-AzSynapseWorkspace</span></span>

## <span data-ttu-id="61122-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="61122-102">SYNOPSIS</span></span>
<span data-ttu-id="61122-103">Hämtar en Synapse Analytics-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="61122-103">Gets a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="61122-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="61122-104">SYNTAX</span></span>

### <span data-ttu-id="61122-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="61122-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61122-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61122-106">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseWorkspace -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61122-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="61122-107">DESCRIPTION</span></span>
<span data-ttu-id="61122-108">Cmdleten **Get-AzSynapseWorkspace** hämtar information om en Azure Synapse Analytics-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="61122-108">The **Get-AzSynapseWorkspace** cmdlet gets information about an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="61122-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="61122-109">EXAMPLES</span></span>

### <span data-ttu-id="61122-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="61122-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace
```

<span data-ttu-id="61122-111">Det här kommandot får alla Azure Synapse-arbetsytor under det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="61122-111">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="61122-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="61122-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup
```

<span data-ttu-id="61122-113">Det här kommandot får alla Azure Synapse-arbetsytor under det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="61122-113">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="61122-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="61122-114">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="61122-115">Det här kommandot får Azure Synapse-arbets ytan med det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="61122-115">This command gets the Azure Synapse Analytics workspace with the specified name.</span></span>

### <span data-ttu-id="61122-116">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="61122-116">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="61122-117">Det här kommandot får Azure Synapse-arbets ytan med angivet resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="61122-117">This command gets the Azure Synapse Analytics workspace with the specified resource ID.</span></span>

## <span data-ttu-id="61122-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="61122-118">PARAMETERS</span></span>

### <span data-ttu-id="61122-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61122-119">-DefaultProfile</span></span>
<span data-ttu-id="61122-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="61122-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61122-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="61122-121">-Name</span></span>
<span data-ttu-id="61122-122">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="61122-122">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: WorkspaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61122-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61122-123">-ResourceGroupName</span></span>
<span data-ttu-id="61122-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="61122-124">Resource group name.</span></span>

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

### <span data-ttu-id="61122-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61122-125">-ResourceId</span></span>
<span data-ttu-id="61122-126">Resurs-ID för Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="61122-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="61122-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61122-127">CommonParameters</span></span>
<span data-ttu-id="61122-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61122-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61122-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61122-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61122-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="61122-130">INPUTS</span></span>

### <span data-ttu-id="61122-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="61122-131">None</span></span>

## <span data-ttu-id="61122-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="61122-132">OUTPUTS</span></span>

### <span data-ttu-id="61122-133">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="61122-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="61122-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="61122-134">NOTES</span></span>

## <span data-ttu-id="61122-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="61122-135">RELATED LINKS</span></span>
