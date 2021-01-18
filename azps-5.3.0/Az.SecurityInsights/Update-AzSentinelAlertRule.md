---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
ms.openlocfilehash: 56f1878507424c1396130aa91a5fc7b086f101c1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525564"
---
# <span data-ttu-id="63bc2-101">Update-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="63bc2-101">Update-AzSentinelAlertRule</span></span>

## <span data-ttu-id="63bc2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="63bc2-102">SYNOPSIS</span></span>
<span data-ttu-id="63bc2-103">Skapa en analys (varnings regel).</span><span class="sxs-lookup"><span data-stu-id="63bc2-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="63bc2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="63bc2-104">SYNTAX</span></span>

### <span data-ttu-id="63bc2-105">AlertRuleId (standard)</span><span class="sxs-lookup"><span data-stu-id="63bc2-105">AlertRuleId (Default)</span></span>
```
Update-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled] [-DisplayName <String>]
 [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63bc2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="63bc2-106">InputObject</span></span>
```
Update-AzSentinelAlertRule [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled]
 [-DisplayName <String>] [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] -InputObject <PSSentinelAlertRule>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63bc2-107">ID</span><span class="sxs-lookup"><span data-stu-id="63bc2-107">ResourceId</span></span>
```
Update-AzSentinelAlertRule [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled]
 [-DisplayName <String>] [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63bc2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="63bc2-108">DESCRIPTION</span></span>
<span data-ttu-id="63bc2-109">Cmdleten **Update-AzSentinelAlertRule** uppdaterar en analys (varnings regel) på den angivna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="63bc2-109">The **Update-AzSentinelAlertRule** cmdlet updates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="63bc2-110">Du kan använda en-InputObject eller-AlertId.</span><span class="sxs-lookup"><span data-stu-id="63bc2-110">You can use an -InputObject or -ResourceId or -AlertId.</span></span>  <span data-ttu-id="63bc2-111">Du kan uppdatera 1 eller fler proprtery-parmaters.</span><span class="sxs-lookup"><span data-stu-id="63bc2-111">You can update 1 or more proprtery parmaters.</span></span>
<span data-ttu-id="63bc2-112">Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="63bc2-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>


## <span data-ttu-id="63bc2-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="63bc2-113">EXAMPLES</span></span>

### <span data-ttu-id="63bc2-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="63bc2-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -Disabled -DisplayName "Disabled-AlertRuleDisplayName"
```

<span data-ttu-id="63bc2-115">Det här exemplet uppdaterar en **AlertRule** som anger att den är *inaktive rad* och byter namn till *Disabled-AlertRuleDisplayName*.</span><span class="sxs-lookup"><span data-stu-id="63bc2-115">This example updates an **AlertRule** setting it to *Disabled* and renames to *Disabled-AlertRuleDisplayName*.</span></span>  <span data-ttu-id="63bc2-116">Alla andra egenskaper förblir desamma.</span><span class="sxs-lookup"><span data-stu-id="63bc2-116">All other properties will remain the same.</span></span>

