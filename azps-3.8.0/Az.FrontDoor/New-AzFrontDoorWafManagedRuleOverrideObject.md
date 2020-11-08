---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: 7fc4a16e6668af017e9666999eabe710b40e7d97
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091563"
---
# <span data-ttu-id="ee523-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="ee523-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="ee523-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ee523-102">SYNOPSIS</span></span>
<span data-ttu-id="ee523-103">Skapa åsidosättning av hanterade regler</span><span class="sxs-lookup"><span data-stu-id="ee523-103">Create managed rule override object</span></span>

## <span data-ttu-id="ee523-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ee523-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-Exclusion <PSManagedRuleExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee523-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ee523-105">DESCRIPTION</span></span>
<span data-ttu-id="ee523-106">Skapa PSAzureManagedRuleOverride-objekt för regel gruppen hanterade WAF åsidosätta objekt.</span><span class="sxs-lookup"><span data-stu-id="ee523-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="ee523-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ee523-107">EXAMPLES</span></span>

### <span data-ttu-id="ee523-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ee523-108">Example 1</span></span>
<span data-ttu-id="ee523-109">Skapa ett objekt för åsidosättning av hanterade regler för regel 942250 (finns i gruppen SQLI).</span><span class="sxs-lookup"><span data-stu-id="ee523-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="ee523-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ee523-110">PARAMETERS</span></span>

### <span data-ttu-id="ee523-111">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="ee523-111">-Action</span></span>
<span data-ttu-id="ee523-112">Åtgärden ignorera</span><span class="sxs-lookup"><span data-stu-id="ee523-112">Override Action</span></span>

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

### <span data-ttu-id="ee523-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee523-113">-DefaultProfile</span></span>
<span data-ttu-id="ee523-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ee523-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee523-115">-Inaktive rad</span><span class="sxs-lookup"><span data-stu-id="ee523-115">-Disabled</span></span>
<span data-ttu-id="ee523-116">Inaktiverat tillstånd</span><span class="sxs-lookup"><span data-stu-id="ee523-116">Disabled state</span></span>

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

### <span data-ttu-id="ee523-117">-Uteslutning</span><span class="sxs-lookup"><span data-stu-id="ee523-117">-Exclusion</span></span>
<span data-ttu-id="ee523-118">Exkludera</span><span class="sxs-lookup"><span data-stu-id="ee523-118">Exclusion</span></span>

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

### <span data-ttu-id="ee523-119">-RuleId</span><span class="sxs-lookup"><span data-stu-id="ee523-119">-RuleId</span></span>
<span data-ttu-id="ee523-120">Regel-ID</span><span class="sxs-lookup"><span data-stu-id="ee523-120">Rule ID</span></span>

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

### <span data-ttu-id="ee523-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee523-121">CommonParameters</span></span>
<span data-ttu-id="ee523-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee523-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee523-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee523-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee523-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ee523-124">INPUTS</span></span>

### <span data-ttu-id="ee523-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="ee523-125">None</span></span>

## <span data-ttu-id="ee523-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ee523-126">OUTPUTS</span></span>

### <span data-ttu-id="ee523-127">Microsoft. Azure. commands. FrontDoor. Models. PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="ee523-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="ee523-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ee523-128">NOTES</span></span>

## <span data-ttu-id="ee523-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ee523-129">RELATED LINKS</span></span>

[<span data-ttu-id="ee523-130">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="ee523-130">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)