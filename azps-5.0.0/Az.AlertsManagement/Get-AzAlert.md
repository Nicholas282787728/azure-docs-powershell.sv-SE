---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: 94cb37a6f98195534e7effcbff8c19b2613923d8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94326069"
---
# <span data-ttu-id="1c9f8-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="1c9f8-101">Get-AzAlert</span></span>

## <span data-ttu-id="1c9f8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c9f8-102">SYNOPSIS</span></span>
<span data-ttu-id="1c9f8-103">Information om att få aviseringar</span><span class="sxs-lookup"><span data-stu-id="1c9f8-103">Get Alerts Information</span></span>

## <span data-ttu-id="1c9f8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c9f8-104">SYNTAX</span></span>

### <span data-ttu-id="1c9f8-105">AlertsListByFilter (standard)</span><span class="sxs-lookup"><span data-stu-id="1c9f8-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c9f8-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="1c9f8-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c9f8-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="1c9f8-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c9f8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c9f8-108">DESCRIPTION</span></span>
<span data-ttu-id="1c9f8-109">Cmdleten **Get-AzAlert**</span><span class="sxs-lookup"><span data-stu-id="1c9f8-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="1c9f8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c9f8-110">EXAMPLES</span></span>

### <span data-ttu-id="1c9f8-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1c9f8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="1c9f8-112">Visa alla aviseringar med Sev2 allvarlighets grad och uppvisade övervaknings villkor.</span><span class="sxs-lookup"><span data-stu-id="1c9f8-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="1c9f8-113">Ange IncludeContext till sant, inklusive egen nytto last för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="1c9f8-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="1c9f8-114">Använd Format-List för att få mer information om varje avisering i listan.</span><span class="sxs-lookup"><span data-stu-id="1c9f8-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="1c9f8-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1c9f8-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="1c9f8-116">Få aviserings uppgifter via ID (GUID) eller resurs-ID (fullständigt ARM-ID)</span><span class="sxs-lookup"><span data-stu-id="1c9f8-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

### <span data-ttu-id="1c9f8-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="1c9f8-117">Example 3</span></span>

