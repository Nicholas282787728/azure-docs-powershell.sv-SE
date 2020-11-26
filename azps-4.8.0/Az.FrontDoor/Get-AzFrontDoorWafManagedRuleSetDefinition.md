---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafmanagedrulesetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
ms.openlocfilehash: d93431066acd3747d6c7dcbea2eae7cd259ee21b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262682"
---
# <span data-ttu-id="3c828-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="3c828-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span></span>

## <span data-ttu-id="3c828-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c828-102">SYNOPSIS</span></span>
<span data-ttu-id="3c828-103">Hämta WAF definitioner för hanterade regel uppsättningar</span><span class="sxs-lookup"><span data-stu-id="3c828-103">Get WAF managed rule set definitions</span></span>

## <span data-ttu-id="3c828-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c828-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafManagedRuleSetDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c828-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c828-105">DESCRIPTION</span></span>
<span data-ttu-id="3c828-106">Hämtar listan över definitioner för WAF hanterade regel uppsättningar som ska användas som referens</span><span class="sxs-lookup"><span data-stu-id="3c828-106">Gets the list of WAF managed rule set definitions to use as reference</span></span>

## <span data-ttu-id="3c828-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c828-107">EXAMPLES</span></span>

### <span data-ttu-id="3c828-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3c828-108">Example 1</span></span>
```powershell
PS C:> Get-AzFrontDoorWafManagedRuleSetDefinition

ProvisioningState RuleSetType                 RuleSetVersion RuleGroups
----------------- -----------                 -------------- ----------
Succeeded         DefaultRuleSet              1.0            {PROTOCOL-ATTACK, LFI, RFI, RCE...}
Succeeded         Microsoft_BotManagerRuleSet 1.0            {BadBots, GoodBots, UnknownBots}
Succeeded         DefaultRuleSet              preview-0.1    {LFI, RFI, RCE, PHP...}
Succeeded         BotProtection               preview-0.1    {KnownBadBots}
```

<span data-ttu-id="3c828-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="3c828-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="3c828-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c828-110">PARAMETERS</span></span>

### <span data-ttu-id="3c828-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c828-111">-DefaultProfile</span></span>
<span data-ttu-id="3c828-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3c828-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c828-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c828-113">CommonParameters</span></span>
<span data-ttu-id="3c828-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c828-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c828-115">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c828-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c828-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c828-116">INPUTS</span></span>

### <span data-ttu-id="3c828-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="3c828-117">None</span></span>

## <span data-ttu-id="3c828-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c828-118">OUTPUTS</span></span>

### <span data-ttu-id="3c828-119">Microsoft. Azure. commands. FrontDoor. Models. PSManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="3c828-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span></span>

## <span data-ttu-id="3c828-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c828-120">NOTES</span></span>

## <span data-ttu-id="3c828-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c828-121">RELATED LINKS</span></span>

<span data-ttu-id="3c828-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="3c828-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>