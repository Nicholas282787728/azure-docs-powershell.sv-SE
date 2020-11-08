---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 70ff3c636f6c88ac89e53a5c2b1acb209aad274a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273415"
---
# <span data-ttu-id="34cee-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="34cee-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="34cee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="34cee-102">SYNOPSIS</span></span>
<span data-ttu-id="34cee-103">Skapa en ny Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="34cee-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="34cee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="34cee-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="34cee-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="34cee-105">DESCRIPTION</span></span>
<span data-ttu-id="34cee-106">Skapa en ny Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="34cee-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="34cee-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="34cee-107">EXAMPLES</span></span>

### <span data-ttu-id="34cee-108">Exempel 1: skapa en configuation för Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="34cee-108">Example 1: Create a configuation for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -Name conf-test01 -ClusterName connaks-d983yc -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="34cee-109">Det här kommandot skapar en configuation för Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="34cee-109">This command creates a configuation for kubernetes cluster.</span></span>

## <span data-ttu-id="34cee-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="34cee-110">PARAMETERS</span></span>

### <span data-ttu-id="34cee-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="34cee-111">-ClusterName</span></span>
<span data-ttu-id="34cee-112">Namnet på Kubernetes-klustret.</span><span class="sxs-lookup"><span data-stu-id="34cee-112">The name of the kubernetes cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34cee-113">-ClusterScoped</span><span class="sxs-lookup"><span data-stu-id="34cee-113">-ClusterScoped</span></span>
<span data-ttu-id="34cee-114">Om du har angett en konfiguration för klustret (standard namn område).</span><span class="sxs-lookup"><span data-stu-id="34cee-114">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

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

### <span data-ttu-id="34cee-115">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="34cee-115">-ClusterType</span></span>
<span data-ttu-id="34cee-116">Kubernetes kluster resurs namn – antingen managedClusters (för AKS-kluster) eller connectedClusters (för lokal K8S-kluster).</span><span class="sxs-lookup"><span data-stu-id="34cee-116">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34cee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34cee-117">-DefaultProfile</span></span>
<span data-ttu-id="34cee-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="34cee-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34cee-119">-EnableHelmOperator</span><span class="sxs-lookup"><span data-stu-id="34cee-119">-EnableHelmOperator</span></span>
<span data-ttu-id="34cee-120">Alternativ för att aktivera Helm-operator för denna git-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="34cee-120">Option to enable Helm Operator for this git configuration.</span></span>

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

### <span data-ttu-id="34cee-121">-HelmOperatorChartValues</span><span class="sxs-lookup"><span data-stu-id="34cee-121">-HelmOperatorChartValues</span></span>
<span data-ttu-id="34cee-122">Värden åsidosätter för Helm-diagrammet.</span><span class="sxs-lookup"><span data-stu-id="34cee-122">Values override for the operator Helm chart.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34cee-123">-HelmOperatorChartVersion</span><span class="sxs-lookup"><span data-stu-id="34cee-123">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="34cee-124">Version av Helm-diagrammet.</span><span class="sxs-lookup"><span data-stu-id="34cee-124">Version of the operator Helm chart.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34cee-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="34cee-125">-Name</span></span>
<span data-ttu-id="34cee-126">Namn på käll kontroll konfiguration.</span><span class="sxs-lookup"><span data-stu-id="34cee-126">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34cee-127">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="34cee-127">-OperatorInstanceName</span></span>
<span data-ttu-id="34cee-128">Instans namn för operatören som identifierar den specifika konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="34cee-128">Instance name of the operator - identifying the specific configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34cee-129">-OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="34cee-129">-OperatorNamespace</span></span>
<span data-ttu-id="34cee-130">Namn området som den här operatorn är installerad till.</span><span class="sxs-lookup"><span data-stu-id="34cee-130">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="34cee-131">Högst 253 gemener alfanumeriska tecken, bindestreck och punkt.</span><span class="sxs-lookup"><span data-stu-id="34cee-131">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34cee-132">-OperatorParameters</span><span class="sxs-lookup"><span data-stu-id="34cee-132">-OperatorParameters</span></span>
<span data-ttu-id="34cee-133">Alla parametrar för Operator instansen i sträng format.</span><span class="sxs-lookup"><span data-stu-id="34cee-133">Any Parameters for the Operator instance in string format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34cee-134">-RepositoryUrl</span><span class="sxs-lookup"><span data-stu-id="34cee-134">-RepositoryUrl</span></span>
<span data-ttu-id="34cee-135">URL-adressen till SourceControl-databasen.</span><span class="sxs-lookup"><span data-stu-id="34cee-135">Url of the SourceControl Repository.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34cee-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34cee-136">-ResourceGroupName</span></span>
<span data-ttu-id="34cee-137">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="34cee-137">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34cee-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="34cee-138">-SubscriptionId</span></span>
<span data-ttu-id="34cee-139">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="34cee-139">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34cee-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="34cee-140">-Confirm</span></span>
<span data-ttu-id="34cee-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="34cee-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34cee-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34cee-142">-WhatIf</span></span>
<span data-ttu-id="34cee-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="34cee-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34cee-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="34cee-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34cee-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34cee-145">CommonParameters</span></span>
<span data-ttu-id="34cee-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34cee-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34cee-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34cee-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34cee-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="34cee-148">INPUTS</span></span>

## <span data-ttu-id="34cee-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="34cee-149">OUTPUTS</span></span>

### <span data-ttu-id="34cee-150">Microsoft. Azure. PowerShell. cmdletar. KubernetesConfiguration. Models. Api20191101Preview. ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="34cee-150">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="34cee-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="34cee-151">NOTES</span></span>

<span data-ttu-id="34cee-152">ALIAS</span><span class="sxs-lookup"><span data-stu-id="34cee-152">ALIASES</span></span>

## <span data-ttu-id="34cee-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="34cee-153">RELATED LINKS</span></span>

