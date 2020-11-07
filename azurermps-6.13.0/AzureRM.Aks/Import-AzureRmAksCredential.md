---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/import-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Import-AzureRmAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Import-AzureRmAksCredential.md
ms.openlocfilehash: b65ac736be5ee5f2f0592bcb2fdc84c873361f9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580896"
---
# <span data-ttu-id="4abdf-101">Import-AzureRmAksCredential</span><span class="sxs-lookup"><span data-stu-id="4abdf-101">Import-AzureRmAksCredential</span></span>

## <span data-ttu-id="4abdf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4abdf-102">SYNOPSIS</span></span>
<span data-ttu-id="4abdf-103">Importera och slå samman Kubectl config för ett hanterat Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="4abdf-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4abdf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4abdf-104">SYNTAX</span></span>

### <span data-ttu-id="4abdf-105">GroupNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4abdf-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzureRmAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4abdf-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4abdf-106">InputObjectParameterSet</span></span>
```
Import-AzureRmAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4abdf-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4abdf-107">IdParameterSet</span></span>
```
Import-AzureRmAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4abdf-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4abdf-108">DESCRIPTION</span></span>
<span data-ttu-id="4abdf-109">Importera och slå samman Kubectl config för ett hanterat Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="4abdf-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="4abdf-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4abdf-110">EXAMPLES</span></span>

### <span data-ttu-id="4abdf-111">Importera och slå samman Kubectl-konfiguration</span><span class="sxs-lookup"><span data-stu-id="4abdf-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzureRmAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="4abdf-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4abdf-112">PARAMETERS</span></span>

### <span data-ttu-id="4abdf-113">-Admin</span><span class="sxs-lookup"><span data-stu-id="4abdf-113">-Admin</span></span>
<span data-ttu-id="4abdf-114">Hämta "clusterAdmin' kubectl config i stället för standard" clusterUser ".</span><span class="sxs-lookup"><span data-stu-id="4abdf-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

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

### <span data-ttu-id="4abdf-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="4abdf-115">-ConfigPath</span></span>
<span data-ttu-id="4abdf-116">En kubectl-konfigurationsfil för att skapa eller uppdatera.</span><span class="sxs-lookup"><span data-stu-id="4abdf-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="4abdf-117">Använd "-" för att skriva ut YAML i stället.</span><span class="sxs-lookup"><span data-stu-id="4abdf-117">Use '-' to print YAML to stdout instead.</span></span> <span data-ttu-id="4abdf-118">Standard:% Start%/.Kube/config.</span><span class="sxs-lookup"><span data-stu-id="4abdf-118">Default: %Home%/.kube/config.</span></span>

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

### <span data-ttu-id="4abdf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4abdf-119">-DefaultProfile</span></span>
<span data-ttu-id="4abdf-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4abdf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4abdf-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4abdf-121">-Force</span></span>
<span data-ttu-id="4abdf-122">Importera Kubernetes-konfiguration även om den är standard</span><span class="sxs-lookup"><span data-stu-id="4abdf-122">Import Kubernetes config even if it is the default</span></span>

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

### <span data-ttu-id="4abdf-123">-ID</span><span class="sxs-lookup"><span data-stu-id="4abdf-123">-Id</span></span>
<span data-ttu-id="4abdf-124">ID för ett hanterat Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="4abdf-124">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="4abdf-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4abdf-125">-InputObject</span></span>
<span data-ttu-id="4abdf-126">Ett PSKubernetesCluster-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="4abdf-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="4abdf-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="4abdf-127">-Name</span></span>
<span data-ttu-id="4abdf-128">Namn på ditt hanterade Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="4abdf-128">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="4abdf-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4abdf-129">-PassThru</span></span>
<span data-ttu-id="4abdf-130">Returnerar true om importen lyckades</span><span class="sxs-lookup"><span data-stu-id="4abdf-130">Returns true if import is successful</span></span>

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

### <span data-ttu-id="4abdf-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4abdf-131">-ResourceGroupName</span></span>
<span data-ttu-id="4abdf-132">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="4abdf-132">Resource group name</span></span>

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

### <span data-ttu-id="4abdf-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4abdf-133">-Confirm</span></span>
<span data-ttu-id="4abdf-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4abdf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4abdf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4abdf-135">-WhatIf</span></span>
<span data-ttu-id="4abdf-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4abdf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4abdf-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4abdf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4abdf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4abdf-138">CommonParameters</span></span>
<span data-ttu-id="4abdf-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4abdf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4abdf-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4abdf-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4abdf-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4abdf-141">INPUTS</span></span>

### <span data-ttu-id="4abdf-142">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="4abdf-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="4abdf-143">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4abdf-143">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="4abdf-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4abdf-144">System.String</span></span>

## <span data-ttu-id="4abdf-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4abdf-145">OUTPUTS</span></span>

### <span data-ttu-id="4abdf-146">System. String</span><span class="sxs-lookup"><span data-stu-id="4abdf-146">System.String</span></span>

## <span data-ttu-id="4abdf-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4abdf-147">NOTES</span></span>

## <span data-ttu-id="4abdf-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4abdf-148">RELATED LINKS</span></span>