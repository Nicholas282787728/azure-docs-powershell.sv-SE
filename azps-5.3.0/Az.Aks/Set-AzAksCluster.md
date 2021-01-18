---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/set-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
ms.openlocfilehash: 0df5c0d9975acc048ba5842543ec2c4d522567c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523314"
---
# <span data-ttu-id="92fdd-101">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="92fdd-101">Set-AzAksCluster</span></span>

## <span data-ttu-id="92fdd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92fdd-102">SYNOPSIS</span></span>
<span data-ttu-id="92fdd-103">Uppdatera eller skapa ett hanterat Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="92fdd-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="92fdd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92fdd-104">SYNTAX</span></span>

### <span data-ttu-id="92fdd-105">defaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="92fdd-105">defaultParameterSet (Default)</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-ServicePrincipalIdAndSecret] <PSCredential>] [-Location <String>] [-LinuxProfileAdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>]
 [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92fdd-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92fdd-106">InputObjectParameterSet</span></span>
```
Set-AzAksCluster -InputObject <PSKubernetesCluster> [-NodePoolMode <String>] [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92fdd-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92fdd-107">IdParameterSet</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-Id] <String> [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92fdd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92fdd-108">DESCRIPTION</span></span>
<span data-ttu-id="92fdd-109">Uppdatera eller skapa ett hanterat Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="92fdd-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="92fdd-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92fdd-110">EXAMPLES</span></span>

### <span data-ttu-id="92fdd-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="92fdd-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="92fdd-112">Ange antalet noder i Kubernetes-klustret till 5.</span><span class="sxs-lookup"><span data-stu-id="92fdd-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="92fdd-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92fdd-113">PARAMETERS</span></span>

### <span data-ttu-id="92fdd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92fdd-114">-AsJob</span></span>
<span data-ttu-id="92fdd-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="92fdd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="92fdd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92fdd-116">-DefaultProfile</span></span>
<span data-ttu-id="92fdd-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="92fdd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92fdd-118">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="92fdd-118">-DnsNamePrefix</span></span>
<span data-ttu-id="92fdd-119">DNS-namnets prefix för klustret.</span><span class="sxs-lookup"><span data-stu-id="92fdd-119">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="92fdd-120">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="92fdd-120">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="92fdd-121">Om du vill aktivera automatisk skalning</span><span class="sxs-lookup"><span data-stu-id="92fdd-121">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="92fdd-122">-ID</span><span class="sxs-lookup"><span data-stu-id="92fdd-122">-Id</span></span>
<span data-ttu-id="92fdd-123">ID för ett hanterat Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="92fdd-123">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="92fdd-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92fdd-124">-InputObject</span></span>
<span data-ttu-id="92fdd-125">Ett PSKubernetesCluster-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="92fdd-125">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="92fdd-126">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="92fdd-126">-KubernetesVersion</span></span>
<span data-ttu-id="92fdd-127">Den version av Kubernetes som ska användas för att skapa klustret.</span><span class="sxs-lookup"><span data-stu-id="92fdd-127">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="92fdd-128">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="92fdd-128">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="92fdd-129">Användar namn för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="92fdd-129">User name for the Linux Virtual Machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AdminUserName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92fdd-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="92fdd-130">-Location</span></span>
<span data-ttu-id="92fdd-131">Azure-plats för klustret.</span><span class="sxs-lookup"><span data-stu-id="92fdd-131">Azure location for the cluster.</span></span>
<span data-ttu-id="92fdd-132">Som standard anges resurs gruppens plats.</span><span class="sxs-lookup"><span data-stu-id="92fdd-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="92fdd-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="92fdd-133">-Name</span></span>
<span data-ttu-id="92fdd-134">Kubernetes hanterat kluster namn.</span><span class="sxs-lookup"><span data-stu-id="92fdd-134">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="92fdd-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="92fdd-135">-NodeCount</span></span>
<span data-ttu-id="92fdd-136">Standardvärdet för noder för nodkonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="92fdd-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="92fdd-137">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="92fdd-137">-NodeMaxCount</span></span>
<span data-ttu-id="92fdd-138">Maximalt antal noder för automatisk skalning</span><span class="sxs-lookup"><span data-stu-id="92fdd-138">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="92fdd-139">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="92fdd-139">-NodeMinCount</span></span>
<span data-ttu-id="92fdd-140">Minsta antal noder för automatisk skalning.</span><span class="sxs-lookup"><span data-stu-id="92fdd-140">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="92fdd-141">-Nodnamn</span><span class="sxs-lookup"><span data-stu-id="92fdd-141">-NodeName</span></span>
<span data-ttu-id="92fdd-142">Unikt namn på mediepoolen i kontexten för prenumerations-och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="92fdd-142">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="92fdd-143">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="92fdd-143">-NodeOsDiskSize</span></span>
<span data-ttu-id="92fdd-144">Standardvärdet för noder för nodkonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="92fdd-144">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="92fdd-145">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="92fdd-145">-NodePoolMode</span></span>
<span data-ttu-id="92fdd-146">NodePoolMode representerar ett läge för en noduppsättning.</span><span class="sxs-lookup"><span data-stu-id="92fdd-146">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="92fdd-147">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="92fdd-147">-NodeVmSize</span></span>
<span data-ttu-id="92fdd-148">Den virtuella datorns storlek.</span><span class="sxs-lookup"><span data-stu-id="92fdd-148">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="92fdd-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92fdd-149">-ResourceGroupName</span></span>
<span data-ttu-id="92fdd-150">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="92fdd-150">Resource Group Name.</span></span>

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

### <span data-ttu-id="92fdd-151">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="92fdd-151">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="92fdd-152">Det klient-ID och den klient hemlighet som är kopplad till AAD-programmet/tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="92fdd-152">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: defaultParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92fdd-153">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="92fdd-153">-SshKeyValue</span></span>
<span data-ttu-id="92fdd-154">Fil värde för SSH-nyckel eller sökväg till nyckel fil.</span><span class="sxs-lookup"><span data-stu-id="92fdd-154">SSH key file value or key file path.</span></span>
<span data-ttu-id="92fdd-155">Standardvärdet är {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="92fdd-155">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="92fdd-156">-Tagg</span><span class="sxs-lookup"><span data-stu-id="92fdd-156">-Tag</span></span>
<span data-ttu-id="92fdd-157">Taggar som ska tillämpas på resursen</span><span class="sxs-lookup"><span data-stu-id="92fdd-157">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="92fdd-158">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="92fdd-158">-Confirm</span></span>
<span data-ttu-id="92fdd-159">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="92fdd-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92fdd-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92fdd-160">-WhatIf</span></span>
<span data-ttu-id="92fdd-161">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="92fdd-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92fdd-162">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="92fdd-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92fdd-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92fdd-163">CommonParameters</span></span>
<span data-ttu-id="92fdd-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92fdd-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92fdd-165">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92fdd-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92fdd-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92fdd-166">INPUTS</span></span>

### <span data-ttu-id="92fdd-167">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="92fdd-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="92fdd-168">System. String</span><span class="sxs-lookup"><span data-stu-id="92fdd-168">System.String</span></span>

## <span data-ttu-id="92fdd-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92fdd-169">OUTPUTS</span></span>

### <span data-ttu-id="92fdd-170">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="92fdd-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="92fdd-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92fdd-171">NOTES</span></span>

## <span data-ttu-id="92fdd-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92fdd-172">RELATED LINKS</span></span>
