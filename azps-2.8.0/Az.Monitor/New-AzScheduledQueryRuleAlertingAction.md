---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 382aa35b9967e016ce87da982b32c97148c9f3c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918919"
---
# <span data-ttu-id="286e6-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="286e6-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="286e6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="286e6-102">SYNOPSIS</span></span>
<span data-ttu-id="286e6-103">Skapar ett objekt av typen varnings åtgärd</span><span class="sxs-lookup"><span data-stu-id="286e6-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="286e6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="286e6-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="286e6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="286e6-105">DESCRIPTION</span></span>
<span data-ttu-id="286e6-106">Skapar ett objekt av typen varnings åtgärd det här objektet måste skickas till det kommando som skapar en varnings regel för loggning</span><span class="sxs-lookup"><span data-stu-id="286e6-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="286e6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="286e6-107">EXAMPLES</span></span>

### <span data-ttu-id="286e6-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="286e6-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="286e6-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="286e6-109">PARAMETERS</span></span>

### <span data-ttu-id="286e6-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="286e6-110">-AznsAction</span></span>
<span data-ttu-id="286e6-111">Information om AzNS-åtgärden</span><span class="sxs-lookup"><span data-stu-id="286e6-111">The AzNS action details</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="286e6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="286e6-112">-DefaultProfile</span></span>
<span data-ttu-id="286e6-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="286e6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="286e6-114">– Allvarlighets grad</span><span class="sxs-lookup"><span data-stu-id="286e6-114">-Severity</span></span>
<span data-ttu-id="286e6-115">Allvarlighets graden för den här aviseringen</span><span class="sxs-lookup"><span data-stu-id="286e6-115">The severity for this alert</span></span>

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

### <span data-ttu-id="286e6-116">-ThrottlingInMinutes</span><span class="sxs-lookup"><span data-stu-id="286e6-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="286e6-117">Varaktigheten i minuter för vilken avisering ska begränsas</span><span class="sxs-lookup"><span data-stu-id="286e6-117">The duration in minutes for which alert should be throttled</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="286e6-118">-Utlös Ande</span><span class="sxs-lookup"><span data-stu-id="286e6-118">-Trigger</span></span>
<span data-ttu-id="286e6-119">Villkor för notifieringar</span><span class="sxs-lookup"><span data-stu-id="286e6-119">The alert trigger condition</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="286e6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="286e6-120">CommonParameters</span></span>
<span data-ttu-id="286e6-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="286e6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="286e6-122">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="286e6-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="286e6-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="286e6-123">INPUTS</span></span>

### <span data-ttu-id="286e6-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="286e6-124">None</span></span>

## <span data-ttu-id="286e6-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="286e6-125">OUTPUTS</span></span>

### <span data-ttu-id="286e6-126">Microsoft. Azure. commands. Insights. OutputClasses. PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="286e6-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="286e6-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="286e6-127">NOTES</span></span>

## <span data-ttu-id="286e6-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="286e6-128">RELATED LINKS</span></span>
