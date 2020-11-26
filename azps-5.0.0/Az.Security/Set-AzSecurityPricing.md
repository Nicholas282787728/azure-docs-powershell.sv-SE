---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: e9dfe0e7ed4612ca99a2decf3aa91b521a7e9664
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271227"
---
# <span data-ttu-id="801cb-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="801cb-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="801cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="801cb-102">SYNOPSIS</span></span>
<span data-ttu-id="801cb-103">Anger prissättningen för Azure Security Center-nivån för ett scope.</span><span class="sxs-lookup"><span data-stu-id="801cb-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="801cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="801cb-104">SYNTAX</span></span>

### <span data-ttu-id="801cb-105">SubscriptionLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="801cb-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="801cb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="801cb-106">InputObject</span></span>
```
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="801cb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="801cb-107">DESCRIPTION</span></span>
<span data-ttu-id="801cb-108">Anger prissättningen för Azure Security Center-nivån för ett scope.</span><span class="sxs-lookup"><span data-stu-id="801cb-108">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="801cb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="801cb-109">EXAMPLES</span></span>

### <span data-ttu-id="801cb-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="801cb-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "virtualmachines" -PricingTier "Standard"
```

<span data-ttu-id="801cb-111">Ställer in pris nivån för abonnemanget Azure Security Center till "standard"</span><span class="sxs-lookup"><span data-stu-id="801cb-111">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>


## <span data-ttu-id="801cb-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="801cb-112">PARAMETERS</span></span>

### <span data-ttu-id="801cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="801cb-113">-DefaultProfile</span></span>
<span data-ttu-id="801cb-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="801cb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="801cb-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="801cb-115">-InputObject</span></span>
<span data-ttu-id="801cb-116">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="801cb-116">Input Object.</span></span>

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

### <span data-ttu-id="801cb-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="801cb-117">-Name</span></span>
<span data-ttu-id="801cb-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="801cb-118">Resource name.</span></span>

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

### <span data-ttu-id="801cb-119">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="801cb-119">-PricingTier</span></span>
<span data-ttu-id="801cb-120">Pris nivå.</span><span class="sxs-lookup"><span data-stu-id="801cb-120">Pricing Tier.</span></span>

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

### <span data-ttu-id="801cb-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="801cb-121">-Confirm</span></span>
<span data-ttu-id="801cb-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="801cb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="801cb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="801cb-123">-WhatIf</span></span>
<span data-ttu-id="801cb-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="801cb-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="801cb-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="801cb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="801cb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="801cb-126">CommonParameters</span></span>
<span data-ttu-id="801cb-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="801cb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="801cb-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="801cb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="801cb-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="801cb-129">INPUTS</span></span>

### <span data-ttu-id="801cb-130">Microsoft. Azure. kommandon. Security. Models. priser. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="801cb-130">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="801cb-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="801cb-131">OUTPUTS</span></span>

### <span data-ttu-id="801cb-132">Microsoft. Azure. kommandon. Security. Models. priser. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="801cb-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="801cb-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="801cb-133">NOTES</span></span>

## <span data-ttu-id="801cb-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="801cb-134">RELATED LINKS</span></span>