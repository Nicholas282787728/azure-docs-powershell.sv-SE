---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: af51b5d864591f868db2ae588eed1d727fc53239
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091481"
---
# <span data-ttu-id="a090f-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="a090f-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="a090f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a090f-102">SYNOPSIS</span></span>
<span data-ttu-id="a090f-103">Anger prissättningen för Azure Security Center-nivån för ett scope.</span><span class="sxs-lookup"><span data-stu-id="a090f-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="a090f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a090f-104">SYNTAX</span></span>

### <span data-ttu-id="a090f-105">SubscriptionLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="a090f-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a090f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a090f-106">InputObject</span></span>
```
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a090f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a090f-107">DESCRIPTION</span></span>
<span data-ttu-id="a090f-108">Anger prissättningen för Azure Security Center-nivån för ett scope.</span><span class="sxs-lookup"><span data-stu-id="a090f-108">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="a090f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a090f-109">EXAMPLES</span></span>

### <span data-ttu-id="a090f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a090f-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "default" -PricingTier "Standard"
Id                                                                                                 Name    PricingTier
--                                                                                                 ----    -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default default Standard
```

<span data-ttu-id="a090f-111">Ställer in pris nivån för abonnemanget Azure Security Center till "standard"</span><span class="sxs-lookup"><span data-stu-id="a090f-111">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>

### <span data-ttu-id="a090f-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a090f-112">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "myService1" -ResourceGroupName "myService1" -PricingTier "Standard"

Id                                                                                                                     
--                                                                                                                     
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/...
```

<span data-ttu-id="a090f-113">Anger "myService1" resurs gruppen Azure Security Center pris nivå till "standard"</span><span class="sxs-lookup"><span data-stu-id="a090f-113">Sets the "myService1" resource group Azure Security Center pricing tier to "Standard"</span></span>

## <span data-ttu-id="a090f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a090f-114">PARAMETERS</span></span>

### <span data-ttu-id="a090f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a090f-115">-DefaultProfile</span></span>
<span data-ttu-id="a090f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a090f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a090f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a090f-117">-InputObject</span></span>
<span data-ttu-id="a090f-118">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="a090f-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a090f-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="a090f-119">-Name</span></span>
<span data-ttu-id="a090f-120">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="a090f-120">Resource name.</span></span>

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

### <span data-ttu-id="a090f-121">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="a090f-121">-PricingTier</span></span>
<span data-ttu-id="a090f-122">Pris nivå.</span><span class="sxs-lookup"><span data-stu-id="a090f-122">Pricing Tier.</span></span>

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

### <span data-ttu-id="a090f-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a090f-123">-Confirm</span></span>
<span data-ttu-id="a090f-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a090f-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a090f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a090f-125">-WhatIf</span></span>
<span data-ttu-id="a090f-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a090f-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a090f-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a090f-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a090f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a090f-128">CommonParameters</span></span>
<span data-ttu-id="a090f-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a090f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a090f-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a090f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a090f-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a090f-131">INPUTS</span></span>

### <span data-ttu-id="a090f-132">Microsoft. Azure. kommandon. Security. Models. priser. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="a090f-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="a090f-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a090f-133">OUTPUTS</span></span>

### <span data-ttu-id="a090f-134">Microsoft. Azure. kommandon. Security. Models. priser. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="a090f-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="a090f-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a090f-135">NOTES</span></span>

## <span data-ttu-id="a090f-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a090f-136">RELATED LINKS</span></span>