### <span data-ttu-id="63bc2-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="63bc2-117">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
PS C:\> Update-AzSentinelAlertRule -InputObject $AlertRule -Disabled
```

<span data-ttu-id="63bc2-118">I det här exemplet uppdateras en **AlertRule** med en InputObject-inställning att den är *inaktive rad*.</span><span class="sxs-lookup"><span data-stu-id="63bc2-118">This example updates an **AlertRule** using an InputObject setting it to *Disabled*.</span></span>  <span data-ttu-id="63bc2-119">Alla andra egenskaper förblir desamma.</span><span class="sxs-lookup"><span data-stu-id="63bc2-119">All other properties will remain the same.</span></span>


## <span data-ttu-id="63bc2-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="63bc2-120">PARAMETERS</span></span>

### <span data-ttu-id="63bc2-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="63bc2-121">-AlertRuleId</span></span>
<span data-ttu-id="63bc2-122">ID för notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="63bc2-122">Alert Rule Id.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="63bc2-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="63bc2-124">Mall för notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="63bc2-124">Alert Rule Template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63bc2-125">-DefaultProfile</span></span>
<span data-ttu-id="63bc2-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="63bc2-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-127">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="63bc2-127">-Description</span></span>
<span data-ttu-id="63bc2-128">Problembeskrivning.</span><span class="sxs-lookup"><span data-stu-id="63bc2-128">Description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-129">-Inaktive rad</span><span class="sxs-lookup"><span data-stu-id="63bc2-129">-Disabled</span></span>
<span data-ttu-id="63bc2-130">Varnings regeln avaktiverad.</span><span class="sxs-lookup"><span data-stu-id="63bc2-130">Alert Rule Disabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="63bc2-131">-DisplayName</span></span>
<span data-ttu-id="63bc2-132">Visnings namn för aviserings regeln.</span><span class="sxs-lookup"><span data-stu-id="63bc2-132">Alert Rule Display Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-133">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="63bc2-133">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="63bc2-134">Visnings namn för aviserings regler exkludera filter.</span><span class="sxs-lookup"><span data-stu-id="63bc2-134">Alert Rule Display Names Exclude Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-135">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="63bc2-135">-DisplayNamesFilter</span></span>
<span data-ttu-id="63bc2-136">Filtret visnings namn för aviserings regler.</span><span class="sxs-lookup"><span data-stu-id="63bc2-136">Alert Rule Display Names Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-137">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="63bc2-137">-Enabled</span></span>
<span data-ttu-id="63bc2-138">Notifieringsregel är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="63bc2-138">Alert Rule Enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63bc2-139">-InputObject</span></span>
<span data-ttu-id="63bc2-140">InputObject.</span><span class="sxs-lookup"><span data-stu-id="63bc2-140">InputObject.</span></span>

```yaml
Type: PSSentinelAlertRule
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="63bc2-141">-ProductFilter</span></span>
<span data-ttu-id="63bc2-142">Produkt filter för notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="63bc2-142">Alert Rule Product Filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Azure Active Directory Identity Protection, Azure Advanced Threat Protection, Azure Security Center, Azure Security Center for IoT, Microsoft Cloud App Security, Microsoft Defender Advanced Threat Protection, Office 365 Advanced Threat Protection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-143">-Fråga</span><span class="sxs-lookup"><span data-stu-id="63bc2-143">-Query</span></span>
<span data-ttu-id="63bc2-144">Varnings regel fråga.</span><span class="sxs-lookup"><span data-stu-id="63bc2-144">Alert Rule Query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="63bc2-145">-QueryFrequency</span></span>
<span data-ttu-id="63bc2-146">Frekvens för aviserings regel frågor.</span><span class="sxs-lookup"><span data-stu-id="63bc2-146">Alert Rule Query Frequency.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="63bc2-147">-QueryPeriod</span></span>
<span data-ttu-id="63bc2-148">Fråge period för aviserings regeln.</span><span class="sxs-lookup"><span data-stu-id="63bc2-148">Alert Rule Query Period.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63bc2-149">-ResourceGroupName</span></span>
<span data-ttu-id="63bc2-150">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="63bc2-150">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63bc2-151">-ResourceId</span></span>
<span data-ttu-id="63bc2-152">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="63bc2-152">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="63bc2-153">-SeveritiesFilter</span></span>
<span data-ttu-id="63bc2-154">Filtret allvarlighets grader för aviseringar.</span><span class="sxs-lookup"><span data-stu-id="63bc2-154">Alert Rule Severities Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-155">– Allvarlighets grad</span><span class="sxs-lookup"><span data-stu-id="63bc2-155">-Severity</span></span>
<span data-ttu-id="63bc2-156">Allvarlighets grad för incidenter.</span><span class="sxs-lookup"><span data-stu-id="63bc2-156">Incident Severity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-157">-SuppressionDisabled</span><span class="sxs-lookup"><span data-stu-id="63bc2-157">-SuppressionDisabled</span></span>
<span data-ttu-id="63bc2-158">Undertrycks regeln avaktiverad.</span><span class="sxs-lookup"><span data-stu-id="63bc2-158">Alert Rule Suppression Disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-159">-SuppressionDuration</span><span class="sxs-lookup"><span data-stu-id="63bc2-159">-SuppressionDuration</span></span>
<span data-ttu-id="63bc2-160">Undertrycks tids längd för varnings regeln.</span><span class="sxs-lookup"><span data-stu-id="63bc2-160">Alert Rule Suppression Duration.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-161">-SuppressionEnabled</span><span class="sxs-lookup"><span data-stu-id="63bc2-161">-SuppressionEnabled</span></span>
<span data-ttu-id="63bc2-162">Undervisning av varnings regel aktive rad.</span><span class="sxs-lookup"><span data-stu-id="63bc2-162">Alert Rule Suppression Enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-163">-Taktiker</span><span class="sxs-lookup"><span data-stu-id="63bc2-163">-Tactics</span></span>
<span data-ttu-id="63bc2-164">Varnings regel taktiker.</span><span class="sxs-lookup"><span data-stu-id="63bc2-164">Alert Rule Tactics.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-165">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="63bc2-165">-TriggerOperator</span></span>
<span data-ttu-id="63bc2-166">Operator för larm regel utlösare.</span><span class="sxs-lookup"><span data-stu-id="63bc2-166">Alert Rule Trigger Operator.</span></span>

```yaml
Type: TriggerOperator
Parameter Sets: (All)
Aliases:
Accepted values: GreaterThan, LessThan, Equal, NotEqual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-167">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="63bc2-167">-TriggerThreshold</span></span>
<span data-ttu-id="63bc2-168">Tröskel för larm regel utlösare.</span><span class="sxs-lookup"><span data-stu-id="63bc2-168">Alert Rule Trigger Threshold.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-169">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="63bc2-169">-WorkspaceName</span></span>
<span data-ttu-id="63bc2-170">Namn på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="63bc2-170">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-171">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="63bc2-171">-Confirm</span></span>
<span data-ttu-id="63bc2-172">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="63bc2-172">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63bc2-173">-WhatIf</span></span>
<span data-ttu-id="63bc2-174">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="63bc2-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63bc2-175">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="63bc2-175">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bc2-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63bc2-176">CommonParameters</span></span>
<span data-ttu-id="63bc2-177">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63bc2-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63bc2-178">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63bc2-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63bc2-179">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="63bc2-179">INPUTS</span></span>

### <span data-ttu-id="63bc2-180">Microsoft. Azure. commands. SecurityInsights. Models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="63bc2-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="63bc2-181">System. String</span><span class="sxs-lookup"><span data-stu-id="63bc2-181">System.String</span></span>

## <span data-ttu-id="63bc2-182">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="63bc2-182">OUTPUTS</span></span>

### <span data-ttu-id="63bc2-183">Microsoft. Azure. commands. SecurityInsights. Models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="63bc2-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

## <span data-ttu-id="63bc2-184">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="63bc2-184">NOTES</span></span>

## <span data-ttu-id="63bc2-185">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="63bc2-185">RELATED LINKS</span></span>
