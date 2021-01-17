---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/remove-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
ms.openlocfilehash: f0ef681f09caf43ac2f2100d1a30af19b1b3c364
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417000"
---
# <span data-ttu-id="78371-101">Remove-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="78371-101">Remove-AzPortalDashboard</span></span>

## <span data-ttu-id="78371-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="78371-102">SYNOPSIS</span></span>
<span data-ttu-id="78371-103">Tar bort instrument panelen.</span><span class="sxs-lookup"><span data-stu-id="78371-103">Deletes the Dashboard.</span></span>

## <span data-ttu-id="78371-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="78371-104">SYNTAX</span></span>

### <span data-ttu-id="78371-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="78371-105">Delete (Default)</span></span>
```
Remove-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="78371-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="78371-106">DeleteViaIdentity</span></span>
```
Remove-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="78371-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="78371-107">DESCRIPTION</span></span>
<span data-ttu-id="78371-108">Tar bort instrument panelen.</span><span class="sxs-lookup"><span data-stu-id="78371-108">Deletes the Dashboard.</span></span>

## <span data-ttu-id="78371-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="78371-109">EXAMPLES</span></span>

### <span data-ttu-id="78371-110">Exempel 1: ta bort en instrument panel</span><span class="sxs-lookup"><span data-stu-id="78371-110">Example 1: Remove a Dashboard</span></span>
```powershell
PS C:\td\> Remove-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02
```

<span data-ttu-id="78371-111">Ta bort en Dashbaord med resurs grupp namn och instrument panels namn.</span><span class="sxs-lookup"><span data-stu-id="78371-111">Remove a Dashbaord using resource group name and dashboard name.</span></span>

### <span data-ttu-id="78371-112">Exempel 2: ta bort en instrument panel med pipelinen</span><span class="sxs-lookup"><span data-stu-id="78371-112">Example 2: Remove a Dashboard using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02 | Remove-AzPortalDashboard
```

<span data-ttu-id="78371-113">Ta bort instrument panelen från ett Get-AzDashboard samtal.</span><span class="sxs-lookup"><span data-stu-id="78371-113">Remove the dashboard returned from a Get-AzDashboard call.</span></span>

## <span data-ttu-id="78371-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="78371-114">PARAMETERS</span></span>

### <span data-ttu-id="78371-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78371-115">-DefaultProfile</span></span>
<span data-ttu-id="78371-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="78371-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78371-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78371-117">-InputObject</span></span>
<span data-ttu-id="78371-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="78371-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78371-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="78371-119">-Name</span></span>
<span data-ttu-id="78371-120">Instrument panelens namn.</span><span class="sxs-lookup"><span data-stu-id="78371-120">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78371-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78371-121">-PassThru</span></span>
<span data-ttu-id="78371-122">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="78371-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="78371-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78371-123">-ResourceGroupName</span></span>
<span data-ttu-id="78371-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="78371-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78371-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="78371-125">-SubscriptionId</span></span>
<span data-ttu-id="78371-126">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="78371-126">The Azure subscription ID.</span></span>
<span data-ttu-id="78371-127">Det här är en GUID-formaterad sträng (till exempel 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="78371-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78371-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="78371-128">-Confirm</span></span>
<span data-ttu-id="78371-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="78371-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78371-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78371-130">-WhatIf</span></span>
<span data-ttu-id="78371-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="78371-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78371-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="78371-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78371-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78371-133">CommonParameters</span></span>
<span data-ttu-id="78371-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78371-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78371-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78371-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78371-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="78371-136">INPUTS</span></span>

### <span data-ttu-id="78371-137">Microsoft. Azure. PowerShell. cmdletar. Portal. Models. IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="78371-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="78371-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="78371-138">OUTPUTS</span></span>

### <span data-ttu-id="78371-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="78371-139">System.Boolean</span></span>

## <span data-ttu-id="78371-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="78371-140">NOTES</span></span>

<span data-ttu-id="78371-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="78371-141">ALIASES</span></span>

<span data-ttu-id="78371-142">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="78371-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="78371-143">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="78371-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="78371-144">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="78371-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="78371-145">INPUTOBJECT <IPortalIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="78371-145">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="78371-146">`[DashboardName <String>]`: Instrument panelens namn.</span><span class="sxs-lookup"><span data-stu-id="78371-146">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="78371-147">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="78371-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="78371-148">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="78371-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="78371-149">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="78371-149">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="78371-150">Det här är en GUID-formaterad sträng (till exempel 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="78371-150">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="78371-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="78371-151">RELATED LINKS</span></span>

