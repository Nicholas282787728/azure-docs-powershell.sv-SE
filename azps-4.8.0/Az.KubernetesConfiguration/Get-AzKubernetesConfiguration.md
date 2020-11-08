---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/get-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
ms.openlocfilehash: 3fd93e42b8f38659f61fcbeb0f49040409f635a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259594"
---
# <span data-ttu-id="8a50d-101">Get-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="8a50d-101">Get-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="8a50d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a50d-102">SYNOPSIS</span></span>
<span data-ttu-id="8a50d-103">Hämtar information om käll kontroll konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="8a50d-103">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="8a50d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a50d-104">SYNTAX</span></span>

### <span data-ttu-id="8a50d-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="8a50d-105">List (Default)</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8a50d-106">Lära</span><span class="sxs-lookup"><span data-stu-id="8a50d-106">Get</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8a50d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8a50d-107">GetViaIdentity</span></span>
```
Get-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a50d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a50d-108">DESCRIPTION</span></span>
<span data-ttu-id="8a50d-109">Hämtar information om käll kontroll konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="8a50d-109">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="8a50d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a50d-110">EXAMPLES</span></span>

### <span data-ttu-id="8a50d-111">Exempel 1: Hämta alla konfigurationer för Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="8a50d-111">Example 1: Get all configurations of kubernetes cluster</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="8a50d-112">Det här kommandot får alla konfigurationer för Kubernetes-klustret.</span><span class="sxs-lookup"><span data-stu-id="8a50d-112">This command gets all configurations of kubernetes cluster.</span></span>

### <span data-ttu-id="8a50d-113">Exempel 2: få en konfiguration av Kubernetes kluster utifrån namn</span><span class="sxs-lookup"><span data-stu-id="8a50d-113">Example 2: Get a configuration of kubernetes cluster by name</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters -Name conf-t02

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="8a50d-114">Det här kommandot får en konfiguration av Kubernetes kluster efter namn.</span><span class="sxs-lookup"><span data-stu-id="8a50d-114">This command gets a configuration of kubernetes cluster by name.</span></span>

### <span data-ttu-id="8a50d-115">Exempel 3: Hämta en konfiguration av Kubernetes-kluster efter objekt</span><span class="sxs-lookup"><span data-stu-id="8a50d-115">Example 3: Get a configuration of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = New-AzKubernetesConfiguration -Name conf-test02 -ClusterName connaks-dkc29c -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx
PS C:\> Get-AzKubernetesConfiguration -InputObject $kubConf

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="8a50d-116">Det här kommandot får en konfiguration av Kubernetes-kluster efter objekt.</span><span class="sxs-lookup"><span data-stu-id="8a50d-116">This command gets a configuration of kubernetes cluster by object.</span></span>

### <span data-ttu-id="8a50d-117">Exempel 4: få en konfiguration av Kubernetes kluster via pipeline</span><span class="sxs-lookup"><span data-stu-id="8a50d-117">Example 4: Get a configuration of kubernetes cluster by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/connaks-rg-w9vlnp/providers/Microsoft.Kubernetes/connectedClusters/connaks-d983yc/providers/Microsoft.KubernetesConfiguration/sourceControlConfigurations/conf-test01'} | Get-AzKubernetesConfiguration

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="8a50d-118">Det här kommandot får en konfiguration av Kubernetes kluster via pipeline.</span><span class="sxs-lookup"><span data-stu-id="8a50d-118">This command gets a configuration of kubernetes cluster by pipeline.</span></span>

## <span data-ttu-id="8a50d-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a50d-119">PARAMETERS</span></span>

### <span data-ttu-id="8a50d-120">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="8a50d-120">-ClusterName</span></span>
<span data-ttu-id="8a50d-121">Namnet på Kubernetes-klustret.</span><span class="sxs-lookup"><span data-stu-id="8a50d-121">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="8a50d-122">-ClusterRp</span><span class="sxs-lookup"><span data-stu-id="8a50d-122">-ClusterRp</span></span>
<span data-ttu-id="8a50d-123">Kubernetes-klustret RP-antingen Microsoft. ContainerService (för AKS-kluster) eller Microsoft. Kubernetes (för lokal K8S-kluster).</span><span class="sxs-lookup"><span data-stu-id="8a50d-123">The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="8a50d-124">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="8a50d-124">-ClusterType</span></span>
<span data-ttu-id="8a50d-125">Kubernetes kluster resurs namn – antingen managedClusters (för AKS-kluster) eller connectedClusters (för lokal K8S-kluster).</span><span class="sxs-lookup"><span data-stu-id="8a50d-125">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="8a50d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a50d-126">-DefaultProfile</span></span>
<span data-ttu-id="8a50d-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8a50d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a50d-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a50d-128">-InputObject</span></span>
<span data-ttu-id="8a50d-129">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="8a50d-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a50d-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="8a50d-130">-Name</span></span>
<span data-ttu-id="8a50d-131">Namn på käll kontroll konfiguration.</span><span class="sxs-lookup"><span data-stu-id="8a50d-131">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a50d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a50d-132">-ResourceGroupName</span></span>
<span data-ttu-id="8a50d-133">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8a50d-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="8a50d-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a50d-134">-SubscriptionId</span></span>
<span data-ttu-id="8a50d-135">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="8a50d-135">The Azure subscription ID.</span></span>
<span data-ttu-id="8a50d-136">Det här är en GUID-formaterad sträng (till exempel 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="8a50d-136">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="8a50d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a50d-137">CommonParameters</span></span>
<span data-ttu-id="8a50d-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a50d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a50d-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a50d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a50d-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a50d-140">INPUTS</span></span>

### <span data-ttu-id="8a50d-141">Microsoft. Azure. PowerShell. cmdletar. KubernetesConfiguration. Models. IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="8a50d-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="8a50d-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a50d-142">OUTPUTS</span></span>

### <span data-ttu-id="8a50d-143">Microsoft. Azure. PowerShell. cmdletar. KubernetesConfiguration. Models. Api20191101Preview. ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="8a50d-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="8a50d-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a50d-144">NOTES</span></span>

<span data-ttu-id="8a50d-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8a50d-145">ALIASES</span></span>

<span data-ttu-id="8a50d-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="8a50d-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8a50d-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="8a50d-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8a50d-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8a50d-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8a50d-149">INPUTOBJECT <IKubernetesConfigurationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="8a50d-149">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8a50d-150">`[ClusterName <String>]`: Namnet på Kubernetes-klustret.</span><span class="sxs-lookup"><span data-stu-id="8a50d-150">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="8a50d-151">`[ClusterResourceName <String>]`: Namnet på Kubernetes-kluster-antingen managedClusters (för AKS-kluster) eller connectedClusters (för lokal K8S-kluster).</span><span class="sxs-lookup"><span data-stu-id="8a50d-151">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="8a50d-152">`[ClusterRp <String>]`: Kubernetes-klustret RP-antingen Microsoft. ContainerService (för AKS-kluster) eller Microsoft. Kubernetes (för lokal K8S-kluster).</span><span class="sxs-lookup"><span data-stu-id="8a50d-152">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="8a50d-153">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="8a50d-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8a50d-154">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8a50d-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="8a50d-155">`[SourceControlConfigurationName <String>]`: Käll kontroll konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="8a50d-155">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="8a50d-156">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="8a50d-156">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="8a50d-157">Det här är en GUID-formaterad sträng (till exempel 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="8a50d-157">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="8a50d-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a50d-158">RELATED LINKS</span></span>

