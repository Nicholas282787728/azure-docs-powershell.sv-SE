---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
ms.openlocfilehash: d5078ac91627cdf9f7b57801e3b7a958b9bd776e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404715"
---
# <span data-ttu-id="f656d-101">Get-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="f656d-101">Get-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="f656d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f656d-102">SYNOPSIS</span></span>
<span data-ttu-id="f656d-103">Hämtar arbets ytans vNet-peering.</span><span class="sxs-lookup"><span data-stu-id="f656d-103">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="f656d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f656d-104">SYNTAX</span></span>

### <span data-ttu-id="f656d-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="f656d-105">List (Default)</span></span>
```
Get-AzDatabricksVNetPeering -ResourceGroupName <String> -WorkspaceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f656d-106">Lära</span><span class="sxs-lookup"><span data-stu-id="f656d-106">Get</span></span>
```
Get-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="f656d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f656d-107">GetViaIdentity</span></span>
```
Get-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="f656d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f656d-108">DESCRIPTION</span></span>
<span data-ttu-id="f656d-109">Hämtar arbets ytans vNet-peering.</span><span class="sxs-lookup"><span data-stu-id="f656d-109">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="f656d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f656d-110">EXAMPLES</span></span>

### <span data-ttu-id="f656d-111">Exempel 1: lista alla VNet-peering under en databricks</span><span class="sxs-lookup"><span data-stu-id="f656d-111">Example 1: List all vnet peering under a databricks</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test

Name            Type
----            ----
vnetpeering-t01
vnetpeering-t02
```

<span data-ttu-id="f656d-112">Det här kommandot listar all VNet-peering under en databricks.</span><span class="sxs-lookup"><span data-stu-id="f656d-112">This command lists all vnet peering under a databricks.</span></span>

### <span data-ttu-id="f656d-113">Exempel 2: skaffa en VNet-peering</span><span class="sxs-lookup"><span data-stu-id="f656d-113">Example 2: Get a vnet peering</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01

Name             Type
----             ----
MyPeering-test01
```

<span data-ttu-id="f656d-114">Det här kommandot får en VNet-peering.</span><span class="sxs-lookup"><span data-stu-id="f656d-114">This command gets a vnet peering.</span></span>

### <span data-ttu-id="f656d-115">Exempel 3: Hämta ett virtuellt nätverk med objekt</span><span class="sxs-lookup"><span data-stu-id="f656d-115">Example 3: Get a vnet peering by object</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t02 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxx-xxxx-xxx-xxxxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test02' | Get-AzDatabricksVNetPeering

Name            Type
----            ----
vnetpeering-t02
```

<span data-ttu-id="f656d-116">Det här kommandot får en VNet-peering med objekt.</span><span class="sxs-lookup"><span data-stu-id="f656d-116">This command gets a vnet peering by object.</span></span>

## <span data-ttu-id="f656d-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f656d-117">PARAMETERS</span></span>

### <span data-ttu-id="f656d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f656d-118">-DefaultProfile</span></span>
<span data-ttu-id="f656d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f656d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f656d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f656d-120">-InputObject</span></span>
<span data-ttu-id="f656d-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f656d-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f656d-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="f656d-122">-Name</span></span>
<span data-ttu-id="f656d-123">Namnet på arbets ytans vNet-peering.</span><span class="sxs-lookup"><span data-stu-id="f656d-123">The name of the workspace vNet peering.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f656d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f656d-124">-PassThru</span></span>
<span data-ttu-id="f656d-125">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="f656d-125">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f656d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f656d-126">-ResourceGroupName</span></span>
<span data-ttu-id="f656d-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f656d-127">The name of the resource group.</span></span>
<span data-ttu-id="f656d-128">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="f656d-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f656d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f656d-129">-SubscriptionId</span></span>
<span data-ttu-id="f656d-130">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f656d-130">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f656d-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f656d-131">-WorkspaceName</span></span>
<span data-ttu-id="f656d-132">Namnet på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="f656d-132">The name of the workspace.</span></span>

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

### <span data-ttu-id="f656d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f656d-133">CommonParameters</span></span>
<span data-ttu-id="f656d-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f656d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f656d-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f656d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f656d-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f656d-136">INPUTS</span></span>

### <span data-ttu-id="f656d-137">Microsoft. Azure. PowerShell. cmdletar. Databricks. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="f656d-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="f656d-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f656d-138">OUTPUTS</span></span>

### <span data-ttu-id="f656d-139">Microsoft. Azure. PowerShell. cmdletar. Databricks. Models. Api20180401. IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f656d-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="f656d-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f656d-140">NOTES</span></span>

<span data-ttu-id="f656d-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f656d-141">ALIASES</span></span>

<span data-ttu-id="f656d-142">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="f656d-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f656d-143">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="f656d-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f656d-144">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f656d-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f656d-145">INPUTOBJECT <IDatabricksIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="f656d-145">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f656d-146">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="f656d-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f656d-147">`[PeeringName <String>]`: Namnet på arbets ytans vNet-peering.</span><span class="sxs-lookup"><span data-stu-id="f656d-147">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="f656d-148">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f656d-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f656d-149">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="f656d-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="f656d-150">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="f656d-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f656d-151">`[WorkspaceName <String>]`: Arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="f656d-151">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="f656d-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f656d-152">RELATED LINKS</span></span>

