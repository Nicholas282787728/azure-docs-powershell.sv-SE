---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/get-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
ms.openlocfilehash: aa11a9828c422069823226b2d5df57efc84f8c7b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272413"
---
# <span data-ttu-id="124a7-101">Get-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="124a7-101">Get-AzPortalDashboard</span></span>

## <span data-ttu-id="124a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="124a7-102">SYNOPSIS</span></span>
<span data-ttu-id="124a7-103">Hämtar instrument panelen.</span><span class="sxs-lookup"><span data-stu-id="124a7-103">Gets the Dashboard.</span></span>

## <span data-ttu-id="124a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="124a7-104">SYNTAX</span></span>

### <span data-ttu-id="124a7-105">List1 (standard)</span><span class="sxs-lookup"><span data-stu-id="124a7-105">List1 (Default)</span></span>
```
Get-AzPortalDashboard [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="124a7-106">Lära</span><span class="sxs-lookup"><span data-stu-id="124a7-106">Get</span></span>
```
Get-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="124a7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="124a7-107">GetViaIdentity</span></span>
```
Get-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="124a7-108">Förteckning</span><span class="sxs-lookup"><span data-stu-id="124a7-108">List</span></span>
```
Get-AzPortalDashboard -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="124a7-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="124a7-109">DESCRIPTION</span></span>
<span data-ttu-id="124a7-110">Hämtar instrument panelen.</span><span class="sxs-lookup"><span data-stu-id="124a7-110">Gets the Dashboard.</span></span>

## <span data-ttu-id="124a7-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="124a7-111">EXAMPLES</span></span>

### <span data-ttu-id="124a7-112">Exempel 1: lista alla instrument paneler i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="124a7-112">Example 1: List all dashboards in a subscription</span></span>
```powershell
PS C:> Get-AzPortalDashboard                                                                                                                     
Location Name                                           Type
-------- ----                                           ----
eastasia my-custom-dashboard1                           Microsoft.Portal/dashboards
westus   my-second-custom-dashboard1                    Microsoft.Portal/dashboards

```

<span data-ttu-id="124a7-113">Visa en lista med alla instrument paneler i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="124a7-113">List all dashboards in a subscription</span></span>

### <span data-ttu-id="124a7-114">Exempel 2: få information om en enda portal instrument panel</span><span class="sxs-lookup"><span data-stu-id="124a7-114">Example 2: Get details for a single Portal Dashboard</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name mydashboard

Location Name        Type
-------- ----        ----
eastus   mydashboard Microsoft.Portal/dashboards
```

<span data-ttu-id="124a7-115">Få information om en enda instrument panel</span><span class="sxs-lookup"><span data-stu-id="124a7-115">Get details for a single dashboard</span></span>

## <span data-ttu-id="124a7-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="124a7-116">PARAMETERS</span></span>

### <span data-ttu-id="124a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="124a7-117">-DefaultProfile</span></span>
<span data-ttu-id="124a7-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="124a7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="124a7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="124a7-119">-InputObject</span></span>
<span data-ttu-id="124a7-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="124a7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="124a7-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="124a7-121">-Name</span></span>
<span data-ttu-id="124a7-122">Instrument panelens namn.</span><span class="sxs-lookup"><span data-stu-id="124a7-122">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="124a7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="124a7-123">-ResourceGroupName</span></span>
<span data-ttu-id="124a7-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="124a7-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="124a7-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="124a7-125">-SubscriptionId</span></span>
<span data-ttu-id="124a7-126">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="124a7-126">The Azure subscription ID.</span></span>
<span data-ttu-id="124a7-127">Det här är en GUID-formaterad sträng (till exempel 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="124a7-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="124a7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="124a7-128">CommonParameters</span></span>
<span data-ttu-id="124a7-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="124a7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="124a7-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="124a7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="124a7-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="124a7-131">INPUTS</span></span>

### <span data-ttu-id="124a7-132">Microsoft. Azure. PowerShell. cmdletar. Portal. Models. IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="124a7-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="124a7-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="124a7-133">OUTPUTS</span></span>

### <span data-ttu-id="124a7-134">Microsoft. Azure. PowerShell. cmdletar. Portal. Models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="124a7-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="124a7-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="124a7-135">NOTES</span></span>

<span data-ttu-id="124a7-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="124a7-136">ALIASES</span></span>

<span data-ttu-id="124a7-137">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="124a7-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="124a7-138">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="124a7-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="124a7-139">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="124a7-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="124a7-140">INPUTOBJECT <IPortalIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="124a7-140">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="124a7-141">`[DashboardName <String>]`: Instrument panelens namn.</span><span class="sxs-lookup"><span data-stu-id="124a7-141">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="124a7-142">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="124a7-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="124a7-143">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="124a7-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="124a7-144">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="124a7-144">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="124a7-145">Det här är en GUID-formaterad sträng (till exempel 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="124a7-145">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="124a7-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="124a7-146">RELATED LINKS</span></span>

