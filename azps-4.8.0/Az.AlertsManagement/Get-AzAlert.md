---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: 94cb37a6f98195534e7effcbff8c19b2613923d8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102511"
---
# <span data-ttu-id="524f1-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="524f1-101">Get-AzAlert</span></span>

## <span data-ttu-id="524f1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="524f1-102">SYNOPSIS</span></span>
<span data-ttu-id="524f1-103">Information om att få aviseringar</span><span class="sxs-lookup"><span data-stu-id="524f1-103">Get Alerts Information</span></span>

## <span data-ttu-id="524f1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="524f1-104">SYNTAX</span></span>

### <span data-ttu-id="524f1-105">AlertsListByFilter (standard)</span><span class="sxs-lookup"><span data-stu-id="524f1-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="524f1-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="524f1-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="524f1-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="524f1-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="524f1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="524f1-108">DESCRIPTION</span></span>
<span data-ttu-id="524f1-109">Cmdleten **Get-AzAlert**</span><span class="sxs-lookup"><span data-stu-id="524f1-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="524f1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="524f1-110">EXAMPLES</span></span>

### <span data-ttu-id="524f1-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="524f1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="524f1-112">Visa alla aviseringar med Sev2 allvarlighets grad och uppvisade övervaknings villkor.</span><span class="sxs-lookup"><span data-stu-id="524f1-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="524f1-113">Ange IncludeContext till sant, inklusive egen nytto last för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="524f1-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="524f1-114">Använd Format-List för att få mer information om varje avisering i listan.</span><span class="sxs-lookup"><span data-stu-id="524f1-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="524f1-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="524f1-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="524f1-116">Få aviserings uppgifter via ID (GUID) eller resurs-ID (fullständigt ARM-ID)</span><span class="sxs-lookup"><span data-stu-id="524f1-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

### <span data-ttu-id="524f1-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="524f1-117">Example 3</span></span>

