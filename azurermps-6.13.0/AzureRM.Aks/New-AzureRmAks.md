---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/new-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
ms.openlocfilehash: f91b4f2afdb1c6aaf7cbac16f952a333d3d362b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756748"
---
# <span data-ttu-id="180cc-101">New-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="180cc-101">New-AzureRmAks</span></span>

## <span data-ttu-id="180cc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="180cc-102">SYNOPSIS</span></span>
<span data-ttu-id="180cc-103">Skapa ett nytt hanterat Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="180cc-103">Create a new managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="180cc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="180cc-104">SYNTAX</span></span>

```
New-AzureRmAks [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="180cc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="180cc-105">DESCRIPTION</span></span>

<span data-ttu-id="180cc-106">Skapa ett nytt hanterat Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="180cc-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="180cc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="180cc-107">EXAMPLES</span></span>

### <span data-ttu-id="180cc-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="180cc-108">Example 1</span></span>

<span data-ttu-id="180cc-109">Skapa ett nytt hanterat Kubernetes-kluster med standard parametrar.</span><span class="sxs-lookup"><span data-stu-id="180cc-109">Create a new managed Kubernetes cluster with default params.</span></span>

```
PS C:\> New-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="180cc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="180cc-110">PARAMETERS</span></span>

### <span data-ttu-id="180cc-111">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="180cc-111">-AdminUserName</span></span>
<span data-ttu-id="180cc-112">Användar namn för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="180cc-112">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="180cc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="180cc-113">-AsJob</span></span>
<span data-ttu-id="180cc-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="180cc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="180cc-115">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="180cc-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="180cc-116">Det klient-ID och den klient hemlighet som är kopplad till AAD-programmet/tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="180cc-116">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180cc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="180cc-117">-DefaultProfile</span></span>
<span data-ttu-id="180cc-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="180cc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="180cc-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="180cc-119">-DnsNamePrefix</span></span>
<span data-ttu-id="180cc-120">DNS-namnets prefix för klustret.</span><span class="sxs-lookup"><span data-stu-id="180cc-120">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="180cc-121">-Force</span><span class="sxs-lookup"><span data-stu-id="180cc-121">-Force</span></span>
<span data-ttu-id="180cc-122">Skapa kluster även om det redan finns</span><span class="sxs-lookup"><span data-stu-id="180cc-122">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="180cc-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="180cc-123">-KubernetesVersion</span></span>
<span data-ttu-id="180cc-124">Den version av Kubernetes som ska användas för att skapa klustret.</span><span class="sxs-lookup"><span data-stu-id="180cc-124">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="180cc-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="180cc-125">-Location</span></span>
<span data-ttu-id="180cc-126">Azure-plats för klustret.</span><span class="sxs-lookup"><span data-stu-id="180cc-126">Azure location for the cluster.</span></span>
<span data-ttu-id="180cc-127">Som standard anges resurs gruppens plats.</span><span class="sxs-lookup"><span data-stu-id="180cc-127">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="180cc-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="180cc-128">-Name</span></span>
<span data-ttu-id="180cc-129">Kubernetes hanterat kluster namn.</span><span class="sxs-lookup"><span data-stu-id="180cc-129">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180cc-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="180cc-130">-NodeCount</span></span>
<span data-ttu-id="180cc-131">Standardvärdet för noder för nodkonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="180cc-131">The default number of nodes for the node pools.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180cc-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="180cc-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="180cc-133">Storlek i GB på OS-disken för varje nod i noduppsättningen.</span><span class="sxs-lookup"><span data-stu-id="180cc-133">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="180cc-134">Minst 30 GB.</span><span class="sxs-lookup"><span data-stu-id="180cc-134">Minimum 30 GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180cc-135">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="180cc-135">-NodeVmSize</span></span>
<span data-ttu-id="180cc-136">Den virtuella datorns storlek.</span><span class="sxs-lookup"><span data-stu-id="180cc-136">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="180cc-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="180cc-137">-ResourceGroupName</span></span>
<span data-ttu-id="180cc-138">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="180cc-138">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180cc-139">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="180cc-139">-SshKeyValue</span></span>
<span data-ttu-id="180cc-140">Fil värde för SSH-nyckel eller sökväg till nyckel fil.</span><span class="sxs-lookup"><span data-stu-id="180cc-140">SSH key file value or key file path.</span></span>
<span data-ttu-id="180cc-141">Standardvärdet är {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="180cc-141">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180cc-142">-Tagg</span><span class="sxs-lookup"><span data-stu-id="180cc-142">-Tag</span></span>
<span data-ttu-id="180cc-143">Taggar som ska tillämpas på resursen</span><span class="sxs-lookup"><span data-stu-id="180cc-143">Tags to be applied to the resource</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180cc-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="180cc-144">-Confirm</span></span>
<span data-ttu-id="180cc-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="180cc-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="180cc-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="180cc-146">-WhatIf</span></span>
<span data-ttu-id="180cc-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="180cc-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="180cc-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="180cc-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="180cc-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="180cc-149">CommonParameters</span></span>
<span data-ttu-id="180cc-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="180cc-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="180cc-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="180cc-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="180cc-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="180cc-152">INPUTS</span></span>

### <span data-ttu-id="180cc-153">Ingen</span><span class="sxs-lookup"><span data-stu-id="180cc-153">None</span></span>

## <span data-ttu-id="180cc-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="180cc-154">OUTPUTS</span></span>

### <span data-ttu-id="180cc-155">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="180cc-155">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="180cc-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="180cc-156">NOTES</span></span>

## <span data-ttu-id="180cc-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="180cc-157">RELATED LINKS</span></span>
