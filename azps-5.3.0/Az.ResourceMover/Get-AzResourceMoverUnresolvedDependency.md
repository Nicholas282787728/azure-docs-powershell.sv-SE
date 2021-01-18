---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemoverunresolveddependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
ms.openlocfilehash: 261ca79618f6d0568647f9126e0fddeaeb8db540
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523046"
---
# <span data-ttu-id="d944f-101">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="d944f-101">Get-AzResourceMoverUnresolvedDependency</span></span>

## <span data-ttu-id="d944f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d944f-102">SYNOPSIS</span></span>
<span data-ttu-id="d944f-103">Hämtar en lista med olösta samband.</span><span class="sxs-lookup"><span data-stu-id="d944f-103">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="d944f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d944f-104">SYNTAX</span></span>

```
Get-AzResourceMoverUnresolvedDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d944f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d944f-105">DESCRIPTION</span></span>
<span data-ttu-id="d944f-106">Hämtar en lista med olösta samband.</span><span class="sxs-lookup"><span data-stu-id="d944f-106">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="d944f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d944f-107">EXAMPLES</span></span>

### <span data-ttu-id="d944f-108">Exempel 1: Hämta lista med ej lösta beroende resurser</span><span class="sxs-lookup"><span data-stu-id="d944f-108">Example 1: Get list of unresolved dependent resources</span></span>
```powershell
PS C:\> Get-AzResourceMoverUnresolvedDependency -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM
Count Id
----- --
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/publicipaddresses/psdemovm-ip
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/virtualnetworks/psdemorm-vnet
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
```

<span data-ttu-id="d944f-109">Få en lista med ej lösta beroende resurser för en flytt mängd.</span><span class="sxs-lookup"><span data-stu-id="d944f-109">Get list of unresolved dependent resources for a Move collection.</span></span>

## <span data-ttu-id="d944f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d944f-110">PARAMETERS</span></span>

### <span data-ttu-id="d944f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d944f-111">-DefaultProfile</span></span>
<span data-ttu-id="d944f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d944f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d944f-113">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="d944f-113">-MoveCollectionName</span></span>
<span data-ttu-id="d944f-114">Namn på flytta-samlingen.</span><span class="sxs-lookup"><span data-stu-id="d944f-114">The Move Collection Name.</span></span>

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

### <span data-ttu-id="d944f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d944f-115">-ResourceGroupName</span></span>
<span data-ttu-id="d944f-116">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="d944f-116">The Resource Group Name.</span></span>

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

### <span data-ttu-id="d944f-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d944f-117">-SubscriptionId</span></span>
<span data-ttu-id="d944f-118">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="d944f-118">The Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d944f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d944f-119">CommonParameters</span></span>
<span data-ttu-id="d944f-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d944f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d944f-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d944f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d944f-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d944f-122">INPUTS</span></span>

## <span data-ttu-id="d944f-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d944f-123">OUTPUTS</span></span>

### <span data-ttu-id="d944f-124">Microsoft. Azure. PowerShell. cmdletar. ResourceMover. Models. Api20191001Preview. IUnresolvedDependencyCollection</span><span class="sxs-lookup"><span data-stu-id="d944f-124">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IUnresolvedDependencyCollection</span></span>

## <span data-ttu-id="d944f-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d944f-125">NOTES</span></span>

<span data-ttu-id="d944f-126">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d944f-126">ALIASES</span></span>

## <span data-ttu-id="d944f-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d944f-127">RELATED LINKS</span></span>

