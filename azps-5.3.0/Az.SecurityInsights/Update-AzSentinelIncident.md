---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
ms.openlocfilehash: c98270b4e69d80e18ba721de0a6379d40d21fc75
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525553"
---
# <span data-ttu-id="5cbe2-101">Update-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="5cbe2-101">Update-AzSentinelIncident</span></span>

## <span data-ttu-id="5cbe2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5cbe2-102">SYNOPSIS</span></span>
<span data-ttu-id="5cbe2-103">Uppdatera ett samtal.</span><span class="sxs-lookup"><span data-stu-id="5cbe2-103">Update an Incident.</span></span>

## <span data-ttu-id="5cbe2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5cbe2-104">SYNTAX</span></span>

### <span data-ttu-id="5cbe2-105">IncidentId (standard)</span><span class="sxs-lookup"><span data-stu-id="5cbe2-105">IncidentId (Default)</span></span>
```
Update-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentID <String>
 [-Classification <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cbe2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5cbe2-106">InputObject</span></span>
```
Update-AzSentinelIncident -InputObject <PSSentinelIncident> [-Classification <String>]
 [-ClassificationComment <String>] [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cbe2-107">ID</span><span class="sxs-lookup"><span data-stu-id="5cbe2-107">ResourceId</span></span>
```
Update-AzSentinelIncident -ResourceId <String> [-Classification <String>] [-ClassificationComment <String>]
 [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cbe2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5cbe2-108">DESCRIPTION</span></span>
<span data-ttu-id="5cbe2-109">Cmdleten **Update-AzSentinelIncident** uppdaterar incidenten på den angivna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="5cbe2-109">The **Update-AzSentinelIncident** cmdlet updates the Incident in the specified workspace.</span></span>
<span data-ttu-id="5cbe2-110">Du kan skicka ett **incident** objekt som en parameter eller med hjälp av pipeline-operatorn eller så kan du ange de parametrar som krävs.</span><span class="sxs-lookup"><span data-stu-id="5cbe2-110">You can pass an **Incident** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="5cbe2-111">Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="5cbe2-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="5cbe2-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5cbe2-112">EXAMPLES</span></span>

### <span data-ttu-id="5cbe2-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5cbe2-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -Severity High
```

<span data-ttu-id="5cbe2-114">Kommandot får händelsen genom att ange *IncidentId* och ställa in egenskapen *allvarlighets grad* på *High*.</span><span class="sxs-lookup"><span data-stu-id="5cbe2-114">The command gets the Incident by *IncidentId* and sets the *Severity* property to *High*.</span></span>  <span data-ttu-id="5cbe2-115">Alla andra egenskaper förblir desamma.</span><span class="sxs-lookup"><span data-stu-id="5cbe2-115">All other properties remain the same.</span></span>

## <span data-ttu-id="5cbe2-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5cbe2-116">PARAMETERS</span></span>

### <span data-ttu-id="5cbe2-117">-Klassificering</span><span class="sxs-lookup"><span data-stu-id="5cbe2-117">-Classification</span></span>
<span data-ttu-id="5cbe2-118">Incident Classificaiton.</span><span class="sxs-lookup"><span data-stu-id="5cbe2-118">Incident Classificaiton.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: BenignPositive, FalsePositive, TruePositive, Undetermined

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbe2-119">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="5cbe2-119">-ClassificationComment</span></span>
<span data-ttu-id="5cbe2-120">Classificaiton för incidenten.</span><span class="sxs-lookup"><span data-stu-id="5cbe2-120">Incident Classificaiton Comment.</span></span>

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

### <span data-ttu-id="5cbe2-121">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="5cbe2-121">-ClassificationReason</span></span>
<span data-ttu-id="5cbe2-122">Classificaiton anledning till incident.</span><span class="sxs-lookup"><span data-stu-id="5cbe2-122">Incident Classificaiton Reason.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: InaccurateData, IncorrectAlertLogic, SuspiciousActivity, SuspiciousButExpected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbe2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cbe2-123">-DefaultProfile</span></span>
<span data-ttu-id="5cbe2-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5cbe2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cbe2-125">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="5cbe2-125">-Description</span></span>
<span data-ttu-id="5cbe2-126">Problembeskrivning.</span><span class="sxs-lookup"><span data-stu-id="5cbe2-126">Description.</span></span>

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

### <span data-ttu-id="5cbe2-127">-IncidentID</span><span class="sxs-lookup"><span data-stu-id="5cbe2-127">-IncidentID</span></span>
<span data-ttu-id="5cbe2-128">Incident-ID.</span><span class="sxs-lookup"><span data-stu-id="5cbe2-128">Incident Id.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId, ParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbe2-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cbe2-129">-InputObject</span></span>
<span data-ttu-id="5cbe2-130">InputObject.</span><span class="sxs-lookup"><span data-stu-id="5cbe2-130">InputObject.</span></span>

```yaml
Type: PSSentinelIncident
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cbe2-131">-Etikett</span><span class="sxs-lookup"><span data-stu-id="5cbe2-131">-Label</span></span>
<span data-ttu-id="5cbe2-132">Incident etiketter.</span><span class="sxs-lookup"><span data-stu-id="5cbe2-132">Incident Labels.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cbe2-133">-Owner</span><span class="sxs-lookup"><span data-stu-id="5cbe2-133">-Owner</span></span>
<span data-ttu-id="5cbe2-134">Incident ägare.</span><span class="sxs-lookup"><span data-stu-id="5cbe2-134">Incident Owner.</span></span>

```yaml
Type: PSSentinelIncidentOwner
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cbe2-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cbe2-135">-ResourceGroupName</span></span>
<span data-ttu-id="5cbe2-136">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="5cbe2-136">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbe2-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5cbe2-137">-ResourceId</span></span>
<span data-ttu-id="5cbe2-138">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="5cbe2-138">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cbe2-139">– Allvarlighets grad</span><span class="sxs-lookup"><span data-stu-id="5cbe2-139">-Severity</span></span>
<span data-ttu-id="5cbe2-140">Allvarlighets grad för incidenter.</span><span class="sxs-lookup"><span data-stu-id="5cbe2-140">Incident Severity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbe2-141">-Status</span><span class="sxs-lookup"><span data-stu-id="5cbe2-141">-Status</span></span>
<span data-ttu-id="5cbe2-142">Incident status.</span><span class="sxs-lookup"><span data-stu-id="5cbe2-142">Incident Status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Active, Closed, New

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbe2-143">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="5cbe2-143">-Title</span></span>
<span data-ttu-id="5cbe2-144">Rubrik för incidenten.</span><span class="sxs-lookup"><span data-stu-id="5cbe2-144">Incident Title.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbe2-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5cbe2-145">-WorkspaceName</span></span>
<span data-ttu-id="5cbe2-146">Namn på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="5cbe2-146">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbe2-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5cbe2-147">-Confirm</span></span>
<span data-ttu-id="5cbe2-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5cbe2-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cbe2-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cbe2-149">-WhatIf</span></span>
<span data-ttu-id="5cbe2-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5cbe2-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cbe2-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5cbe2-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cbe2-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cbe2-152">CommonParameters</span></span>
<span data-ttu-id="5cbe2-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cbe2-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cbe2-154">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5cbe2-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cbe2-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5cbe2-155">INPUTS</span></span>

### <span data-ttu-id="5cbe2-156">Microsoft. Azure. commands. SecurityInsights. Models. incidenter. PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="5cbe2-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

### <span data-ttu-id="5cbe2-157">System. String</span><span class="sxs-lookup"><span data-stu-id="5cbe2-157">System.String</span></span>

### <span data-ttu-id="5cbe2-158">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. commands. SecurityInsights. Models. PSSentinelIncidentLabels, Microsoft. Azure. PowerShell. cmdletar. SecurityInsights, version = 0.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5cbe2-158">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="5cbe2-159">Microsoft. Azure. commands. SecurityInsights. Models. incidenter. PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="5cbe2-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>

## <span data-ttu-id="5cbe2-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5cbe2-160">OUTPUTS</span></span>

### <span data-ttu-id="5cbe2-161">Microsoft. Azure. commands. SecurityInsights. Models. incidenter. PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="5cbe2-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

## <span data-ttu-id="5cbe2-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5cbe2-162">NOTES</span></span>

## <span data-ttu-id="5cbe2-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5cbe2-163">RELATED LINKS</span></span>
