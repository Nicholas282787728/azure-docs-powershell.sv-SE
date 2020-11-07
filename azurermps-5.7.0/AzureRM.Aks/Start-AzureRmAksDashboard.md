---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/start-azurermaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Start-AzureRmAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Start-AzureRmAksDashboard.md
ms.openlocfilehash: 5858a1f17bcae3c003ed7b40200c065c36eb2b1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756526"
---
# <span data-ttu-id="d5e9a-101">Start-AzureRmAksDashboard</span><span class="sxs-lookup"><span data-stu-id="d5e9a-101">Start-AzureRmAksDashboard</span></span>

## <span data-ttu-id="d5e9a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d5e9a-102">SYNOPSIS</span></span>
<span data-ttu-id="d5e9a-103">Skapa en Kubectl SSH-tunnel till instrument panelen för hanterade kluster.</span><span class="sxs-lookup"><span data-stu-id="d5e9a-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5e9a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d5e9a-104">SYNTAX</span></span>

### <span data-ttu-id="d5e9a-105">GroupNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d5e9a-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzureRmAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5e9a-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5e9a-106">InputObjectParameterSet</span></span>
```
Start-AzureRmAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5e9a-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5e9a-107">IdParameterSet</span></span>
```
Start-AzureRmAksDashboard [-Id] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5e9a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d5e9a-108">DESCRIPTION</span></span>
<span data-ttu-id="d5e9a-109">Skapa en Kubectl SSH-tunnel till instrument panelen för hanterade kluster.</span><span class="sxs-lookup"><span data-stu-id="d5e9a-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="d5e9a-110">SSH-tunneln installeras i ett PowerShell-jobb som heter Kubectl-Tunnel och kan hittas genom att köra `Get-Job` .</span><span class="sxs-lookup"><span data-stu-id="d5e9a-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="d5e9a-111">Tunneln ska kunna nås via [http://127.0.0.1:8001](http://127.0.0.1:8001) .</span><span class="sxs-lookup"><span data-stu-id="d5e9a-111">The tunnel should be accessable via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="d5e9a-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d5e9a-112">EXAMPLES</span></span>

### <span data-ttu-id="d5e9a-113">Starta en SSH-tunnel och öppna en webbläsare på Kubernetes instrument panel</span><span class="sxs-lookup"><span data-stu-id="d5e9a-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzureRmAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="d5e9a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d5e9a-114">PARAMETERS</span></span>

### <span data-ttu-id="d5e9a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5e9a-115">-DefaultProfile</span></span>
<span data-ttu-id="d5e9a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d5e9a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e9a-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="d5e9a-117">-DisableBrowser</span></span>
<span data-ttu-id="d5e9a-118">Visa inte en webbläsare med establising kubectl-Port-Forward.</span><span class="sxs-lookup"><span data-stu-id="d5e9a-118">Do not pop open a browser after establising the kubectl port-forward.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e9a-119">-ID</span><span class="sxs-lookup"><span data-stu-id="d5e9a-119">-Id</span></span>
<span data-ttu-id="d5e9a-120">ID för ett hanterat Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="d5e9a-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5e9a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5e9a-121">-InputObject</span></span>
<span data-ttu-id="d5e9a-122">Ett PSKubernetesCluster-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="d5e9a-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5e9a-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="d5e9a-123">-Name</span></span>
<span data-ttu-id="d5e9a-124">Namn på ditt hanterade Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="d5e9a-124">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e9a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5e9a-125">-PassThru</span></span>
<span data-ttu-id="d5e9a-126">Cmdlet returnerar KubeTunnelJob om den är klar.</span><span class="sxs-lookup"><span data-stu-id="d5e9a-126">Cmdlet returns the KubeTunnelJob if passed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e9a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5e9a-127">-ResourceGroupName</span></span>
<span data-ttu-id="d5e9a-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d5e9a-128">Resource group name</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e9a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5e9a-129">CommonParameters</span></span>
<span data-ttu-id="d5e9a-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5e9a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5e9a-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5e9a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5e9a-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d5e9a-132">INPUTS</span></span>

### <span data-ttu-id="d5e9a-133">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="d5e9a-133">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="d5e9a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d5e9a-134">System.String</span></span>

## <span data-ttu-id="d5e9a-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d5e9a-135">OUTPUTS</span></span>

### <span data-ttu-id="d5e9a-136">Microsoft. Azure. commands. AKS. KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="d5e9a-136">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="d5e9a-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d5e9a-137">NOTES</span></span>

## <span data-ttu-id="d5e9a-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d5e9a-138">RELATED LINKS</span></span>
