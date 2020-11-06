---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 6d93775a028e7a590a8da9cc008640fb8484bdf2
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/23/2019
ms.locfileid: "93570695"
---
# <span data-ttu-id="6284b-101">Modulen AzureRM. ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6284b-101">AzureRM.ServiceFabric Module</span></span>
## <span data-ttu-id="6284b-102">Problembeskrivning</span><span class="sxs-lookup"><span data-stu-id="6284b-102">Description</span></span>
<span data-ttu-id="6284b-103">Modul för Azure Service Fabric som du kan använda för att automatisera slut 2-avsluta-åtgärderna som att skapa ett säkert kluster, rulla över kluster certifikat, lägga till eller ta bort noder från klustret osv. Den fullständiga listan över alla åtgärder visas nedan.</span><span class="sxs-lookup"><span data-stu-id="6284b-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="6284b-104">AzureRM. ServiceFabric-cmdletar</span><span class="sxs-lookup"><span data-stu-id="6284b-104">AzureRM.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="6284b-105">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="6284b-105">Add-AzureRmServiceFabricApplicationCertificate</span></span>](Add-AzureRmServiceFabricApplicationCertificate.md)
<span data-ttu-id="6284b-106">Lägg till ett nytt certifikat till den virtuella datorns skal uppsättning (er) som utgör klustret.</span><span class="sxs-lookup"><span data-stu-id="6284b-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="6284b-107">Certifikatet är avsett att användas som ett program certifikat.</span><span class="sxs-lookup"><span data-stu-id="6284b-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="6284b-108">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6284b-108">Add-AzureRmServiceFabricClientCertificate</span></span>](Add-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="6284b-109">Lägg till vanligt namn eller tumavtryck i klustret för användning av klientautentisering.</span><span class="sxs-lookup"><span data-stu-id="6284b-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="6284b-110">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="6284b-110">Add-AzureRmServiceFabricClusterCertificate</span></span>](Add-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="6284b-111">Lägg till ett sekundärt kluster certifikat i klustret.</span><span class="sxs-lookup"><span data-stu-id="6284b-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="6284b-112">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="6284b-112">Add-AzureRmServiceFabricNode</span></span>](Add-AzureRmServiceFabricNode.md)
<span data-ttu-id="6284b-113">Lägga till noder till den specifika nodtypen i klustret.</span><span class="sxs-lookup"><span data-stu-id="6284b-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="6284b-114">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="6284b-114">Add-AzureRmServiceFabricNodeType</span></span>](Add-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="6284b-115">Lägg till en ny nodtyp i det befintliga klustret.</span><span class="sxs-lookup"><span data-stu-id="6284b-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="6284b-116">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="6284b-116">Get-AzureRmServiceFabricCluster</span></span>](Get-AzureRmServiceFabricCluster.md)
<span data-ttu-id="6284b-117">Hämta information om kluster resursen.</span><span class="sxs-lookup"><span data-stu-id="6284b-117">Get the cluster resource details.</span></span>

### [<span data-ttu-id="6284b-118">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="6284b-118">New-AzureRmServiceFabricCluster</span></span>](New-AzureRmServiceFabricCluster.md)
<span data-ttu-id="6284b-119">I det här kommandot används certifikat som du tillhandahåller eller systemgenererade självsignerade certifikat för att skapa ett nytt tjänst Fabric-kluster.</span><span class="sxs-lookup"><span data-stu-id="6284b-119">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="6284b-120">Den kan använda en standardmall eller en anpassad mall som du anger.</span><span class="sxs-lookup"><span data-stu-id="6284b-120">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="6284b-121">Du kan välja att ange en mapp att exportera självsignerade certifikat till eller hämta dem senare från huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="6284b-121">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="6284b-122">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6284b-122">Remove-AzureRmServiceFabricClientCertificate</span></span>](Remove-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="6284b-123">Ta bort ett eller flera klient certifikat eller certifikat subjekt namn som används för klientautentisering till klustret.</span><span class="sxs-lookup"><span data-stu-id="6284b-123">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="6284b-124">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="6284b-124">Remove-AzureRmServiceFabricClusterCertificate</span></span>](Remove-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="6284b-125">Ta bort ett kluster certifikat från att användas för kluster säkerhet.</span><span class="sxs-lookup"><span data-stu-id="6284b-125">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="6284b-126">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="6284b-126">Remove-AzureRmServiceFabricNode</span></span>](Remove-AzureRmServiceFabricNode.md)
<span data-ttu-id="6284b-127">Ta bort noder från en viss nodtyp från ett kluster.</span><span class="sxs-lookup"><span data-stu-id="6284b-127">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="6284b-128">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="6284b-128">Remove-AzureRmServiceFabricNodeType</span></span>](Remove-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="6284b-129">Ta bort en fullständig nodtyp från ett kluster.</span><span class="sxs-lookup"><span data-stu-id="6284b-129">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="6284b-130">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="6284b-130">Remove-AzureRmServiceFabricSetting</span></span>](Remove-AzureRmServiceFabricSetting.md)
<span data-ttu-id="6284b-131">Ta bort en eller flera tjänst Fabric-inställningar från klustret.</span><span class="sxs-lookup"><span data-stu-id="6284b-131">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="6284b-132">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="6284b-132">Set-AzureRmServiceFabricSetting</span></span>](Set-AzureRmServiceFabricSetting.md)
<span data-ttu-id="6284b-133">Lägga till eller uppdatera en eller flera tjänst infrastruktur inställningar i klustret.</span><span class="sxs-lookup"><span data-stu-id="6284b-133">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="6284b-134">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="6284b-134">Set-AzureRmServiceFabricUpgradeType</span></span>](Set-AzureRmServiceFabricUpgradeType.md)
<span data-ttu-id="6284b-135">Ändra kluster för Service Fabric-uppgradering.</span><span class="sxs-lookup"><span data-stu-id="6284b-135">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="6284b-136">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="6284b-136">Update-AzureRmServiceFabricDurability</span></span>](Update-AzureRmServiceFabricDurability.md)
<span data-ttu-id="6284b-137">Uppdatera livs längden eller VmSku för en nodtyp i klustret.</span><span class="sxs-lookup"><span data-stu-id="6284b-137">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="6284b-138">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="6284b-138">Update-AzureRmServiceFabricReliability</span></span>](Update-AzureRmServiceFabricReliability.md)
<span data-ttu-id="6284b-139">Uppdatera Tillförlitlighets nivån för den primära nodtypen i ett kluster.</span><span class="sxs-lookup"><span data-stu-id="6284b-139">Update the reliability tier of the primary node type in a cluster.</span></span>

