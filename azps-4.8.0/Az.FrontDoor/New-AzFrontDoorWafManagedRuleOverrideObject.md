---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: 7fc4a16e6668af017e9666999eabe710b40e7d97
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261300"
---
# <span data-ttu-id="b19e0-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="b19e0-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="b19e0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b19e0-102">SYNOPSIS</span></span>
<span data-ttu-id="b19e0-103">Skapa åsidosättning av hanterade regler</span><span class="sxs-lookup"><span data-stu-id="b19e0-103">Create managed rule override object</span></span>

## <span data-ttu-id="b19e0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b19e0-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-Exclusion <PSManagedRuleExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b19e0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b19e0-105">DESCRIPTION</span></span>
<span data-ttu-id="b19e0-106">Skapa PSAzureManagedRuleOverride-objekt för regel gruppen hanterade WAF åsidosätta objekt.</span><span class="sxs-lookup"><span data-stu-id="b19e0-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="b19e0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b19e0-107">EXAMPLES</span></span>

### <span data-ttu-id="b19e0-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b19e0-108">Example 1</span></span>
<span data-ttu-id="b19e0-109">Skapa ett objekt för åsidosättning av hanterade regler för regel 942250 (finns i gruppen SQLI).</span><span class="sxs-lookup"><span data-stu-id="b19e0-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="b19e0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b19e0-110">PARAMETERS</span></span>

### <span data-ttu-id="b19e0-111">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="b19e0-111">-Action</span></span>
<span data-ttu-id="b19e0-112">Åtgärden ignorera</span><span class="sxs-lookup"><span data-stu-id="b19e0-112">Override Action</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b19e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b19e0-113">-DefaultProfile</span></span>
<span data-ttu-id="b19e0-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b19e0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b19e0-115">-Inaktive rad</span><span class="sxs-lookup"><span data-stu-id="b19e0-115">-Disabled</span></span>
<span data-ttu-id="b19e0-116">Inaktiverat tillstånd</span><span class="sxs-lookup"><span data-stu-id="b19e0-116">Disabled state</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b19e0-117">-Uteslutning</span><span class="sxs-lookup"><span data-stu-id="b19e0-117">-Exclusion</span></span>
<span data-ttu-id="b19e0-118">Exkludera</span><span class="sxs-lookup"><span data-stu-id="b19e0-118">Exclusion</span></span>

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

### <span data-ttu-id="b19e0-119">-RuleId</span><span class="sxs-lookup"><span data-stu-id="b19e0-119">-RuleId</span></span>
<span data-ttu-id="b19e0-120">Regel-ID</span><span class="sxs-lookup"><span data-stu-id="b19e0-120">Rule ID</span></span>

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

### <span data-ttu-id="b19e0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b19e0-121">CommonParameters</span></span>
<span data-ttu-id="b19e0-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b19e0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b19e0-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b19e0-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b19e0-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b19e0-124">INPUTS</span></span>

### <span data-ttu-id="b19e0-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="b19e0-125">None</span></span>

## <span data-ttu-id="b19e0-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b19e0-126">OUTPUTS</span></span>

### <span data-ttu-id="b19e0-127">Microsoft. Azure. commands. FrontDoor. Models. PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="b19e0-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="b19e0-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b19e0-128">NOTES</span></span>

## <span data-ttu-id="b19e0-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b19e0-129">RELATED LINKS</span></span>

[<span data-ttu-id="b19e0-130">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="b19e0-130">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)