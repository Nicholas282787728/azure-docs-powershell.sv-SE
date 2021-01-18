---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
ms.openlocfilehash: 97a07b515cff6cfd8521033dbe7380eb2a7bc1d1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525586"
---
# <span data-ttu-id="30bb7-101">New-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="30bb7-101">New-AzSentinelAlertRule</span></span>

## <span data-ttu-id="30bb7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30bb7-102">SYNOPSIS</span></span>
<span data-ttu-id="30bb7-103">Skapa en analys (varnings regel).</span><span class="sxs-lookup"><span data-stu-id="30bb7-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="30bb7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30bb7-104">SYNTAX</span></span>

### <span data-ttu-id="30bb7-105">ScheduledAlertRule (standard)</span><span class="sxs-lookup"><span data-stu-id="30bb7-105">ScheduledAlertRule (Default)</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Scheduled]
 [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled] -DisplayName <String>
 [-Description <String>] [-SuppressionDuration <TimeSpan>] [-SuppressionEnabled] -Query <String>
 -QueryFrequency <TimeSpan> -QueryPeriod <TimeSpan> -Severity <String>
 [-Tactics <System.Collections.Generic.IList`1[System.String]>] [-TriggerOperator <TriggerOperator>]
 -TriggerThreshold <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30bb7-106">FusionAlertRule</span><span class="sxs-lookup"><span data-stu-id="30bb7-106">FusionAlertRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Fusion] [-AlertRuleId <String>]
 -AlertRuleTemplateName <String> [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="30bb7-107">MicrosoftSecurityIncidentCreationRule</span><span class="sxs-lookup"><span data-stu-id="30bb7-107">MicrosoftSecurityIncidentCreationRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-MicrosoftSecurityIncidentCreation] [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled]
 -DisplayName <String> -ProductFilter <String> [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30bb7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30bb7-108">DESCRIPTION</span></span>
<span data-ttu-id="30bb7-109">Cmdleten **New-AzSentinelAlertRule** skapar en analys (notifieringsregel) på den angivna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="30bb7-109">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="30bb7-110">Du måste ange en av de tre parametrarna, *fusion*, *schemalagd* eller *MicrosoftSecurityIncidentCreation*, för att ange vilken typ av notifieringsregel som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="30bb7-110">You must specify one of the three parameters, *Fusion*, *Scheduled* or *MicrosoftSecurityIncidentCreation*, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="30bb7-111">Varje slag har olika obligatoriska paramaters.</span><span class="sxs-lookup"><span data-stu-id="30bb7-111">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="30bb7-112">Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="30bb7-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="30bb7-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30bb7-113">EXAMPLES</span></span>

### <span data-ttu-id="30bb7-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="30bb7-114">Example 1</span></span>
```powershell
PS C:\>$AlertRuleTemplateName = "f71aba3d-28fb-450b-b192-4e76a83015c8"
PS C:\>$AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Fusion -Enabled -AlertRuleTemplateName $AlertRuleTemplateName
```

<span data-ttu-id="30bb7-115">I det här exemplet skapas en **AlertRule** av *fusion* -typen baserat på mallen för *Avancerad skadlig* och lagrar den sedan i $AlertRule variabel.</span><span class="sxs-lookup"><span data-stu-id="30bb7-115">This example creates a **AlertRule** of the *Fusion* kind based on the Template for *Advanced Multistage Attack Detection*, and then stores it in the $AlertRule variable.</span></span>

### <span data-ttu-id="30bb7-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="30bb7-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplateName = "a2e0eb51-1f11-461a-999b-cd0ebe5c7a72"
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftSecurityIncidentCreation -Enabled -AlertRuleTemplateName $AlertRuleTemplateName -DisplayName "Create incidents based on Azure Security Center for IoT" -ProductFilter "Azure Security Center for IoT"
```

<span data-ttu-id="30bb7-117">I det här exemplet skapas en **AlertRule** av *MicrosoftSecurityIncidentCreation* -typen baserat på mallen för att *skapa händelser baserat på dina IoT-larm i Azure Security Center* och sedan lagras de i $AlertRule varaible.</span><span class="sxs-lookup"><span data-stu-id="30bb7-117">This example creates a **AlertRule** of the *MicrosoftSecurityIncidentCreation* kind based on the template for *Create incidents based on Azure Security Center for IoT alerts*, and then stores it in the $AlertRule varaible.</span></span>

### <span data-ttu-id="30bb7-118">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="30bb7-118">Example 2</span></span>
```powershell
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Scheduled -Enabled -DisplayName "Powershell Exection Alert (Several Times per Hour)" -Severity Low -Query "SecurityEvent | where EventId == 4688" -QueryFrequency (New-TimeSpan -Hours 1) -QueryPeriod (New-TimeSpan -Hours 1) -TriggerThreshold 10
```

<span data-ttu-id="30bb7-119">I det här exemplet skapas en **DataConnector** av den *schemalagda* typen och lagrar den sedan i $AlertRule varaible.</span><span class="sxs-lookup"><span data-stu-id="30bb7-119">This example creates a **DataConnector** of the *Scheduled* kind, and then stores it in the $AlertRule varaible.</span></span>

## <span data-ttu-id="30bb7-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30bb7-120">PARAMETERS</span></span>

### <span data-ttu-id="30bb7-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="30bb7-121">-AlertRuleId</span></span>
<span data-ttu-id="30bb7-122">ID för notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="30bb7-122">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30bb7-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="30bb7-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="30bb7-124">Mall för notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="30bb7-124">Alert Rule Template.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: FusionAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30bb7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30bb7-125">-DefaultProfile</span></span>
<span data-ttu-id="30bb7-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="30bb7-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30bb7-127">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="30bb7-127">-Description</span></span>
<span data-ttu-id="30bb7-128">Problembeskrivning.</span><span class="sxs-lookup"><span data-stu-id="30bb7-128">Description.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30bb7-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="30bb7-129">-DisplayName</span></span>
<span data-ttu-id="30bb7-130">Visnings namn för aviserings regeln.</span><span class="sxs-lookup"><span data-stu-id="30bb7-130">Alert Rule Display Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30bb7-131">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="30bb7-131">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="30bb7-132">Visnings namn för aviserings regler exkludera filter.</span><span class="sxs-lookup"><span data-stu-id="30bb7-132">Alert Rule Display Names Exclude Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30bb7-133">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="30bb7-133">-DisplayNamesFilter</span></span>
<span data-ttu-id="30bb7-134">Filtret visnings namn för aviserings regler.</span><span class="sxs-lookup"><span data-stu-id="30bb7-134">Alert Rule Display Names Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30bb7-135">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="30bb7-135">-Enabled</span></span>
<span data-ttu-id="30bb7-136">Notifieringsregel är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="30bb7-136">Alert Rule Enabled.</span></span>

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

### <span data-ttu-id="30bb7-137">-Fusion</span><span class="sxs-lookup"><span data-stu-id="30bb7-137">-Fusion</span></span>
<span data-ttu-id="30bb7-138">Typ av varnings regel.</span><span class="sxs-lookup"><span data-stu-id="30bb7-138">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FusionAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30bb7-139">-MicrosoftSecurityIncidentCreation</span><span class="sxs-lookup"><span data-stu-id="30bb7-139">-MicrosoftSecurityIncidentCreation</span></span>
<span data-ttu-id="30bb7-140">Typ av varnings regel.</span><span class="sxs-lookup"><span data-stu-id="30bb7-140">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30bb7-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="30bb7-141">-ProductFilter</span></span>
<span data-ttu-id="30bb7-142">Produkt filter för notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="30bb7-142">Alert Rule Product Filter.</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:
Accepted values: Azure Active Directory Identity Protection, Azure Advanced Threat Protection, Azure Security Center, Azure Security Center for IoT, Microsoft Cloud App Security, Microsoft Defender Advanced Threat Protection, Office 365 Advanced Threat Protection

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30bb7-143">-Fråga</span><span class="sxs-lookup"><span data-stu-id="30bb7-143">-Query</span></span>
<span data-ttu-id="30bb7-144">Varnings regel fråga.</span><span class="sxs-lookup"><span data-stu-id="30bb7-144">Alert Rule Query.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30bb7-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="30bb7-145">-QueryFrequency</span></span>
<span data-ttu-id="30bb7-146">Frekvens för aviserings regel frågor.</span><span class="sxs-lookup"><span data-stu-id="30bb7-146">Alert Rule Query Frequency.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30bb7-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="30bb7-147">-QueryPeriod</span></span>
<span data-ttu-id="30bb7-148">Fråge period för aviserings regeln.</span><span class="sxs-lookup"><span data-stu-id="30bb7-148">Alert Rule Query Period.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30bb7-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30bb7-149">-ResourceGroupName</span></span>
<span data-ttu-id="30bb7-150">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="30bb7-150">Resource group name.</span></span>

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

### <span data-ttu-id="30bb7-151">-Schemalagd</span><span class="sxs-lookup"><span data-stu-id="30bb7-151">-Scheduled</span></span>
<span data-ttu-id="30bb7-152">Typ av varnings regel.</span><span class="sxs-lookup"><span data-stu-id="30bb7-152">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30bb7-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="30bb7-153">-SeveritiesFilter</span></span>
<span data-ttu-id="30bb7-154">Filtret allvarlighets grader för aviseringar.</span><span class="sxs-lookup"><span data-stu-id="30bb7-154">Alert Rule Severities Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30bb7-155">– Allvarlighets grad</span><span class="sxs-lookup"><span data-stu-id="30bb7-155">-Severity</span></span>
<span data-ttu-id="30bb7-156">Allvarlighets grad för incidenter.</span><span class="sxs-lookup"><span data-stu-id="30bb7-156">Incident Severity.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30bb7-157">-SuppressionDuration</span><span class="sxs-lookup"><span data-stu-id="30bb7-157">-SuppressionDuration</span></span>
<span data-ttu-id="30bb7-158">Undertrycks tids längd för varnings regeln.</span><span class="sxs-lookup"><span data-stu-id="30bb7-158">Alert Rule Suppression Duration.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30bb7-159">-SuppressionEnabled</span><span class="sxs-lookup"><span data-stu-id="30bb7-159">-SuppressionEnabled</span></span>
<span data-ttu-id="30bb7-160">Undervisning av varnings regel aktive rad.</span><span class="sxs-lookup"><span data-stu-id="30bb7-160">Alert Rule Suppression Enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30bb7-161">-Taktiker</span><span class="sxs-lookup"><span data-stu-id="30bb7-161">-Tactics</span></span>
<span data-ttu-id="30bb7-162">Varnings regel taktiker.</span><span class="sxs-lookup"><span data-stu-id="30bb7-162">Alert Rule Tactics.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30bb7-163">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="30bb7-163">-TriggerOperator</span></span>
<span data-ttu-id="30bb7-164">Operator för larm regel utlösare.</span><span class="sxs-lookup"><span data-stu-id="30bb7-164">Alert Rule Trigger Operator.</span></span>

```yaml
Type: Microsoft.Azure.Management.SecurityInsights.Models.TriggerOperator
Parameter Sets: ScheduledAlertRule
Aliases:
Accepted values: Equal, GreaterThan, LessThan, NotEqual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30bb7-165">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="30bb7-165">-TriggerThreshold</span></span>
<span data-ttu-id="30bb7-166">Tröskel för larm regel utlösare.</span><span class="sxs-lookup"><span data-stu-id="30bb7-166">Alert Rule Trigger Threshold.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30bb7-167">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="30bb7-167">-WorkspaceName</span></span>
<span data-ttu-id="30bb7-168">Namn på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="30bb7-168">Workspace Name.</span></span>

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

### <span data-ttu-id="30bb7-169">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="30bb7-169">-Confirm</span></span>
<span data-ttu-id="30bb7-170">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="30bb7-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30bb7-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30bb7-171">-WhatIf</span></span>
<span data-ttu-id="30bb7-172">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="30bb7-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30bb7-173">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="30bb7-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30bb7-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30bb7-174">CommonParameters</span></span>
<span data-ttu-id="30bb7-175">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30bb7-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30bb7-176">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30bb7-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30bb7-177">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30bb7-177">INPUTS</span></span>

### <span data-ttu-id="30bb7-178">Ingen</span><span class="sxs-lookup"><span data-stu-id="30bb7-178">None</span></span>
## <span data-ttu-id="30bb7-179">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30bb7-179">OUTPUTS</span></span>

### <span data-ttu-id="30bb7-180">Microsoft. Azure. commands. SecurityInsights. Models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="30bb7-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="30bb7-181">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30bb7-181">NOTES</span></span>

## <span data-ttu-id="30bb7-182">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30bb7-182">RELATED LINKS</span></span>
