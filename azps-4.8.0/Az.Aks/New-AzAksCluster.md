---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: f7a3479fb7fd70c47d5d4d3b80004cb25d9baa0c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258421"
---
# <span data-ttu-id="db0b9-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="db0b9-101">New-AzAksCluster</span></span>

## <span data-ttu-id="db0b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db0b9-102">SYNOPSIS</span></span>
<span data-ttu-id="db0b9-103">Skapa ett nytt hanterat Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="db0b9-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="db0b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db0b9-104">SYNTAX</span></span>

```
New-AzAksCluster [-Force] [-GenerateSshKey] [-NodeVmSetType <String>] [-NodeVnetSubnetID <String>]
 [-NodeMaxPodCount <Int32>] [-NodeOsType <String>] [-NodeSetPriority <String>] [-NodePoolMode <String>]
 [-NodeScaleSetEvictionPolicy <String>] [-AddOnNameToBeEnabled <String[]>] [-WorkspaceResourceId <String>]
 [-SubnetName <String>] [-AcrNameToAttach <String>] [-EnableRbac] [-WindowsProfileAdminUserName <String>]
 [-WindowsProfileAdminUserPassword <SecureString>] [-NetworkPlugin <String>] [-LoadBalancerSku <String>]
 [-ResourceGroupName] <String> [-Name] <String> [[-ServicePrincipalIdAndSecret] <PSCredential>]
 [-Location <String>] [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>]
 [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>]
 [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>]
 [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db0b9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db0b9-105">DESCRIPTION</span></span>

<span data-ttu-id="db0b9-106">Skapa ett nytt Azure Kubernetes-tjänst-kluster (AKS).</span><span class="sxs-lookup"><span data-stu-id="db0b9-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="db0b9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db0b9-107">EXAMPLES</span></span>

### <span data-ttu-id="db0b9-108">Ny AKS med standard parametrar.</span><span class="sxs-lookup"><span data-stu-id="db0b9-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="db0b9-109">Skapa en Windows Server-behållare på en AKS.</span><span class="sxs-lookup"><span data-stu-id="db0b9-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="db0b9-110">Om du vill skapa en Windows Server-behållare på en AKS måste du ange minst fyra parametrar när du skapar AKS och värdet för `NetworkPlugin` och `NodeVmSetType` måste vara respektive `azure` `VirtualMachineScaleSets` .</span><span class="sxs-lookup"><span data-stu-id="db0b9-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword *** -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="db0b9-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db0b9-111">PARAMETERS</span></span>

### <span data-ttu-id="db0b9-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="db0b9-112">-AcrNameToAttach</span></span>
<span data-ttu-id="db0b9-113">Tilldela rollen "acrpull" för den angivna ACR till AKS tjänstens huvud namn, t. ex myacr</span><span class="sxs-lookup"><span data-stu-id="db0b9-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

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

### <span data-ttu-id="db0b9-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="db0b9-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="db0b9-115">Tilläggs namn som ska aktive ras när klustret skapas.</span><span class="sxs-lookup"><span data-stu-id="db0b9-115">Add-on names to be enabled when cluster is created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db0b9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db0b9-116">-AsJob</span></span>
<span data-ttu-id="db0b9-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="db0b9-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db0b9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db0b9-118">-DefaultProfile</span></span>
<span data-ttu-id="db0b9-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="db0b9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db0b9-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="db0b9-120">-DnsNamePrefix</span></span>
<span data-ttu-id="db0b9-121">DNS-namnets prefix för klustret.</span><span class="sxs-lookup"><span data-stu-id="db0b9-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="db0b9-122">Längden måste vara <= 9 om användare planerar att lägga till Windows-behållare.</span><span class="sxs-lookup"><span data-stu-id="db0b9-122">The length must be <= 9 if users plan to add windows container.</span></span>

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

### <span data-ttu-id="db0b9-123">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="db0b9-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="db0b9-124">Om du vill aktivera automatisk skalning</span><span class="sxs-lookup"><span data-stu-id="db0b9-124">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="db0b9-125">-EnableRbac</span><span class="sxs-lookup"><span data-stu-id="db0b9-125">-EnableRbac</span></span>
<span data-ttu-id="db0b9-126">Om du vill aktivera Kubernetes Role-Based Access</span><span class="sxs-lookup"><span data-stu-id="db0b9-126">Whether to enable Kubernetes Role-Based Access</span></span>

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

### <span data-ttu-id="db0b9-127">-Force</span><span class="sxs-lookup"><span data-stu-id="db0b9-127">-Force</span></span>
<span data-ttu-id="db0b9-128">Skapa kluster även om det redan finns</span><span class="sxs-lookup"><span data-stu-id="db0b9-128">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="db0b9-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="db0b9-129">-GenerateSshKey</span></span>
<span data-ttu-id="db0b9-130">Skapa SSH Key-filen till {HOME}/.ssh/id_rsa.</span><span class="sxs-lookup"><span data-stu-id="db0b9-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

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

### <span data-ttu-id="db0b9-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="db0b9-131">-KubernetesVersion</span></span>
<span data-ttu-id="db0b9-132">Den version av Kubernetes som ska användas för att skapa klustret.</span><span class="sxs-lookup"><span data-stu-id="db0b9-132">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="db0b9-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="db0b9-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="db0b9-134">Användar namn för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="db0b9-134">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="db0b9-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="db0b9-135">-LoadBalancerSku</span></span>
<span data-ttu-id="db0b9-136">SKU för det hanterade klustret.</span><span class="sxs-lookup"><span data-stu-id="db0b9-136">The load balancer sku for the managed cluster.</span></span>

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

### <span data-ttu-id="db0b9-137">-Plats</span><span class="sxs-lookup"><span data-stu-id="db0b9-137">-Location</span></span>
<span data-ttu-id="db0b9-138">Azure-plats för klustret.</span><span class="sxs-lookup"><span data-stu-id="db0b9-138">Azure location for the cluster.</span></span>
<span data-ttu-id="db0b9-139">Som standard anges resurs gruppens plats.</span><span class="sxs-lookup"><span data-stu-id="db0b9-139">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="db0b9-140">-Namn</span><span class="sxs-lookup"><span data-stu-id="db0b9-140">-Name</span></span>
<span data-ttu-id="db0b9-141">Kubernetes hanterat kluster namn.</span><span class="sxs-lookup"><span data-stu-id="db0b9-141">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="db0b9-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="db0b9-142">-NetworkPlugin</span></span>
<span data-ttu-id="db0b9-143">Nätverks-plugin som används för att bygga Kubernetes nätverk.</span><span class="sxs-lookup"><span data-stu-id="db0b9-143">Network plugin used for building Kubernetes network.</span></span>

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

### <span data-ttu-id="db0b9-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="db0b9-144">-NodeCount</span></span>
<span data-ttu-id="db0b9-145">Standardvärdet för noder för nodkonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="db0b9-145">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="db0b9-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="db0b9-146">-NodeMaxCount</span></span>
<span data-ttu-id="db0b9-147">Maximalt antal noder för automatisk skalning</span><span class="sxs-lookup"><span data-stu-id="db0b9-147">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="db0b9-148">-NodeMaxPodCount</span><span class="sxs-lookup"><span data-stu-id="db0b9-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="db0b9-149">Maximalt antal Pods som kan köras på noden.</span><span class="sxs-lookup"><span data-stu-id="db0b9-149">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="db0b9-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="db0b9-150">-NodeMinCount</span></span>
<span data-ttu-id="db0b9-151">Minsta antal noder för automatisk skalning.</span><span class="sxs-lookup"><span data-stu-id="db0b9-151">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="db0b9-152">-Nodnamn</span><span class="sxs-lookup"><span data-stu-id="db0b9-152">-NodeName</span></span>
<span data-ttu-id="db0b9-153">Unikt namn på mediepoolen i kontexten för prenumerations-och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="db0b9-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="db0b9-154">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="db0b9-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="db0b9-155">Storlek i GB på OS-disken för varje nod i noduppsättningen.</span><span class="sxs-lookup"><span data-stu-id="db0b9-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="db0b9-156">Minst 30 GB.</span><span class="sxs-lookup"><span data-stu-id="db0b9-156">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="db0b9-157">-NodeOsType</span><span class="sxs-lookup"><span data-stu-id="db0b9-157">-NodeOsType</span></span>
<span data-ttu-id="db0b9-158">OsType som ska användas för att ange OS-typ.</span><span class="sxs-lookup"><span data-stu-id="db0b9-158">OsType to be used to specify os type.</span></span> <span data-ttu-id="db0b9-159">Välj från Linux och Windows.</span><span class="sxs-lookup"><span data-stu-id="db0b9-159">Choose from Linux and Windows.</span></span> <span data-ttu-id="db0b9-160">Standard för Linux.</span><span class="sxs-lookup"><span data-stu-id="db0b9-160">Default to Linux.</span></span>

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

### <span data-ttu-id="db0b9-161">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="db0b9-161">-NodePoolMode</span></span>
<span data-ttu-id="db0b9-162">NodePoolMode representerar ett läge för en noduppsättning.</span><span class="sxs-lookup"><span data-stu-id="db0b9-162">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="db0b9-163">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="db0b9-163">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="db0b9-164">ScaleSetEvictionPolicy ska användas för att ange borttagnings princip för skalnings uppsättning för den virtuella datorns Pro.</span><span class="sxs-lookup"><span data-stu-id="db0b9-164">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="db0b9-165">Standard för att ta bort.</span><span class="sxs-lookup"><span data-stu-id="db0b9-165">Default to Delete.</span></span>

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

### <span data-ttu-id="db0b9-166">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="db0b9-166">-NodeSetPriority</span></span>
<span data-ttu-id="db0b9-167">ScaleSetPriority används för att ange prioritet för den virtuella datorns skalnings uppsättning.</span><span class="sxs-lookup"><span data-stu-id="db0b9-167">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="db0b9-168">Standard är normal.</span><span class="sxs-lookup"><span data-stu-id="db0b9-168">Default to regular.</span></span>

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

### <span data-ttu-id="db0b9-169">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="db0b9-169">-NodeVmSetType</span></span>
<span data-ttu-id="db0b9-170">AgentPoolType representerar typer av en programpool.</span><span class="sxs-lookup"><span data-stu-id="db0b9-170">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="db0b9-171">Möjliga värden är: ' VirtualMachineScaleSets ', ' AvailabilitySet '</span><span class="sxs-lookup"><span data-stu-id="db0b9-171">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="db0b9-172">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="db0b9-172">-NodeVmSize</span></span>
<span data-ttu-id="db0b9-173">Den virtuella datorns storlek.</span><span class="sxs-lookup"><span data-stu-id="db0b9-173">The size of the Virtual Machine.</span></span> <span data-ttu-id="db0b9-174">Standardvärdet är Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="db0b9-174">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="db0b9-175">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="db0b9-175">-NodeVnetSubnetID</span></span>
<span data-ttu-id="db0b9-176">VNet-SubnetID anger VNet-nätmask.</span><span class="sxs-lookup"><span data-stu-id="db0b9-176">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="db0b9-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db0b9-177">-ResourceGroupName</span></span>
<span data-ttu-id="db0b9-178">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="db0b9-178">Resource Group Name.</span></span>

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

### <span data-ttu-id="db0b9-179">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="db0b9-179">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="db0b9-180">Det klient-ID och den klient hemlighet som är kopplad till AAD-programmet/tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="db0b9-180">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClientIdAndSecret

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db0b9-181">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="db0b9-181">-SshKeyValue</span></span>
<span data-ttu-id="db0b9-182">Fil värde för SSH-nyckel eller sökväg till nyckel fil.</span><span class="sxs-lookup"><span data-stu-id="db0b9-182">SSH key file value or key file path.</span></span>
<span data-ttu-id="db0b9-183">Standardvärdet är {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="db0b9-183">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="db0b9-184">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="db0b9-184">-SubnetName</span></span>
<span data-ttu-id="db0b9-185">VirtualNode addon-namn.</span><span class="sxs-lookup"><span data-stu-id="db0b9-185">Subnet name of VirtualNode addon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db0b9-186">-Tagg</span><span class="sxs-lookup"><span data-stu-id="db0b9-186">-Tag</span></span>
<span data-ttu-id="db0b9-187">Taggar som ska tillämpas på resursen</span><span class="sxs-lookup"><span data-stu-id="db0b9-187">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="db0b9-188">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="db0b9-188">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="db0b9-189">Det administratörs användar namn som ska användas för Windows VMs.</span><span class="sxs-lookup"><span data-stu-id="db0b9-189">The administrator username to use for Windows VMs.</span></span>

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

### <span data-ttu-id="db0b9-190">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="db0b9-190">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="db0b9-191">Det administratörs lösen ord som ska användas för Windows-VMs och dess längd måste vara minst 12 som innehåller minst ett gement tecken, d.v.s. `[a-z]` ett `[A-Z]` och ett specialtecken `[!@#$%^&*()]` .</span><span class="sxs-lookup"><span data-stu-id="db0b9-191">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&*()]`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db0b9-192">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="db0b9-192">-WorkspaceResourceId</span></span>
<span data-ttu-id="db0b9-193">Resurs-ID för arbets ytan som övervakar addon.</span><span class="sxs-lookup"><span data-stu-id="db0b9-193">Resource Id of the workspace of Monitoring addon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db0b9-194">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="db0b9-194">-Confirm</span></span>
<span data-ttu-id="db0b9-195">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="db0b9-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db0b9-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db0b9-196">-WhatIf</span></span>
<span data-ttu-id="db0b9-197">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="db0b9-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db0b9-198">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="db0b9-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db0b9-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db0b9-199">CommonParameters</span></span>
<span data-ttu-id="db0b9-200">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db0b9-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db0b9-201">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db0b9-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db0b9-202">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db0b9-202">INPUTS</span></span>

### <span data-ttu-id="db0b9-203">Ingen</span><span class="sxs-lookup"><span data-stu-id="db0b9-203">None</span></span>

## <span data-ttu-id="db0b9-204">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db0b9-204">OUTPUTS</span></span>

### <span data-ttu-id="db0b9-205">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="db0b9-205">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="db0b9-206">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db0b9-206">NOTES</span></span>

## <span data-ttu-id="db0b9-207">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db0b9-207">RELATED LINKS</span></span>