<span data-ttu-id="524f1-118">Information om att få aviseringar.</span><span class="sxs-lookup"><span data-stu-id="524f1-118">Get Alerts Information.</span></span> <span data-ttu-id="524f1-119">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="524f1-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAlert -IncludeContext $true -TimeRange '1h'
```

## <span data-ttu-id="524f1-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="524f1-120">PARAMETERS</span></span>

### <span data-ttu-id="524f1-121">-AlertId</span><span class="sxs-lookup"><span data-stu-id="524f1-121">-AlertId</span></span>
<span data-ttu-id="524f1-122">Unik identifierare för avisering/ResourceId för avisering.</span><span class="sxs-lookup"><span data-stu-id="524f1-122">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="524f1-123">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="524f1-123">-AlertRuleId</span></span>
<span data-ttu-id="524f1-124">Filter för ID för notifieringsregel</span><span class="sxs-lookup"><span data-stu-id="524f1-124">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="524f1-125">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="524f1-125">-CustomTimeRange</span></span>
<span data-ttu-id="524f1-126">Format som stöds, \<start-time\> / \<end-time\> där tiden är i ISO-8601-format</span><span class="sxs-lookup"><span data-stu-id="524f1-126">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="524f1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="524f1-127">-DefaultProfile</span></span>
<span data-ttu-id="524f1-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="524f1-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="524f1-129">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="524f1-129">-IncludeContext</span></span>
<span data-ttu-id="524f1-130">Inkludera kontext (anpassad nytto Last) för aviseringen</span><span class="sxs-lookup"><span data-stu-id="524f1-130">Include context (custom payload) of alert</span></span>

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

### <span data-ttu-id="524f1-131">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="524f1-131">-IncludeEgressConfig</span></span>
<span data-ttu-id="524f1-132">Inkludera EgressConfig</span><span class="sxs-lookup"><span data-stu-id="524f1-132">Include EgressConfig</span></span>

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

### <span data-ttu-id="524f1-133">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="524f1-133">-MonitorCondition</span></span>
<span data-ttu-id="524f1-134">Filtrerar på Monitor villkor</span><span class="sxs-lookup"><span data-stu-id="524f1-134">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="524f1-135">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="524f1-135">-MonitorService</span></span>
<span data-ttu-id="524f1-136">Filtrera på moniter-tjänsten</span><span class="sxs-lookup"><span data-stu-id="524f1-136">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="524f1-137">-PageCount</span><span class="sxs-lookup"><span data-stu-id="524f1-137">-PageCount</span></span>
<span data-ttu-id="524f1-138">Antal aviseringar som ska hämtas på en sida.</span><span class="sxs-lookup"><span data-stu-id="524f1-138">Number of alerts to be fetched in a page.</span></span>

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

### <span data-ttu-id="524f1-139">-Välj</span><span class="sxs-lookup"><span data-stu-id="524f1-139">-Select</span></span>
<span data-ttu-id="524f1-140">Projekt de obligatoriska fälten i grundläggande version.</span><span class="sxs-lookup"><span data-stu-id="524f1-140">Project the required fields out of essentials.</span></span>
<span data-ttu-id="524f1-141">Förväntad inmatning avgränsas med kommatecken.</span><span class="sxs-lookup"><span data-stu-id="524f1-141">Expected input is comma-separated.</span></span>

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

### <span data-ttu-id="524f1-142">– Allvarlighets grad</span><span class="sxs-lookup"><span data-stu-id="524f1-142">-Severity</span></span>
<span data-ttu-id="524f1-143">Filtrera på allvarlighets graden för aviseringar</span><span class="sxs-lookup"><span data-stu-id="524f1-143">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="524f1-144">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="524f1-144">-SmartGroupId</span></span>
<span data-ttu-id="524f1-145">Filtrera alla meddelanden med det smarta grupp-ID: t</span><span class="sxs-lookup"><span data-stu-id="524f1-145">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="524f1-146">-SorteraEfter</span><span class="sxs-lookup"><span data-stu-id="524f1-146">-SortBy</span></span>
<span data-ttu-id="524f1-147">Varnings egenskapen som ska användas vid sortering</span><span class="sxs-lookup"><span data-stu-id="524f1-147">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="524f1-148">-Sortering</span><span class="sxs-lookup"><span data-stu-id="524f1-148">-SortOrder</span></span>
<span data-ttu-id="524f1-149">Sorterings ordning</span><span class="sxs-lookup"><span data-stu-id="524f1-149">Sort Order</span></span>

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

### <span data-ttu-id="524f1-150">-State</span><span class="sxs-lookup"><span data-stu-id="524f1-150">-State</span></span>
<span data-ttu-id="524f1-151">Filtrera efter status för avisering</span><span class="sxs-lookup"><span data-stu-id="524f1-151">Filter on State of alert</span></span>

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

### <span data-ttu-id="524f1-152">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="524f1-152">-TargetResourceGroup</span></span>
<span data-ttu-id="524f1-153">Filtrera efter resurs grupp namn för mål resursen för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="524f1-153">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="524f1-154">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="524f1-154">-TargetResourceId</span></span>
<span data-ttu-id="524f1-155">Filtrera efter resurs-ID för mål resursen för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="524f1-155">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="524f1-156">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="524f1-156">-TargetResourceType</span></span>
<span data-ttu-id="524f1-157">Filtrera efter resurs typen för mål resursen för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="524f1-157">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="524f1-158">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="524f1-158">-TimeRange</span></span>
<span data-ttu-id="524f1-159">Tidsintervalls värden som stöds – 1H, 1d, 7d, 30d (standard är 1d)</span><span class="sxs-lookup"><span data-stu-id="524f1-159">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="524f1-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="524f1-160">CommonParameters</span></span>
<span data-ttu-id="524f1-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="524f1-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="524f1-162">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="524f1-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="524f1-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="524f1-163">INPUTS</span></span>

### <span data-ttu-id="524f1-164">Ingen</span><span class="sxs-lookup"><span data-stu-id="524f1-164">None</span></span>

## <span data-ttu-id="524f1-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="524f1-165">OUTPUTS</span></span>

### <span data-ttu-id="524f1-166">Microsoft. Azure. commands. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="524f1-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="524f1-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="524f1-167">NOTES</span></span>

## <span data-ttu-id="524f1-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="524f1-168">RELATED LINKS</span></span>
