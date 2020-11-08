---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: a1b07c5fb76d912ec117d42497f0d0b14bfb298c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258021"
---
# <span data-ttu-id="d457e-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="d457e-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="d457e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d457e-102">SYNOPSIS</span></span>
<span data-ttu-id="d457e-103">Hämtar pris nivå data för Azure Security Center för ett scope.</span><span class="sxs-lookup"><span data-stu-id="d457e-103">Gets the pricing tier data for Azure Security Center for a scope.</span></span>

## <span data-ttu-id="d457e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d457e-104">SYNTAX</span></span>

### <span data-ttu-id="d457e-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="d457e-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d457e-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="d457e-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d457e-107">ID</span><span class="sxs-lookup"><span data-stu-id="d457e-107">ResourceId</span></span>
```
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d457e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d457e-108">DESCRIPTION</span></span>
<span data-ttu-id="d457e-109">Pris nivån för Azure Security Center bestäms per omfattning, med denna cmdlet kan du skaffa de konfigurerade pris nivåerna.</span><span class="sxs-lookup"><span data-stu-id="d457e-109">Azure Security Center pricing tier is decided per scope, with this cmdlet you can get the configured pricing tiers.</span></span>
<span data-ttu-id="d457e-110">Pris nivån för abonnemanget inkluderar alla resurs grupper under den.</span><span class="sxs-lookup"><span data-stu-id="d457e-110">Subscription pricing tier include all the resource groups under it.</span></span>
<span data-ttu-id="d457e-111">Pris nivån för resurs gruppen åsidosätter pris nivån för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="d457e-111">Resource Group pricing tier will override the subscription pricing tier.</span></span>

## <span data-ttu-id="d457e-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d457e-112">EXAMPLES</span></span>

### <span data-ttu-id="d457e-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d457e-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityPricing
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
Id--/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/VirtualMachines
--                                                                                                                             ----       -----------
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/SqlServers
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default                              default    Standard
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/AppServices
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/StorageAccounts
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/SqlServerVirtualMachin…
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KubernetesService
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/ContainerRegistry
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KeyVaults
```

<span data-ttu-id="d457e-114">Hämtar alla konfigurerade pris nivåer för abonnemanget och resurs grupperna under den.</span><span class="sxs-lookup"><span data-stu-id="d457e-114">Gets all the configured pricing tiers for the subscription and the resource groups under it.</span></span>

### <span data-ttu-id="d457e-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d457e-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityPricing -ResourceGroupName "myService1"
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="d457e-116">Hämtar den konfigurerade pris nivån för resurs gruppen "myService1".</span><span class="sxs-lookup"><span data-stu-id="d457e-116">Gets the configured pricing tier for the "myService1" resource group.</span></span>

## <span data-ttu-id="d457e-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d457e-117">PARAMETERS</span></span>

### <span data-ttu-id="d457e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d457e-118">-DefaultProfile</span></span>
<span data-ttu-id="d457e-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d457e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d457e-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="d457e-120">-Name</span></span>
<span data-ttu-id="d457e-121">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="d457e-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d457e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d457e-122">-ResourceId</span></span>
<span data-ttu-id="d457e-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="d457e-123">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d457e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d457e-124">CommonParameters</span></span>
<span data-ttu-id="d457e-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d457e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d457e-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d457e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d457e-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d457e-127">INPUTS</span></span>

### <span data-ttu-id="d457e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d457e-128">System.String</span></span>

## <span data-ttu-id="d457e-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d457e-129">OUTPUTS</span></span>

### <span data-ttu-id="d457e-130">Microsoft. Azure. kommandon. Security. Models. priser. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="d457e-130">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="d457e-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d457e-131">NOTES</span></span>

## <span data-ttu-id="d457e-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d457e-132">RELATED LINKS</span></span>
