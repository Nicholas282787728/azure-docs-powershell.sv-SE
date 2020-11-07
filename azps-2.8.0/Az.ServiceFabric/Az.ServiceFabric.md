---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: d94e7001df730b22fb900b284c6fac47b5d81b8b
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/15/2019
ms.locfileid: "93743330"
---
# <span data-ttu-id="a36cc-101">Modulen AZ. ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a36cc-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="a36cc-102">Problembeskrivning</span><span class="sxs-lookup"><span data-stu-id="a36cc-102">Description</span></span>
<span data-ttu-id="a36cc-103">Modul för Azure Service Fabric som du kan använda för att automatisera slut 2-avsluta-åtgärderna som att skapa ett säkert kluster, rulla över kluster certifikat, lägga till eller ta bort noder från klustret osv. Den fullständiga listan över alla åtgärder visas nedan.</span><span class="sxs-lookup"><span data-stu-id="a36cc-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="a36cc-104">AZ. ServiceFabric-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a36cc-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="a36cc-105">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="a36cc-105">Add-AzServiceFabricApplicationCertificate</span></span>](Add-AzServiceFabricApplicationCertificate.md)
<span data-ttu-id="a36cc-106">Lägg till ett nytt certifikat till den virtuella datorns skal uppsättning (er) som utgör klustret.</span><span class="sxs-lookup"><span data-stu-id="a36cc-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="a36cc-107">Certifikatet är avsett att användas som ett program certifikat.</span><span class="sxs-lookup"><span data-stu-id="a36cc-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="a36cc-108">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a36cc-108">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="a36cc-109">Lägg till vanligt namn eller tumavtryck i klustret för användning av klientautentisering.</span><span class="sxs-lookup"><span data-stu-id="a36cc-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="a36cc-110">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="a36cc-110">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="a36cc-111">Lägg till ett sekundärt kluster certifikat i klustret.</span><span class="sxs-lookup"><span data-stu-id="a36cc-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="a36cc-112">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="a36cc-112">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="a36cc-113">Lägga till noder till den specifika nodtypen i klustret.</span><span class="sxs-lookup"><span data-stu-id="a36cc-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="a36cc-114">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="a36cc-114">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="a36cc-115">Lägg till en ny nodtyp i det befintliga klustret.</span><span class="sxs-lookup"><span data-stu-id="a36cc-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="a36cc-116">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a36cc-116">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="a36cc-117">Få information om tjänstens Fabric-program.</span><span class="sxs-lookup"><span data-stu-id="a36cc-117">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="a36cc-118">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a36cc-118">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="a36cc-119">Information om hur du skaffar Service Fabric-programmet.</span><span class="sxs-lookup"><span data-stu-id="a36cc-119">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="a36cc-120">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a36cc-120">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="a36cc-121">Hämta versions information för Service Fabric program typ.</span><span class="sxs-lookup"><span data-stu-id="a36cc-121">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="a36cc-122">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="a36cc-122">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="a36cc-123">Hämta information om kluster resursen.</span><span class="sxs-lookup"><span data-stu-id="a36cc-123">Get the cluster resource details.</span></span>

