---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/new-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
ms.openlocfilehash: ed68271ae29c7af0219fa08d1c342b636d7d3fbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757730"
---
# <span data-ttu-id="d4e66-101">New-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="d4e66-101">New-AzureRmAks</span></span>

## <span data-ttu-id="d4e66-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d4e66-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e66-103">Skapa ett nytt hanterat Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="d4e66-103">Create a new managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4e66-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d4e66-104">SYNTAX</span></span>

```
New-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-Force] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4e66-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d4e66-105">DESCRIPTION</span></span>
<span data-ttu-id="d4e66-106">Skapa ett nytt hanterat Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="d4e66-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="d4e66-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d4e66-107">EXAMPLES</span></span>

### <span data-ttu-id="d4e66-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d4e66-108">Example 1</span></span>
<span data-ttu-id="d4e66-109">Skapa ett nytt hanterat Kubernetes-kluster med standard parametrar</span><span class="sxs-lookup"><span data-stu-id="d4e66-109">Create a new managed Kubernetes cluster with default params</span></span>

```
PS C:\> New-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="d4e66-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d4e66-110">PARAMETERS</span></span>

### <span data-ttu-id="d4e66-111">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="d4e66-111">-AdminUserName</span></span>
<span data-ttu-id="d4e66-112">Användar namn för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="d4e66-112">User name for the Linux Virtual Machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e66-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4e66-113">-AsJob</span></span>
<span data-ttu-id="d4e66-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d4e66-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4e66-115">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="d4e66-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="d4e66-116">Det klient-ID och den klient hemlighet som är kopplad till AAD-programmet/tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="d4e66-116">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e66-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4e66-117">-DefaultProfile</span></span>
<span data-ttu-id="d4e66-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d4e66-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4e66-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="d4e66-119">-DnsNamePrefix</span></span>
<span data-ttu-id="d4e66-120">DNS-namnets prefix för klustret.</span><span class="sxs-lookup"><span data-stu-id="d4e66-120">The DNS name prefix for the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e66-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d4e66-121">-Force</span></span>
<span data-ttu-id="d4e66-122">Skapa kluster även om det redan finns</span><span class="sxs-lookup"><span data-stu-id="d4e66-122">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="d4e66-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="d4e66-123">-KubernetesVersion</span></span>
<span data-ttu-id="d4e66-124">Den version av Kubernetes som ska användas för att skapa klustret.</span><span class="sxs-lookup"><span data-stu-id="d4e66-124">The version of Kubernetes to use for creating the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e66-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="d4e66-125">-Location</span></span>
<span data-ttu-id="d4e66-126">Azure-plats för klustret.</span><span class="sxs-lookup"><span data-stu-id="d4e66-126">Azure location for the cluster.</span></span>
<span data-ttu-id="d4e66-127">Som standard anges resurs gruppens plats.</span><span class="sxs-lookup"><span data-stu-id="d4e66-127">Defaults to the location of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e66-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="d4e66-128">-Name</span></span>
<span data-ttu-id="d4e66-129">Kubernetes hanterat kluster namn.</span><span class="sxs-lookup"><span data-stu-id="d4e66-129">Kubernetes managed cluster Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e66-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="d4e66-130">-NodeCount</span></span>
<span data-ttu-id="d4e66-131">Standardvärdet för noder för nodkonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="d4e66-131">The default number of nodes for the node pools.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e66-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="d4e66-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="d4e66-133">Standardvärdet för noder för nodkonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="d4e66-133">The default number of nodes for the node pools.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e66-134">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="d4e66-134">-NodeVmSize</span></span>
<span data-ttu-id="d4e66-135">Den virtuella datorns storlek.</span><span class="sxs-lookup"><span data-stu-id="d4e66-135">The size of the Virtual Machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e66-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4e66-136">-ResourceGroupName</span></span>
<span data-ttu-id="d4e66-137">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="d4e66-137">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e66-138">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="d4e66-138">-SshKeyValue</span></span>
<span data-ttu-id="d4e66-139">Fil värde för SSH-nyckel eller sökväg till nyckel fil.</span><span class="sxs-lookup"><span data-stu-id="d4e66-139">SSH key file value or key file path.</span></span>
<span data-ttu-id="d4e66-140">Standardvärdet är {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="d4e66-140">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e66-141">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d4e66-141">-Tag</span></span>
<span data-ttu-id="d4e66-142">Taggar som ska tillämpas på resursen</span><span class="sxs-lookup"><span data-stu-id="d4e66-142">Tags to be applied to the resource</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e66-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d4e66-143">-Confirm</span></span>
<span data-ttu-id="d4e66-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d4e66-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e66-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4e66-145">-WhatIf</span></span>
<span data-ttu-id="d4e66-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d4e66-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4e66-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d4e66-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e66-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e66-148">CommonParameters</span></span>
<span data-ttu-id="d4e66-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4e66-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e66-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4e66-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e66-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d4e66-151">INPUTS</span></span>

### <span data-ttu-id="d4e66-152">Ingen</span><span class="sxs-lookup"><span data-stu-id="d4e66-152">None</span></span>

## <span data-ttu-id="d4e66-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d4e66-153">OUTPUTS</span></span>

### <span data-ttu-id="d4e66-154">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="d4e66-154">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="d4e66-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d4e66-155">NOTES</span></span>

## <span data-ttu-id="d4e66-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d4e66-156">RELATED LINKS</span></span>
