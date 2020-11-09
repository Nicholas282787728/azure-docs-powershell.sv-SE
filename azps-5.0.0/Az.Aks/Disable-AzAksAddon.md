---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/disable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
ms.openlocfilehash: 0fca409546822ef596897adbbf755a1a4ae43e38
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94326064"
---
# <span data-ttu-id="2427a-101">Disable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="2427a-101">Disable-AzAksAddOn</span></span>

## <span data-ttu-id="2427a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2427a-102">SYNOPSIS</span></span>
<span data-ttu-id="2427a-103">Inaktivera tillägg för AKS.</span><span class="sxs-lookup"><span data-stu-id="2427a-103">Disable the addons for aks.</span></span>

## <span data-ttu-id="2427a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2427a-104">SYNTAX</span></span>

### <span data-ttu-id="2427a-105">defaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2427a-105">defaultParameterSet (Default)</span></span>
```
Disable-AzAksAddOn [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2427a-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2427a-106">InputObjectParameterSet</span></span>
```
Disable-AzAksAddOn -ClusterObject <PSKubernetesCluster> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2427a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2427a-107">DESCRIPTION</span></span>
<span data-ttu-id="2427a-108">Inaktivera tillägg för AKS.</span><span class="sxs-lookup"><span data-stu-id="2427a-108">Disable the addons for aks.</span></span>

## <span data-ttu-id="2427a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2427a-109">EXAMPLES</span></span>

### <span data-ttu-id="2427a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2427a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Disable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard
```

<span data-ttu-id="2427a-111">Inaktivera tillägg `HttpApplicationRouting` , `Monitoring` , `AzurePolicy` `VirtualNode` och `KubeDashboard` för AKS.</span><span class="sxs-lookup"><span data-stu-id="2427a-111">Disable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="2427a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2427a-112">PARAMETERS</span></span>

### <span data-ttu-id="2427a-113">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="2427a-113">-ClusterName</span></span>
<span data-ttu-id="2427a-114">Kubernetes hanterat kluster namn.</span><span class="sxs-lookup"><span data-stu-id="2427a-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="2427a-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="2427a-115">-ClusterObject</span></span>
<span data-ttu-id="2427a-116">Ett PSKubernetesCluster-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="2427a-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="2427a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2427a-117">-DefaultProfile</span></span>
<span data-ttu-id="2427a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2427a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2427a-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="2427a-119">-Name</span></span>
<span data-ttu-id="2427a-120">Kubernetes hanterat kluster namn.</span><span class="sxs-lookup"><span data-stu-id="2427a-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="2427a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2427a-121">-ResourceGroupName</span></span>
<span data-ttu-id="2427a-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="2427a-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="2427a-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2427a-123">-Confirm</span></span>
<span data-ttu-id="2427a-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2427a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2427a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2427a-125">-WhatIf</span></span>
<span data-ttu-id="2427a-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2427a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2427a-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2427a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2427a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2427a-128">CommonParameters</span></span>
<span data-ttu-id="2427a-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2427a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2427a-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2427a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2427a-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2427a-131">INPUTS</span></span>

### <span data-ttu-id="2427a-132">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="2427a-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="2427a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2427a-133">System.String</span></span>

## <span data-ttu-id="2427a-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2427a-134">OUTPUTS</span></span>

### <span data-ttu-id="2427a-135">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="2427a-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="2427a-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2427a-136">NOTES</span></span>

## <span data-ttu-id="2427a-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2427a-137">RELATED LINKS</span></span>
