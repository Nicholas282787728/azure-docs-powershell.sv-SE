---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/close-azsalert
schema: 2.0.0
ms.openlocfilehash: 885ffca453cd7a13e9ec137da89a402375eeec55
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100205"
---
# <span data-ttu-id="6da08-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="6da08-101">Close-AzsAlert</span></span>

## <span data-ttu-id="6da08-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6da08-102">SYNOPSIS</span></span>
<span data-ttu-id="6da08-103">Stänger den angivna varningen.</span><span class="sxs-lookup"><span data-stu-id="6da08-103">Closes the given alert.</span></span>

## <span data-ttu-id="6da08-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6da08-104">SYNTAX</span></span>

### <span data-ttu-id="6da08-105">CloseExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="6da08-105">CloseExpanded (Default)</span></span>
```
Close-AzsAlert -Name <String> -User <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>]
 [-ClosedTimestamp <String>] [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>]
 [-FaultTypeId <String>] [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>]
 [-ImpactedResourceId <String>] [-LastUpdatedTimestamp <String>] [-Location1 <String>]
 [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>] [-ResourceRegistrationId <String>]
 [-Severity <String>] [-State <String>] [-Tag <Hashtable>] [-Title <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6da08-106">Nästan</span><span class="sxs-lookup"><span data-stu-id="6da08-106">Close</span></span>
```
Close-AzsAlert -Name <String> -User <String> -Alert <IAlert> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6da08-107">CloseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6da08-107">CloseViaIdentity</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> -Alert <IAlert>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6da08-108">CloseViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6da08-108">CloseViaIdentityExpanded</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> [-Location <String>]
 [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>] [-ClosedTimestamp <String>]
 [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>] [-FaultTypeId <String>]
 [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>] [-ImpactedResourceId <String>]
 [-LastUpdatedTimestamp <String>] [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>]
 [-ResourceRegistrationId <String>] [-Severity <String>] [-State <String>] [-Tag <Hashtable>]
 [-Title <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6da08-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6da08-109">DESCRIPTION</span></span>
<span data-ttu-id="6da08-110">Stänger den angivna varningen.</span><span class="sxs-lookup"><span data-stu-id="6da08-110">Closes the given alert.</span></span>

## <span data-ttu-id="6da08-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6da08-111">EXAMPLES</span></span>

### <span data-ttu-id="6da08-112">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="6da08-112">Example 1:</span></span>
```powershell
PS C:\> Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="6da08-113">Stänga en avisering efter namn.</span><span class="sxs-lookup"><span data-stu-id="6da08-113">Close an alert by Name.</span></span>

### <span data-ttu-id="6da08-114">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="6da08-114">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="6da08-115">Stänga en avisering genom att flytta.</span><span class="sxs-lookup"><span data-stu-id="6da08-115">Close an alert through piping.</span></span>

## <span data-ttu-id="6da08-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6da08-116">PARAMETERS</span></span>

### <span data-ttu-id="6da08-117">-Avisera</span><span class="sxs-lookup"><span data-stu-id="6da08-117">-Alert</span></span>
<span data-ttu-id="6da08-118">Det här objektet representerar en aviserings resurs.</span><span class="sxs-lookup"><span data-stu-id="6da08-118">This object represents an alert resource.</span></span>
<span data-ttu-id="6da08-119">Om du vill skapa läser du avsnittet anteckningar och skapar en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="6da08-119">To construct, see NOTES section for ALERT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert
Parameter Sets: Close, CloseViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-120">-AlertId</span><span class="sxs-lookup"><span data-stu-id="6da08-120">-AlertId</span></span>
<span data-ttu-id="6da08-121">Hämtar eller anger aviseringens ID.</span><span class="sxs-lookup"><span data-stu-id="6da08-121">Gets or sets the ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-122">-AlertProperty</span><span class="sxs-lookup"><span data-stu-id="6da08-122">-AlertProperty</span></span>
<span data-ttu-id="6da08-123">Egenskaper för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="6da08-123">Properties of the alert.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-124">-ClosedByUserAlias</span><span class="sxs-lookup"><span data-stu-id="6da08-124">-ClosedByUserAlias</span></span>
<span data-ttu-id="6da08-125">Användarens alias som stängde aviseringen.</span><span class="sxs-lookup"><span data-stu-id="6da08-125">User alias who closed the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-126">-ClosedTimestamp</span><span class="sxs-lookup"><span data-stu-id="6da08-126">-ClosedTimestamp</span></span>
<span data-ttu-id="6da08-127">Tidsstämpel när aviseringen stängdes.</span><span class="sxs-lookup"><span data-stu-id="6da08-127">Timestamp when the alert was closed.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-128">-CreatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="6da08-128">-CreatedTimestamp</span></span>
<span data-ttu-id="6da08-129">Tidsstämpel när aviseringen skapades.</span><span class="sxs-lookup"><span data-stu-id="6da08-129">Timestamp when the alert was created.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6da08-130">-DefaultProfile</span></span>
<span data-ttu-id="6da08-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6da08-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6da08-132">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="6da08-132">-Description</span></span>
<span data-ttu-id="6da08-133">Beskrivning av aviseringen.</span><span class="sxs-lookup"><span data-stu-id="6da08-133">Description of the alert.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-134">-FaultId</span><span class="sxs-lookup"><span data-stu-id="6da08-134">-FaultId</span></span>
<span data-ttu-id="6da08-135">Hämtar eller anger aviseringens fel-ID.</span><span class="sxs-lookup"><span data-stu-id="6da08-135">Gets or sets the fault ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-136">-FaultTypeId</span><span class="sxs-lookup"><span data-stu-id="6da08-136">-FaultTypeId</span></span>
<span data-ttu-id="6da08-137">Hämtar eller anger aviseringens feltyp-ID.</span><span class="sxs-lookup"><span data-stu-id="6da08-137">Gets or sets the fault type ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-138">-HasValidRemediationAction</span><span class="sxs-lookup"><span data-stu-id="6da08-138">-HasValidRemediationAction</span></span>
<span data-ttu-id="6da08-139">Anger om aviseringen kan åtgärdas.</span><span class="sxs-lookup"><span data-stu-id="6da08-139">Indicates if the alert can be remediated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-140">-ImpactedResourceDisplayName</span><span class="sxs-lookup"><span data-stu-id="6da08-140">-ImpactedResourceDisplayName</span></span>
<span data-ttu-id="6da08-141">Visnings namn för den påverkade posten.</span><span class="sxs-lookup"><span data-stu-id="6da08-141">Display name for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-142">-ImpactedResourceId</span><span class="sxs-lookup"><span data-stu-id="6da08-142">-ImpactedResourceId</span></span>
<span data-ttu-id="6da08-143">Hämtar eller anger resurs-ID för det påverkade objektet.</span><span class="sxs-lookup"><span data-stu-id="6da08-143">Gets or sets the Resource ID for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6da08-144">-InputObject</span></span>
<span data-ttu-id="6da08-145">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="6da08-145">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: CloseViaIdentity, CloseViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-146">-LastUpdatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="6da08-146">-LastUpdatedTimestamp</span></span>
<span data-ttu-id="6da08-147">Tidsstämpel när aviseringen senast uppdaterades.</span><span class="sxs-lookup"><span data-stu-id="6da08-147">Timestamp when the alert was last updated.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-148">-Plats</span><span class="sxs-lookup"><span data-stu-id="6da08-148">-Location</span></span>
<span data-ttu-id="6da08-149">Regionens namn</span><span class="sxs-lookup"><span data-stu-id="6da08-149">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-150">-Location1</span><span class="sxs-lookup"><span data-stu-id="6da08-150">-Location1</span></span>
<span data-ttu-id="6da08-151">Azure-regionen där resursen bor</span><span class="sxs-lookup"><span data-stu-id="6da08-151">The Azure Region where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-152">-Namn</span><span class="sxs-lookup"><span data-stu-id="6da08-152">-Name</span></span>
<span data-ttu-id="6da08-153">Namn på aviseringen.</span><span class="sxs-lookup"><span data-stu-id="6da08-153">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-154">-Reparation</span><span class="sxs-lookup"><span data-stu-id="6da08-154">-Remediation</span></span>
<span data-ttu-id="6da08-155">Hämtar eller anger de egna administratörs anvisningarna för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="6da08-155">Gets or sets the admin friendly remediation instructions for the alert.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6da08-156">-ResourceGroupName</span></span>
<span data-ttu-id="6da08-157">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6da08-157">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-158">-ResourceProviderRegistrationId</span><span class="sxs-lookup"><span data-stu-id="6da08-158">-ResourceProviderRegistrationId</span></span>
<span data-ttu-id="6da08-159">Hämtar eller anger registrerings-ID för den tjänst som notifieringen tillhör.</span><span class="sxs-lookup"><span data-stu-id="6da08-159">Gets or sets the registration ID of the service the alert belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-160">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="6da08-160">-ResourceRegistrationId</span></span>
<span data-ttu-id="6da08-161">Hämtar eller anger registrerings-ID för den resurs som är associerad med aviseringen.</span><span class="sxs-lookup"><span data-stu-id="6da08-161">Gets or sets the registration ID of the resource associated with the alert.</span></span>
<span data-ttu-id="6da08-162">Om aviseringen inte är kopplad till en resurs är resurs registrerings-ID: t null.</span><span class="sxs-lookup"><span data-stu-id="6da08-162">If the alert is not associated with a resource, the resource registration ID is null.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-163">– Allvarlighets grad</span><span class="sxs-lookup"><span data-stu-id="6da08-163">-Severity</span></span>
<span data-ttu-id="6da08-164">Allvarlighets grad för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="6da08-164">Severity of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-165">-State</span><span class="sxs-lookup"><span data-stu-id="6da08-165">-State</span></span>
<span data-ttu-id="6da08-166">Status för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="6da08-166">State of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-167">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6da08-167">-SubscriptionId</span></span>
<span data-ttu-id="6da08-168">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="6da08-168">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6da08-169">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="6da08-169">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-170">-Tagg</span><span class="sxs-lookup"><span data-stu-id="6da08-170">-Tag</span></span>
<span data-ttu-id="6da08-171">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="6da08-171">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-172">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="6da08-172">-Title</span></span>
<span data-ttu-id="6da08-173">Hämtar eller anger resurs-ID för det påverkade objektet.</span><span class="sxs-lookup"><span data-stu-id="6da08-173">Gets or sets the Resource ID for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6da08-174">-Användare</span><span class="sxs-lookup"><span data-stu-id="6da08-174">-User</span></span>
<span data-ttu-id="6da08-175">Det användar namn som används för att utföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="6da08-175">The username used to perform the operation.</span></span>

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

### <span data-ttu-id="6da08-176">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6da08-176">-Confirm</span></span>
<span data-ttu-id="6da08-177">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6da08-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6da08-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6da08-178">-WhatIf</span></span>
<span data-ttu-id="6da08-179">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6da08-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6da08-180">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6da08-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6da08-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6da08-181">CommonParameters</span></span>
<span data-ttu-id="6da08-182">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6da08-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6da08-183">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6da08-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6da08-184">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6da08-184">INPUTS</span></span>

### <span data-ttu-id="6da08-185">Microsoft. Azure. PowerShell. cmdletar. InfrastructureInsightsAdmin. Models. Api20160501. IAlert</span><span class="sxs-lookup"><span data-stu-id="6da08-185">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>

### <span data-ttu-id="6da08-186">Microsoft. Azure. PowerShell. cmdletar. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="6da08-186">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="6da08-187">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6da08-187">OUTPUTS</span></span>

### <span data-ttu-id="6da08-188">Microsoft. Azure. PowerShell. cmdletar. InfrastructureInsightsAdmin. Models. Api20160501. IAlert</span><span class="sxs-lookup"><span data-stu-id="6da08-188">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>



## <span data-ttu-id="6da08-189">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6da08-189">NOTES</span></span>

<span data-ttu-id="6da08-190">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="6da08-190">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6da08-191">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6da08-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6da08-192">Varning <IAlert> : det här objektet representerar en aviserings resurs.</span><span class="sxs-lookup"><span data-stu-id="6da08-192">ALERT <IAlert>: This object represents an alert resource.</span></span>
  - <span data-ttu-id="6da08-193">`[Location <String>]`: Azure-regionen där resursen bor</span><span class="sxs-lookup"><span data-stu-id="6da08-193">`[Location <String>]`: The Azure Region where the resource lives</span></span>
  - <span data-ttu-id="6da08-194">`[Tag <ITrackedResourceTags>]`: Resursfiler.</span><span class="sxs-lookup"><span data-stu-id="6da08-194">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="6da08-195">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="6da08-195">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="6da08-196">`[AlertId <String>]`: Hämtar eller anger aviseringens ID.</span><span class="sxs-lookup"><span data-stu-id="6da08-196">`[AlertId <String>]`: Gets or sets the ID of the alert.</span></span>
  - <span data-ttu-id="6da08-197">`[AlertProperty <IAlertModelAlertProperties>]`: Aviseringens egenskaper.</span><span class="sxs-lookup"><span data-stu-id="6da08-197">`[AlertProperty <IAlertModelAlertProperties>]`: Properties of the alert.</span></span>
    - <span data-ttu-id="6da08-198">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="6da08-198">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="6da08-199">`[ClosedByUserAlias <String>]`: Användaralias som stängde aviseringen.</span><span class="sxs-lookup"><span data-stu-id="6da08-199">`[ClosedByUserAlias <String>]`: User alias who closed the alert.</span></span>
  - <span data-ttu-id="6da08-200">`[ClosedTimestamp <String>]`: Tidsstämpel när aviseringen var stängd.</span><span class="sxs-lookup"><span data-stu-id="6da08-200">`[ClosedTimestamp <String>]`: Timestamp when the alert was closed.</span></span>
  - <span data-ttu-id="6da08-201">`[CreatedTimestamp <String>]`: Tidsstämpel när aviseringen skapades.</span><span class="sxs-lookup"><span data-stu-id="6da08-201">`[CreatedTimestamp <String>]`: Timestamp when the alert was created.</span></span>
  - <span data-ttu-id="6da08-202">`[Description <IDictionary[]>]`: Beskrivning av aviseringen.</span><span class="sxs-lookup"><span data-stu-id="6da08-202">`[Description <IDictionary[]>]`: Description of the alert.</span></span>
  - <span data-ttu-id="6da08-203">`[FaultId <String>]`: Hämtar eller anger aviseringens fel-ID.</span><span class="sxs-lookup"><span data-stu-id="6da08-203">`[FaultId <String>]`: Gets or sets the fault ID of the alert.</span></span>
  - <span data-ttu-id="6da08-204">`[FaultTypeId <String>]`: Hämtar eller anger aviseringens feltyp-ID.</span><span class="sxs-lookup"><span data-stu-id="6da08-204">`[FaultTypeId <String>]`: Gets or sets the fault type ID of the alert.</span></span>
  - <span data-ttu-id="6da08-205">`[HasValidRemediationAction <Boolean?>]`: Anger om aviseringen kan åtgärdas.</span><span class="sxs-lookup"><span data-stu-id="6da08-205">`[HasValidRemediationAction <Boolean?>]`: Indicates if the alert can be remediated.</span></span>
  - <span data-ttu-id="6da08-206">`[ImpactedResourceDisplayName <String>]`: Visnings namn för den påverkade posten.</span><span class="sxs-lookup"><span data-stu-id="6da08-206">`[ImpactedResourceDisplayName <String>]`: Display name for the impacted item.</span></span>
  - <span data-ttu-id="6da08-207">`[ImpactedResourceId <String>]`: Hämtar eller anger resurs-ID för det påverkade objektet.</span><span class="sxs-lookup"><span data-stu-id="6da08-207">`[ImpactedResourceId <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>
  - <span data-ttu-id="6da08-208">`[LastUpdatedTimestamp <String>]`: Tidsstämpel när aviseringen uppdaterades senast.</span><span class="sxs-lookup"><span data-stu-id="6da08-208">`[LastUpdatedTimestamp <String>]`: Timestamp when the alert was last updated.</span></span>
  - <span data-ttu-id="6da08-209">`[Remediation <IDictionary[]>]`: Hämtar eller anger de egna administratörs anvisningarna för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="6da08-209">`[Remediation <IDictionary[]>]`: Gets or sets the admin friendly remediation instructions for the alert.</span></span>
  - <span data-ttu-id="6da08-210">`[ResourceProviderRegistrationId <String>]`: Hämtar eller anger registrerings-ID för den tjänst som notifieringen tillhör.</span><span class="sxs-lookup"><span data-stu-id="6da08-210">`[ResourceProviderRegistrationId <String>]`: Gets or sets the registration ID of the service the alert belongs to.</span></span>
  - <span data-ttu-id="6da08-211">`[ResourceRegistrationId <String>]`: Hämtar eller anger registrerings-ID för resursen som är associerad med aviseringen.</span><span class="sxs-lookup"><span data-stu-id="6da08-211">`[ResourceRegistrationId <String>]`: Gets or sets the registration ID of the resource associated with the alert.</span></span> <span data-ttu-id="6da08-212">Om aviseringen inte är kopplad till en resurs är resurs registrerings-ID: t null.</span><span class="sxs-lookup"><span data-stu-id="6da08-212">If the alert is not associated with a resource, the resource registration ID is null.</span></span>
  - <span data-ttu-id="6da08-213">`[Severity <String>]`: Meddelandets allvarlighets grad.</span><span class="sxs-lookup"><span data-stu-id="6da08-213">`[Severity <String>]`: Severity of the alert.</span></span>
  - <span data-ttu-id="6da08-214">`[State <String>]`: Status för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="6da08-214">`[State <String>]`: State of the alert.</span></span>
  - <span data-ttu-id="6da08-215">`[Title <String>]`: Hämtar eller anger resurs-ID för det påverkade objektet.</span><span class="sxs-lookup"><span data-stu-id="6da08-215">`[Title <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>

<span data-ttu-id="6da08-216">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="6da08-216">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6da08-217">`[AlertName <String>]`: Aviseringens namn.</span><span class="sxs-lookup"><span data-stu-id="6da08-217">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="6da08-218">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="6da08-218">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6da08-219">`[Location <String>]`: Regionens namn</span><span class="sxs-lookup"><span data-stu-id="6da08-219">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="6da08-220">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6da08-220">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="6da08-221">`[ResourceRegistrationId <String>]`: Registrerings-ID för resurs.</span><span class="sxs-lookup"><span data-stu-id="6da08-221">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="6da08-222">`[ServiceHealth <String>]`: Tjänstens hälso namn.</span><span class="sxs-lookup"><span data-stu-id="6da08-222">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="6da08-223">`[ServiceRegistrationId <String>]`: ID för tjänste registrering.</span><span class="sxs-lookup"><span data-stu-id="6da08-223">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="6da08-224">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="6da08-224">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6da08-225">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="6da08-225">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6da08-226">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6da08-226">RELATED LINKS</span></span>
