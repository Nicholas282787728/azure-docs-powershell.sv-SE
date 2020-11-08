---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: da462e5a8fd95b32275e37097bef18a2e7928d6e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088933"
---
# <span data-ttu-id="3288a-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="3288a-101">Get-AzAlert</span></span>

## <span data-ttu-id="3288a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3288a-102">SYNOPSIS</span></span>
<span data-ttu-id="3288a-103">Information om att få aviseringar</span><span class="sxs-lookup"><span data-stu-id="3288a-103">Get Alerts Information</span></span>

## <span data-ttu-id="3288a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3288a-104">SYNTAX</span></span>

### <span data-ttu-id="3288a-105">AlertsListByFilter (standard)</span><span class="sxs-lookup"><span data-stu-id="3288a-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3288a-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="3288a-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3288a-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="3288a-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3288a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3288a-108">DESCRIPTION</span></span>
<span data-ttu-id="3288a-109">Cmdleten **Get-AzAlert**</span><span class="sxs-lookup"><span data-stu-id="3288a-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="3288a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3288a-110">EXAMPLES</span></span>

### <span data-ttu-id="3288a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3288a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="3288a-112">Visa alla aviseringar med Sev2 allvarlighets grad och uppvisade övervaknings villkor.</span><span class="sxs-lookup"><span data-stu-id="3288a-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="3288a-113">Ange IncludeContext till sant, inklusive egen nytto last för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="3288a-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="3288a-114">Använd Format-List för att få mer information om varje avisering i listan.</span><span class="sxs-lookup"><span data-stu-id="3288a-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="3288a-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3288a-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="3288a-116">Få aviserings uppgifter via ID (GUID) eller resurs-ID (fullständigt ARM-ID)</span><span class="sxs-lookup"><span data-stu-id="3288a-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="3288a-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3288a-117">PARAMETERS</span></span>

### <span data-ttu-id="3288a-118">-AlertId</span><span class="sxs-lookup"><span data-stu-id="3288a-118">-AlertId</span></span>
<span data-ttu-id="3288a-119">Unik identifierare för avisering/ResourceId för avisering.</span><span class="sxs-lookup"><span data-stu-id="3288a-119">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3288a-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="3288a-120">-AlertRuleId</span></span>
<span data-ttu-id="3288a-121">Filter för ID för notifieringsregel</span><span class="sxs-lookup"><span data-stu-id="3288a-121">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3288a-122">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="3288a-122">-CustomTimeRange</span></span>
<span data-ttu-id="3288a-123">Format som stöds-Start-Time-Time-Time \< \> / \< \> i ISO-8601-format</span><span class="sxs-lookup"><span data-stu-id="3288a-123">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3288a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3288a-124">-DefaultProfile</span></span>
<span data-ttu-id="3288a-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3288a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3288a-126">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="3288a-126">-IncludeContext</span></span>
<span data-ttu-id="3288a-127">Inkludera kontext (anpassad nytto Last) för aviseringen</span><span class="sxs-lookup"><span data-stu-id="3288a-127">Include context (custom payload) of alert</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3288a-128">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="3288a-128">-IncludeEgressConfig</span></span>
<span data-ttu-id="3288a-129">Inkludera EgressConfig</span><span class="sxs-lookup"><span data-stu-id="3288a-129">Include EgressConfig</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3288a-130">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="3288a-130">-MonitorCondition</span></span>
<span data-ttu-id="3288a-131">Filtrerar på Monitor villkor</span><span class="sxs-lookup"><span data-stu-id="3288a-131">Filter on Monitor Condition</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3288a-132">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="3288a-132">-MonitorService</span></span>
<span data-ttu-id="3288a-133">Filtrera på moniter-tjänsten</span><span class="sxs-lookup"><span data-stu-id="3288a-133">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3288a-134">-PageCount</span><span class="sxs-lookup"><span data-stu-id="3288a-134">-PageCount</span></span>
<span data-ttu-id="3288a-135">Antal aviseringar som ska hämtas på en sida.</span><span class="sxs-lookup"><span data-stu-id="3288a-135">Number of alerts to be fetched in a page.</span></span>

```yaml
Type: System.Int32
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3288a-136">-Välj</span><span class="sxs-lookup"><span data-stu-id="3288a-136">-Select</span></span>
<span data-ttu-id="3288a-137">Projekt de obligatoriska fälten i grundläggande version.</span><span class="sxs-lookup"><span data-stu-id="3288a-137">Project the required fields out of essentials.</span></span>
<span data-ttu-id="3288a-138">Förväntad inmatning avgränsas med kommatecken.</span><span class="sxs-lookup"><span data-stu-id="3288a-138">Expected input is comma-separated.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3288a-139">– Allvarlighets grad</span><span class="sxs-lookup"><span data-stu-id="3288a-139">-Severity</span></span>
<span data-ttu-id="3288a-140">Filtrera på allvarlighets graden för aviseringar</span><span class="sxs-lookup"><span data-stu-id="3288a-140">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3288a-141">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="3288a-141">-SmartGroupId</span></span>
<span data-ttu-id="3288a-142">Filtrera alla meddelanden med det smarta grupp-ID: t</span><span class="sxs-lookup"><span data-stu-id="3288a-142">Filter all the alerts having the Smart Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3288a-143">-SorteraEfter</span><span class="sxs-lookup"><span data-stu-id="3288a-143">-SortBy</span></span>
<span data-ttu-id="3288a-144">Varnings egenskapen som ska användas vid sortering</span><span class="sxs-lookup"><span data-stu-id="3288a-144">Alert property to use while sorting</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3288a-145">-Sortering</span><span class="sxs-lookup"><span data-stu-id="3288a-145">-SortOrder</span></span>
<span data-ttu-id="3288a-146">Sorterings ordning</span><span class="sxs-lookup"><span data-stu-id="3288a-146">Sort Order</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3288a-147">-State</span><span class="sxs-lookup"><span data-stu-id="3288a-147">-State</span></span>
<span data-ttu-id="3288a-148">Filtrera efter status för avisering</span><span class="sxs-lookup"><span data-stu-id="3288a-148">Filter on State of alert</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3288a-149">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3288a-149">-TargetResourceGroup</span></span>
<span data-ttu-id="3288a-150">Filtrera efter resurs grupp namn för mål resursen för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="3288a-150">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3288a-151">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="3288a-151">-TargetResourceId</span></span>
<span data-ttu-id="3288a-152">Filtrera efter resurs-ID för mål resursen för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="3288a-152">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3288a-153">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="3288a-153">-TargetResourceType</span></span>
<span data-ttu-id="3288a-154">Filtrera efter resurs typen för mål resursen för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="3288a-154">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3288a-155">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="3288a-155">-TimeRange</span></span>
<span data-ttu-id="3288a-156">Tidsintervalls värden som stöds – 1H, 1d, 7d, 30d (standard är 1d)</span><span class="sxs-lookup"><span data-stu-id="3288a-156">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3288a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3288a-157">CommonParameters</span></span>
<span data-ttu-id="3288a-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3288a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3288a-159">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3288a-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3288a-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3288a-160">INPUTS</span></span>

### <span data-ttu-id="3288a-161">Ingen</span><span class="sxs-lookup"><span data-stu-id="3288a-161">None</span></span>

## <span data-ttu-id="3288a-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3288a-162">OUTPUTS</span></span>

### <span data-ttu-id="3288a-163">Microsoft. Azure. commands. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="3288a-163">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="3288a-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3288a-164">NOTES</span></span>

## <span data-ttu-id="3288a-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3288a-165">RELATED LINKS</span></span>
