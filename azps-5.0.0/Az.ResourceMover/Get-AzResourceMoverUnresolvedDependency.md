---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemoverunresolveddependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
ms.openlocfilehash: 261ca79618f6d0568647f9126e0fddeaeb8db540
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324335"
---
# <span data-ttu-id="4352c-101">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="4352c-101">Get-AzResourceMoverUnresolvedDependency</span></span>

## <span data-ttu-id="4352c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4352c-102">SYNOPSIS</span></span>
<span data-ttu-id="4352c-103">Hämtar en lista med olösta samband.</span><span class="sxs-lookup"><span data-stu-id="4352c-103">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="4352c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4352c-104">SYNTAX</span></span>

```
Get-AzResourceMoverUnresolvedDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4352c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4352c-105">DESCRIPTION</span></span>
<span data-ttu-id="4352c-106">Hämtar en lista med olösta samband.</span><span class="sxs-lookup"><span data-stu-id="4352c-106">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="4352c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4352c-107">EXAMPLES</span></span>

### <span data-ttu-id="4352c-108">Exempel 1: Hämta lista med ej lösta beroende resurser</span><span class="sxs-lookup"><span data-stu-id="4352c-108">Example 1: Get list of unresolved dependent resources</span></span>
```powershell
PS C:\> Get-AzResourceMoverUnresolvedDependency -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM
Count Id
----- --
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/publicipaddresses/psdemovm-ip
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/virtualnetworks/psdemorm-vnet
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
```

<span data-ttu-id="4352c-109">Få en lista med ej lösta beroende resurser för en flytt mängd.</span><span class="sxs-lookup"><span data-stu-id="4352c-109">Get list of unresolved dependent resources for a Move collection.</span></span>

## <span data-ttu-id="4352c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4352c-110">PARAMETERS</span></span>

### <span data-ttu-id="4352c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4352c-111">-DefaultProfile</span></span>
<span data-ttu-id="4352c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4352c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4352c-113">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="4352c-113">-MoveCollectionName</span></span>
<span data-ttu-id="4352c-114">Namn på flytta-samlingen.</span><span class="sxs-lookup"><span data-stu-id="4352c-114">The Move Collection Name.</span></span>

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

### <span data-ttu-id="4352c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4352c-115">-ResourceGroupName</span></span>
<span data-ttu-id="4352c-116">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4352c-116">The Resource Group Name.</span></span>

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

### <span data-ttu-id="4352c-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4352c-117">-SubscriptionId</span></span>
<span data-ttu-id="4352c-118">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="4352c-118">The Subscription ID.</span></span>

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

### <span data-ttu-id="4352c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4352c-119">CommonParameters</span></span>
<span data-ttu-id="4352c-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4352c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4352c-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4352c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4352c-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4352c-122">INPUTS</span></span>

## <span data-ttu-id="4352c-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4352c-123">OUTPUTS</span></span>

### <span data-ttu-id="4352c-124">Microsoft. Azure. PowerShell. cmdletar. ResourceMover. Models. Api20191001Preview. IUnresolvedDependencyCollection</span><span class="sxs-lookup"><span data-stu-id="4352c-124">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IUnresolvedDependencyCollection</span></span>

## <span data-ttu-id="4352c-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4352c-125">NOTES</span></span>

<span data-ttu-id="4352c-126">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4352c-126">ALIASES</span></span>

## <span data-ttu-id="4352c-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4352c-127">RELATED LINKS</span></span>

