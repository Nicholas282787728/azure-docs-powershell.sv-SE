---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
ms.openlocfilehash: 27d27cf3df8c41eaa507d9223c73f2b36637a04c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573898"
---
# <span data-ttu-id="e3fd3-101">Get-AzureRmSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="e3fd3-101">Get-AzureRmSecurityPricing</span></span>

## <span data-ttu-id="e3fd3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3fd3-102">SYNOPSIS</span></span>
<span data-ttu-id="e3fd3-103">Hämtar pris nivå data för Azure Security Center för ett scope.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-103">Gets the pricing tier data for Azure Security Center for a scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3fd3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3fd3-104">SYNTAX</span></span>

### <span data-ttu-id="e3fd3-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="e3fd3-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3fd3-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="e3fd3-106">ResourceGroupLevelResource</span></span>
```
Get-AzureRmSecurityPricing -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3fd3-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="e3fd3-107">ResourceGroupScope</span></span>
```
Get-AzureRmSecurityPricing -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3fd3-108">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="e3fd3-108">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3fd3-109">ID</span><span class="sxs-lookup"><span data-stu-id="e3fd3-109">ResourceId</span></span>
```
Get-AzureRmSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3fd3-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3fd3-110">DESCRIPTION</span></span>
<span data-ttu-id="e3fd3-111">Pris nivån för Azure Security Center bestäms per omfattning, med denna cmdlet kan du skaffa de konfigurerade pris nivåerna.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-111">Azure Security Center pricing tier is decided per scope, with this cmdlet you can get the configured pricing tiers.</span></span>
<span data-ttu-id="e3fd3-112">Pris nivån för abonnemanget inkluderar alla resurs grupper under den.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-112">Subscription pricing tier include all the resource groups under it.</span></span>
<span data-ttu-id="e3fd3-113">Pris nivån för resurs gruppen åsidosätter pris nivån för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-113">Resource Group pricing tier will override the subscription pricing tier.</span></span>

## <span data-ttu-id="e3fd3-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3fd3-114">EXAMPLES</span></span>

### <span data-ttu-id="e3fd3-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e3fd3-115">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityPricing
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default                              default    Standard
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="e3fd3-116">Hämtar alla konfigurerade pris nivåer för abonnemanget och resurs grupperna under den.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-116">Gets all the configured pricing tiers for the subscription and the resource groups under it.</span></span>

### <span data-ttu-id="e3fd3-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="e3fd3-117">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmSecurityPricing -ResourceGroupName "myService1"
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="e3fd3-118">Hämtar den konfigurerade pris nivån för resurs-gorup "myService1".</span><span class="sxs-lookup"><span data-stu-id="e3fd3-118">Gets the configured pricing tier for the "myService1" resource gorup.</span></span>

## <span data-ttu-id="e3fd3-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3fd3-119">PARAMETERS</span></span>

### <span data-ttu-id="e3fd3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3fd3-120">-DefaultProfile</span></span>
<span data-ttu-id="e3fd3-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3fd3-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="e3fd3-122">-Name</span></span>
<span data-ttu-id="e3fd3-123">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-123">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3fd3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3fd3-124">-ResourceGroupName</span></span>
<span data-ttu-id="e3fd3-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, ResourceGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3fd3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3fd3-126">-ResourceId</span></span>
<span data-ttu-id="e3fd3-127">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3fd3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3fd3-128">CommonParameters</span></span>
<span data-ttu-id="e3fd3-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3fd3-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3fd3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3fd3-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3fd3-131">INPUTS</span></span>

### <span data-ttu-id="e3fd3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e3fd3-132">System.String</span></span>

## <span data-ttu-id="e3fd3-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3fd3-133">OUTPUTS</span></span>

### <span data-ttu-id="e3fd3-134">Microsoft. Azure. kommandon. Security. Models. priser. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="e3fd3-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="e3fd3-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3fd3-135">NOTES</span></span>

## <span data-ttu-id="e3fd3-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3fd3-136">RELATED LINKS</span></span>
