---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/new-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
ms.openlocfilehash: 5ee758c305a960f6a06fb72290996bbec8037ed7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103007"
---
# <span data-ttu-id="6bb23-101">New-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="6bb23-101">New-AzConnectedKubernetes</span></span>

## <span data-ttu-id="6bb23-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6bb23-102">SYNOPSIS</span></span>
<span data-ttu-id="6bb23-103">API för att registrera ett nytt K8s-kluster och därmed skapa en spårad resurs i armar</span><span class="sxs-lookup"><span data-stu-id="6bb23-103">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="6bb23-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6bb23-104">SYNTAX</span></span>

```
New-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6bb23-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6bb23-105">DESCRIPTION</span></span>
<span data-ttu-id="6bb23-106">API för att registrera ett nytt K8s-kluster och därmed skapa en spårad resurs i armar</span><span class="sxs-lookup"><span data-stu-id="6bb23-106">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="6bb23-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6bb23-107">EXAMPLES</span></span>

### <span data-ttu-id="6bb23-108">Exempel 1: skapa en ansluten Kubernetes</span><span class="sxs-lookup"><span data-stu-id="6bb23-108">Example 1: Create a connected kubernetes</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t01 -ResourceGroupName connected-aks -Location 
Location Name         Type
-------- ----         ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="6bb23-109">Det här kommandot skapar en ansluten Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="6bb23-109">This command creates a connected kubernetes.</span></span>

### <span data-ttu-id="6bb23-110">Exempel 1: skapa en ansluten Kubernetes med parametrarna kubeConfig och kubeContext</span><span class="sxs-lookup"><span data-stu-id="6bb23-110">Example 1: Create a connected kubernetes with parameters kubeConfig and kubeContext</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t02 -ResourceGroupName connected-aks -Location eastus -KubeConfig $HOME\.kube\config -KubeContext portal-aks-t01

Location Name         Type
-------- ----         ----
eastus   ps-connaks-t02 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="6bb23-111">Det här kommandot skapar en ansluten Kubernetes med parametrarna kubeConfig och kubeContext.</span><span class="sxs-lookup"><span data-stu-id="6bb23-111">This command creates a connected kubernetes with parameters kubeConfig and kubeContext.</span></span>

## <span data-ttu-id="6bb23-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6bb23-112">PARAMETERS</span></span>

### <span data-ttu-id="6bb23-113">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="6bb23-113">-ClusterName</span></span>
<span data-ttu-id="6bb23-114">Namnet på det Kubernetes-kluster där get anropas.</span><span class="sxs-lookup"><span data-stu-id="6bb23-114">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb23-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bb23-115">-DefaultProfile</span></span>
<span data-ttu-id="6bb23-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6bb23-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bb23-117">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="6bb23-117">-KubeConfig</span></span>
<span data-ttu-id="6bb23-118">Sökvägen till Kube-konfigurations filen</span><span class="sxs-lookup"><span data-stu-id="6bb23-118">Path to the kube config file</span></span>

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

### <span data-ttu-id="6bb23-119">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="6bb23-119">-KubeContext</span></span>
<span data-ttu-id="6bb23-120">Kubconfig kontext från aktuell dator</span><span class="sxs-lookup"><span data-stu-id="6bb23-120">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="6bb23-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="6bb23-121">-Location</span></span>
<span data-ttu-id="6bb23-122">Kluster plats</span><span class="sxs-lookup"><span data-stu-id="6bb23-122">Location of the cluster</span></span>

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

### <span data-ttu-id="6bb23-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bb23-123">-ResourceGroupName</span></span>
<span data-ttu-id="6bb23-124">Namnet på resurs gruppen som Kubernetes-klustret är registrerat i.</span><span class="sxs-lookup"><span data-stu-id="6bb23-124">The name of the resource group to which the kubernetes cluster is registered.</span></span>

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

### <span data-ttu-id="6bb23-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6bb23-125">-SubscriptionId</span></span>
<span data-ttu-id="6bb23-126">ID för det abonnemang som Kubernetes-klustret är registrerat för.</span><span class="sxs-lookup"><span data-stu-id="6bb23-126">The ID of the subscription to which the kubernetes cluster is registered.</span></span>

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

### <span data-ttu-id="6bb23-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6bb23-127">-Confirm</span></span>
<span data-ttu-id="6bb23-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6bb23-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bb23-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bb23-129">-WhatIf</span></span>
<span data-ttu-id="6bb23-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6bb23-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bb23-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6bb23-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bb23-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bb23-132">CommonParameters</span></span>
<span data-ttu-id="6bb23-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bb23-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bb23-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6bb23-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bb23-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6bb23-135">INPUTS</span></span>

## <span data-ttu-id="6bb23-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6bb23-136">OUTPUTS</span></span>

### <span data-ttu-id="6bb23-137">Microsoft. Azure. PowerShell. cmdletar. ConnectedKubernetes. Models. Api202001Preview. IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="6bb23-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="6bb23-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6bb23-138">NOTES</span></span>

<span data-ttu-id="6bb23-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6bb23-139">ALIASES</span></span>

## <span data-ttu-id="6bb23-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6bb23-140">RELATED LINKS</span></span>

