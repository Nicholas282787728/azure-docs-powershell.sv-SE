---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/set-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Set-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Set-AzureRmAks.md
ms.openlocfilehash: b5d3248c81507abf6092aa4354691975c4b4bc13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575406"
---
# <span data-ttu-id="17f13-101">Set-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="17f13-101">Set-AzureRmAks</span></span>

## <span data-ttu-id="17f13-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="17f13-102">SYNOPSIS</span></span>
<span data-ttu-id="17f13-103">Uppdatera eller skapa ett hanterat Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="17f13-103">Update or create a managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17f13-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="17f13-104">SYNTAX</span></span>

### <span data-ttu-id="17f13-105">defaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="17f13-105">defaultParameterSet (Default)</span></span>
```
Set-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17f13-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="17f13-106">InputObjectParameterSet</span></span>
```
Set-AzureRmAks -InputObject <PSKubernetesCluster> [-Location <String>] [-AdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17f13-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="17f13-107">IdParameterSet</span></span>
```
Set-AzureRmAks [-Id] <String> [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>]
 [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>]
 [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17f13-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="17f13-108">DESCRIPTION</span></span>
<span data-ttu-id="17f13-109">Uppdatera eller skapa ett hanterat Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="17f13-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="17f13-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="17f13-110">EXAMPLES</span></span>

### <span data-ttu-id="17f13-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="17f13-111">Example 1</span></span>
```
PS C:\> Get-AzureRmAks -ResourceGroupName group -Name myCluster | Set-AzureRmAks -NodeCount 5
```

<span data-ttu-id="17f13-112">Ange antalet noder i Kubernetes-klustret till 5.</span><span class="sxs-lookup"><span data-stu-id="17f13-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="17f13-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="17f13-113">PARAMETERS</span></span>

### <span data-ttu-id="17f13-114">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="17f13-114">-AdminUserName</span></span>
<span data-ttu-id="17f13-115">Användar namn för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="17f13-115">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="17f13-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17f13-116">-AsJob</span></span>
<span data-ttu-id="17f13-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="17f13-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="17f13-118">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="17f13-118">-ClientIdAndSecret</span></span>
<span data-ttu-id="17f13-119">Det klient-ID och den klient hemlighet som är kopplad till AAD-programmet/tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="17f13-119">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="17f13-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17f13-120">-DefaultProfile</span></span>
<span data-ttu-id="17f13-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="17f13-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17f13-122">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="17f13-122">-DnsNamePrefix</span></span>
<span data-ttu-id="17f13-123">DNS-namnets prefix för klustret.</span><span class="sxs-lookup"><span data-stu-id="17f13-123">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="17f13-124">-ID</span><span class="sxs-lookup"><span data-stu-id="17f13-124">-Id</span></span>
<span data-ttu-id="17f13-125">ID för ett hanterat Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="17f13-125">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="17f13-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17f13-126">-InputObject</span></span>
<span data-ttu-id="17f13-127">Ett PSKubernetesCluster-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="17f13-127">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="17f13-128">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="17f13-128">-KubernetesVersion</span></span>
<span data-ttu-id="17f13-129">Den version av Kubernetes som ska användas för att skapa klustret.</span><span class="sxs-lookup"><span data-stu-id="17f13-129">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="17f13-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="17f13-130">-Location</span></span>
<span data-ttu-id="17f13-131">Azure-plats för klustret.</span><span class="sxs-lookup"><span data-stu-id="17f13-131">Azure location for the cluster.</span></span>
<span data-ttu-id="17f13-132">Som standard anges resurs gruppens plats.</span><span class="sxs-lookup"><span data-stu-id="17f13-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="17f13-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="17f13-133">-Name</span></span>
<span data-ttu-id="17f13-134">Kubernetes hanterat kluster namn.</span><span class="sxs-lookup"><span data-stu-id="17f13-134">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="17f13-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="17f13-135">-NodeCount</span></span>
<span data-ttu-id="17f13-136">Standardvärdet för noder för nodkonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="17f13-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="17f13-137">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="17f13-137">-NodeOsDiskSize</span></span>
<span data-ttu-id="17f13-138">Standardvärdet för noder för nodkonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="17f13-138">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="17f13-139">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="17f13-139">-NodeVmSize</span></span>
<span data-ttu-id="17f13-140">Den virtuella datorns storlek.</span><span class="sxs-lookup"><span data-stu-id="17f13-140">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="17f13-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17f13-141">-ResourceGroupName</span></span>
<span data-ttu-id="17f13-142">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="17f13-142">Resource Group Name.</span></span>

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

### <span data-ttu-id="17f13-143">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="17f13-143">-SshKeyValue</span></span>
<span data-ttu-id="17f13-144">Fil värde för SSH-nyckel eller sökväg till nyckel fil.</span><span class="sxs-lookup"><span data-stu-id="17f13-144">SSH key file value or key file path.</span></span>
<span data-ttu-id="17f13-145">Standardvärdet är {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="17f13-145">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="17f13-146">-Tagg</span><span class="sxs-lookup"><span data-stu-id="17f13-146">-Tag</span></span>
<span data-ttu-id="17f13-147">Taggar som ska tillämpas på resursen</span><span class="sxs-lookup"><span data-stu-id="17f13-147">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="17f13-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="17f13-148">-Confirm</span></span>
<span data-ttu-id="17f13-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="17f13-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17f13-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17f13-150">-WhatIf</span></span>
<span data-ttu-id="17f13-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="17f13-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17f13-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="17f13-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17f13-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17f13-153">CommonParameters</span></span>
<span data-ttu-id="17f13-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17f13-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17f13-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17f13-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17f13-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="17f13-156">INPUTS</span></span>

### <span data-ttu-id="17f13-157">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="17f13-157">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="17f13-158">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="17f13-158">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="17f13-159">System. String</span><span class="sxs-lookup"><span data-stu-id="17f13-159">System.String</span></span>

## <span data-ttu-id="17f13-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="17f13-160">OUTPUTS</span></span>

### <span data-ttu-id="17f13-161">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="17f13-161">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="17f13-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="17f13-162">NOTES</span></span>

## <span data-ttu-id="17f13-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="17f13-163">RELATED LINKS</span></span>