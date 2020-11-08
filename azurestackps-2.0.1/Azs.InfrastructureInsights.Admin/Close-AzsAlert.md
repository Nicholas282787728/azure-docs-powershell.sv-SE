---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/close-azsalert
schema: 2.0.0
ms.openlocfilehash: 885ffca453cd7a13e9ec137da89a402375eeec55
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94093025"
---
# <span data-ttu-id="0fe42-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="0fe42-101">Close-AzsAlert</span></span>

## <span data-ttu-id="0fe42-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0fe42-102">SYNOPSIS</span></span>
<span data-ttu-id="0fe42-103">Stänger den angivna varningen.</span><span class="sxs-lookup"><span data-stu-id="0fe42-103">Closes the given alert.</span></span>

## <span data-ttu-id="0fe42-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0fe42-104">SYNTAX</span></span>

### <span data-ttu-id="0fe42-105">CloseExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="0fe42-105">CloseExpanded (Default)</span></span>
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

### <span data-ttu-id="0fe42-106">Nästan</span><span class="sxs-lookup"><span data-stu-id="0fe42-106">Close</span></span>
```
Close-AzsAlert -Name <String> -User <String> -Alert <IAlert> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0fe42-107">CloseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0fe42-107">CloseViaIdentity</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> -Alert <IAlert>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0fe42-108">CloseViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0fe42-108">CloseViaIdentityExpanded</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> [-Location <String>]
 [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>] [-ClosedTimestamp <String>]
 [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>] [-FaultTypeId <String>]
 [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>] [-ImpactedResourceId <String>]
 [-LastUpdatedTimestamp <String>] [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>]
 [-ResourceRegistrationId <String>] [-Severity <String>] [-State <String>] [-Tag <Hashtable>]
 [-Title <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0fe42-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0fe42-109">DESCRIPTION</span></span>
<span data-ttu-id="0fe42-110">Stänger den angivna varningen.</span><span class="sxs-lookup"><span data-stu-id="0fe42-110">Closes the given alert.</span></span>

## <span data-ttu-id="0fe42-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0fe42-111">EXAMPLES</span></span>

### <span data-ttu-id="0fe42-112">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="0fe42-112">Example 1:</span></span>
```powershell
PS C:\> Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="0fe42-113">Stänga en avisering efter namn.</span><span class="sxs-lookup"><span data-stu-id="0fe42-113">Close an alert by Name.</span></span>

### <span data-ttu-id="0fe42-114">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="0fe42-114">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="0fe42-115">Stänga en avisering genom att flytta.</span><span class="sxs-lookup"><span data-stu-id="0fe42-115">Close an alert through piping.</span></span>

## <span data-ttu-id="0fe42-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0fe42-116">PARAMETERS</span></span>

### <span data-ttu-id="0fe42-117">-Avisera</span><span class="sxs-lookup"><span data-stu-id="0fe42-117">-Alert</span></span>
<span data-ttu-id="0fe42-118">Det här objektet representerar en aviserings resurs.</span><span class="sxs-lookup"><span data-stu-id="0fe42-118">This object represents an alert resource.</span></span>
<span data-ttu-id="0fe42-119">Om du vill skapa läser du avsnittet anteckningar och skapar en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="0fe42-119">To construct, see NOTES section for ALERT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0fe42-120">-AlertId</span><span class="sxs-lookup"><span data-stu-id="0fe42-120">-AlertId</span></span>
<span data-ttu-id="0fe42-121">Hämtar eller anger aviseringens ID.</span><span class="sxs-lookup"><span data-stu-id="0fe42-121">Gets or sets the ID of the alert.</span></span>

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

### <span data-ttu-id="0fe42-122">-AlertProperty</span><span class="sxs-lookup"><span data-stu-id="0fe42-122">-AlertProperty</span></span>
<span data-ttu-id="0fe42-123">Egenskaper för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="0fe42-123">Properties of the alert.</span></span>

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

### <span data-ttu-id="0fe42-124">-ClosedByUserAlias</span><span class="sxs-lookup"><span data-stu-id="0fe42-124">-ClosedByUserAlias</span></span>
<span data-ttu-id="0fe42-125">Användarens alias som stängde aviseringen.</span><span class="sxs-lookup"><span data-stu-id="0fe42-125">User alias who closed the alert.</span></span>

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