### [<span data-ttu-id="a36cc-124">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="a36cc-124">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="a36cc-125">Få information om tjänstens infrastruktur tjänst under angiven program och ett kluster.</span><span class="sxs-lookup"><span data-stu-id="a36cc-125">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="a36cc-126">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a36cc-126">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="a36cc-127">Skapa ett nytt tjänst Fabric-program under den angivna resurs gruppen och klustret.</span><span class="sxs-lookup"><span data-stu-id="a36cc-127">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="a36cc-128">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a36cc-128">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="a36cc-129">Skapa en ny program typ för tjänst Fabric under den angivna resurs gruppen och klustret.</span><span class="sxs-lookup"><span data-stu-id="a36cc-129">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="a36cc-130">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a36cc-130">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="a36cc-131">Skapa en ny program typs version under den angivna resurs gruppen och klustret.</span><span class="sxs-lookup"><span data-stu-id="a36cc-131">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="a36cc-132">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="a36cc-132">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="a36cc-133">I det här kommandot används certifikat som du tillhandahåller eller systemgenererade självsignerade certifikat för att skapa ett nytt tjänst Fabric-kluster.</span><span class="sxs-lookup"><span data-stu-id="a36cc-133">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="a36cc-134">Den kan använda en standardmall eller en anpassad mall som du anger.</span><span class="sxs-lookup"><span data-stu-id="a36cc-134">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="a36cc-135">Du kan välja att ange en mapp att exportera självsignerade certifikat till eller hämta dem senare från huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="a36cc-135">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="a36cc-136">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="a36cc-136">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="a36cc-137">Skapa en ny tjänst infrastruktur tjänst under det angivna programmet och klustret.</span><span class="sxs-lookup"><span data-stu-id="a36cc-137">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="a36cc-138">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a36cc-138">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="a36cc-139">Ta bort ett program från klustret.</span><span class="sxs-lookup"><span data-stu-id="a36cc-139">Remove an application from the cluster.</span></span> <span data-ttu-id="a36cc-140">Detta tar bort alla tjänster under programmet.</span><span class="sxs-lookup"><span data-stu-id="a36cc-140">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="a36cc-141">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a36cc-141">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="a36cc-142">Ta bort tjänstens infrastruktur program typ från klustret.</span><span class="sxs-lookup"><span data-stu-id="a36cc-142">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="a36cc-143">Detta tar bort alla typ versioner under den här resursen.</span><span class="sxs-lookup"><span data-stu-id="a36cc-143">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="a36cc-144">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a36cc-144">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="a36cc-145">Ta bort Service Fabric en program typ version från klustret.</span><span class="sxs-lookup"><span data-stu-id="a36cc-145">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="a36cc-146">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a36cc-146">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="a36cc-147">Ta bort ett eller flera klient certifikat eller certifikat subjekt namn som används för klientautentisering till klustret.</span><span class="sxs-lookup"><span data-stu-id="a36cc-147">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="a36cc-148">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="a36cc-148">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="a36cc-149">Ta bort ett kluster certifikat från att användas för kluster säkerhet.</span><span class="sxs-lookup"><span data-stu-id="a36cc-149">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="a36cc-150">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="a36cc-150">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="a36cc-151">Ta bort noder från en viss nodtyp från ett kluster.</span><span class="sxs-lookup"><span data-stu-id="a36cc-151">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="a36cc-152">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="a36cc-152">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="a36cc-153">Ta bort en fullständig nodtyp från ett kluster.</span><span class="sxs-lookup"><span data-stu-id="a36cc-153">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="a36cc-154">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="a36cc-154">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="a36cc-155">Ta bort en tjänst från klustret.</span><span class="sxs-lookup"><span data-stu-id="a36cc-155">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="a36cc-156">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="a36cc-156">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="a36cc-157">Ta bort en eller flera tjänst Fabric-inställningar från klustret.</span><span class="sxs-lookup"><span data-stu-id="a36cc-157">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="a36cc-158">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="a36cc-158">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="a36cc-159">Lägga till eller uppdatera en eller flera tjänst infrastruktur inställningar i klustret.</span><span class="sxs-lookup"><span data-stu-id="a36cc-159">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="a36cc-160">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="a36cc-160">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="a36cc-161">Ändra kluster för Service Fabric-uppgradering.</span><span class="sxs-lookup"><span data-stu-id="a36cc-161">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="a36cc-162">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a36cc-162">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="a36cc-163">Uppdatera ett tjänst Fabric-program.</span><span class="sxs-lookup"><span data-stu-id="a36cc-163">Update a service fabric application.</span></span> <span data-ttu-id="a36cc-164">Då kan du uppdatera program parametrarna och/eller uppgradera program typs versionen som utlöser en program uppgradering.</span><span class="sxs-lookup"><span data-stu-id="a36cc-164">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="a36cc-165">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="a36cc-165">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="a36cc-166">Uppdatera livs längden eller VmSku för en nodtyp i klustret.</span><span class="sxs-lookup"><span data-stu-id="a36cc-166">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="a36cc-167">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="a36cc-167">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="a36cc-168">Uppdatera Tillförlitlighets nivån för den primära nodtypen i ett kluster.</span><span class="sxs-lookup"><span data-stu-id="a36cc-168">Update the reliability tier of the primary node type in a cluster.</span></span>

