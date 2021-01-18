---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
ms.openlocfilehash: b3618f178ea5dee54991c037da78ac51f2ed4502
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525578"
---
# <span data-ttu-id="8fbb7-101">New-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="8fbb7-101">New-AzSentinelIncident</span></span>

## <span data-ttu-id="8fbb7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8fbb7-102">SYNOPSIS</span></span>
<span data-ttu-id="8fbb7-103">Skapa ett samtal.</span><span class="sxs-lookup"><span data-stu-id="8fbb7-103">Create an Incident.</span></span>

## <span data-ttu-id="8fbb7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8fbb7-104">SYNTAX</span></span>

```
New-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-Classificaton <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fbb7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8fbb7-105">DESCRIPTION</span></span>
<span data-ttu-id="8fbb7-106">Cmdleten **New-AzSentinelIncident** skapar en incident från den angivna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="8fbb7-106">The **New-AzSentinelIncident** cmdlet creates a Incident from the specified workspace.</span></span>
<span data-ttu-id="8fbb7-107">Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="8fbb7-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="8fbb7-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8fbb7-108">EXAMPLES</span></span>

### <span data-ttu-id="8fbb7-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8fbb7-109">Example 1</span></span>
```powershell
PS C:\> $Incident = New-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Title "NewIncident" -Severity Low -Status New
```

<span data-ttu-id="8fbb7-110">I det här exemplet skapas en **incident** på den angivna arbets ytan och den lagras sedan i $incident variabel.</span><span class="sxs-lookup"><span data-stu-id="8fbb7-110">This example creates an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="8fbb7-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8fbb7-111">PARAMETERS</span></span>

### <span data-ttu-id="8fbb7-112">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="8fbb7-112">-ClassificationComment</span></span>
<span data-ttu-id="8fbb7-113">Classificaiton för incidenten.</span><span class="sxs-lookup"><span data-stu-id="8fbb7-113">Incident Classificaiton Comment.</span></span>

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

### <span data-ttu-id="8fbb7-114">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="8fbb7-114">-ClassificationReason</span></span>
<span data-ttu-id="8fbb7-115">Classificaiton anledning till incident.</span><span class="sxs-lookup"><span data-stu-id="8fbb7-115">Incident Classificaiton Reason.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: InaccurateData, IncorrectAlertLogic, SuspiciousActivity, SuspiciousButExpected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fbb7-116">-Classificaton</span><span class="sxs-lookup"><span data-stu-id="8fbb7-116">-Classificaton</span></span>
<span data-ttu-id="8fbb7-117">Incident Classificaiton.</span><span class="sxs-lookup"><span data-stu-id="8fbb7-117">Incident Classificaiton.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: BenignPositive, FalsePositive, TruePositive, Undetermined

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fbb7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fbb7-118">-DefaultProfile</span></span>
<span data-ttu-id="8fbb7-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8fbb7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fbb7-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="8fbb7-120">-Description</span></span>
<span data-ttu-id="8fbb7-121">Problembeskrivning.</span><span class="sxs-lookup"><span data-stu-id="8fbb7-121">Description.</span></span>

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

### <span data-ttu-id="8fbb7-122">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="8fbb7-122">-IncidentId</span></span>
<span data-ttu-id="8fbb7-123">Incident-ID.</span><span class="sxs-lookup"><span data-stu-id="8fbb7-123">Incident Id.</span></span>

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

### <span data-ttu-id="8fbb7-124">-Etikett</span><span class="sxs-lookup"><span data-stu-id="8fbb7-124">-Label</span></span>
<span data-ttu-id="8fbb7-125">Incident etiketter.</span><span class="sxs-lookup"><span data-stu-id="8fbb7-125">Incident Labels.</span></span>

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

### <span data-ttu-id="8fbb7-126">-Owner</span><span class="sxs-lookup"><span data-stu-id="8fbb7-126">-Owner</span></span>
<span data-ttu-id="8fbb7-127">Incident ägare.</span><span class="sxs-lookup"><span data-stu-id="8fbb7-127">Incident Owner.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fbb7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fbb7-128">-ResourceGroupName</span></span>
<span data-ttu-id="8fbb7-129">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="8fbb7-129">Resource group name.</span></span>

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

### <span data-ttu-id="8fbb7-130">– Allvarlighets grad</span><span class="sxs-lookup"><span data-stu-id="8fbb7-130">-Severity</span></span>
<span data-ttu-id="8fbb7-131">Allvarlighets grad för incidenter.</span><span class="sxs-lookup"><span data-stu-id="8fbb7-131">Incident Severity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fbb7-132">-Status</span><span class="sxs-lookup"><span data-stu-id="8fbb7-132">-Status</span></span>
<span data-ttu-id="8fbb7-133">Incident status.</span><span class="sxs-lookup"><span data-stu-id="8fbb7-133">Incident Status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Active, Closed, New

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fbb7-134">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="8fbb7-134">-Title</span></span>
<span data-ttu-id="8fbb7-135">Rubrik för incidenten.</span><span class="sxs-lookup"><span data-stu-id="8fbb7-135">Incident Title.</span></span>

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

### <span data-ttu-id="8fbb7-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8fbb7-136">-WorkspaceName</span></span>
<span data-ttu-id="8fbb7-137">Namn på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="8fbb7-137">Workspace Name.</span></span>

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

### <span data-ttu-id="8fbb7-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8fbb7-138">-Confirm</span></span>
<span data-ttu-id="8fbb7-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8fbb7-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fbb7-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fbb7-140">-WhatIf</span></span>
<span data-ttu-id="8fbb7-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8fbb7-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8fbb7-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8fbb7-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fbb7-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fbb7-143">CommonParameters</span></span>
<span data-ttu-id="8fbb7-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fbb7-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fbb7-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8fbb7-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fbb7-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8fbb7-146">INPUTS</span></span>

### <span data-ttu-id="8fbb7-147">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. commands. SecurityInsights. Models. PSSentinelIncidentLabels, Microsoft. Azure. PowerShell. cmdletar. SecurityInsights, version = 0.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8fbb7-147">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
### <span data-ttu-id="8fbb7-148">Microsoft. Azure. commands. SecurityInsights. Models. incidenter. PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="8fbb7-148">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>
## <span data-ttu-id="8fbb7-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8fbb7-149">OUTPUTS</span></span>

### <span data-ttu-id="8fbb7-150">Microsoft. Azure. commands. SecurityInsights. Models. incidenter. PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="8fbb7-150">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="8fbb7-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8fbb7-151">NOTES</span></span>

## <span data-ttu-id="8fbb7-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8fbb7-152">RELATED LINKS</span></span>
