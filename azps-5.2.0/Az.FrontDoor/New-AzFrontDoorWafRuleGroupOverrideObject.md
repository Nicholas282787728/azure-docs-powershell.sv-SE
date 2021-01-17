---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
ms.openlocfilehash: 9d05502b518dcd10a22c9583546a2d010b424902
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392619"
---
# <span data-ttu-id="598de-101">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="598de-101">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>

## <span data-ttu-id="598de-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="598de-102">SYNOPSIS</span></span>
<span data-ttu-id="598de-103">Skapa RuleGroupOverride-objekt för WAF-princip</span><span class="sxs-lookup"><span data-stu-id="598de-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="598de-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="598de-104">SYNTAX</span></span>

```
New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="598de-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="598de-105">DESCRIPTION</span></span>
<span data-ttu-id="598de-106">Skapa RuleGroupOverride-objekt för WAF-princip</span><span class="sxs-lookup"><span data-stu-id="598de-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="598de-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="598de-107">EXAMPLES</span></span>

### <span data-ttu-id="598de-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="598de-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="598de-109">Skapa ett RuleGroupOverride-objekt</span><span class="sxs-lookup"><span data-stu-id="598de-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="598de-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="598de-110">PARAMETERS</span></span>

### <span data-ttu-id="598de-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="598de-111">-DefaultProfile</span></span>
<span data-ttu-id="598de-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="598de-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="598de-113">-Uteslutning</span><span class="sxs-lookup"><span data-stu-id="598de-113">-Exclusion</span></span>
<span data-ttu-id="598de-114">Exkludera</span><span class="sxs-lookup"><span data-stu-id="598de-114">Exclusion</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="598de-115">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="598de-115">-ManagedRuleOverride</span></span>
<span data-ttu-id="598de-116">Regel för att åsidosätta regeln</span><span class="sxs-lookup"><span data-stu-id="598de-116">Rule override list</span></span>

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

### <span data-ttu-id="598de-117">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="598de-117">-RuleGroupName</span></span>
<span data-ttu-id="598de-118">Regel grupp namn för vilka dessa åsidosättningar gäller</span><span class="sxs-lookup"><span data-stu-id="598de-118">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="598de-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="598de-119">CommonParameters</span></span>
<span data-ttu-id="598de-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="598de-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="598de-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="598de-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="598de-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="598de-122">INPUTS</span></span>

### <span data-ttu-id="598de-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="598de-123">None</span></span>

## <span data-ttu-id="598de-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="598de-124">OUTPUTS</span></span>

### <span data-ttu-id="598de-125">Microsoft. Azure. commands. FrontDoor. Models. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="598de-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="598de-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="598de-126">NOTES</span></span>

## <span data-ttu-id="598de-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="598de-127">RELATED LINKS</span></span>

[<span data-ttu-id="598de-128">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="598de-128">New-AzFrontDoorWafManagedRuleObject</span></span>](./New-AzFrontDoorWafManagedRuleObject.md)
