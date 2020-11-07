---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleOverrideObject.md
ms.openlocfilehash: e45abaae34f3b8449920dad122736c46b9d946ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916718"
---
# <span data-ttu-id="10bb8-101">New-AzFrontDoorManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="10bb8-101">New-AzFrontDoorManagedRuleOverrideObject</span></span>

## <span data-ttu-id="10bb8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10bb8-102">SYNOPSIS</span></span>
<span data-ttu-id="10bb8-103">Skapa åsidosättning av hanterade regler</span><span class="sxs-lookup"><span data-stu-id="10bb8-103">Create managed rule override object</span></span>

## <span data-ttu-id="10bb8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10bb8-104">SYNTAX</span></span>

```
New-AzFrontDoorManagedRuleOverrideObject -RuleId <String> [-Action <PSAction>] [-Disabled]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10bb8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10bb8-105">DESCRIPTION</span></span>
<span data-ttu-id="10bb8-106">Skapa PSAzureManagedRuleOverride-objekt för regel gruppen hanterade WAF åsidosätta objekt.</span><span class="sxs-lookup"><span data-stu-id="10bb8-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="10bb8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10bb8-107">EXAMPLES</span></span>

### <span data-ttu-id="10bb8-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="10bb8-108">Example 1</span></span>
<span data-ttu-id="10bb8-109">Skapa ett objekt för åsidosättning av hanterade regler för regel 942250 (finns i gruppen SQLI).</span><span class="sxs-lookup"><span data-stu-id="10bb8-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="10bb8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10bb8-110">PARAMETERS</span></span>

### <span data-ttu-id="10bb8-111">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="10bb8-111">-Action</span></span>
<span data-ttu-id="10bb8-112">Åtgärden ignorera</span><span class="sxs-lookup"><span data-stu-id="10bb8-112">Override Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log, Redirect

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10bb8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10bb8-113">-DefaultProfile</span></span>
<span data-ttu-id="10bb8-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="10bb8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10bb8-115">-Inaktive rad</span><span class="sxs-lookup"><span data-stu-id="10bb8-115">-Disabled</span></span>
<span data-ttu-id="10bb8-116">Inaktiverat tillstånd</span><span class="sxs-lookup"><span data-stu-id="10bb8-116">Disabled state</span></span>

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

### <span data-ttu-id="10bb8-117">-RuleId</span><span class="sxs-lookup"><span data-stu-id="10bb8-117">-RuleId</span></span>
<span data-ttu-id="10bb8-118">Regel-ID</span><span class="sxs-lookup"><span data-stu-id="10bb8-118">Rule ID</span></span>

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

### <span data-ttu-id="10bb8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10bb8-119">CommonParameters</span></span>
<span data-ttu-id="10bb8-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10bb8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10bb8-121">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10bb8-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10bb8-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10bb8-122">INPUTS</span></span>

### <span data-ttu-id="10bb8-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="10bb8-123">None</span></span>

## <span data-ttu-id="10bb8-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10bb8-124">OUTPUTS</span></span>

### <span data-ttu-id="10bb8-125">Microsoft. Azure. commands. FrontDoor. Models. PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="10bb8-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="10bb8-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10bb8-126">NOTES</span></span>

## <span data-ttu-id="10bb8-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10bb8-127">RELATED LINKS</span></span>

[<span data-ttu-id="10bb8-128">New-AzFrontDoorRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="10bb8-128">New-AzFrontDoorRuleGroupOverrideObject</span></span>](./New-AzFrontDoorRuleGroupOverrideObject.md)