---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/remove-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
ms.openlocfilehash: 2a9547b88129a199f97bbcff9281348f9d2c4659
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272264"
---
# <span data-ttu-id="3d942-101">Remove-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d942-101">Remove-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="3d942-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d942-102">SYNOPSIS</span></span>
<span data-ttu-id="3d942-103">Då raderas den YAML-fil som används för att konfigurera käll kontrolls konfigurationen och därför stoppas synkronisering från käll repo.</span><span class="sxs-lookup"><span data-stu-id="3d942-103">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="3d942-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d942-104">SYNTAX</span></span>

### <span data-ttu-id="3d942-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="3d942-105">Delete (Default)</span></span>
```
Remove-AzKubernetesConfiguration -ClusterName <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3d942-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3d942-106">DeleteViaIdentity</span></span>
```
Remove-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3d942-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d942-107">DESCRIPTION</span></span>
<span data-ttu-id="3d942-108">Då raderas den YAML-fil som används för att konfigurera käll kontrolls konfigurationen och därför stoppas synkronisering från käll repo.</span><span class="sxs-lookup"><span data-stu-id="3d942-108">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="3d942-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d942-109">EXAMPLES</span></span>

### <span data-ttu-id="3d942-110">Exempel 1: ta bort en configuation för Kubernetes-kluster efter namn</span><span class="sxs-lookup"><span data-stu-id="3d942-110">Example 1: Remove a configuation of kubernetes cluster by name</span></span>
```powershell
PS C:\> Remove-AzKubernetesConfiguration -ClusterName connaks-d983yc -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test01

```

<span data-ttu-id="3d942-111">Det här kommandot tar bort en configuation för Kubernetes-kluster efter namn.</span><span class="sxs-lookup"><span data-stu-id="3d942-111">This command removes a configuation of kubernetes cluster by name.</span></span>

### <span data-ttu-id="3d942-112">Exempel 2: ta bort en configuation för Kubernetes-kluster efter objekt</span><span class="sxs-lookup"><span data-stu-id="3d942-112">Example 2: Remove a configuation of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = Get-AzKubernetesConfiguration -ClusterName connaks-dkc29c -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test02 -ClusterRp Microsoft.Kubernetes
PS C:\> Remove-AzKubernetesConfiguration -InputObject $kubConf

```

<span data-ttu-id="3d942-113">Det här kommandot tar bort en configuation för Kubernetes-kluster efter objekt.</span><span class="sxs-lookup"><span data-stu-id="3d942-113">This command removes a configuation of kubernetes cluster by object.</span></span>

## <span data-ttu-id="3d942-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d942-114">PARAMETERS</span></span>

### <span data-ttu-id="3d942-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d942-115">-AsJob</span></span>
<span data-ttu-id="3d942-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="3d942-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3d942-117">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="3d942-117">-ClusterName</span></span>
<span data-ttu-id="3d942-118">Namnet på Kubernetes-klustret.</span><span class="sxs-lookup"><span data-stu-id="3d942-118">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="3d942-119">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="3d942-119">-ClusterType</span></span>
<span data-ttu-id="3d942-120">Kubernetes kluster resurs namn – antingen managedClusters (för AKS-kluster) eller connectedClusters (för lokal K8S-kluster).</span><span class="sxs-lookup"><span data-stu-id="3d942-120">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="3d942-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d942-121">-DefaultProfile</span></span>
<span data-ttu-id="3d942-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3d942-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d942-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d942-123">-InputObject</span></span>
<span data-ttu-id="3d942-124">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="3d942-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d942-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="3d942-125">-Name</span></span>
<span data-ttu-id="3d942-126">Namn på käll kontroll konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3d942-126">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d942-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="3d942-127">-NoWait</span></span>
<span data-ttu-id="3d942-128">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="3d942-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3d942-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d942-129">-PassThru</span></span>
<span data-ttu-id="3d942-130">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="3d942-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3d942-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d942-131">-ResourceGroupName</span></span>
<span data-ttu-id="3d942-132">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3d942-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="3d942-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3d942-133">-SubscriptionId</span></span>
<span data-ttu-id="3d942-134">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="3d942-134">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="3d942-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3d942-135">-Confirm</span></span>
<span data-ttu-id="3d942-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3d942-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d942-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d942-137">-WhatIf</span></span>
<span data-ttu-id="3d942-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3d942-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d942-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3d942-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d942-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d942-140">CommonParameters</span></span>
<span data-ttu-id="3d942-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d942-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d942-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d942-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d942-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d942-143">INPUTS</span></span>

### <span data-ttu-id="3d942-144">Microsoft. Azure. PowerShell. cmdletar. KubernetesConfiguration. Models. IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="3d942-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="3d942-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d942-145">OUTPUTS</span></span>

### <span data-ttu-id="3d942-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3d942-146">System.Boolean</span></span>

## <span data-ttu-id="3d942-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d942-147">NOTES</span></span>

<span data-ttu-id="3d942-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3d942-148">ALIASES</span></span>

<span data-ttu-id="3d942-149">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="3d942-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3d942-150">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="3d942-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3d942-151">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3d942-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3d942-152">INPUTOBJECT <IKubernetesConfigurationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="3d942-152">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3d942-153">`[ClusterName <String>]`: Namnet på Kubernetes-klustret.</span><span class="sxs-lookup"><span data-stu-id="3d942-153">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="3d942-154">`[ClusterResourceName <String>]`: Namnet på Kubernetes-kluster-antingen managedClusters (för AKS-kluster) eller connectedClusters (för lokal K8S-kluster).</span><span class="sxs-lookup"><span data-stu-id="3d942-154">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="3d942-155">`[ClusterRp <String>]`: Kubernetes-klustret RP-antingen Microsoft. ContainerService (för AKS-kluster) eller Microsoft. Kubernetes (för lokal K8S-kluster).</span><span class="sxs-lookup"><span data-stu-id="3d942-155">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="3d942-156">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="3d942-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3d942-157">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3d942-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="3d942-158">`[SourceControlConfigurationName <String>]`: Käll kontroll konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="3d942-158">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="3d942-159">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="3d942-159">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="3d942-160">Det här är en GUID-formaterad sträng (till exempel 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="3d942-160">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="3d942-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d942-161">RELATED LINKS</span></span>

