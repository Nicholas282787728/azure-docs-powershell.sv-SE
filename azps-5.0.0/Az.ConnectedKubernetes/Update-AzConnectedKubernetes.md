---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/update-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
ms.openlocfilehash: 2913a4288bad6c1cb8c908d80b8c751a08483a8b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269980"
---
# <span data-ttu-id="5aa04-101">Update-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="5aa04-101">Update-AzConnectedKubernetes</span></span>

## <span data-ttu-id="5aa04-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5aa04-102">SYNOPSIS</span></span>
<span data-ttu-id="5aa04-103">API för att uppdatera vissa egenskaper för den anslutna kluster resursen</span><span class="sxs-lookup"><span data-stu-id="5aa04-103">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="5aa04-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5aa04-104">SYNTAX</span></span>

### <span data-ttu-id="5aa04-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="5aa04-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5aa04-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5aa04-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5aa04-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5aa04-107">DESCRIPTION</span></span>
<span data-ttu-id="5aa04-108">API för att uppdatera vissa egenskaper för den anslutna kluster resursen</span><span class="sxs-lookup"><span data-stu-id="5aa04-108">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="5aa04-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5aa04-109">EXAMPLES</span></span>

### <span data-ttu-id="5aa04-110">Exempel 1: uppdatera en ansluten Kubernetes</span><span class="sxs-lookup"><span data-stu-id="5aa04-110">Example 1: Update a connected kubernetes</span></span>
```powershell
PS C:\> Update-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t01 -Tag @{'key'='1'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="5aa04-111">Det här kommandot uppdaterar en ansluten Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="5aa04-111">This command updates a connected kubernetes.</span></span>

### <span data-ttu-id="5aa04-112">Exempel 2: uppdatera en ansluten Kubernetes efter objekt</span><span class="sxs-lookup"><span data-stu-id="5aa04-112">Example 2: Update a connected kubernetes by object</span></span>
```powershell
PS C:\> $conn = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t03
PS C:\> Update-AzConnectedKubernetes -InputObject $conn -Tag @{'key'='2'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t03 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="5aa04-113">Det här kommandot uppdaterar en ansluten Kubernetes efter objekt.</span><span class="sxs-lookup"><span data-stu-id="5aa04-113">This command updates a connected kubernetes by object.</span></span>

## <span data-ttu-id="5aa04-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5aa04-114">PARAMETERS</span></span>

### <span data-ttu-id="5aa04-115">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="5aa04-115">-ClusterName</span></span>
<span data-ttu-id="5aa04-116">Namnet på det Kubernetes-kluster där get anropas.</span><span class="sxs-lookup"><span data-stu-id="5aa04-116">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aa04-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aa04-117">-DefaultProfile</span></span>
<span data-ttu-id="5aa04-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5aa04-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5aa04-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5aa04-119">-InputObject</span></span>
<span data-ttu-id="5aa04-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="5aa04-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5aa04-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5aa04-121">-ResourceGroupName</span></span>
<span data-ttu-id="5aa04-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5aa04-122">The name of the resource group.</span></span>
<span data-ttu-id="5aa04-123">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="5aa04-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5aa04-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5aa04-124">-SubscriptionId</span></span>
<span data-ttu-id="5aa04-125">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="5aa04-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5aa04-126">-Tagg</span><span class="sxs-lookup"><span data-stu-id="5aa04-126">-Tag</span></span>
<span data-ttu-id="5aa04-127">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="5aa04-127">Resource tags.</span></span>

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

### <span data-ttu-id="5aa04-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5aa04-128">-Confirm</span></span>
<span data-ttu-id="5aa04-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5aa04-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5aa04-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5aa04-130">-WhatIf</span></span>
<span data-ttu-id="5aa04-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5aa04-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5aa04-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5aa04-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5aa04-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aa04-133">CommonParameters</span></span>
<span data-ttu-id="5aa04-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5aa04-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aa04-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5aa04-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aa04-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5aa04-136">INPUTS</span></span>

### <span data-ttu-id="5aa04-137">Microsoft. Azure. PowerShell. cmdletar. ConnectedKubernetes. Models. IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="5aa04-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="5aa04-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5aa04-138">OUTPUTS</span></span>

### <span data-ttu-id="5aa04-139">Microsoft. Azure. PowerShell. cmdletar. ConnectedKubernetes. Models. Api202001Preview. IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="5aa04-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="5aa04-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5aa04-140">NOTES</span></span>

<span data-ttu-id="5aa04-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5aa04-141">ALIASES</span></span>

<span data-ttu-id="5aa04-142">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="5aa04-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5aa04-143">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="5aa04-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5aa04-144">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5aa04-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5aa04-145">INPUTOBJECT <IConnectedKubernetesIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="5aa04-145">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5aa04-146">`[ClusterName <String>]`: Namnet på det Kubernetes-kluster där get anropas.</span><span class="sxs-lookup"><span data-stu-id="5aa04-146">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="5aa04-147">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="5aa04-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5aa04-148">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5aa04-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5aa04-149">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="5aa04-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="5aa04-150">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="5aa04-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="5aa04-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5aa04-151">RELATED LINKS</span></span>
