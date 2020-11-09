---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/new-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
ms.openlocfilehash: 80b2289b4f481fff126d9cd5dfc98ca94536cfa0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325613"
---
# <span data-ttu-id="13551-101">New-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="13551-101">New-AzPortalDashboard</span></span>

## <span data-ttu-id="13551-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13551-102">SYNOPSIS</span></span>
<span data-ttu-id="13551-103">Skapar eller uppdaterar en instrument panel.</span><span class="sxs-lookup"><span data-stu-id="13551-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="13551-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13551-104">SYNTAX</span></span>

### <span data-ttu-id="13551-105">CreateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="13551-105">CreateExpanded (Default)</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="13551-106">Göra</span><span class="sxs-lookup"><span data-stu-id="13551-106">Create</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Dashboard <IDashboard>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="13551-107">CreateByFile</span><span class="sxs-lookup"><span data-stu-id="13551-107">CreateByFile</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="13551-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13551-108">DESCRIPTION</span></span>
<span data-ttu-id="13551-109">Skapar eller uppdaterar en instrument panel.</span><span class="sxs-lookup"><span data-stu-id="13551-109">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="13551-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13551-110">EXAMPLES</span></span>

### <span data-ttu-id="13551-111">Exempel 1: skapa en instrument panel med hjälp av en kontrollpanelflik</span><span class="sxs-lookup"><span data-stu-id="13551-111">Example 1: Create a dashboard using a dashboard template file</span></span>
```powershell
PS C:\> New-AzPortalDashboard -DashboardPath .\resources\dash1.json -ResourceGroupName mydash-rg -DashboardName my-dashboard03

Location Name           Type
-------- ----           ----
eastasia my-dashboard03 Microsoft.Portal/dashboards
```

<span data-ttu-id="13551-112">Skapa en ny instrument panel med den medföljande mallsida mal len.</span><span class="sxs-lookup"><span data-stu-id="13551-112">Create a new dashboard using the provided dashboard template file.</span></span>

## <span data-ttu-id="13551-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13551-113">PARAMETERS</span></span>

### <span data-ttu-id="13551-114">-Instrument panel</span><span class="sxs-lookup"><span data-stu-id="13551-114">-Dashboard</span></span>
<span data-ttu-id="13551-115">Resurs definitionen för den delade instrument panelen.</span><span class="sxs-lookup"><span data-stu-id="13551-115">The shared dashboard resource definition.</span></span>
<span data-ttu-id="13551-116">Om du vill skapa läser du avsnittet anteckningar för instrument PANELENs egenskaper och skapar en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="13551-116">To construct, see NOTES section for DASHBOARD properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13551-117">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="13551-117">-DashboardPath</span></span>
<span data-ttu-id="13551-118">Sökvägen till en befintlig kontrollpanelflik.</span><span class="sxs-lookup"><span data-stu-id="13551-118">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="13551-119">Instrumentpanelsdesignern kan hämtas från portalen.</span><span class="sxs-lookup"><span data-stu-id="13551-119">Dashboard templates may be downloaded from the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13551-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13551-120">-DefaultProfile</span></span>
<span data-ttu-id="13551-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="13551-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13551-122">-Lins</span><span class="sxs-lookup"><span data-stu-id="13551-122">-Lens</span></span>
<span data-ttu-id="13551-123">Instrument panels linser.</span><span class="sxs-lookup"><span data-stu-id="13551-123">The dashboard lenses.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13551-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="13551-124">-Location</span></span>
<span data-ttu-id="13551-125">Resurs plats</span><span class="sxs-lookup"><span data-stu-id="13551-125">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13551-126">-Metadata</span><span class="sxs-lookup"><span data-stu-id="13551-126">-Metadata</span></span>
<span data-ttu-id="13551-127">Instrument panelens metadata.</span><span class="sxs-lookup"><span data-stu-id="13551-127">The dashboard metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13551-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="13551-128">-Name</span></span>
<span data-ttu-id="13551-129">Instrument panelens namn.</span><span class="sxs-lookup"><span data-stu-id="13551-129">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13551-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13551-130">-ResourceGroupName</span></span>
<span data-ttu-id="13551-131">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="13551-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="13551-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="13551-132">-SubscriptionId</span></span>
<span data-ttu-id="13551-133">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="13551-133">The Azure subscription ID.</span></span>
<span data-ttu-id="13551-134">Det här är en GUID-formaterad sträng (till exempel 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="13551-134">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13551-135">-Tagg</span><span class="sxs-lookup"><span data-stu-id="13551-135">-Tag</span></span>
<span data-ttu-id="13551-136">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="13551-136">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13551-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="13551-137">-Confirm</span></span>
<span data-ttu-id="13551-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="13551-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13551-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13551-139">-WhatIf</span></span>
<span data-ttu-id="13551-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="13551-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13551-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="13551-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13551-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13551-142">CommonParameters</span></span>
<span data-ttu-id="13551-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13551-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13551-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13551-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13551-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13551-145">INPUTS</span></span>

### <span data-ttu-id="13551-146">Microsoft. Azure. PowerShell. cmdletar. Portal. Models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="13551-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="13551-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13551-147">OUTPUTS</span></span>

### <span data-ttu-id="13551-148">Microsoft. Azure. PowerShell. cmdletar. Portal. Models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="13551-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="13551-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13551-149">NOTES</span></span>

<span data-ttu-id="13551-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="13551-150">ALIASES</span></span>

<span data-ttu-id="13551-151">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="13551-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="13551-152">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="13551-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="13551-153">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="13551-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="13551-154">INSTRUMENT panel <IDashboard> : resurs definitionen för den delade instrument panelen.</span><span class="sxs-lookup"><span data-stu-id="13551-154">DASHBOARD <IDashboard>: The shared dashboard resource definition.</span></span>
  - <span data-ttu-id="13551-155">`Location <String>`: Resurs plats</span><span class="sxs-lookup"><span data-stu-id="13551-155">`Location <String>`: Resource location</span></span>
  - <span data-ttu-id="13551-156">`[Lens <IDashboardPropertiesLenses>]`: Instrument panels linser.</span><span class="sxs-lookup"><span data-stu-id="13551-156">`[Lens <IDashboardPropertiesLenses>]`: The dashboard lenses.</span></span>
    - <span data-ttu-id="13551-157">`[(Any) <IDashboardLens>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="13551-157">`[(Any) <IDashboardLens>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="13551-158">`[Metadata <IDashboardPropertiesMetadata>]`: Instrument panelens metadata.</span><span class="sxs-lookup"><span data-stu-id="13551-158">`[Metadata <IDashboardPropertiesMetadata>]`: The dashboard metadata.</span></span>
    - <span data-ttu-id="13551-159">`[(Any) <Object>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="13551-159">`[(Any) <Object>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="13551-160">`[Tag <IDashboardTags>]`: Resursfiler</span><span class="sxs-lookup"><span data-stu-id="13551-160">`[Tag <IDashboardTags>]`: Resource tags</span></span>
    - <span data-ttu-id="13551-161">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="13551-161">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="13551-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13551-162">RELATED LINKS</span></span>

