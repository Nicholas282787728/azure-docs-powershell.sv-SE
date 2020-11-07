---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 563fac9587165a0c4b23ac37b9dc0f2b5fbc99cc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745925"
---
# <span data-ttu-id="17042-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="17042-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="17042-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="17042-102">SYNOPSIS</span></span>
<span data-ttu-id="17042-103">Skapa en Kubectl SSH-tunnel till instrument panelen för hanterade kluster.</span><span class="sxs-lookup"><span data-stu-id="17042-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="17042-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="17042-104">SYNTAX</span></span>

### <span data-ttu-id="17042-105">GroupNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="17042-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17042-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="17042-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17042-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="17042-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17042-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="17042-108">DESCRIPTION</span></span>
<span data-ttu-id="17042-109">Skapa en Kubectl SSH-tunnel till instrument panelen för hanterade kluster.</span><span class="sxs-lookup"><span data-stu-id="17042-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="17042-110">SSH-tunneln installeras i ett PowerShell-jobb som heter Kubectl-Tunnel och kan hittas genom att köra `Get-Job` .</span><span class="sxs-lookup"><span data-stu-id="17042-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="17042-111">Tunneln ska vara tillgänglig via [http://127.0.0.1:8001](http://127.0.0.1:8001) .</span><span class="sxs-lookup"><span data-stu-id="17042-111">The tunnel should be accessible via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="17042-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="17042-112">EXAMPLES</span></span>

### <span data-ttu-id="17042-113">Starta en SSH-tunnel och öppna en webbläsare på Kubernetes instrument panel</span><span class="sxs-lookup"><span data-stu-id="17042-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="17042-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="17042-114">PARAMETERS</span></span>

### <span data-ttu-id="17042-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17042-115">-DefaultProfile</span></span>
<span data-ttu-id="17042-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="17042-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17042-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="17042-117">-DisableBrowser</span></span>
<span data-ttu-id="17042-118">Visa inte pop öppna en webbläsare när du har fastställt kubectl-porten-forward.</span><span class="sxs-lookup"><span data-stu-id="17042-118">Do not pop open a browser after establishing the kubectl port-forward.</span></span>

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

### <span data-ttu-id="17042-119">-ID</span><span class="sxs-lookup"><span data-stu-id="17042-119">-Id</span></span>
<span data-ttu-id="17042-120">ID för ett hanterat Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="17042-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="17042-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17042-121">-InputObject</span></span>
<span data-ttu-id="17042-122">Ett PSKubernetesCluster-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="17042-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="17042-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="17042-123">-Name</span></span>
<span data-ttu-id="17042-124">Namn på ditt hanterade Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="17042-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="17042-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17042-125">-PassThru</span></span>
<span data-ttu-id="17042-126">Cmdlet returnerar KubeTunnelJob om den är klar.</span><span class="sxs-lookup"><span data-stu-id="17042-126">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="17042-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17042-127">-ResourceGroupName</span></span>
<span data-ttu-id="17042-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="17042-128">Resource group name</span></span>

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

### <span data-ttu-id="17042-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17042-129">CommonParameters</span></span>
<span data-ttu-id="17042-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17042-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17042-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17042-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17042-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="17042-132">INPUTS</span></span>

### <span data-ttu-id="17042-133">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="17042-133">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="17042-134">System. String</span><span class="sxs-lookup"><span data-stu-id="17042-134">System.String</span></span>

## <span data-ttu-id="17042-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="17042-135">OUTPUTS</span></span>

### <span data-ttu-id="17042-136">Microsoft. Azure. commands. AKS. KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="17042-136">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="17042-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="17042-137">NOTES</span></span>

## <span data-ttu-id="17042-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="17042-138">RELATED LINKS</span></span>