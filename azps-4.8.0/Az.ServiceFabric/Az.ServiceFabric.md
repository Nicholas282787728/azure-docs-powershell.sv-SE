---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 6c58f25209a0acd227e2f04e7ca808916f283d46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103514"
---
# <span data-ttu-id="dd5ff-101">Modulen AZ. ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dd5ff-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="dd5ff-102">Problembeskrivning</span><span class="sxs-lookup"><span data-stu-id="dd5ff-102">Description</span></span>
<span data-ttu-id="dd5ff-103">Modul för Azure Service Fabric som du kan använda för att automatisera slut 2-avsluta-åtgärderna som att skapa ett säkert kluster, rulla över kluster certifikat, lägga till eller ta bort noder från klustret osv. Den fullständiga listan över alla åtgärder visas nedan.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="dd5ff-104">AZ. ServiceFabric-cmdletar</span><span class="sxs-lookup"><span data-stu-id="dd5ff-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="dd5ff-105">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="dd5ff-105">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="dd5ff-106">Lägg till vanligt namn eller tumavtryck i klustret för användning av klientautentisering.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-106">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="dd5ff-107">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="dd5ff-107">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="dd5ff-108">Lägg till ett sekundärt kluster certifikat i klustret.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-108">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="dd5ff-109">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="dd5ff-109">Add-AzServiceFabricManagedClusterClientCertificate</span></span>](Add-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="dd5ff-110">Lägg till certifikatets namn eller tumavtryck i klustret.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-110">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="dd5ff-111">Detta registrerar certifikatet igen i klustret för klientautentisering.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-111">This will register the certificate agains the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="dd5ff-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="dd5ff-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="dd5ff-113">Lägg till virtuellt dator tillägg till nodtypen.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-113">Add vm extension to the node type.</span></span>

### [<span data-ttu-id="dd5ff-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="dd5ff-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
<span data-ttu-id="dd5ff-115">Lägg till certifikat hemlighet till nodtyp.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-115">Add certificate secret to the node type.</span></span>

### [<span data-ttu-id="dd5ff-116">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="dd5ff-116">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="dd5ff-117">Lägga till noder till den specifika nodtypen i klustret.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-117">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="dd5ff-118">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="dd5ff-118">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="dd5ff-119">Lägg till en ny nodtyp i det befintliga klustret.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-119">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="dd5ff-120">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="dd5ff-120">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="dd5ff-121">Få information om tjänstens Fabric-program.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-121">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="dd5ff-122">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="dd5ff-122">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="dd5ff-123">Information om hur du skaffar Service Fabric-programmet.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-123">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="dd5ff-124">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="dd5ff-124">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="dd5ff-125">Hämta versions information för Service Fabric program typ.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-125">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="dd5ff-126">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="dd5ff-126">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="dd5ff-127">Hämta information om kluster resursen.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-127">Get the cluster resource details.</span></span>

### [<span data-ttu-id="dd5ff-128">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="dd5ff-128">Get-AzServiceFabricManagedCluster</span></span>](Get-AzServiceFabricManagedCluster.md)
<span data-ttu-id="dd5ff-129">Få information om de hanterade kluster resurserna.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-129">Get the managed cluster resource details.</span></span>

### [<span data-ttu-id="dd5ff-130">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="dd5ff-130">Get-AzServiceFabricManagedNodeType</span></span>](Get-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="dd5ff-131">Hämta resursinformation för hanterad nod.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-131">Get the managed node type resource details.</span></span>

### [<span data-ttu-id="dd5ff-132">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="dd5ff-132">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="dd5ff-133">Få information om tjänstens infrastruktur tjänst under angiven program och ett kluster.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-133">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="dd5ff-134">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="dd5ff-134">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="dd5ff-135">Skapa ett nytt tjänst Fabric-program under den angivna resurs gruppen och klustret.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-135">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="dd5ff-136">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="dd5ff-136">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="dd5ff-137">Skapa en ny program typ för tjänst Fabric under den angivna resurs gruppen och klustret.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-137">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="dd5ff-138">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="dd5ff-138">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="dd5ff-139">Skapa en ny program typs version under den angivna resurs gruppen och klustret.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-139">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="dd5ff-140">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="dd5ff-140">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="dd5ff-141">I det här kommandot används certifikat som du tillhandahåller eller systemgenererade självsignerade certifikat för att skapa ett nytt tjänst Fabric-kluster.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-141">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="dd5ff-142">Den kan använda en standardmall eller en anpassad mall som du anger.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-142">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="dd5ff-143">Du kan välja att ange en mapp att exportera självsignerade certifikat till eller hämta dem senare från huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-143">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

### [<span data-ttu-id="dd5ff-144">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="dd5ff-144">New-AzServiceFabricManagedCluster</span></span>](New-AzServiceFabricManagedCluster.md)
<span data-ttu-id="dd5ff-145">Skapa ett nytt hanterat kluster.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-145">Create new managed cluster.</span></span>

