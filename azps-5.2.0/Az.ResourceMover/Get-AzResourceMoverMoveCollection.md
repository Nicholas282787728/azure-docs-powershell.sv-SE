---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 73bb67577a9160440c2e42e1e5b3259ad8435c5c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396483"
---
# <span data-ttu-id="f5d66-101">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="f5d66-101">Get-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="f5d66-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f5d66-102">SYNOPSIS</span></span>
<span data-ttu-id="f5d66-103">Hämtar flytt mängden.</span><span class="sxs-lookup"><span data-stu-id="f5d66-103">Gets the move collection.</span></span>

## <span data-ttu-id="f5d66-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f5d66-104">SYNTAX</span></span>

### <span data-ttu-id="f5d66-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="f5d66-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveCollection [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f5d66-106">Lära</span><span class="sxs-lookup"><span data-stu-id="f5d66-106">Get</span></span>
```
Get-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f5d66-107">List1</span><span class="sxs-lookup"><span data-stu-id="f5d66-107">List1</span></span>
```
Get-AzResourceMoverMoveCollection -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f5d66-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f5d66-108">DESCRIPTION</span></span>
<span data-ttu-id="f5d66-109">Hämtar flytt mängden.</span><span class="sxs-lookup"><span data-stu-id="f5d66-109">Gets the move collection.</span></span>

## <span data-ttu-id="f5d66-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f5d66-110">EXAMPLES</span></span>

### <span data-ttu-id="f5d66-111">Exempel 1: få information om alla flytt samlingar i prenumerationen</span><span class="sxs-lookup"><span data-stu-id="f5d66-111">Example 1:  Get details of all the Move collections in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection  -SubscriptionId e80eb9fa-c996-4435-aa32-5af6f3d3077c

Location    Name                                            Type
--------    ----                                            ----
eastus2     mvcolle2e07001                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e34745                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e56720                                  Microsoft.Migrate/moveCollections


```

<span data-ttu-id="f5d66-112">Få information om alla flytt samlingar i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f5d66-112">Get details of all the Move collections in the subscription.</span></span>

### <span data-ttu-id="f5d66-113">Exempel 2: få information om flytt samlingen med ett angivet namn för flytta i prenumerationen</span><span class="sxs-lookup"><span data-stu-id="f5d66-113">Example 2: Get details of the Move collection with a specified move collection name in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM -Name PS-centralus-westcentralus-demoRM

Location    Name                              Type
--------    ----                              ----
eastus2     PS-centralus-westcentralus-demoRM Microsoft.Migrate/moveCollections

```

<span data-ttu-id="f5d66-114">Få information om flytt samlingen med ett angivet namn för flytta i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f5d66-114">Get details of the Move collection with a specified move collection name in the subscription.</span></span>

### <span data-ttu-id="f5d66-115">Exempel 3: få information om flytt samlingen med ett angivet resurs grupp namn i prenumerationen</span><span class="sxs-lookup"><span data-stu-id="f5d66-115">Example 3: Get details of the Move collection with a specified resource group name in the subscription</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM 

Location    Name                               Type
--------    ----                               ----
eastus2     PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
eastus2euap PS-centralus-westcentralus-demoRM2 Microsoft.Migrate/moveCollections


```

<span data-ttu-id="f5d66-116">Få information om flytt samlingen med ett angivet resurs grupp namn i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f5d66-116">Get details of the Move Collection with a specified resource group name in the subscription.</span></span>

## <span data-ttu-id="f5d66-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f5d66-117">PARAMETERS</span></span>

### <span data-ttu-id="f5d66-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5d66-118">-DefaultProfile</span></span>
<span data-ttu-id="f5d66-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f5d66-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5d66-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="f5d66-120">-Name</span></span>
<span data-ttu-id="f5d66-121">Namn på flytta-samlingen.</span><span class="sxs-lookup"><span data-stu-id="f5d66-121">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5d66-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5d66-122">-ResourceGroupName</span></span>
<span data-ttu-id="f5d66-123">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="f5d66-123">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5d66-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f5d66-124">-SubscriptionId</span></span>
<span data-ttu-id="f5d66-125">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="f5d66-125">The Subscription ID.</span></span>

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

### <span data-ttu-id="f5d66-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5d66-126">CommonParameters</span></span>
<span data-ttu-id="f5d66-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5d66-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5d66-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5d66-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5d66-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f5d66-129">INPUTS</span></span>

## <span data-ttu-id="f5d66-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f5d66-130">OUTPUTS</span></span>

### <span data-ttu-id="f5d66-131">Microsoft. Azure. PowerShell. cmdletar. ResourceMover. Models. Api20191001Preview. IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="f5d66-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="f5d66-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f5d66-132">NOTES</span></span>

<span data-ttu-id="f5d66-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f5d66-133">ALIASES</span></span>

## <span data-ttu-id="f5d66-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f5d66-134">RELATED LINKS</span></span>

