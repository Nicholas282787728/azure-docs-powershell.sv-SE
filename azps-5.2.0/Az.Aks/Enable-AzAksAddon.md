---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/enable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
ms.openlocfilehash: de4453129ee626ac7eeeaa20fa14c1068011c001
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399448"
---
# <span data-ttu-id="ce3b8-101">Enable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="ce3b8-101">Enable-AzAksAddOn</span></span>

## <span data-ttu-id="ce3b8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce3b8-102">SYNOPSIS</span></span>
<span data-ttu-id="ce3b8-103">Aktivera tillägg för AKS.</span><span class="sxs-lookup"><span data-stu-id="ce3b8-103">Enable the addons for aks.</span></span>

## <span data-ttu-id="ce3b8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce3b8-104">SYNTAX</span></span>

### <span data-ttu-id="ce3b8-105">defaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ce3b8-105">defaultParameterSet (Default)</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] [-ResourceGroupName] <String>
 [-ClusterName] <String> [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ce3b8-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce3b8-106">InputObjectParameterSet</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] -ClusterObject <PSKubernetesCluster>
 [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce3b8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce3b8-107">DESCRIPTION</span></span>
<span data-ttu-id="ce3b8-108">Aktivera tillägg för AKS.</span><span class="sxs-lookup"><span data-stu-id="ce3b8-108">Enable the addons for aks.</span></span>

## <span data-ttu-id="ce3b8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce3b8-109">EXAMPLES</span></span>

### <span data-ttu-id="ce3b8-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ce3b8-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Enable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard -WorkspaceResourceId xxxxx/xxxx -SubnetName subnet
```

<span data-ttu-id="ce3b8-111">Aktivera tilläggen `HttpApplicationRouting` , `Monitoring` , `AzurePolicy` `VirtualNode` och `KubeDashboard` för AKS.</span><span class="sxs-lookup"><span data-stu-id="ce3b8-111">Enable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="ce3b8-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce3b8-112">PARAMETERS</span></span>

### <span data-ttu-id="ce3b8-113">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="ce3b8-113">-ClusterName</span></span>
<span data-ttu-id="ce3b8-114">Kubernetes hanterat kluster namn.</span><span class="sxs-lookup"><span data-stu-id="ce3b8-114">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce3b8-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="ce3b8-115">-ClusterObject</span></span>
<span data-ttu-id="ce3b8-116">Ett PSKubernetesCluster-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="ce3b8-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce3b8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce3b8-117">-DefaultProfile</span></span>
<span data-ttu-id="ce3b8-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ce3b8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce3b8-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="ce3b8-119">-Name</span></span>
<span data-ttu-id="ce3b8-120">Kubernetes hanterat kluster namn.</span><span class="sxs-lookup"><span data-stu-id="ce3b8-120">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce3b8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce3b8-121">-ResourceGroupName</span></span>
<span data-ttu-id="ce3b8-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="ce3b8-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce3b8-123">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="ce3b8-123">-SubnetName</span></span>
<span data-ttu-id="ce3b8-124">Namn på VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="ce3b8-124">Subnet name of VirtualNode.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce3b8-125">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="ce3b8-125">-WorkspaceResourceId</span></span>
<span data-ttu-id="ce3b8-126">Resurs-ID för arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="ce3b8-126">Resource Id of the workspace of Monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce3b8-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ce3b8-127">-Confirm</span></span>
<span data-ttu-id="ce3b8-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ce3b8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce3b8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce3b8-129">-WhatIf</span></span>
<span data-ttu-id="ce3b8-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ce3b8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce3b8-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ce3b8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce3b8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce3b8-132">CommonParameters</span></span>
<span data-ttu-id="ce3b8-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce3b8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce3b8-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce3b8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce3b8-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce3b8-135">INPUTS</span></span>

### <span data-ttu-id="ce3b8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ce3b8-136">System.String</span></span>

### <span data-ttu-id="ce3b8-137">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="ce3b8-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="ce3b8-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce3b8-138">OUTPUTS</span></span>

### <span data-ttu-id="ce3b8-139">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="ce3b8-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="ce3b8-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce3b8-140">NOTES</span></span>

## <span data-ttu-id="ce3b8-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce3b8-141">RELATED LINKS</span></span>
