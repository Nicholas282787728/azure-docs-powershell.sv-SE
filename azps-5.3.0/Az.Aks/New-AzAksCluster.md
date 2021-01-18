---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: aaab86d7943072ae861acb71ec5021bb098a48ef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523324"
---
# <span data-ttu-id="f8775-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="f8775-101">New-AzAksCluster</span></span>

## <span data-ttu-id="f8775-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f8775-102">SYNOPSIS</span></span>
<span data-ttu-id="f8775-103">Skapa ett nytt hanterat Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="f8775-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="f8775-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f8775-104">SYNTAX</span></span>

```
New-AzAksCluster [-Force] [-GenerateSshKey] [-NodeVmSetType <String>] [-NodeVnetSubnetID <String>]
 [-NodeMaxPodCount <Int32>] [-NodeSetPriority <String>] [-NodePoolMode <String>]
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

## <span data-ttu-id="f8775-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f8775-105">DESCRIPTION</span></span>

<span data-ttu-id="f8775-106">Skapa ett nytt Azure Kubernetes-tjänst-kluster (AKS).</span><span class="sxs-lookup"><span data-stu-id="f8775-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="f8775-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f8775-107">EXAMPLES</span></span>

### <span data-ttu-id="f8775-108">Ny AKS med standard parametrar.</span><span class="sxs-lookup"><span data-stu-id="f8775-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="f8775-109">Skapa en Windows Server-behållare på en AKS.</span><span class="sxs-lookup"><span data-stu-id="f8775-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="f8775-110">Om du vill skapa en Windows Server-behållare på en AKS måste du ange minst fyra parametrar när du skapar AKS och värdet för `NetworkPlugin` och `NodeVmSetType` måste vara respektive `azure` `VirtualMachineScaleSets` .</span><span class="sxs-lookup"><span data-stu-id="f8775-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword **_ -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="f8775-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f8775-111">PARAMETERS</span></span>

### <span data-ttu-id="f8775-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="f8775-112">-AcrNameToAttach</span></span>
<span data-ttu-id="f8775-113">Tilldela rollen "acrpull" för den angivna ACR till AKS tjänstens huvud namn, t. ex myacr</span><span class="sxs-lookup"><span data-stu-id="f8775-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

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

### <span data-ttu-id="f8775-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="f8775-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="f8775-115">Tilläggs namn som ska aktive ras när klustret skapas.</span><span class="sxs-lookup"><span data-stu-id="f8775-115">Add-on names to be enabled when cluster is created.</span></span>

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

### <span data-ttu-id="f8775-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8775-116">-AsJob</span></span>
<span data-ttu-id="f8775-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f8775-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8775-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8775-118">-DefaultProfile</span></span>
<span data-ttu-id="f8775-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f8775-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8775-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="f8775-120">-DnsNamePrefix</span></span>
<span data-ttu-id="f8775-121">DNS-namnets prefix för klustret.</span><span class="sxs-lookup"><span data-stu-id="f8775-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="f8775-122">Längden måste vara <= 9 om användare planerar att lägga till Windows-behållare.</span><span class="sxs-lookup"><span data-stu-id="f8775-122">The length must be <= 9 if users plan to add windows container.</span></span>

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

### <span data-ttu-id="f8775-123">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="f8775-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="f8775-124">Om du vill aktivera automatisk skalning</span><span class="sxs-lookup"><span data-stu-id="f8775-124">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="f8775-125">-EnableRbac</span><span class="sxs-lookup"><span data-stu-id="f8775-125">-EnableRbac</span></span>
<span data-ttu-id="f8775-126">Om du vill aktivera Kubernetes Role-Based Access</span><span class="sxs-lookup"><span data-stu-id="f8775-126">Whether to enable Kubernetes Role-Based Access</span></span>

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

### <span data-ttu-id="f8775-127">-Force</span><span class="sxs-lookup"><span data-stu-id="f8775-127">-Force</span></span>
<span data-ttu-id="f8775-128">Skapa kluster även om det redan finns</span><span class="sxs-lookup"><span data-stu-id="f8775-128">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="f8775-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="f8775-129">-GenerateSshKey</span></span>
<span data-ttu-id="f8775-130">Skapa SSH Key-filen till {HOME}/.ssh/id_rsa.</span><span class="sxs-lookup"><span data-stu-id="f8775-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

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

### <span data-ttu-id="f8775-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="f8775-131">-KubernetesVersion</span></span>
<span data-ttu-id="f8775-132">Den version av Kubernetes som ska användas för att skapa klustret.</span><span class="sxs-lookup"><span data-stu-id="f8775-132">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="f8775-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="f8775-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="f8775-134">Användar namn för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="f8775-134">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="f8775-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="f8775-135">-LoadBalancerSku</span></span>
<span data-ttu-id="f8775-136">SKU för det hanterade klustret.</span><span class="sxs-lookup"><span data-stu-id="f8775-136">The load balancer sku for the managed cluster.</span></span>

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

### <span data-ttu-id="f8775-137">-Plats</span><span class="sxs-lookup"><span data-stu-id="f8775-137">-Location</span></span>
<span data-ttu-id="f8775-138">Azure-plats för klustret.</span><span class="sxs-lookup"><span data-stu-id="f8775-138">Azure location for the cluster.</span></span>
<span data-ttu-id="f8775-139">Som standard anges resurs gruppens plats.</span><span class="sxs-lookup"><span data-stu-id="f8775-139">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="f8775-140">-Namn</span><span class="sxs-lookup"><span data-stu-id="f8775-140">-Name</span></span>
<span data-ttu-id="f8775-141">Kubernetes hanterat kluster namn.</span><span class="sxs-lookup"><span data-stu-id="f8775-141">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="f8775-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="f8775-142">-NetworkPlugin</span></span>
<span data-ttu-id="f8775-143">Nätverks-plugin som används för att bygga Kubernetes nätverk.</span><span class="sxs-lookup"><span data-stu-id="f8775-143">Network plugin used for building Kubernetes network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: azure
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8775-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="f8775-144">-NodeCount</span></span>
<span data-ttu-id="f8775-145">Standardvärdet för noder för nodkonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="f8775-145">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="f8775-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="f8775-146">-NodeMaxCount</span></span>
<span data-ttu-id="f8775-147">Maximalt antal noder för automatisk skalning</span><span class="sxs-lookup"><span data-stu-id="f8775-147">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="f8775-148">-NodeMaxPodCount</span><span class="sxs-lookup"><span data-stu-id="f8775-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="f8775-149">Maximalt antal Pods som kan köras på noden.</span><span class="sxs-lookup"><span data-stu-id="f8775-149">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="f8775-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="f8775-150">-NodeMinCount</span></span>
<span data-ttu-id="f8775-151">Minsta antal noder för automatisk skalning.</span><span class="sxs-lookup"><span data-stu-id="f8775-151">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="f8775-152">-Nodnamn</span><span class="sxs-lookup"><span data-stu-id="f8775-152">-NodeName</span></span>
<span data-ttu-id="f8775-153">Unikt namn på mediepoolen i kontexten för prenumerations-och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f8775-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="f8775-154">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="f8775-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="f8775-155">Storlek i GB på OS-disken för varje nod i noduppsättningen.</span><span class="sxs-lookup"><span data-stu-id="f8775-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="f8775-156">Minst 30 GB.</span><span class="sxs-lookup"><span data-stu-id="f8775-156">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="f8775-157">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="f8775-157">-NodePoolMode</span></span>
<span data-ttu-id="f8775-158">NodePoolMode representerar ett läge för en noduppsättning.</span><span class="sxs-lookup"><span data-stu-id="f8775-158">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="f8775-159">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="f8775-159">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="f8775-160">ScaleSetEvictionPolicy ska användas för att ange borttagnings princip för skalnings uppsättning för den virtuella datorns Pro.</span><span class="sxs-lookup"><span data-stu-id="f8775-160">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="f8775-161">Standard för att ta bort.</span><span class="sxs-lookup"><span data-stu-id="f8775-161">Default to Delete.</span></span>

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

### <span data-ttu-id="f8775-162">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="f8775-162">-NodeSetPriority</span></span>
<span data-ttu-id="f8775-163">ScaleSetPriority används för att ange prioritet för den virtuella datorns skalnings uppsättning.</span><span class="sxs-lookup"><span data-stu-id="f8775-163">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="f8775-164">Standard är normal.</span><span class="sxs-lookup"><span data-stu-id="f8775-164">Default to regular.</span></span>

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

### <span data-ttu-id="f8775-165">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="f8775-165">-NodeVmSetType</span></span>
<span data-ttu-id="f8775-166">AgentPoolType representerar typer av en programpool.</span><span class="sxs-lookup"><span data-stu-id="f8775-166">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="f8775-167">Möjliga värden är: ' VirtualMachineScaleSets ', ' AvailabilitySet '</span><span class="sxs-lookup"><span data-stu-id="f8775-167">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: VirtualMachineScaleSets
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8775-168">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="f8775-168">-NodeVmSize</span></span>
<span data-ttu-id="f8775-169">Den virtuella datorns storlek.</span><span class="sxs-lookup"><span data-stu-id="f8775-169">The size of the Virtual Machine.</span></span> <span data-ttu-id="f8775-170">Standardvärdet är Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="f8775-170">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="f8775-171">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="f8775-171">-NodeVnetSubnetID</span></span>
<span data-ttu-id="f8775-172">VNet-SubnetID anger VNet-nätmask.</span><span class="sxs-lookup"><span data-stu-id="f8775-172">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="f8775-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8775-173">-ResourceGroupName</span></span>
<span data-ttu-id="f8775-174">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="f8775-174">Resource Group Name.</span></span>

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

### <span data-ttu-id="f8775-175">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="f8775-175">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="f8775-176">Det klient-ID och den klient hemlighet som är kopplad till AAD-programmet/tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="f8775-176">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="f8775-177">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="f8775-177">-SshKeyValue</span></span>
<span data-ttu-id="f8775-178">Fil värde för SSH-nyckel eller sökväg till nyckel fil.</span><span class="sxs-lookup"><span data-stu-id="f8775-178">SSH key file value or key file path.</span></span>
<span data-ttu-id="f8775-179">Standardvärdet är {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="f8775-179">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="f8775-180">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="f8775-180">-SubnetName</span></span>
<span data-ttu-id="f8775-181">VirtualNode addon-namn.</span><span class="sxs-lookup"><span data-stu-id="f8775-181">Subnet name of VirtualNode addon.</span></span>

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

### <span data-ttu-id="f8775-182">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f8775-182">-Tag</span></span>
<span data-ttu-id="f8775-183">Taggar som ska tillämpas på resursen</span><span class="sxs-lookup"><span data-stu-id="f8775-183">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="f8775-184">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="f8775-184">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="f8775-185">Det administratörs användar namn som ska användas för Windows VMs.</span><span class="sxs-lookup"><span data-stu-id="f8775-185">The administrator username to use for Windows VMs.</span></span>

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

### <span data-ttu-id="f8775-186">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="f8775-186">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="f8775-187">Det administratörs lösen ord som ska användas för Windows-VMs och dess längd måste vara minst 12 som innehåller minst ett gement tecken, d.v.s. `[a-z]` ett `[A-Z]` och ett specialtecken `[!@#$%^&_()]` .</span><span class="sxs-lookup"><span data-stu-id="f8775-187">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&_()]`.</span></span>

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

### <span data-ttu-id="f8775-188">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="f8775-188">-WorkspaceResourceId</span></span>
<span data-ttu-id="f8775-189">Resurs-ID för arbets ytan som övervakar addon.</span><span class="sxs-lookup"><span data-stu-id="f8775-189">Resource Id of the workspace of Monitoring addon.</span></span>

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

### <span data-ttu-id="f8775-190">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f8775-190">-Confirm</span></span>
<span data-ttu-id="f8775-191">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f8775-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8775-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8775-192">-WhatIf</span></span>
<span data-ttu-id="f8775-193">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f8775-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8775-194">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f8775-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8775-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8775-195">CommonParameters</span></span>
<span data-ttu-id="f8775-196">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8775-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8775-197">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8775-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8775-198">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f8775-198">INPUTS</span></span>

### <span data-ttu-id="f8775-199">Ingen</span><span class="sxs-lookup"><span data-stu-id="f8775-199">None</span></span>

## <span data-ttu-id="f8775-200">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f8775-200">OUTPUTS</span></span>

### <span data-ttu-id="f8775-201">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="f8775-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="f8775-202">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f8775-202">NOTES</span></span>

## <span data-ttu-id="f8775-203">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f8775-203">RELATED LINKS</span></span>