### <span data-ttu-id="0fe42-126">-ClosedTimestamp</span><span class="sxs-lookup"><span data-stu-id="0fe42-126">-ClosedTimestamp</span></span>
<span data-ttu-id="0fe42-127">Tidsstämpel när aviseringen stängdes.</span><span class="sxs-lookup"><span data-stu-id="0fe42-127">Timestamp when the alert was closed.</span></span>

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

### <span data-ttu-id="0fe42-128">-CreatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="0fe42-128">-CreatedTimestamp</span></span>
<span data-ttu-id="0fe42-129">Tidsstämpel när aviseringen skapades.</span><span class="sxs-lookup"><span data-stu-id="0fe42-129">Timestamp when the alert was created.</span></span>

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

### <span data-ttu-id="0fe42-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fe42-130">-DefaultProfile</span></span>
<span data-ttu-id="0fe42-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0fe42-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fe42-132">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="0fe42-132">-Description</span></span>
<span data-ttu-id="0fe42-133">Beskrivning av aviseringen.</span><span class="sxs-lookup"><span data-stu-id="0fe42-133">Description of the alert.</span></span>

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

### <span data-ttu-id="0fe42-134">-FaultId</span><span class="sxs-lookup"><span data-stu-id="0fe42-134">-FaultId</span></span>
<span data-ttu-id="0fe42-135">Hämtar eller anger aviseringens fel-ID.</span><span class="sxs-lookup"><span data-stu-id="0fe42-135">Gets or sets the fault ID of the alert.</span></span>

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

### <span data-ttu-id="0fe42-136">-FaultTypeId</span><span class="sxs-lookup"><span data-stu-id="0fe42-136">-FaultTypeId</span></span>
<span data-ttu-id="0fe42-137">Hämtar eller anger aviseringens feltyp-ID.</span><span class="sxs-lookup"><span data-stu-id="0fe42-137">Gets or sets the fault type ID of the alert.</span></span>

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

### <span data-ttu-id="0fe42-138">-HasValidRemediationAction</span><span class="sxs-lookup"><span data-stu-id="0fe42-138">-HasValidRemediationAction</span></span>
<span data-ttu-id="0fe42-139">Anger om aviseringen kan åtgärdas.</span><span class="sxs-lookup"><span data-stu-id="0fe42-139">Indicates if the alert can be remediated.</span></span>

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

### <span data-ttu-id="0fe42-140">-ImpactedResourceDisplayName</span><span class="sxs-lookup"><span data-stu-id="0fe42-140">-ImpactedResourceDisplayName</span></span>
<span data-ttu-id="0fe42-141">Visnings namn för den påverkade posten.</span><span class="sxs-lookup"><span data-stu-id="0fe42-141">Display name for the impacted item.</span></span>

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

### <span data-ttu-id="0fe42-142">-ImpactedResourceId</span><span class="sxs-lookup"><span data-stu-id="0fe42-142">-ImpactedResourceId</span></span>
<span data-ttu-id="0fe42-143">Hämtar eller anger resurs-ID för det påverkade objektet.</span><span class="sxs-lookup"><span data-stu-id="0fe42-143">Gets or sets the Resource ID for the impacted item.</span></span>

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

### <span data-ttu-id="0fe42-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fe42-144">-InputObject</span></span>
<span data-ttu-id="0fe42-145">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="0fe42-145">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0fe42-146">-LastUpdatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="0fe42-146">-LastUpdatedTimestamp</span></span>
<span data-ttu-id="0fe42-147">Tidsstämpel när aviseringen senast uppdaterades.</span><span class="sxs-lookup"><span data-stu-id="0fe42-147">Timestamp when the alert was last updated.</span></span>

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

### <span data-ttu-id="0fe42-148">-Plats</span><span class="sxs-lookup"><span data-stu-id="0fe42-148">-Location</span></span>
<span data-ttu-id="0fe42-149">Regionens namn</span><span class="sxs-lookup"><span data-stu-id="0fe42-149">Name of the region</span></span>

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

