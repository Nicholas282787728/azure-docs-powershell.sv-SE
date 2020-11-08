---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 5a03df969421ea87d907efb5fe23027acfde0834
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088939"
---
# <span data-ttu-id="a9790-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="a9790-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="a9790-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a9790-102">SYNOPSIS</span></span>
<span data-ttu-id="a9790-103">Skapa en Kubectl SSH-tunnel till instrument panelen för hanterade kluster.</span><span class="sxs-lookup"><span data-stu-id="a9790-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="a9790-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a9790-104">SYNTAX</span></span>

### <span data-ttu-id="a9790-105">GroupNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a9790-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9790-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9790-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9790-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9790-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9790-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a9790-108">DESCRIPTION</span></span>
<span data-ttu-id="a9790-109">Skapa en Kubectl SSH-tunnel till instrument panelen för hanterade kluster.</span><span class="sxs-lookup"><span data-stu-id="a9790-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="a9790-110">SSH-tunneln installeras i ett PowerShell-jobb som heter Kubectl-Tunnel och kan hittas genom att köra `Get-Job` .</span><span class="sxs-lookup"><span data-stu-id="a9790-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="a9790-111">Tunneln ska vara tillgänglig via [http://127.0.0.1:8001](http://127.0.0.1:8001) .</span><span class="sxs-lookup"><span data-stu-id="a9790-111">The tunnel should be accessible via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="a9790-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a9790-112">EXAMPLES</span></span>

### <span data-ttu-id="a9790-113">Starta en SSH-tunnel och öppna en webbläsare på Kubernetes instrument panel</span><span class="sxs-lookup"><span data-stu-id="a9790-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="a9790-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a9790-114">PARAMETERS</span></span>

### <span data-ttu-id="a9790-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9790-115">-DefaultProfile</span></span>
<span data-ttu-id="a9790-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a9790-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9790-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="a9790-117">-DisableBrowser</span></span>
<span data-ttu-id="a9790-118">Visa inte pop öppna en webbläsare när du har fastställt kubectl-porten-forward.</span><span class="sxs-lookup"><span data-stu-id="a9790-118">Do not pop open a browser after establishing the kubectl port-forward.</span></span>

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

### <span data-ttu-id="a9790-119">-ID</span><span class="sxs-lookup"><span data-stu-id="a9790-119">-Id</span></span>
<span data-ttu-id="a9790-120">ID för ett hanterat Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="a9790-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9790-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9790-121">-InputObject</span></span>
<span data-ttu-id="a9790-122">Ett PSKubernetesCluster-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="a9790-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9790-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="a9790-123">-Name</span></span>
<span data-ttu-id="a9790-124">Namn på ditt hanterade Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="a9790-124">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9790-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9790-125">-PassThru</span></span>
<span data-ttu-id="a9790-126">Cmdlet returnerar KubeTunnelJob om den är klar.</span><span class="sxs-lookup"><span data-stu-id="a9790-126">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="a9790-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9790-127">-ResourceGroupName</span></span>
<span data-ttu-id="a9790-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a9790-128">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9790-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9790-129">CommonParameters</span></span>
<span data-ttu-id="a9790-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9790-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9790-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9790-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9790-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a9790-132">INPUTS</span></span>

### <span data-ttu-id="a9790-133">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="a9790-133">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="a9790-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a9790-134">System.String</span></span>

## <span data-ttu-id="a9790-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a9790-135">OUTPUTS</span></span>

### <span data-ttu-id="a9790-136">Microsoft. Azure. commands. AKS. KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="a9790-136">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="a9790-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a9790-137">NOTES</span></span>

## <span data-ttu-id="a9790-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a9790-138">RELATED LINKS</span></span>
