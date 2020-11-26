---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: 7c9ace339da9639404072fd802782aee43d8ab37
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261298"
---
# <span data-ttu-id="56b6d-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="56b6d-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="56b6d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="56b6d-102">SYNOPSIS</span></span>
<span data-ttu-id="56b6d-103">Skapa ManagedRule-objekt för WAF-princip</span><span class="sxs-lookup"><span data-stu-id="56b6d-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="56b6d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="56b6d-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56b6d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="56b6d-105">DESCRIPTION</span></span>
<span data-ttu-id="56b6d-106">Skapa ManagedRule-objekt för WAF-princip</span><span class="sxs-lookup"><span data-stu-id="56b6d-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="56b6d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="56b6d-107">EXAMPLES</span></span>

### <span data-ttu-id="56b6d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="56b6d-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled
PS C:\> $override1 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "941280" -Action Log -EnabledState Enabled
PS C:\> $override2 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorWafManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="56b6d-109">Skapa ett ManagedRule-objekt</span><span class="sxs-lookup"><span data-stu-id="56b6d-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="56b6d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="56b6d-110">PARAMETERS</span></span>

### <span data-ttu-id="56b6d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56b6d-111">-DefaultProfile</span></span>
<span data-ttu-id="56b6d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="56b6d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56b6d-113">-Uteslutning</span><span class="sxs-lookup"><span data-stu-id="56b6d-113">-Exclusion</span></span>
<span data-ttu-id="56b6d-114">Exkludera</span><span class="sxs-lookup"><span data-stu-id="56b6d-114">Exclusion</span></span>

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

### <span data-ttu-id="56b6d-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="56b6d-115">-RuleGroupOverride</span></span>
<span data-ttu-id="56b6d-116">Lista över åsidosättning av Azure Managed Provider</span><span class="sxs-lookup"><span data-stu-id="56b6d-116">List of azure managed provider override configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56b6d-117">– Skriv</span><span class="sxs-lookup"><span data-stu-id="56b6d-117">-Type</span></span>
<span data-ttu-id="56b6d-118">Typ av ruleset</span><span class="sxs-lookup"><span data-stu-id="56b6d-118">Type of the ruleset</span></span>

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

### <span data-ttu-id="56b6d-119">-Version</span><span class="sxs-lookup"><span data-stu-id="56b6d-119">-Version</span></span>
<span data-ttu-id="56b6d-120">Version av ruleset</span><span class="sxs-lookup"><span data-stu-id="56b6d-120">Version of the ruleset</span></span>

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

### <span data-ttu-id="56b6d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56b6d-121">CommonParameters</span></span>
<span data-ttu-id="56b6d-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56b6d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56b6d-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56b6d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56b6d-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="56b6d-124">INPUTS</span></span>

### <span data-ttu-id="56b6d-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="56b6d-125">None</span></span>

## <span data-ttu-id="56b6d-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="56b6d-126">OUTPUTS</span></span>

### <span data-ttu-id="56b6d-127">Microsoft. Azure. commands. FrontDoor. Models. PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="56b6d-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="56b6d-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="56b6d-128">NOTES</span></span>

## <span data-ttu-id="56b6d-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="56b6d-129">RELATED LINKS</span></span>

<span data-ttu-id="56b6d-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="56b6d-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>