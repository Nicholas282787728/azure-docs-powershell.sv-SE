---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
ms.openlocfilehash: a6308120303684a8e87280ef903056361fbaf848
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395899"
---
# <span data-ttu-id="ae1d0-101">Get-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="ae1d0-101">Get-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="ae1d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ae1d0-102">SYNOPSIS</span></span>
<span data-ttu-id="ae1d0-103">Få eller Visa en lista över närhets resurser.</span><span class="sxs-lookup"><span data-stu-id="ae1d0-103">Get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="ae1d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ae1d0-104">SYNTAX</span></span>

### <span data-ttu-id="ae1d0-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="ae1d0-105">DefaultParameter (Default)</span></span>
```
Get-AzProximityPlacementGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-ColocationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae1d0-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="ae1d0-106">ResourceIdParameter</span></span>
```
Get-AzProximityPlacementGroup [-ColocationStatus] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae1d0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ae1d0-107">DESCRIPTION</span></span>
<span data-ttu-id="ae1d0-108">Denna cmdlet hämtar eller visar en lista över närhets placeringar.</span><span class="sxs-lookup"><span data-stu-id="ae1d0-108">This cmdlet will get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="ae1d0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ae1d0-109">EXAMPLES</span></span>

### <span data-ttu-id="ae1d0-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ae1d0-110">Example 1</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName

ResourceGroupName           : rg0
ProximityPlacementGroupType : Standard
VirtualMachines             : {}
VirtualMachineScaleSets     : {}
AvailabilitySets            : {}
Id                          : /subscriptions/5393f919-a68a-43d0-9063-4b2bda6bffdf/resourceGroups/rg0/providers/Microsoft.Compute/proximityPlacementGroups/ppg0
Name                        : ppg0
Type                        : Microsoft.Compute/proximityPlacementGroups
Location                    : westcentralus
Tags                        : {[key1, val1]}
```

<span data-ttu-id="ae1d0-111">Det här kommandot får plats gruppen närhet</span><span class="sxs-lookup"><span data-stu-id="ae1d0-111">This command gets the proximity placement group</span></span>

### <span data-ttu-id="ae1d0-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ae1d0-112">Example 2</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
```

<span data-ttu-id="ae1d0-113">Det här kommandot visar alla närhets placerings grupper under den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ae1d0-113">This command list all proximity placement groups under the given resource group.</span></span>

### <span data-ttu-id="ae1d0-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="ae1d0-114">Example 3</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
rg1                          ppg2     centralus Standard
```

<span data-ttu-id="ae1d0-115">Det här kommandot visar alla närhets placerings grupper under abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="ae1d0-115">This command list all proximity placement groups under the subscription.</span></span>

## <span data-ttu-id="ae1d0-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ae1d0-116">PARAMETERS</span></span>

### <span data-ttu-id="ae1d0-117">-ColocationStatus</span><span class="sxs-lookup"><span data-stu-id="ae1d0-117">-ColocationStatus</span></span>
<span data-ttu-id="ae1d0-118">Visar statusen för en resurs i gruppen närhets placering.</span><span class="sxs-lookup"><span data-stu-id="ae1d0-118">Shows the colocation status of a resource in the proximity placement group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae1d0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae1d0-119">-DefaultProfile</span></span>
<span data-ttu-id="ae1d0-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ae1d0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae1d0-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="ae1d0-121">-Name</span></span>
<span data-ttu-id="ae1d0-122">Namnet på närhets placerings gruppen.</span><span class="sxs-lookup"><span data-stu-id="ae1d0-122">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: ProximityPlacementGroupName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="ae1d0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae1d0-123">-ResourceGroupName</span></span>
<span data-ttu-id="ae1d0-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ae1d0-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="ae1d0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae1d0-125">-ResourceId</span></span>
<span data-ttu-id="ae1d0-126">Resurs-ID för placering av närhet.</span><span class="sxs-lookup"><span data-stu-id="ae1d0-126">The resource id for the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae1d0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae1d0-127">CommonParameters</span></span>
<span data-ttu-id="ae1d0-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae1d0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae1d0-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae1d0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae1d0-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ae1d0-130">INPUTS</span></span>

### <span data-ttu-id="ae1d0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ae1d0-131">System.String</span></span>

## <span data-ttu-id="ae1d0-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ae1d0-132">OUTPUTS</span></span>

### <span data-ttu-id="ae1d0-133">Microsoft. Azure. commands. Compute. Automation. Models. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="ae1d0-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="ae1d0-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ae1d0-134">NOTES</span></span>

## <span data-ttu-id="ae1d0-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ae1d0-135">RELATED LINKS</span></span>
