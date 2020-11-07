---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/start-azurermaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Start-AzureRmAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Start-AzureRmAksDashboard.md
ms.openlocfilehash: bf9ad8306a8158d9a8087de1f299ba66a02717fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757157"
---
# <span data-ttu-id="7dadd-101">Start-AzureRmAksDashboard</span><span class="sxs-lookup"><span data-stu-id="7dadd-101">Start-AzureRmAksDashboard</span></span>

## <span data-ttu-id="7dadd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7dadd-102">SYNOPSIS</span></span>
<span data-ttu-id="7dadd-103">Skapa en Kubectl SSH-tunnel till instrument panelen för hanterade kluster.</span><span class="sxs-lookup"><span data-stu-id="7dadd-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7dadd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7dadd-104">SYNTAX</span></span>

### <span data-ttu-id="7dadd-105">GroupNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7dadd-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzureRmAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7dadd-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7dadd-106">InputObjectParameterSet</span></span>
```
Start-AzureRmAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7dadd-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7dadd-107">IdParameterSet</span></span>
```
Start-AzureRmAksDashboard [-Id] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7dadd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7dadd-108">DESCRIPTION</span></span>
<span data-ttu-id="7dadd-109">Skapa en Kubectl SSH-tunnel till instrument panelen för hanterade kluster.</span><span class="sxs-lookup"><span data-stu-id="7dadd-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="7dadd-110">SSH-tunneln installeras i ett PowerShell-jobb som heter Kubectl-Tunnel och kan hittas genom att köra `Get-Job` .</span><span class="sxs-lookup"><span data-stu-id="7dadd-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="7dadd-111">Tunneln ska kunna nås via [http://127.0.0.1:8001](http://127.0.0.1:8001) .</span><span class="sxs-lookup"><span data-stu-id="7dadd-111">The tunnel should be accessable via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="7dadd-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7dadd-112">EXAMPLES</span></span>

### <span data-ttu-id="7dadd-113">Starta en SSH-tunnel och öppna en webbläsare på Kubernetes instrument panel</span><span class="sxs-lookup"><span data-stu-id="7dadd-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzureRmAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="7dadd-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7dadd-114">PARAMETERS</span></span>

### <span data-ttu-id="7dadd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dadd-115">-DefaultProfile</span></span>
<span data-ttu-id="7dadd-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7dadd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dadd-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="7dadd-117">-DisableBrowser</span></span>
<span data-ttu-id="7dadd-118">Visa inte en webbläsare med establising kubectl-Port-Forward.</span><span class="sxs-lookup"><span data-stu-id="7dadd-118">Do not pop open a browser after establising the kubectl port-forward.</span></span>

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

### <span data-ttu-id="7dadd-119">-ID</span><span class="sxs-lookup"><span data-stu-id="7dadd-119">-Id</span></span>
<span data-ttu-id="7dadd-120">ID för ett hanterat Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="7dadd-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="7dadd-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7dadd-121">-InputObject</span></span>
<span data-ttu-id="7dadd-122">Ett PSKubernetesCluster-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="7dadd-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="7dadd-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="7dadd-123">-Name</span></span>
<span data-ttu-id="7dadd-124">Namn på ditt hanterade Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="7dadd-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="7dadd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7dadd-125">-PassThru</span></span>
<span data-ttu-id="7dadd-126">Cmdlet returnerar KubeTunnelJob om den är klar.</span><span class="sxs-lookup"><span data-stu-id="7dadd-126">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="7dadd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dadd-127">-ResourceGroupName</span></span>
<span data-ttu-id="7dadd-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="7dadd-128">Resource group name</span></span>

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

### <span data-ttu-id="7dadd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dadd-129">CommonParameters</span></span>
<span data-ttu-id="7dadd-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dadd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dadd-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dadd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dadd-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7dadd-132">INPUTS</span></span>

### <span data-ttu-id="7dadd-133">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="7dadd-133">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="7dadd-134">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7dadd-134">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="7dadd-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7dadd-135">System.String</span></span>

## <span data-ttu-id="7dadd-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7dadd-136">OUTPUTS</span></span>

### <span data-ttu-id="7dadd-137">Microsoft. Azure. commands. AKS. KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="7dadd-137">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="7dadd-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7dadd-138">NOTES</span></span>

## <span data-ttu-id="7dadd-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7dadd-139">RELATED LINKS</span></span>
