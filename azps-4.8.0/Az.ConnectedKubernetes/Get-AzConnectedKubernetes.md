---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/get-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
ms.openlocfilehash: 1df844fc9a040fe20b6fdcdaa6f5dccda191aba4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261122"
---
# <span data-ttu-id="f8251-101">Get-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="f8251-101">Get-AzConnectedKubernetes</span></span>

## <span data-ttu-id="f8251-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f8251-102">SYNOPSIS</span></span>
<span data-ttu-id="f8251-103">Returnerar egenskaperna för det angivna anslutna klustret, inklusive namn, identitet, egenskaper och ytterligare kluster information.</span><span class="sxs-lookup"><span data-stu-id="f8251-103">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="f8251-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f8251-104">SYNTAX</span></span>

### <span data-ttu-id="f8251-105">List1 (standard)</span><span class="sxs-lookup"><span data-stu-id="f8251-105">List1 (Default)</span></span>
```
Get-AzConnectedKubernetes [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f8251-106">Lära</span><span class="sxs-lookup"><span data-stu-id="f8251-106">Get</span></span>
```
Get-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f8251-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f8251-107">GetViaIdentity</span></span>
```
Get-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8251-108">Förteckning</span><span class="sxs-lookup"><span data-stu-id="f8251-108">List</span></span>
```
Get-AzConnectedKubernetes -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f8251-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f8251-109">DESCRIPTION</span></span>
<span data-ttu-id="f8251-110">Returnerar egenskaperna för det angivna anslutna klustret, inklusive namn, identitet, egenskaper och ytterligare kluster information.</span><span class="sxs-lookup"><span data-stu-id="f8251-110">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="f8251-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f8251-111">EXAMPLES</span></span>

### <span data-ttu-id="f8251-112">Exempel 1: Hämta alla anslutna Kubernetes under ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="f8251-112">Example 1: Get all connected kubernetes under a subscription</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes

Location Name              Type
-------- ----              ----
eastus   connected-aks       Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks  Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks1 Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks3 Microsoft.Kubernetes/connectedClusters
eastus   connected-aks-cli1  Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="f8251-113">Det här kommandot får alla anslutna Kubernetes under ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="f8251-113">This command gets all connected kubernetes under a subscription.</span></span>

### <span data-ttu-id="f8251-114">Exempel 2: Hämta alla anslutna Kubernetes under resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="f8251-114">Example 2: Get all connected kubernetes under the resource group</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks

Location Name              Type
-------- ----              ----
eastus   connected-aks       Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks  Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks1 Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks3 Microsoft.Kubernetes/connectedClusters
eastus   connected-aks-cli1  Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="f8251-115">Det här kommandot får alla anslutna Kubernetes under resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f8251-115">This command gets all connected kubernetes under the resource group.</span></span>

### <span data-ttu-id="f8251-116">Exempel 3: skaffa en ansluten Kubernetes</span><span class="sxs-lookup"><span data-stu-id="f8251-116">Example 3: Get a connected kubernetes</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="f8251-117">Det här kommandot får en ansluten Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="f8251-117">This command gets a connected kubernetes.</span></span>

### <span data-ttu-id="f8251-118">Exempel 4: skaffa en ansluten Kubernetes efter objekt</span><span class="sxs-lookup"><span data-stu-id="f8251-118">Example 4: Get a connected kubernetes by object</span></span>
```powershell
PS C:\> $conAks = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks
PS C:\> Get-AzConnectedKubernetes -InputObject $conAks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="f8251-119">Det här kommandot får ett anslutet Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="f8251-119">This command gets a connected kubernetes by object.</span></span>

## <span data-ttu-id="f8251-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f8251-120">PARAMETERS</span></span>

### <span data-ttu-id="f8251-121">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="f8251-121">-ClusterName</span></span>
<span data-ttu-id="f8251-122">Namnet på det Kubernetes-kluster där get anropas.</span><span class="sxs-lookup"><span data-stu-id="f8251-122">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8251-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8251-123">-DefaultProfile</span></span>
<span data-ttu-id="f8251-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f8251-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8251-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8251-125">-InputObject</span></span>
<span data-ttu-id="f8251-126">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f8251-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8251-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8251-127">-ResourceGroupName</span></span>
<span data-ttu-id="f8251-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f8251-128">The name of the resource group.</span></span>
<span data-ttu-id="f8251-129">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="f8251-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f8251-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f8251-130">-SubscriptionId</span></span>
<span data-ttu-id="f8251-131">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f8251-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f8251-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8251-132">CommonParameters</span></span>
<span data-ttu-id="f8251-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8251-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8251-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8251-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8251-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f8251-135">INPUTS</span></span>

### <span data-ttu-id="f8251-136">Microsoft. Azure. PowerShell. cmdletar. ConnectedKubernetes. Models. IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="f8251-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="f8251-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f8251-137">OUTPUTS</span></span>

### <span data-ttu-id="f8251-138">Microsoft. Azure. PowerShell. cmdletar. ConnectedKubernetes. Models. Api202001Preview. IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="f8251-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="f8251-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f8251-139">NOTES</span></span>

<span data-ttu-id="f8251-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f8251-140">ALIASES</span></span>

<span data-ttu-id="f8251-141">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="f8251-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f8251-142">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="f8251-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f8251-143">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f8251-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f8251-144">INPUTOBJECT <IConnectedKubernetesIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="f8251-144">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f8251-145">`[ClusterName <String>]`: Namnet på det Kubernetes-kluster där get anropas.</span><span class="sxs-lookup"><span data-stu-id="f8251-145">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="f8251-146">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="f8251-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f8251-147">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f8251-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f8251-148">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="f8251-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="f8251-149">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="f8251-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="f8251-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f8251-150">RELATED LINKS</span></span>