### <span data-ttu-id="0fe42-150">-Location1</span><span class="sxs-lookup"><span data-stu-id="0fe42-150">-Location1</span></span>
<span data-ttu-id="0fe42-151">Azure-regionen där resursen bor</span><span class="sxs-lookup"><span data-stu-id="0fe42-151">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="0fe42-152">-Namn</span><span class="sxs-lookup"><span data-stu-id="0fe42-152">-Name</span></span>
<span data-ttu-id="0fe42-153">Namn på aviseringen.</span><span class="sxs-lookup"><span data-stu-id="0fe42-153">Name of the alert.</span></span>

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

### <span data-ttu-id="0fe42-154">-Reparation</span><span class="sxs-lookup"><span data-stu-id="0fe42-154">-Remediation</span></span>
<span data-ttu-id="0fe42-155">Hämtar eller anger de egna administratörs anvisningarna för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="0fe42-155">Gets or sets the admin friendly remediation instructions for the alert.</span></span>

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

### <span data-ttu-id="0fe42-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fe42-156">-ResourceGroupName</span></span>
<span data-ttu-id="0fe42-157">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0fe42-157">The name of the resource group.</span></span>

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

### <span data-ttu-id="0fe42-158">-ResourceProviderRegistrationId</span><span class="sxs-lookup"><span data-stu-id="0fe42-158">-ResourceProviderRegistrationId</span></span>
<span data-ttu-id="0fe42-159">Hämtar eller anger registrerings-ID för den tjänst som notifieringen tillhör.</span><span class="sxs-lookup"><span data-stu-id="0fe42-159">Gets or sets the registration ID of the service the alert belongs to.</span></span>

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

### <span data-ttu-id="0fe42-160">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="0fe42-160">-ResourceRegistrationId</span></span>
<span data-ttu-id="0fe42-161">Hämtar eller anger registrerings-ID för den resurs som är associerad med aviseringen.</span><span class="sxs-lookup"><span data-stu-id="0fe42-161">Gets or sets the registration ID of the resource associated with the alert.</span></span>
<span data-ttu-id="0fe42-162">Om aviseringen inte är kopplad till en resurs är resurs registrerings-ID: t null.</span><span class="sxs-lookup"><span data-stu-id="0fe42-162">If the alert is not associated with a resource, the resource registration ID is null.</span></span>

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

### <span data-ttu-id="0fe42-163">– Allvarlighets grad</span><span class="sxs-lookup"><span data-stu-id="0fe42-163">-Severity</span></span>
<span data-ttu-id="0fe42-164">Allvarlighets grad för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="0fe42-164">Severity of the alert.</span></span>

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

### <span data-ttu-id="0fe42-165">-State</span><span class="sxs-lookup"><span data-stu-id="0fe42-165">-State</span></span>
<span data-ttu-id="0fe42-166">Status för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="0fe42-166">State of the alert.</span></span>

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

### <span data-ttu-id="0fe42-167">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0fe42-167">-SubscriptionId</span></span>
<span data-ttu-id="0fe42-168">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="0fe42-168">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0fe42-169">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="0fe42-169">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0fe42-170">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0fe42-170">-Tag</span></span>
<span data-ttu-id="0fe42-171">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="0fe42-171">Resource tags.</span></span>

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

### <span data-ttu-id="0fe42-172">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="0fe42-172">-Title</span></span>
<span data-ttu-id="0fe42-173">Hämtar eller anger resurs-ID för det påverkade objektet.</span><span class="sxs-lookup"><span data-stu-id="0fe42-173">Gets or sets the Resource ID for the impacted item.</span></span>

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

### <span data-ttu-id="0fe42-174">-Användare</span><span class="sxs-lookup"><span data-stu-id="0fe42-174">-User</span></span>
<span data-ttu-id="0fe42-175">Det användar namn som används för att utföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="0fe42-175">The username used to perform the operation.</span></span>

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

### <span data-ttu-id="0fe42-176">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0fe42-176">-Confirm</span></span>
<span data-ttu-id="0fe42-177">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0fe42-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fe42-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fe42-178">-WhatIf</span></span>
<span data-ttu-id="0fe42-179">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0fe42-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fe42-180">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0fe42-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fe42-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fe42-181">CommonParameters</span></span>
<span data-ttu-id="0fe42-182">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fe42-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fe42-183">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0fe42-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fe42-184">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0fe42-184">INPUTS</span></span>

