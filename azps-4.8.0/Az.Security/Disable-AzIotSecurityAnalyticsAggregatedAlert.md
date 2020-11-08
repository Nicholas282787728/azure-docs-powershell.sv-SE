---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Disable-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 3747109d13fd4224b0f86bc5ecf2992ed4229487
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261726"
---
# <span data-ttu-id="5826d-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="5826d-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="5826d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5826d-102">SYNOPSIS</span></span>
<span data-ttu-id="5826d-103">Stäng IoT-summerad varning</span><span class="sxs-lookup"><span data-stu-id="5826d-103">Dismiss Iot aggregated alert</span></span>

## <span data-ttu-id="5826d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5826d-104">SYNTAX</span></span>

### <span data-ttu-id="5826d-105">SolutionLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="5826d-105">SolutionLevelResource (Default)</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5826d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5826d-106">InputObject</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -InputObject <PSIoTSecurityAggregatedAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5826d-107">ID</span><span class="sxs-lookup"><span data-stu-id="5826d-107">ResourceId</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5826d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5826d-108">DESCRIPTION</span></span>
<span data-ttu-id="5826d-109">Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet avaktiverar en viss aggragated-varning på enheter i IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="5826d-109">The Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet dismisses a specific aggragated alert on devices of iot hub.</span></span> <span data-ttu-id="5826d-110">Namnet på de aggregerade varningarna är en kombination av varnings typen och aviseringens aggragted-datum, avgränsade med "/".</span><span class="sxs-lookup"><span data-stu-id="5826d-110">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="5826d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5826d-111">EXAMPLES</span></span>

### <span data-ttu-id="5826d-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5826d-112">Example 1</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolutionName" -Name "IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="5826d-113">Ignorera den sammanslagna varningen "IoT_SucessfulLocalLogin/2020-03-15" (namn kombinerat med aviserings typen och dess aggregerade datum) från IoT Security-lösningen "MySolutionName" i resurs gruppen "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="5826d-113">Dismiss aggregated alert "IoT_SucessfulLocalLogin/2020-03-15" (name combined from alert type and its aggregated date) from the IoT security solution "MySolutionName" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="5826d-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5826d-114">Example 2</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="5826d-115">Ignorera summerad avisering med resurs-ID "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span><span class="sxs-lookup"><span data-stu-id="5826d-115">Dismiss aggregated alert with resource Id "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span></span>

## <span data-ttu-id="5826d-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5826d-116">PARAMETERS</span></span>

### <span data-ttu-id="5826d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5826d-117">-DefaultProfile</span></span>
<span data-ttu-id="5826d-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5826d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5826d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5826d-119">-InputObject</span></span>
<span data-ttu-id="5826d-120">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="5826d-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5826d-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="5826d-121">-Name</span></span>
<span data-ttu-id="5826d-122">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="5826d-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5826d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5826d-123">-PassThru</span></span>
<span data-ttu-id="5826d-124">Returnera om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="5826d-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="5826d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5826d-125">-ResourceGroupName</span></span>
<span data-ttu-id="5826d-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="5826d-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5826d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5826d-127">-ResourceId</span></span>
<span data-ttu-id="5826d-128">ID för den säkerhets resurs som du vill starta kommandot på.</span><span class="sxs-lookup"><span data-stu-id="5826d-128">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5826d-129">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="5826d-129">-SolutionName</span></span>
<span data-ttu-id="5826d-130">Lösningens namn</span><span class="sxs-lookup"><span data-stu-id="5826d-130">Solution name</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5826d-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5826d-131">-Confirm</span></span>
<span data-ttu-id="5826d-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5826d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5826d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5826d-133">-WhatIf</span></span>
<span data-ttu-id="5826d-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5826d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5826d-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5826d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5826d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5826d-136">CommonParameters</span></span>
<span data-ttu-id="5826d-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5826d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5826d-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5826d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5826d-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5826d-139">INPUTS</span></span>

### <span data-ttu-id="5826d-140">Microsoft. Azure. commands. Security. Models. IotSecuritySolutionAnalytics. PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="5826d-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

### <span data-ttu-id="5826d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5826d-141">System.String</span></span>

## <span data-ttu-id="5826d-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5826d-142">OUTPUTS</span></span>

### <span data-ttu-id="5826d-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5826d-143">System.Boolean</span></span>

## <span data-ttu-id="5826d-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5826d-144">NOTES</span></span>

## <span data-ttu-id="5826d-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5826d-145">RELATED LINKS</span></span>
