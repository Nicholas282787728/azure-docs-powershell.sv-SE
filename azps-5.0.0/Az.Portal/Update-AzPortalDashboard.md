---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/update-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
ms.openlocfilehash: 42c5d90a24e671c47245ace0046c6f5987dbcd94
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323123"
---
# <span data-ttu-id="bb024-101">Update-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="bb024-101">Update-AzPortalDashboard</span></span>

## <span data-ttu-id="bb024-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bb024-102">SYNOPSIS</span></span>
<span data-ttu-id="bb024-103">Uppdaterar en befintlig instrument panel.</span><span class="sxs-lookup"><span data-stu-id="bb024-103">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="bb024-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bb024-104">SYNTAX</span></span>

### <span data-ttu-id="bb024-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="bb024-105">UpdateExpanded (Default)</span></span>
```
Update-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bb024-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="bb024-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPortalDashboard -InputObject <IPortalIdentity> [-Lens <Hashtable>] [-Metadata <Hashtable>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bb024-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bb024-107">DESCRIPTION</span></span>
<span data-ttu-id="bb024-108">Uppdaterar en befintlig instrument panel.</span><span class="sxs-lookup"><span data-stu-id="bb024-108">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="bb024-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bb024-109">EXAMPLES</span></span>

### <span data-ttu-id="bb024-110">Exempel 1: uppdatera taggarna för en instrument panel</span><span class="sxs-lookup"><span data-stu-id="bb024-110">Example 1: Update the Tags of a Dashboard</span></span>
```powershell
PS C:\> Update-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="bb024-111">Uppdatera taggarna i en instrument panel.</span><span class="sxs-lookup"><span data-stu-id="bb024-111">Update the tags in a dashboard.</span></span>
<span data-ttu-id="bb024-112">Taggar representeras som en infogad hash.</span><span class="sxs-lookup"><span data-stu-id="bb024-112">Tags are represented as an inline hashtable.</span></span>

### <span data-ttu-id="bb024-113">Exempel 2: uppdatera instrument panels Taggar med pipelinen</span><span class="sxs-lookup"><span data-stu-id="bb024-113">Example 2: Update Dashboard tags using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 | Update-AzPortalDashboard -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="bb024-114">Uppdatera taggarna i en instrument panel återkallas med Get-AzPortalDashboard.</span><span class="sxs-lookup"><span data-stu-id="bb024-114">Update the Tags in a Dashboard retried using Get-AzPortalDashboard.</span></span>
<span data-ttu-id="bb024-115">Det här kan användas för att uppdatera märkningarna över en enskild instrument panel eller flera dashboardfs.</span><span class="sxs-lookup"><span data-stu-id="bb024-115">This can be used to update the tags over a single dashboard, or multiple dashboardfs.</span></span>

## <span data-ttu-id="bb024-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bb024-116">PARAMETERS</span></span>

### <span data-ttu-id="bb024-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb024-117">-DefaultProfile</span></span>
<span data-ttu-id="bb024-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bb024-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb024-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb024-119">-InputObject</span></span>
<span data-ttu-id="bb024-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="bb024-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb024-121">-Lins</span><span class="sxs-lookup"><span data-stu-id="bb024-121">-Lens</span></span>
<span data-ttu-id="bb024-122">Instrument panels linser.</span><span class="sxs-lookup"><span data-stu-id="bb024-122">The dashboard lenses.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb024-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="bb024-123">-Metadata</span></span>
<span data-ttu-id="bb024-124">Instrument panelens metadata.</span><span class="sxs-lookup"><span data-stu-id="bb024-124">The dashboard metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb024-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="bb024-125">-Name</span></span>
<span data-ttu-id="bb024-126">Instrument panelens namn.</span><span class="sxs-lookup"><span data-stu-id="bb024-126">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb024-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb024-127">-ResourceGroupName</span></span>
<span data-ttu-id="bb024-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="bb024-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb024-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bb024-129">-SubscriptionId</span></span>
<span data-ttu-id="bb024-130">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="bb024-130">The Azure subscription ID.</span></span>
<span data-ttu-id="bb024-131">Det här är en GUID-formaterad sträng (till exempel 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="bb024-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb024-132">-Tagg</span><span class="sxs-lookup"><span data-stu-id="bb024-132">-Tag</span></span>
<span data-ttu-id="bb024-133">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="bb024-133">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb024-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bb024-134">-Confirm</span></span>
<span data-ttu-id="bb024-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bb024-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb024-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb024-136">-WhatIf</span></span>
<span data-ttu-id="bb024-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bb024-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb024-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bb024-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb024-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb024-139">CommonParameters</span></span>
<span data-ttu-id="bb024-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb024-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb024-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb024-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb024-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bb024-142">INPUTS</span></span>

### <span data-ttu-id="bb024-143">Microsoft. Azure. PowerShell. cmdletar. Portal. Models. IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="bb024-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="bb024-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bb024-144">OUTPUTS</span></span>

### <span data-ttu-id="bb024-145">Microsoft. Azure. PowerShell. cmdletar. Portal. Models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="bb024-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="bb024-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bb024-146">NOTES</span></span>

<span data-ttu-id="bb024-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="bb024-147">ALIASES</span></span>

<span data-ttu-id="bb024-148">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="bb024-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bb024-149">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="bb024-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bb024-150">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bb024-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bb024-151">INPUTOBJECT <IPortalIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="bb024-151">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bb024-152">`[DashboardName <String>]`: Instrument panelens namn.</span><span class="sxs-lookup"><span data-stu-id="bb024-152">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="bb024-153">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="bb024-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bb024-154">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="bb024-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="bb024-155">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="bb024-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="bb024-156">Det här är en GUID-formaterad sträng (till exempel 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="bb024-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="bb024-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bb024-157">RELATED LINKS</span></span>