### <span data-ttu-id="0fe42-185">Microsoft. Azure. PowerShell. cmdletar. InfrastructureInsightsAdmin. Models. Api20160501. IAlert</span><span class="sxs-lookup"><span data-stu-id="0fe42-185">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>

### <span data-ttu-id="0fe42-186">Microsoft. Azure. PowerShell. cmdletar. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="0fe42-186">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="0fe42-187">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0fe42-187">OUTPUTS</span></span>

### <span data-ttu-id="0fe42-188">Microsoft. Azure. PowerShell. cmdletar. InfrastructureInsightsAdmin. Models. Api20160501. IAlert</span><span class="sxs-lookup"><span data-stu-id="0fe42-188">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>



## <span data-ttu-id="0fe42-189">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0fe42-189">NOTES</span></span>

<span data-ttu-id="0fe42-190">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="0fe42-190">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0fe42-191">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0fe42-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="0fe42-192">Varning <IAlert> : det här objektet representerar en aviserings resurs.</span><span class="sxs-lookup"><span data-stu-id="0fe42-192">ALERT <IAlert>: This object represents an alert resource.</span></span>
  - <span data-ttu-id="0fe42-193">`[Location <String>]`: Azure-regionen där resursen bor</span><span class="sxs-lookup"><span data-stu-id="0fe42-193">`[Location <String>]`: The Azure Region where the resource lives</span></span>
  - <span data-ttu-id="0fe42-194">`[Tag <ITrackedResourceTags>]`: Resursfiler.</span><span class="sxs-lookup"><span data-stu-id="0fe42-194">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="0fe42-195">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="0fe42-195">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="0fe42-196">`[AlertId <String>]`: Hämtar eller anger aviseringens ID.</span><span class="sxs-lookup"><span data-stu-id="0fe42-196">`[AlertId <String>]`: Gets or sets the ID of the alert.</span></span>
  - <span data-ttu-id="0fe42-197">`[AlertProperty <IAlertModelAlertProperties>]`: Aviseringens egenskaper.</span><span class="sxs-lookup"><span data-stu-id="0fe42-197">`[AlertProperty <IAlertModelAlertProperties>]`: Properties of the alert.</span></span>
    - <span data-ttu-id="0fe42-198">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="0fe42-198">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="0fe42-199">`[ClosedByUserAlias <String>]`: Användaralias som stängde aviseringen.</span><span class="sxs-lookup"><span data-stu-id="0fe42-199">`[ClosedByUserAlias <String>]`: User alias who closed the alert.</span></span>
  - <span data-ttu-id="0fe42-200">`[ClosedTimestamp <String>]`: Tidsstämpel när aviseringen var stängd.</span><span class="sxs-lookup"><span data-stu-id="0fe42-200">`[ClosedTimestamp <String>]`: Timestamp when the alert was closed.</span></span>
  - <span data-ttu-id="0fe42-201">`[CreatedTimestamp <String>]`: Tidsstämpel när aviseringen skapades.</span><span class="sxs-lookup"><span data-stu-id="0fe42-201">`[CreatedTimestamp <String>]`: Timestamp when the alert was created.</span></span>
  - <span data-ttu-id="0fe42-202">`[Description <IDictionary[]>]`: Beskrivning av aviseringen.</span><span class="sxs-lookup"><span data-stu-id="0fe42-202">`[Description <IDictionary[]>]`: Description of the alert.</span></span>
  - <span data-ttu-id="0fe42-203">`[FaultId <String>]`: Hämtar eller anger aviseringens fel-ID.</span><span class="sxs-lookup"><span data-stu-id="0fe42-203">`[FaultId <String>]`: Gets or sets the fault ID of the alert.</span></span>
  - <span data-ttu-id="0fe42-204">`[FaultTypeId <String>]`: Hämtar eller anger aviseringens feltyp-ID.</span><span class="sxs-lookup"><span data-stu-id="0fe42-204">`[FaultTypeId <String>]`: Gets or sets the fault type ID of the alert.</span></span>
  - <span data-ttu-id="0fe42-205">`[HasValidRemediationAction <Boolean?>]`: Anger om aviseringen kan åtgärdas.</span><span class="sxs-lookup"><span data-stu-id="0fe42-205">`[HasValidRemediationAction <Boolean?>]`: Indicates if the alert can be remediated.</span></span>
  - <span data-ttu-id="0fe42-206">`[ImpactedResourceDisplayName <String>]`: Visnings namn för den påverkade posten.</span><span class="sxs-lookup"><span data-stu-id="0fe42-206">`[ImpactedResourceDisplayName <String>]`: Display name for the impacted item.</span></span>
  - <span data-ttu-id="0fe42-207">`[ImpactedResourceId <String>]`: Hämtar eller anger resurs-ID för det påverkade objektet.</span><span class="sxs-lookup"><span data-stu-id="0fe42-207">`[ImpactedResourceId <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>
  - <span data-ttu-id="0fe42-208">`[LastUpdatedTimestamp <String>]`: Tidsstämpel när aviseringen uppdaterades senast.</span><span class="sxs-lookup"><span data-stu-id="0fe42-208">`[LastUpdatedTimestamp <String>]`: Timestamp when the alert was last updated.</span></span>
  - <span data-ttu-id="0fe42-209">`[Remediation <IDictionary[]>]`: Hämtar eller anger de egna administratörs anvisningarna för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="0fe42-209">`[Remediation <IDictionary[]>]`: Gets or sets the admin friendly remediation instructions for the alert.</span></span>
  - <span data-ttu-id="0fe42-210">`[ResourceProviderRegistrationId <String>]`: Hämtar eller anger registrerings-ID för den tjänst som notifieringen tillhör.</span><span class="sxs-lookup"><span data-stu-id="0fe42-210">`[ResourceProviderRegistrationId <String>]`: Gets or sets the registration ID of the service the alert belongs to.</span></span>
  - <span data-ttu-id="0fe42-211">`[ResourceRegistrationId <String>]`: Hämtar eller anger registrerings-ID för resursen som är associerad med aviseringen.</span><span class="sxs-lookup"><span data-stu-id="0fe42-211">`[ResourceRegistrationId <String>]`: Gets or sets the registration ID of the resource associated with the alert.</span></span> <span data-ttu-id="0fe42-212">Om aviseringen inte är kopplad till en resurs är resurs registrerings-ID: t null.</span><span class="sxs-lookup"><span data-stu-id="0fe42-212">If the alert is not associated with a resource, the resource registration ID is null.</span></span>
  - <span data-ttu-id="0fe42-213">`[Severity <String>]`: Meddelandets allvarlighets grad.</span><span class="sxs-lookup"><span data-stu-id="0fe42-213">`[Severity <String>]`: Severity of the alert.</span></span>
  - <span data-ttu-id="0fe42-214">`[State <String>]`: Status för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="0fe42-214">`[State <String>]`: State of the alert.</span></span>
  - <span data-ttu-id="0fe42-215">`[Title <String>]`: Hämtar eller anger resurs-ID för det påverkade objektet.</span><span class="sxs-lookup"><span data-stu-id="0fe42-215">`[Title <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>

<span data-ttu-id="0fe42-216">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="0fe42-216">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0fe42-217">`[AlertName <String>]`: Aviseringens namn.</span><span class="sxs-lookup"><span data-stu-id="0fe42-217">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="0fe42-218">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="0fe42-218">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0fe42-219">`[Location <String>]`: Regionens namn</span><span class="sxs-lookup"><span data-stu-id="0fe42-219">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="0fe42-220">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0fe42-220">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="0fe42-221">`[ResourceRegistrationId <String>]`: Registrerings-ID för resurs.</span><span class="sxs-lookup"><span data-stu-id="0fe42-221">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="0fe42-222">`[ServiceHealth <String>]`: Tjänstens hälso namn.</span><span class="sxs-lookup"><span data-stu-id="0fe42-222">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="0fe42-223">`[ServiceRegistrationId <String>]`: ID för tjänste registrering.</span><span class="sxs-lookup"><span data-stu-id="0fe42-223">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="0fe42-224">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="0fe42-224">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0fe42-225">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="0fe42-225">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0fe42-226">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0fe42-226">RELATED LINKS</span></span>

