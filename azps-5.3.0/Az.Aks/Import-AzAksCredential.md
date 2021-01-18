---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/import-azakscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
ms.openlocfilehash: fe4e56e809dd2cda7c650e24b55ae3867a23a7b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523328"
---
# <span data-ttu-id="92003-101">Import-AzAksCredential</span><span class="sxs-lookup"><span data-stu-id="92003-101">Import-AzAksCredential</span></span>

## <span data-ttu-id="92003-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92003-102">SYNOPSIS</span></span>
<span data-ttu-id="92003-103">Importera och slå samman Kubectl config för ett hanterat Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="92003-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="92003-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92003-104">SYNTAX</span></span>

### <span data-ttu-id="92003-105">GroupNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="92003-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92003-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92003-106">InputObjectParameterSet</span></span>
```
Import-AzAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92003-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92003-107">IdParameterSet</span></span>
```
Import-AzAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92003-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92003-108">DESCRIPTION</span></span>
<span data-ttu-id="92003-109">Importera och slå samman Kubectl config för ett hanterat Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="92003-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="92003-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92003-110">EXAMPLES</span></span>

### <span data-ttu-id="92003-111">Importera och slå samman Kubectl-konfiguration</span><span class="sxs-lookup"><span data-stu-id="92003-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="92003-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92003-112">PARAMETERS</span></span>

### <span data-ttu-id="92003-113">-Admin</span><span class="sxs-lookup"><span data-stu-id="92003-113">-Admin</span></span>
<span data-ttu-id="92003-114">Hämta "clusterAdmin' kubectl config i stället för standard" clusterUser ".</span><span class="sxs-lookup"><span data-stu-id="92003-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

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

### <span data-ttu-id="92003-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="92003-115">-ConfigPath</span></span>
<span data-ttu-id="92003-116">En kubectl-konfigurationsfil för att skapa eller uppdatera.</span><span class="sxs-lookup"><span data-stu-id="92003-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="92003-117">Använd "-" för att skriva ut YAML i stället.</span><span class="sxs-lookup"><span data-stu-id="92003-117">Use '-' to print YAML to stdout instead.</span></span>
<span data-ttu-id="92003-118">Standard:% Start%/.Kube/config.</span><span class="sxs-lookup"><span data-stu-id="92003-118">Default: %Home%/.kube/config.</span></span>

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

### <span data-ttu-id="92003-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92003-119">-DefaultProfile</span></span>
<span data-ttu-id="92003-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="92003-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92003-121">-Force</span><span class="sxs-lookup"><span data-stu-id="92003-121">-Force</span></span>
<span data-ttu-id="92003-122">Importera Kubernetes-konfiguration även om den är standard</span><span class="sxs-lookup"><span data-stu-id="92003-122">Import Kubernetes config even if it is the default</span></span>

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

### <span data-ttu-id="92003-123">-ID</span><span class="sxs-lookup"><span data-stu-id="92003-123">-Id</span></span>
<span data-ttu-id="92003-124">ID för ett hanterat Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="92003-124">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="92003-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92003-125">-InputObject</span></span>
<span data-ttu-id="92003-126">Ett PSKubernetesCluster-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="92003-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="92003-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="92003-127">-Name</span></span>
<span data-ttu-id="92003-128">Namn på ditt hanterade Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="92003-128">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="92003-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92003-129">-PassThru</span></span>
<span data-ttu-id="92003-130">Returnerar true om importen lyckades</span><span class="sxs-lookup"><span data-stu-id="92003-130">Returns true if import is successful</span></span>

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

### <span data-ttu-id="92003-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92003-131">-ResourceGroupName</span></span>
<span data-ttu-id="92003-132">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="92003-132">Resource group name</span></span>

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

### <span data-ttu-id="92003-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="92003-133">-Confirm</span></span>
<span data-ttu-id="92003-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="92003-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92003-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92003-135">-WhatIf</span></span>
<span data-ttu-id="92003-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="92003-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92003-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="92003-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92003-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92003-138">CommonParameters</span></span>
<span data-ttu-id="92003-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92003-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92003-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92003-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92003-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92003-141">INPUTS</span></span>

### <span data-ttu-id="92003-142">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="92003-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="92003-143">System. String</span><span class="sxs-lookup"><span data-stu-id="92003-143">System.String</span></span>

## <span data-ttu-id="92003-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92003-144">OUTPUTS</span></span>

### <span data-ttu-id="92003-145">System. String</span><span class="sxs-lookup"><span data-stu-id="92003-145">System.String</span></span>

## <span data-ttu-id="92003-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92003-146">NOTES</span></span>

## <span data-ttu-id="92003-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92003-147">RELATED LINKS</span></span>
