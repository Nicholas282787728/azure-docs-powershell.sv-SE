---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
ms.openlocfilehash: 7f2bb3f1d378afec5b0774aec2977b507654b931
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260003"
---
# <span data-ttu-id="a42f7-101">Get-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="a42f7-101">Get-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="a42f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a42f7-102">SYNOPSIS</span></span>
<span data-ttu-id="a42f7-103">Hämtar arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="a42f7-103">Gets the workspace.</span></span>

## <span data-ttu-id="a42f7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a42f7-104">SYNTAX</span></span>

### <span data-ttu-id="a42f7-105">List1 (standard)</span><span class="sxs-lookup"><span data-stu-id="a42f7-105">List1 (Default)</span></span>
```
Get-AzDatabricksWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a42f7-106">Lära</span><span class="sxs-lookup"><span data-stu-id="a42f7-106">Get</span></span>
```
Get-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a42f7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a42f7-107">GetViaIdentity</span></span>
```
Get-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a42f7-108">Förteckning</span><span class="sxs-lookup"><span data-stu-id="a42f7-108">List</span></span>
```
Get-AzDatabricksWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a42f7-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a42f7-109">DESCRIPTION</span></span>
<span data-ttu-id="a42f7-110">Hämtar arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="a42f7-110">Gets the workspace.</span></span>

## <span data-ttu-id="a42f7-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a42f7-111">EXAMPLES</span></span>

### <span data-ttu-id="a42f7-112">Exempel 1: skaffa en Databricks-arbetsyta med namn</span><span class="sxs-lookup"><span data-stu-id="a42f7-112">Example 1: Get a Databricks workspace with name</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="a42f7-113">Det här kommandot får en Databricks-arbetsyta i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a42f7-113">This command gets a Databricks workspace in a resource group.</span></span>

### <span data-ttu-id="a42f7-114">Exempel 2: lista alla Databricks-arbetsytor i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="a42f7-114">Example 2: List all Databricks workspaces in a subscription</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="a42f7-115">Det här kommandot visar alla Databricks arbets ytor i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="a42f7-115">This command lists all Databricks workspaces in a subscription.</span></span>

### <span data-ttu-id="a42f7-116">Exempel 3: lista alla Databricks-arbetsytor i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="a42f7-116">Example 3: List all Databricks workspaces in a resource group</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -ResourceGroupName testgroup

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="a42f7-117">Det här kommandot visar alla Databricks arbets ytor i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a42f7-117">This command lists all Databricks workspaces in a resource group.</span></span>

## <span data-ttu-id="a42f7-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a42f7-118">PARAMETERS</span></span>

### <span data-ttu-id="a42f7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a42f7-119">-DefaultProfile</span></span>
<span data-ttu-id="a42f7-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a42f7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a42f7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a42f7-121">-InputObject</span></span>
<span data-ttu-id="a42f7-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="a42f7-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a42f7-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="a42f7-123">-Name</span></span>
<span data-ttu-id="a42f7-124">Namnet på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="a42f7-124">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a42f7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a42f7-125">-ResourceGroupName</span></span>
<span data-ttu-id="a42f7-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a42f7-126">The name of the resource group.</span></span>
<span data-ttu-id="a42f7-127">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="a42f7-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a42f7-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a42f7-128">-SubscriptionId</span></span>
<span data-ttu-id="a42f7-129">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="a42f7-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a42f7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a42f7-130">CommonParameters</span></span>
<span data-ttu-id="a42f7-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a42f7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a42f7-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a42f7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a42f7-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a42f7-133">INPUTS</span></span>

### <span data-ttu-id="a42f7-134">Microsoft. Azure. PowerShell. cmdletar. Databricks. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="a42f7-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="a42f7-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a42f7-135">OUTPUTS</span></span>

### <span data-ttu-id="a42f7-136">Microsoft. Azure. PowerShell. cmdletar. Databricks. Models. Api20180401. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="a42f7-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="a42f7-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a42f7-137">NOTES</span></span>

<span data-ttu-id="a42f7-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a42f7-138">ALIASES</span></span>

<span data-ttu-id="a42f7-139">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="a42f7-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a42f7-140">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="a42f7-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a42f7-141">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a42f7-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a42f7-142">INPUTOBJECT <IDatabricksIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="a42f7-142">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a42f7-143">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="a42f7-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a42f7-144">`[PeeringName <String>]`: Namnet på arbets ytans vNet-peering.</span><span class="sxs-lookup"><span data-stu-id="a42f7-144">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="a42f7-145">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a42f7-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a42f7-146">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="a42f7-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="a42f7-147">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="a42f7-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a42f7-148">`[WorkspaceName <String>]`: Arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="a42f7-148">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="a42f7-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a42f7-149">RELATED LINKS</span></span>