### [<span data-ttu-id="dd5ff-146">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="dd5ff-146">New-AzServiceFabricManagedNodeType</span></span>](New-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="dd5ff-147">Skapa en ny resurs för nodtyp.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-147">Create new node type resource.</span></span>

### [<span data-ttu-id="dd5ff-148">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="dd5ff-148">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="dd5ff-149">Skapa en ny tjänst infrastruktur tjänst under det angivna programmet och klustret.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-149">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="dd5ff-150">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="dd5ff-150">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="dd5ff-151">Ta bort ett program från klustret.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-151">Remove an application from the cluster.</span></span> <span data-ttu-id="dd5ff-152">Detta tar bort alla tjänster under programmet.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-152">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="dd5ff-153">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="dd5ff-153">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="dd5ff-154">Ta bort tjänstens infrastruktur program typ från klustret.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-154">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="dd5ff-155">Detta tar bort alla typ versioner under den här resursen.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-155">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="dd5ff-156">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="dd5ff-156">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="dd5ff-157">Ta bort Service Fabric en program typ version från klustret.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-157">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="dd5ff-158">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="dd5ff-158">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="dd5ff-159">Ta bort ett eller flera klient certifikat eller certifikat subjekt namn som används för klientautentisering till klustret.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-159">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="dd5ff-160">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="dd5ff-160">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="dd5ff-161">Ta bort ett kluster certifikat från att användas för kluster säkerhet.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-161">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="dd5ff-162">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="dd5ff-162">Remove-AzServiceFabricManagedCluster</span></span>](Remove-AzServiceFabricManagedCluster.md)
<span data-ttu-id="dd5ff-163">Ta bort en kluster resurs.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-163">Remove cluster resource.</span></span>

### [<span data-ttu-id="dd5ff-164">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="dd5ff-164">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>](Remove-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="dd5ff-165">Remvoe klient certifikat via tumavtryck eller eget namn.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-165">Remvoe client certificate by thumbprint or common name.</span></span>

### [<span data-ttu-id="dd5ff-166">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="dd5ff-166">Remove-AzServiceFabricManagedNodeType</span></span>](Remove-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="dd5ff-167">Ta bort nodtypen eller specifika noder inom nodtypen.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-167">Remove the node type or specific nodes within the node type.</span></span>

### [<span data-ttu-id="dd5ff-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="dd5ff-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="dd5ff-169">Ta bort virtuellt dator tillägg från nodtyp.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-169">Remove vm extension from the node type.</span></span>

### [<span data-ttu-id="dd5ff-170">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="dd5ff-170">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="dd5ff-171">Ta bort noder från en viss nodtyp från ett kluster.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-171">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="dd5ff-172">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="dd5ff-172">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="dd5ff-173">Ta bort en fullständig nodtyp från ett kluster.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-173">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="dd5ff-174">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="dd5ff-174">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="dd5ff-175">Ta bort en tjänst från klustret.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-175">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="dd5ff-176">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="dd5ff-176">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="dd5ff-177">Ta bort en eller flera tjänst Fabric-inställningar från klustret.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-177">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="dd5ff-178">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="dd5ff-178">Restart-AzServiceFabricManagedNodeType</span></span>](Restart-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="dd5ff-179">Starta om specifika noder från nodtypen.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-179">Restart specific nodes from the node type.</span></span>

### [<span data-ttu-id="dd5ff-180">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="dd5ff-180">Set-AzServiceFabricManagedCluster</span></span>](Set-AzServiceFabricManagedCluster.md)
<span data-ttu-id="dd5ff-181">Ange egenskaper för en kluster resurs.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-181">Set cluster resource properties.</span></span>

### [<span data-ttu-id="dd5ff-182">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="dd5ff-182">Set-AzServiceFabricManagedNodeType</span></span>](Set-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="dd5ff-183">Anger resurs egenskaper för nodtyp eller kör återavbildnings åtgärder för specifika NDES för noden nodtyp med-Rebild.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-183">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

### [<span data-ttu-id="dd5ff-184">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="dd5ff-184">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="dd5ff-185">Lägga till eller uppdatera en eller flera tjänst infrastruktur inställningar i klustret.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-185">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="dd5ff-186">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="dd5ff-186">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="dd5ff-187">Ändra kluster för Service Fabric-uppgradering.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-187">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="dd5ff-188">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="dd5ff-188">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="dd5ff-189">Uppdatera ett tjänst Fabric-program.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-189">Update a service fabric application.</span></span> <span data-ttu-id="dd5ff-190">Då kan du uppdatera program parametrarna och/eller uppgradera program typs versionen som utlöser en program uppgradering.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-190">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="dd5ff-191">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="dd5ff-191">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="dd5ff-192">Uppdatera livs längden eller VmSku för en nodtyp i klustret.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-192">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="dd5ff-193">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="dd5ff-193">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="dd5ff-194">Uppdatera Tillförlitlighets nivån för den primära nodtypen i ett kluster.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-194">Update the reliability tier of the primary node type in a cluster.</span></span>