<span data-ttu-id="1c9f8-118">Information om att få aviseringar.</span><span class="sxs-lookup"><span data-stu-id="1c9f8-118">Get Alerts Information.</span></span> <span data-ttu-id="1c9f8-119">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="1c9f8-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAlert -IncludeContext $true -TimeRange '1h'
```

## <span data-ttu-id="1c9f8-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c9f8-120">PARAMETERS</span></span>

### <span data-ttu-id="1c9f8-121">-AlertId</span><span class="sxs-lookup"><span data-stu-id="1c9f8-121">-AlertId</span></span>
<span data-ttu-id="1c9f8-122">Unik identifierare för avisering/ResourceId för avisering.</span><span class="sxs-lookup"><span data-stu-id="1c9f8-122">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="1c9f8-123">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="1c9f8-123">-AlertRuleId</span></span>
<span data-ttu-id="1c9f8-124">Filter för ID för notifieringsregel</span><span class="sxs-lookup"><span data-stu-id="1c9f8-124">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="1c9f8-125">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="1c9f8-125">-CustomTimeRange</span></span>
<span data-ttu-id="1c9f8-126">Format som stöds, \<start-time\> / \<end-time\> där tiden är i ISO-8601-format</span><span class="sxs-lookup"><span data-stu-id="1c9f8-126">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="1c9f8-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c9f8-127">-DefaultProfile</span></span>
<span data-ttu-id="1c9f8-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1c9f8-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c9f8-129">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="1c9f8-129">-IncludeContext</span></span>
<span data-ttu-id="1c9f8-130">Inkludera kontext (anpassad nytto Last) för aviseringen</span><span class="sxs-lookup"><span data-stu-id="1c9f8-130">Include context (custom payload) of alert</span></span>

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

### <span data-ttu-id="1c9f8-131">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="1c9f8-131">-IncludeEgressConfig</span></span>
<span data-ttu-id="1c9f8-132">Inkludera EgressConfig</span><span class="sxs-lookup"><span data-stu-id="1c9f8-132">Include EgressConfig</span></span>

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

### <span data-ttu-id="1c9f8-133">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="1c9f8-133">-MonitorCondition</span></span>
<span data-ttu-id="1c9f8-134">Filtrerar på Monitor villkor</span><span class="sxs-lookup"><span data-stu-id="1c9f8-134">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="1c9f8-135">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="1c9f8-135">-MonitorService</span></span>
<span data-ttu-id="1c9f8-136">Filtrera på moniter-tjänsten</span><span class="sxs-lookup"><span data-stu-id="1c9f8-136">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="1c9f8-137">-PageCount</span><span class="sxs-lookup"><span data-stu-id="1c9f8-137">-PageCount</span></span>
<span data-ttu-id="1c9f8-138">Antal aviseringar som ska hämtas på en sida.</span><span class="sxs-lookup"><span data-stu-id="1c9f8-138">Number of alerts to be fetched in a page.</span></span>

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

### <span data-ttu-id="1c9f8-139">-Välj</span><span class="sxs-lookup"><span data-stu-id="1c9f8-139">-Select</span></span>
<span data-ttu-id="1c9f8-140">Projekt de obligatoriska fälten i grundläggande version.</span><span class="sxs-lookup"><span data-stu-id="1c9f8-140">Project the required fields out of essentials.</span></span>
<span data-ttu-id="1c9f8-141">Förväntad inmatning avgränsas med kommatecken.</span><span class="sxs-lookup"><span data-stu-id="1c9f8-141">Expected input is comma-separated.</span></span>

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

### <span data-ttu-id="1c9f8-142">– Allvarlighets grad</span><span class="sxs-lookup"><span data-stu-id="1c9f8-142">-Severity</span></span>
<span data-ttu-id="1c9f8-143">Filtrera på allvarlighets graden för aviseringar</span><span class="sxs-lookup"><span data-stu-id="1c9f8-143">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="1c9f8-144">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="1c9f8-144">-SmartGroupId</span></span>
<span data-ttu-id="1c9f8-145">Filtrera alla meddelanden med det smarta grupp-ID: t</span><span class="sxs-lookup"><span data-stu-id="1c9f8-145">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="1c9f8-146">-SorteraEfter</span><span class="sxs-lookup"><span data-stu-id="1c9f8-146">-SortBy</span></span>
<span data-ttu-id="1c9f8-147">Varnings egenskapen som ska användas vid sortering</span><span class="sxs-lookup"><span data-stu-id="1c9f8-147">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="1c9f8-148">-Sortering</span><span class="sxs-lookup"><span data-stu-id="1c9f8-148">-SortOrder</span></span>
<span data-ttu-id="1c9f8-149">Sorterings ordning</span><span class="sxs-lookup"><span data-stu-id="1c9f8-149">Sort Order</span></span>

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

### <span data-ttu-id="1c9f8-150">-State</span><span class="sxs-lookup"><span data-stu-id="1c9f8-150">-State</span></span>
<span data-ttu-id="1c9f8-151">Filtrera efter status för avisering</span><span class="sxs-lookup"><span data-stu-id="1c9f8-151">Filter on State of alert</span></span>

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

### <span data-ttu-id="1c9f8-152">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1c9f8-152">-TargetResourceGroup</span></span>
<span data-ttu-id="1c9f8-153">Filtrera efter resurs grupp namn för mål resursen för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="1c9f8-153">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="1c9f8-154">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="1c9f8-154">-TargetResourceId</span></span>
<span data-ttu-id="1c9f8-155">Filtrera efter resurs-ID för mål resursen för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="1c9f8-155">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="1c9f8-156">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="1c9f8-156">-TargetResourceType</span></span>
<span data-ttu-id="1c9f8-157">Filtrera efter resurs typen för mål resursen för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="1c9f8-157">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="1c9f8-158">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="1c9f8-158">-TimeRange</span></span>
<span data-ttu-id="1c9f8-159">Tidsintervalls värden som stöds – 1H, 1d, 7d, 30d (standard är 1d)</span><span class="sxs-lookup"><span data-stu-id="1c9f8-159">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="1c9f8-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c9f8-160">CommonParameters</span></span>
<span data-ttu-id="1c9f8-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c9f8-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c9f8-162">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c9f8-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c9f8-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c9f8-163">INPUTS</span></span>

### <span data-ttu-id="1c9f8-164">Ingen</span><span class="sxs-lookup"><span data-stu-id="1c9f8-164">None</span></span>

## <span data-ttu-id="1c9f8-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c9f8-165">OUTPUTS</span></span>

### <span data-ttu-id="1c9f8-166">Microsoft. Azure. commands. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="1c9f8-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="1c9f8-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c9f8-167">NOTES</span></span>

## <span data-ttu-id="1c9f8-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c9f8-168">RELATED LINKS</span></span>