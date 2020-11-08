---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/set-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
ms.openlocfilehash: 60569a05fc3770119844b05e65ec3dc7989a85ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262017"
---
# <span data-ttu-id="32392-101">Set-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="32392-101">Set-AzPortalDashboard</span></span>

## <span data-ttu-id="32392-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="32392-102">SYNOPSIS</span></span>
<span data-ttu-id="32392-103">Skapar eller uppdaterar en instrument panel.</span><span class="sxs-lookup"><span data-stu-id="32392-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="32392-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="32392-104">SYNTAX</span></span>

```
Set-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="32392-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="32392-105">DESCRIPTION</span></span>
<span data-ttu-id="32392-106">Skapar eller uppdaterar en instrument panel.</span><span class="sxs-lookup"><span data-stu-id="32392-106">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="32392-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="32392-107">EXAMPLES</span></span>

### <span data-ttu-id="32392-108">Exempel 1: uppdatera instrument panelen med hjälp av en kontrollpanelflik</span><span class="sxs-lookup"><span data-stu-id="32392-108">Example 1: Update the dashboard definition using a dashboard template</span></span>
```powershell
PS C:\> Set-AzPortalDashboard -DashboardPath .\resources\dash1-update.json -ResourceGroupName my-rg -DashboardName dashbase03

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="32392-109">Uppdatera en instrument panels definition med en dashbaord.</span><span class="sxs-lookup"><span data-stu-id="32392-109">Update a dashboard definition using a dashbaord template file.</span></span>

## <span data-ttu-id="32392-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="32392-110">PARAMETERS</span></span>

### <span data-ttu-id="32392-111">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="32392-111">-DashboardPath</span></span>
<span data-ttu-id="32392-112">Sökvägen till en befintlig kontrollpanelflik.</span><span class="sxs-lookup"><span data-stu-id="32392-112">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="32392-113">Instrumentpanelsdesignern kan hämtas från portalen.</span><span class="sxs-lookup"><span data-stu-id="32392-113">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="32392-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32392-114">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32392-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="32392-115">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32392-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32392-116">-ResourceGroupName</span></span>


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

### <span data-ttu-id="32392-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="32392-117">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32392-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="32392-118">-Confirm</span></span>
<span data-ttu-id="32392-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="32392-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32392-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32392-120">-WhatIf</span></span>
<span data-ttu-id="32392-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="32392-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32392-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="32392-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32392-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32392-123">CommonParameters</span></span>
<span data-ttu-id="32392-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32392-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32392-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32392-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32392-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="32392-126">INPUTS</span></span>

## <span data-ttu-id="32392-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="32392-127">OUTPUTS</span></span>

### <span data-ttu-id="32392-128">Microsoft. Azure. PowerShell. cmdletar. Portal. Models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="32392-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="32392-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="32392-129">NOTES</span></span>

<span data-ttu-id="32392-130">ALIAS</span><span class="sxs-lookup"><span data-stu-id="32392-130">ALIASES</span></span>

## <span data-ttu-id="32392-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="32392-131">RELATED LINKS</span></span>

