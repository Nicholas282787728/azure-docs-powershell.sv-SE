---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: 2043a2cf31354c7fc14b1b03794dff6f82af67b8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918912"
---
# <span data-ttu-id="2e5b2-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="2e5b2-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="2e5b2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2e5b2-102">SYNOPSIS</span></span>
<span data-ttu-id="2e5b2-103">Skapar ett objekt av typen schema</span><span class="sxs-lookup"><span data-stu-id="2e5b2-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="2e5b2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2e5b2-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e5b2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2e5b2-105">DESCRIPTION</span></span>
<span data-ttu-id="2e5b2-106">Skapar ett objekt av typen schema.</span><span class="sxs-lookup"><span data-stu-id="2e5b2-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="2e5b2-107">Det här objektet måste skickas till det kommando som skapar en regel för loggnings varning.</span><span class="sxs-lookup"><span data-stu-id="2e5b2-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="2e5b2-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2e5b2-108">EXAMPLES</span></span>

### <span data-ttu-id="2e5b2-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2e5b2-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="2e5b2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2e5b2-110">PARAMETERS</span></span>

### <span data-ttu-id="2e5b2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e5b2-111">-DefaultProfile</span></span>
<span data-ttu-id="2e5b2-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2e5b2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e5b2-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="2e5b2-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="2e5b2-114">Aviserings frekvensen</span><span class="sxs-lookup"><span data-stu-id="2e5b2-114">The alert frequency</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e5b2-115">-TimeWindowInMinutes</span><span class="sxs-lookup"><span data-stu-id="2e5b2-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="2e5b2-116">Fönstret varnings tid</span><span class="sxs-lookup"><span data-stu-id="2e5b2-116">The alert time window</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e5b2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e5b2-117">CommonParameters</span></span>
<span data-ttu-id="2e5b2-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e5b2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e5b2-119">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e5b2-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e5b2-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2e5b2-120">INPUTS</span></span>

### <span data-ttu-id="2e5b2-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="2e5b2-121">None</span></span>

## <span data-ttu-id="2e5b2-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2e5b2-122">OUTPUTS</span></span>

### <span data-ttu-id="2e5b2-123">Microsoft. Azure. commands. Insights. OutputClasses. PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="2e5b2-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="2e5b2-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2e5b2-124">NOTES</span></span>

## <span data-ttu-id="2e5b2-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2e5b2-125">RELATED LINKS</span></span>
