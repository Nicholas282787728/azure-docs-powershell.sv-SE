---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 01bf8c630f4fc4d137e98be5b1996eaf47ea3363
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/23/2019
ms.locfileid: "93743139"
---
# <span data-ttu-id="2c982-101">Modulen AZ. ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2c982-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="2c982-102">Problembeskrivning</span><span class="sxs-lookup"><span data-stu-id="2c982-102">Description</span></span>
<span data-ttu-id="2c982-103">Modul för Azure Service Fabric som du kan använda för att automatisera slut 2-avsluta-åtgärderna som att skapa ett säkert kluster, rulla över kluster certifikat, lägga till eller ta bort noder från klustret osv. Den fullständiga listan över alla åtgärder visas nedan.</span><span class="sxs-lookup"><span data-stu-id="2c982-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="2c982-104">AZ. ServiceFabric-cmdletar</span><span class="sxs-lookup"><span data-stu-id="2c982-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="2c982-105">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="2c982-105">Add-AzServiceFabricApplicationCertificate</span></span>](Add-AzServiceFabricApplicationCertificate.md)
<span data-ttu-id="2c982-106">Lägg till ett nytt certifikat till den virtuella datorns skal uppsättning (er) som utgör klustret.</span><span class="sxs-lookup"><span data-stu-id="2c982-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="2c982-107">Certifikatet är avsett att användas som ett program certifikat.</span><span class="sxs-lookup"><span data-stu-id="2c982-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="2c982-108">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2c982-108">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="2c982-109">Lägg till vanligt namn eller tumavtryck i klustret för användning av klientautentisering.</span><span class="sxs-lookup"><span data-stu-id="2c982-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="2c982-110">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="2c982-110">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="2c982-111">Lägg till ett sekundärt kluster certifikat i klustret.</span><span class="sxs-lookup"><span data-stu-id="2c982-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="2c982-112">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="2c982-112">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="2c982-113">Lägga till noder till den specifika nodtypen i klustret.</span><span class="sxs-lookup"><span data-stu-id="2c982-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="2c982-114">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="2c982-114">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="2c982-115">Lägg till en ny nodtyp i det befintliga klustret.</span><span class="sxs-lookup"><span data-stu-id="2c982-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="2c982-116">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="2c982-116">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="2c982-117">Hämta information om kluster resursen.</span><span class="sxs-lookup"><span data-stu-id="2c982-117">Get the cluster resource details.</span></span>

### [<span data-ttu-id="2c982-118">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="2c982-118">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="2c982-119">I det här kommandot används certifikat som du tillhandahåller eller systemgenererade självsignerade certifikat för att skapa ett nytt tjänst Fabric-kluster.</span><span class="sxs-lookup"><span data-stu-id="2c982-119">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="2c982-120">Den kan använda en standardmall eller en anpassad mall som du anger.</span><span class="sxs-lookup"><span data-stu-id="2c982-120">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="2c982-121">Du kan välja att ange en mapp att exportera självsignerade certifikat till eller hämta dem senare från huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="2c982-121">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="2c982-122">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2c982-122">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="2c982-123">Ta bort ett eller flera klient certifikat eller certifikat subjekt namn som används för klientautentisering till klustret.</span><span class="sxs-lookup"><span data-stu-id="2c982-123">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="2c982-124">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="2c982-124">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="2c982-125">Ta bort ett kluster certifikat från att användas för kluster säkerhet.</span><span class="sxs-lookup"><span data-stu-id="2c982-125">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="2c982-126">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="2c982-126">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="2c982-127">Ta bort noder från en viss nodtyp från ett kluster.</span><span class="sxs-lookup"><span data-stu-id="2c982-127">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="2c982-128">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="2c982-128">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="2c982-129">Ta bort en fullständig nodtyp från ett kluster.</span><span class="sxs-lookup"><span data-stu-id="2c982-129">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="2c982-130">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="2c982-130">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="2c982-131">Ta bort en eller flera tjänst Fabric-inställningar från klustret.</span><span class="sxs-lookup"><span data-stu-id="2c982-131">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="2c982-132">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="2c982-132">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="2c982-133">Lägga till eller uppdatera en eller flera tjänst infrastruktur inställningar i klustret.</span><span class="sxs-lookup"><span data-stu-id="2c982-133">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="2c982-134">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="2c982-134">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="2c982-135">Ändra kluster för Service Fabric-uppgradering.</span><span class="sxs-lookup"><span data-stu-id="2c982-135">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="2c982-136">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="2c982-136">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="2c982-137">Uppdatera livs längden eller VmSku för en nodtyp i klustret.</span><span class="sxs-lookup"><span data-stu-id="2c982-137">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="2c982-138">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="2c982-138">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="2c982-139">Uppdatera Tillförlitlighets nivån för den primära nodtypen i ett kluster.</span><span class="sxs-lookup"><span data-stu-id="2c982-139">Update the reliability tier of the primary node type in a cluster.</span></span>

