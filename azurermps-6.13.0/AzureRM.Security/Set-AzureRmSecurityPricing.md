---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
ms.openlocfilehash: f5b23c9221fe8d344e9220590283ab7799a0a3fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576764"
---
# <span data-ttu-id="0af93-101">Set-AzureRmSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="0af93-101">Set-AzureRmSecurityPricing</span></span>

## <span data-ttu-id="0af93-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0af93-102">SYNOPSIS</span></span>
<span data-ttu-id="0af93-103">Anger prissättningen för Azure Security Center-nivån för ett scope.</span><span class="sxs-lookup"><span data-stu-id="0af93-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0af93-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0af93-104">SYNTAX</span></span>

### <span data-ttu-id="0af93-105">SubscriptionLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="0af93-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0af93-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="0af93-106">ResourceGroupLevelResource</span></span>
```
Set-AzureRmSecurityPricing -ResourceGroupName <String> -Name <String> -PricingTier <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0af93-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="0af93-107">InputObject</span></span>
```
Set-AzureRmSecurityPricing -InputObject <PSAddPricingInputObject> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0af93-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0af93-108">DESCRIPTION</span></span>
<span data-ttu-id="0af93-109">Anger prissättningen för Azure Security Center-nivån för ett scope.</span><span class="sxs-lookup"><span data-stu-id="0af93-109">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="0af93-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0af93-110">EXAMPLES</span></span>

### <span data-ttu-id="0af93-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0af93-111">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityPricing -Name "default" -PricingTier "Standard"
Id                                                                                                 Name    PricingTier
--                                                                                                 ----    -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default default Standard
```

<span data-ttu-id="0af93-112">Ställer in pris nivån för abonnemanget Azure Security Center till "standard"</span><span class="sxs-lookup"><span data-stu-id="0af93-112">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>

### <span data-ttu-id="0af93-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0af93-113">Example 2</span></span>
```powershell
PS C:\> Set-AzureRmSecurityPricing -Name "myService1" -ResourceGroupName "myService1" -PricingTier "Standard"

Id                                                                                                                     
--                                                                                                                     
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/...
```

<span data-ttu-id="0af93-114">Anger "myService1" resurs gruppen Azure Security Center pris nivå till "standard"</span><span class="sxs-lookup"><span data-stu-id="0af93-114">Sets the "myService1" resource group Azure Security Center pricing tier to "Standard"</span></span>

## <span data-ttu-id="0af93-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0af93-115">PARAMETERS</span></span>

### <span data-ttu-id="0af93-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0af93-116">-DefaultProfile</span></span>
<span data-ttu-id="0af93-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0af93-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0af93-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0af93-118">-InputObject</span></span>
<span data-ttu-id="0af93-119">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="0af93-119">Input Object.</span></span>

```yaml
Type: PSAddPricingInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0af93-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="0af93-120">-Name</span></span>
<span data-ttu-id="0af93-121">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="0af93-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af93-122">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="0af93-122">-PricingTier</span></span>
<span data-ttu-id="0af93-123">Pris nivå.</span><span class="sxs-lookup"><span data-stu-id="0af93-123">Pricing Tier.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af93-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0af93-124">-ResourceGroupName</span></span>
<span data-ttu-id="0af93-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="0af93-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af93-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0af93-126">-Confirm</span></span>
<span data-ttu-id="0af93-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0af93-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af93-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0af93-128">-WhatIf</span></span>
<span data-ttu-id="0af93-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0af93-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0af93-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0af93-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af93-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0af93-131">CommonParameters</span></span>
<span data-ttu-id="0af93-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0af93-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0af93-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0af93-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0af93-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0af93-134">INPUTS</span></span>

### <span data-ttu-id="0af93-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0af93-135">System.String</span></span>
<span data-ttu-id="0af93-136">Microsoft. Azure. kommandon. Security. cmdletar. priser. PSAddPricingInputObject</span><span class="sxs-lookup"><span data-stu-id="0af93-136">Microsoft.Azure.Commands.Security.Cmdlets.Pricings.PSAddPricingInputObject</span></span>

## <span data-ttu-id="0af93-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0af93-137">OUTPUTS</span></span>

### <span data-ttu-id="0af93-138">Microsoft. Azure. kommandon. Security. Models. priser. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="0af93-138">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="0af93-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0af93-139">NOTES</span></span>

## <span data-ttu-id="0af93-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0af93-140">RELATED LINKS</span></span>
