---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: 52f929cea9f2017ad6a2c2ea16475ec7d5d8a5a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102225"
---
# <span data-ttu-id="61a49-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="61a49-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="61a49-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="61a49-102">SYNOPSIS</span></span>
<span data-ttu-id="61a49-103">Skapar ett objekt av typen schema</span><span class="sxs-lookup"><span data-stu-id="61a49-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="61a49-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="61a49-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61a49-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="61a49-105">DESCRIPTION</span></span>
<span data-ttu-id="61a49-106">Skapar ett objekt av typen schema.</span><span class="sxs-lookup"><span data-stu-id="61a49-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="61a49-107">Det här objektet måste skickas till det kommando som skapar en regel för loggnings varning.</span><span class="sxs-lookup"><span data-stu-id="61a49-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="61a49-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="61a49-108">EXAMPLES</span></span>

### <span data-ttu-id="61a49-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="61a49-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="61a49-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="61a49-110">PARAMETERS</span></span>

### <span data-ttu-id="61a49-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61a49-111">-DefaultProfile</span></span>
<span data-ttu-id="61a49-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="61a49-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61a49-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="61a49-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="61a49-114">Aviserings frekvensen</span><span class="sxs-lookup"><span data-stu-id="61a49-114">The alert frequency</span></span>

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

### <span data-ttu-id="61a49-115">-TimeWindowInMinutes</span><span class="sxs-lookup"><span data-stu-id="61a49-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="61a49-116">Fönstret varnings tid</span><span class="sxs-lookup"><span data-stu-id="61a49-116">The alert time window</span></span>

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

### <span data-ttu-id="61a49-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61a49-117">CommonParameters</span></span>
<span data-ttu-id="61a49-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61a49-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61a49-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61a49-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61a49-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="61a49-120">INPUTS</span></span>

### <span data-ttu-id="61a49-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="61a49-121">None</span></span>

## <span data-ttu-id="61a49-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="61a49-122">OUTPUTS</span></span>

### <span data-ttu-id="61a49-123">Microsoft. Azure. commands. Insights. OutputClasses. PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="61a49-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="61a49-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="61a49-124">NOTES</span></span>

## <span data-ttu-id="61a49-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="61a49-125">RELATED LINKS</span></span>
