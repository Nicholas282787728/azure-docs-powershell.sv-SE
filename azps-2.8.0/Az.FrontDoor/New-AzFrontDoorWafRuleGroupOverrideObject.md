---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
ms.openlocfilehash: c55be8e72e3c5bb5418d3be4b74555eb20168113
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744131"
---
# <span data-ttu-id="cac80-101">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="cac80-101">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>

## <span data-ttu-id="cac80-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cac80-102">SYNOPSIS</span></span>
<span data-ttu-id="cac80-103">Skapa RuleGroupOverride-objekt för WAF-princip</span><span class="sxs-lookup"><span data-stu-id="cac80-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="cac80-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cac80-104">SYNTAX</span></span>

```
New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cac80-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cac80-105">DESCRIPTION</span></span>
<span data-ttu-id="cac80-106">Skapa RuleGroupOverride-objekt för WAF-princip</span><span class="sxs-lookup"><span data-stu-id="cac80-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="cac80-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cac80-107">EXAMPLES</span></span>

### <span data-ttu-id="cac80-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cac80-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="cac80-109">Skapa ett RuleGroupOverride-objekt</span><span class="sxs-lookup"><span data-stu-id="cac80-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="cac80-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cac80-110">PARAMETERS</span></span>

### <span data-ttu-id="cac80-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cac80-111">-DefaultProfile</span></span>
<span data-ttu-id="cac80-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cac80-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cac80-113">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="cac80-113">-ManagedRuleOverride</span></span>
<span data-ttu-id="cac80-114">Regel för att åsidosätta regeln</span><span class="sxs-lookup"><span data-stu-id="cac80-114">Rule override list</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cac80-115">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="cac80-115">-RuleGroupName</span></span>
<span data-ttu-id="cac80-116">Regel grupp namn för vilka dessa åsidosättningar gäller</span><span class="sxs-lookup"><span data-stu-id="cac80-116">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="cac80-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cac80-117">CommonParameters</span></span>
<span data-ttu-id="cac80-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cac80-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cac80-119">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cac80-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cac80-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cac80-120">INPUTS</span></span>

### <span data-ttu-id="cac80-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="cac80-121">None</span></span>

## <span data-ttu-id="cac80-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cac80-122">OUTPUTS</span></span>

### <span data-ttu-id="cac80-123">Microsoft. Azure. commands. FrontDoor. Models. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="cac80-123">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="cac80-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cac80-124">NOTES</span></span>

## <span data-ttu-id="cac80-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cac80-125">RELATED LINKS</span></span>

[<span data-ttu-id="cac80-126">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="cac80-126">New-AzFrontDoorWafManagedRuleObject</span></span>](./New-AzFrontDoorWafManagedRuleObject.md)
