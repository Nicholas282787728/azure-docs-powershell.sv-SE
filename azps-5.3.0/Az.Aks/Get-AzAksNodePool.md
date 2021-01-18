---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
ms.openlocfilehash: 5c690b377d658e3ebc4eddaf49d546efd503a01c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523329"
---
# <span data-ttu-id="684f3-101">Get-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="684f3-101">Get-AzAksNodePool</span></span>

## <span data-ttu-id="684f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="684f3-102">SYNOPSIS</span></span>
<span data-ttu-id="684f3-103">Skapa en antecknings pool i ett angivet kluster.</span><span class="sxs-lookup"><span data-stu-id="684f3-103">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="684f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="684f3-104">SYNTAX</span></span>

### <span data-ttu-id="684f3-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="684f3-105">NameParameterSet (Default)</span></span>
```
Get-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="684f3-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="684f3-106">IdParameterSet</span></span>
```
Get-AzAksNodePool -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="684f3-107">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="684f3-107">ParentObjectParameterSet</span></span>
```
Get-AzAksNodePool -ClusterObject <PSKubernetesCluster> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="684f3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="684f3-108">DESCRIPTION</span></span>
<span data-ttu-id="684f3-109">Skapa en antecknings pool i ett angivet kluster.</span><span class="sxs-lookup"><span data-stu-id="684f3-109">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="684f3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="684f3-110">EXAMPLES</span></span>

### <span data-ttu-id="684f3-111">Hämta alla nodtyper i ett angivet kluster</span><span class="sxs-lookup"><span data-stu-id="684f3-111">Get all node pools within specified cluster</span></span>
```powershell
PS C:\> Get-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster
```

## <span data-ttu-id="684f3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="684f3-112">PARAMETERS</span></span>

### <span data-ttu-id="684f3-113">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="684f3-113">-ClusterName</span></span>
<span data-ttu-id="684f3-114">Namnet på den hanterade kluster resursen.</span><span class="sxs-lookup"><span data-stu-id="684f3-114">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="684f3-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="684f3-115">-ClusterObject</span></span>
<span data-ttu-id="684f3-116">Cluster-objekt.</span><span class="sxs-lookup"><span data-stu-id="684f3-116">The cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="684f3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="684f3-117">-DefaultProfile</span></span>
<span data-ttu-id="684f3-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="684f3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="684f3-119">-ID</span><span class="sxs-lookup"><span data-stu-id="684f3-119">-Id</span></span>
<span data-ttu-id="684f3-120">ID för en noduppsättning i hanterat Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="684f3-120">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="684f3-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="684f3-121">-Name</span></span>
<span data-ttu-id="684f3-122">Namnet på Node-poolen.</span><span class="sxs-lookup"><span data-stu-id="684f3-122">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="684f3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="684f3-123">-ResourceGroupName</span></span>
<span data-ttu-id="684f3-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="684f3-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="684f3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="684f3-125">CommonParameters</span></span>
<span data-ttu-id="684f3-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="684f3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="684f3-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="684f3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="684f3-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="684f3-128">INPUTS</span></span>

### <span data-ttu-id="684f3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="684f3-129">System.String</span></span>

## <span data-ttu-id="684f3-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="684f3-130">OUTPUTS</span></span>

### <span data-ttu-id="684f3-131">Microsoft. Azure. commands. AKS. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="684f3-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="684f3-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="684f3-132">NOTES</span></span>

## <span data-ttu-id="684f3-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="684f3-133">RELATED LINKS</span></span>
