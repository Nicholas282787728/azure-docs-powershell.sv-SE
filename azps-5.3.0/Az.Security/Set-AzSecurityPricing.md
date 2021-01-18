---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: 96f5a9d4791dc2668e4ec82abc140f17cbce7c44
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525613"
---
# <span data-ttu-id="929a0-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="929a0-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="929a0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="929a0-102">SYNOPSIS</span></span>

<span data-ttu-id="929a0-103">Aktiverar eller inaktiverar Azure Defender-abonnemang för en prenumeration i Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="929a0-103">Enables or disables Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="929a0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="929a0-104">SYNTAX</span></span>

### <span data-ttu-id="929a0-105">SubscriptionLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="929a0-105">SubscriptionLevelResource (Default)</span></span>

```powershell
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="929a0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="929a0-106">InputObject</span></span>

```powershell
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="929a0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="929a0-107">DESCRIPTION</span></span>

<span data-ttu-id="929a0-108">Aktivera eller inaktivera något av Azure Defender-abonnemangen för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="929a0-108">Enable or disable any of the Azure Defender plans for a subscription.</span></span>

<span data-ttu-id="929a0-109">Mer information om Azure Defender och tillgängliga abonnemang finns i [Introduktion till Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span><span class="sxs-lookup"><span data-stu-id="929a0-109">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="929a0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="929a0-110">EXAMPLES</span></span>

### <span data-ttu-id="929a0-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="929a0-111">Example 1</span></span>

```powershell
PS C:\> Set-AzSecurityPricing -Name "virtualmachines" -PricingTier "Standard"
```

<span data-ttu-id="929a0-112">Aktiverar **Azure Defender för servrar** för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="929a0-112">Enables **Azure Defender for servers** for the subscription.</span></span>

<span data-ttu-id="929a0-113">"Standard" syftar på tillståndet "on" för en Azure Defender-plan som visas i Azure Security Centers området för prissättning och inställningar i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="929a0-113">"Standard" refers to the "On" state for an Azure Defender plan as shown in Azure Security Center's pricing and settings area of the Azure portal.</span></span>


## <span data-ttu-id="929a0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="929a0-114">PARAMETERS</span></span>

### <span data-ttu-id="929a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="929a0-115">-DefaultProfile</span></span>

<span data-ttu-id="929a0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="929a0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="929a0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="929a0-117">-InputObject</span></span>

<span data-ttu-id="929a0-118">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="929a0-118">Input Object.</span></span>

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

### <span data-ttu-id="929a0-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="929a0-119">-Name</span></span>

<span data-ttu-id="929a0-120">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="929a0-120">Resource name.</span></span>

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

### <span data-ttu-id="929a0-121">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="929a0-121">-PricingTier</span></span>

<span data-ttu-id="929a0-122">Pris nivå.</span><span class="sxs-lookup"><span data-stu-id="929a0-122">Pricing Tier.</span></span>

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

### <span data-ttu-id="929a0-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="929a0-123">-Confirm</span></span>

<span data-ttu-id="929a0-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="929a0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="929a0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="929a0-125">-WhatIf</span></span>

<span data-ttu-id="929a0-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="929a0-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="929a0-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="929a0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="929a0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="929a0-128">CommonParameters</span></span>

<span data-ttu-id="929a0-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="929a0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="929a0-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="929a0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="929a0-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="929a0-131">INPUTS</span></span>

### <span data-ttu-id="929a0-132">Microsoft. Azure. kommandon. Security. Models. priser. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="929a0-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="929a0-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="929a0-133">OUTPUTS</span></span>

### <span data-ttu-id="929a0-134">Microsoft. Azure. kommandon. Security. Models. priser. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="929a0-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="929a0-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="929a0-135">NOTES</span></span>

## <span data-ttu-id="929a0-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="929a0-136">RELATED LINKS</span></span>
