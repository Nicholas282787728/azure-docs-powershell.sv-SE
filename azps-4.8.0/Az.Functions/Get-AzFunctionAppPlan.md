---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
ms.openlocfilehash: d08d050253842e13967d001889e1b7d1b331ce17
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261301"
---
# <span data-ttu-id="dc8f9-101">Get-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="dc8f9-101">Get-AzFunctionAppPlan</span></span>

## <span data-ttu-id="dc8f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dc8f9-102">SYNOPSIS</span></span>
<span data-ttu-id="dc8f9-103">Prenumerera på funktions programs planer.</span><span class="sxs-lookup"><span data-stu-id="dc8f9-103">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="dc8f9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dc8f9-104">SYNTAX</span></span>

### <span data-ttu-id="dc8f9-105">GetAll (standard)</span><span class="sxs-lookup"><span data-stu-id="dc8f9-105">GetAll (Default)</span></span>
```
Get-AzFunctionAppPlan [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dc8f9-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="dc8f9-106">ByLocation</span></span>
```
Get-AzFunctionAppPlan -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc8f9-107">ByName</span><span class="sxs-lookup"><span data-stu-id="dc8f9-107">ByName</span></span>
```
Get-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dc8f9-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc8f9-108">ByResourceGroupName</span></span>
```
Get-AzFunctionAppPlan [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc8f9-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dc8f9-109">DESCRIPTION</span></span>
<span data-ttu-id="dc8f9-110">Prenumerera på funktions programs planer.</span><span class="sxs-lookup"><span data-stu-id="dc8f9-110">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="dc8f9-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dc8f9-111">EXAMPLES</span></span>

### <span data-ttu-id="dc8f9-112">Exempel 1: Hämta alla program planer för funktioner.</span><span class="sxs-lookup"><span data-stu-id="dc8f9-112">Example 1: Get all function app plans.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium428118799    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium677505437    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium711892854    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium819994758    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="dc8f9-113">Det här kommandot får alla program planer för funktioner.</span><span class="sxs-lookup"><span data-stu-id="dc8f9-113">This command gets all function app plans.</span></span>

### <span data-ttu-id="dc8f9-114">Exempel 2: Hämta program abonnemang efter resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="dc8f9-114">Example 2: Get function app plans by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -ResourceGroupName "West Europe"

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="dc8f9-115">Det här kommandot hämtar funktions program planer efter resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="dc8f9-115">This command gets function app plans by resource group name.</span></span>

### <span data-ttu-id="dc8f9-116">Exempel 3: skaffa program abonnemang för de angivna abonnemangen.</span><span class="sxs-lookup"><span data-stu-id="dc8f9-116">Example 3: Get function app plans for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8z

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8z
```

<span data-ttu-id="dc8f9-117">Det här kommandot får ett program abonnemang för de angivna prenumerationerna.</span><span class="sxs-lookup"><span data-stu-id="dc8f9-117">This command gets function app plans for the given subscriptions.</span></span>

### <span data-ttu-id="dc8f9-118">Exempel 4: Hämta program planering för funktioner efter plats.</span><span class="sxs-lookup"><span data-stu-id="dc8f9-118">Example 4: Get function app plans by location.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Location "Central US"

Name                               WorkerType SkuTier        SkuName Location   ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------   -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     Central US Func99-West-Europe-Win-Premium   3r16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="dc8f9-119">Det här kommandot får ett funktions program abonnemang efter plats.</span><span class="sxs-lookup"><span data-stu-id="dc8f9-119">This command gets function app plans by location.</span></span>

## <span data-ttu-id="dc8f9-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dc8f9-120">PARAMETERS</span></span>

### <span data-ttu-id="dc8f9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc8f9-121">-DefaultProfile</span></span>
<span data-ttu-id="dc8f9-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dc8f9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc8f9-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="dc8f9-123">-Location</span></span>
<span data-ttu-id="dc8f9-124">Platsen för funktionen program plan.</span><span class="sxs-lookup"><span data-stu-id="dc8f9-124">The location of the function app plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc8f9-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="dc8f9-125">-Name</span></span>
<span data-ttu-id="dc8f9-126">Namnet på service abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="dc8f9-126">The service plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc8f9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc8f9-127">-ResourceGroupName</span></span>
<span data-ttu-id="dc8f9-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="dc8f9-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc8f9-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dc8f9-129">-SubscriptionId</span></span>
<span data-ttu-id="dc8f9-130">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="dc8f9-130">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="dc8f9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc8f9-131">CommonParameters</span></span>
<span data-ttu-id="dc8f9-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc8f9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc8f9-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc8f9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc8f9-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dc8f9-134">INPUTS</span></span>

## <span data-ttu-id="dc8f9-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dc8f9-135">OUTPUTS</span></span>

### <span data-ttu-id="dc8f9-136">Microsoft. Azure. PowerShell. cmdletar. functions. Models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="dc8f9-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="dc8f9-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dc8f9-137">NOTES</span></span>

<span data-ttu-id="dc8f9-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="dc8f9-138">ALIASES</span></span>

## <span data-ttu-id="dc8f9-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dc8f9-139">RELATED LINKS</span></span>
