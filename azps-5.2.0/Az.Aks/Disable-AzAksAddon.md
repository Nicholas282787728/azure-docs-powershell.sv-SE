---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/disable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
ms.openlocfilehash: 0fca409546822ef596897adbbf755a1a4ae43e38
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399451"
---
# <span data-ttu-id="5c067-101">Disable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="5c067-101">Disable-AzAksAddOn</span></span>

## <span data-ttu-id="5c067-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5c067-102">SYNOPSIS</span></span>
<span data-ttu-id="5c067-103">Inaktivera tillägg för AKS.</span><span class="sxs-lookup"><span data-stu-id="5c067-103">Disable the addons for aks.</span></span>

## <span data-ttu-id="5c067-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5c067-104">SYNTAX</span></span>

### <span data-ttu-id="5c067-105">defaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5c067-105">defaultParameterSet (Default)</span></span>
```
Disable-AzAksAddOn [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c067-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c067-106">InputObjectParameterSet</span></span>
```
Disable-AzAksAddOn -ClusterObject <PSKubernetesCluster> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c067-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5c067-107">DESCRIPTION</span></span>
<span data-ttu-id="5c067-108">Inaktivera tillägg för AKS.</span><span class="sxs-lookup"><span data-stu-id="5c067-108">Disable the addons for aks.</span></span>

## <span data-ttu-id="5c067-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5c067-109">EXAMPLES</span></span>

### <span data-ttu-id="5c067-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5c067-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Disable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard
```

<span data-ttu-id="5c067-111">Inaktivera tillägg `HttpApplicationRouting` , `Monitoring` , `AzurePolicy` `VirtualNode` och `KubeDashboard` för AKS.</span><span class="sxs-lookup"><span data-stu-id="5c067-111">Disable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="5c067-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5c067-112">PARAMETERS</span></span>

### <span data-ttu-id="5c067-113">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="5c067-113">-ClusterName</span></span>
<span data-ttu-id="5c067-114">Kubernetes hanterat kluster namn.</span><span class="sxs-lookup"><span data-stu-id="5c067-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="5c067-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="5c067-115">-ClusterObject</span></span>
<span data-ttu-id="5c067-116">Ett PSKubernetesCluster-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="5c067-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="5c067-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c067-117">-DefaultProfile</span></span>
<span data-ttu-id="5c067-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5c067-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c067-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="5c067-119">-Name</span></span>
<span data-ttu-id="5c067-120">Kubernetes hanterat kluster namn.</span><span class="sxs-lookup"><span data-stu-id="5c067-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="5c067-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c067-121">-ResourceGroupName</span></span>
<span data-ttu-id="5c067-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="5c067-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="5c067-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5c067-123">-Confirm</span></span>
<span data-ttu-id="5c067-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5c067-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c067-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c067-125">-WhatIf</span></span>
<span data-ttu-id="5c067-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5c067-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c067-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5c067-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c067-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c067-128">CommonParameters</span></span>
<span data-ttu-id="5c067-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c067-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c067-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c067-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c067-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5c067-131">INPUTS</span></span>

### <span data-ttu-id="5c067-132">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="5c067-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="5c067-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5c067-133">System.String</span></span>

## <span data-ttu-id="5c067-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5c067-134">OUTPUTS</span></span>

### <span data-ttu-id="5c067-135">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="5c067-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="5c067-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5c067-136">NOTES</span></span>

## <span data-ttu-id="5c067-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5c067-137">RELATED LINKS</span></span>
