---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
ms.openlocfilehash: 7f2bb3f1d378afec5b0774aec2977b507654b931
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320228"
---
# <span data-ttu-id="d6a72-101">Get-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="d6a72-101">Get-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="d6a72-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6a72-102">SYNOPSIS</span></span>
<span data-ttu-id="d6a72-103">Hämtar arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="d6a72-103">Gets the workspace.</span></span>

## <span data-ttu-id="d6a72-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6a72-104">SYNTAX</span></span>

### <span data-ttu-id="d6a72-105">List1 (standard)</span><span class="sxs-lookup"><span data-stu-id="d6a72-105">List1 (Default)</span></span>
```
Get-AzDatabricksWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d6a72-106">Lära</span><span class="sxs-lookup"><span data-stu-id="d6a72-106">Get</span></span>
```
Get-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d6a72-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d6a72-107">GetViaIdentity</span></span>
```
Get-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d6a72-108">Förteckning</span><span class="sxs-lookup"><span data-stu-id="d6a72-108">List</span></span>
```
Get-AzDatabricksWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d6a72-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6a72-109">DESCRIPTION</span></span>
<span data-ttu-id="d6a72-110">Hämtar arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="d6a72-110">Gets the workspace.</span></span>

## <span data-ttu-id="d6a72-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6a72-111">EXAMPLES</span></span>

### <span data-ttu-id="d6a72-112">Exempel 1: skaffa en Databricks-arbetsyta med namn</span><span class="sxs-lookup"><span data-stu-id="d6a72-112">Example 1: Get a Databricks workspace with name</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="d6a72-113">Det här kommandot får en Databricks-arbetsyta i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d6a72-113">This command gets a Databricks workspace in a resource group.</span></span>

### <span data-ttu-id="d6a72-114">Exempel 2: lista alla Databricks-arbetsytor i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="d6a72-114">Example 2: List all Databricks workspaces in a subscription</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="d6a72-115">Det här kommandot visar alla Databricks arbets ytor i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="d6a72-115">This command lists all Databricks workspaces in a subscription.</span></span>

### <span data-ttu-id="d6a72-116">Exempel 3: lista alla Databricks-arbetsytor i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="d6a72-116">Example 3: List all Databricks workspaces in a resource group</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -ResourceGroupName testgroup

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="d6a72-117">Det här kommandot visar alla Databricks arbets ytor i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d6a72-117">This command lists all Databricks workspaces in a resource group.</span></span>

## <span data-ttu-id="d6a72-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6a72-118">PARAMETERS</span></span>

### <span data-ttu-id="d6a72-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6a72-119">-DefaultProfile</span></span>
<span data-ttu-id="d6a72-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d6a72-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6a72-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6a72-121">-InputObject</span></span>
<span data-ttu-id="d6a72-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="d6a72-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d6a72-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="d6a72-123">-Name</span></span>
<span data-ttu-id="d6a72-124">Namnet på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="d6a72-124">The name of the workspace.</span></span>

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

### <span data-ttu-id="d6a72-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6a72-125">-ResourceGroupName</span></span>
<span data-ttu-id="d6a72-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d6a72-126">The name of the resource group.</span></span>
<span data-ttu-id="d6a72-127">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="d6a72-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d6a72-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d6a72-128">-SubscriptionId</span></span>
<span data-ttu-id="d6a72-129">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="d6a72-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d6a72-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6a72-130">CommonParameters</span></span>
<span data-ttu-id="d6a72-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6a72-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6a72-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6a72-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6a72-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6a72-133">INPUTS</span></span>

### <span data-ttu-id="d6a72-134">Microsoft. Azure. PowerShell. cmdletar. Databricks. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="d6a72-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="d6a72-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6a72-135">OUTPUTS</span></span>

### <span data-ttu-id="d6a72-136">Microsoft. Azure. PowerShell. cmdletar. Databricks. Models. Api20180401. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="d6a72-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="d6a72-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6a72-137">NOTES</span></span>

<span data-ttu-id="d6a72-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d6a72-138">ALIASES</span></span>

<span data-ttu-id="d6a72-139">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="d6a72-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d6a72-140">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="d6a72-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d6a72-141">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d6a72-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d6a72-142">INPUTOBJECT <IDatabricksIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="d6a72-142">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d6a72-143">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="d6a72-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d6a72-144">`[PeeringName <String>]`: Namnet på arbets ytans vNet-peering.</span><span class="sxs-lookup"><span data-stu-id="d6a72-144">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="d6a72-145">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d6a72-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d6a72-146">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="d6a72-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="d6a72-147">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="d6a72-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d6a72-148">`[WorkspaceName <String>]`: Arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="d6a72-148">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="d6a72-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6a72-149">RELATED LINKS</span></span>
