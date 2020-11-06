---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 9c71788abd7707931df2c25279c265bbe9967bbf
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/23/2019
ms.locfileid: "93570908"
---
# <span data-ttu-id="3543a-101">Modulen AzureRM. ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3543a-101">AzureRM.ServiceFabric Module</span></span>
## <span data-ttu-id="3543a-102">Problembeskrivning</span><span class="sxs-lookup"><span data-stu-id="3543a-102">Description</span></span>
<span data-ttu-id="3543a-103">Modul för Azure Service Fabric som du kan använda för att automatisera slut 2-avsluta-åtgärderna som att skapa ett säkert kluster, rulla över kluster certifikat, lägga till eller ta bort noder från klustret osv. Den fullständiga listan över alla åtgärder visas nedan.</span><span class="sxs-lookup"><span data-stu-id="3543a-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="3543a-104">AzureRM. ServiceFabric-cmdletar</span><span class="sxs-lookup"><span data-stu-id="3543a-104">AzureRM.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="3543a-105">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="3543a-105">Add-AzureRmServiceFabricApplicationCertificate</span></span>](Add-AzureRmServiceFabricApplicationCertificate.md)
<span data-ttu-id="3543a-106">Lägga till ett certifikat som används som program certifikat</span><span class="sxs-lookup"><span data-stu-id="3543a-106">Add a certificate that will be used as application certificate</span></span>

### [<span data-ttu-id="3543a-107">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="3543a-107">Add-AzureRmServiceFabricClientCertificate</span></span>](Add-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="3543a-108">Lägga till gemensamt namn eller tumavtryck i kluster inställningarna för klientautentisering</span><span class="sxs-lookup"><span data-stu-id="3543a-108">Add common name or thumbprint to the cluster settings for client authentication</span></span>

### [<span data-ttu-id="3543a-109">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="3543a-109">Add-AzureRmServiceFabricClusterCertificate</span></span>](Add-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="3543a-110">Lägga till ett sekundärt kluster certifikat i klustret för att rulla över det befintliga certifikatet</span><span class="sxs-lookup"><span data-stu-id="3543a-110">Add a secondary cluster certificate to the cluster for rolling over the existing certificate</span></span> 

### [<span data-ttu-id="3543a-111">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="3543a-111">Add-AzureRmServiceFabricNode</span></span>](Add-AzureRmServiceFabricNode.md)
<span data-ttu-id="3543a-112">Lägga till noder/VMs till en viss nodtyp i ett kluster</span><span class="sxs-lookup"><span data-stu-id="3543a-112">Add nodes/VMs to a specific node type to a cluster</span></span>

### [<span data-ttu-id="3543a-113">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="3543a-113">Add-AzureRmServiceFabricNodeType</span></span>](Add-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="3543a-114">Lägga till en nodtyp/VMs-datorer i ett befintligt kluster</span><span class="sxs-lookup"><span data-stu-id="3543a-114">Add a node type/VMs to an existing cluster</span></span>

### [<span data-ttu-id="3543a-115">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="3543a-115">Get-AzureRmServiceFabricCluster</span></span>](Get-AzureRmServiceFabricCluster.md)
<span data-ttu-id="3543a-116">Få information om kluster resursen</span><span class="sxs-lookup"><span data-stu-id="3543a-116">Get the details of the cluster resource</span></span> 

### [<span data-ttu-id="3543a-117">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="3543a-117">New-AzureRmServiceFabricCluster</span></span>](New-AzureRmServiceFabricCluster.md)
<span data-ttu-id="3543a-118">Skapa ett nytt ServiceFabric-kluster.</span><span class="sxs-lookup"><span data-stu-id="3543a-118">Create an new ServiceFabric cluster.</span></span> <span data-ttu-id="3543a-119">Det här kommandot har många överbelastningar för olika scenarier</span><span class="sxs-lookup"><span data-stu-id="3543a-119">This command has many overloads to cover various scenarios</span></span>

### [<span data-ttu-id="3543a-120">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="3543a-120">Remove-AzureRmServiceFabricClientCertificate</span></span>](Remove-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="3543a-121">Ta bort klient certifikatet från att användas för åtkomst till klustret</span><span class="sxs-lookup"><span data-stu-id="3543a-121">Remove client certificate from being used to access the cluster</span></span>

### [<span data-ttu-id="3543a-122">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="3543a-122">Remove-AzureRmServiceFabricClusterCertificate</span></span>](Remove-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="3543a-123">Ta bort kluster certifikat från att användas för kluster säkerhet</span><span class="sxs-lookup"><span data-stu-id="3543a-123">Remove cluster certificate from being used for cluster security</span></span>

### [<span data-ttu-id="3543a-124">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="3543a-124">Remove-AzureRmServiceFabricNode</span></span>](Remove-AzureRmServiceFabricNode.md)
<span data-ttu-id="3543a-125">Ta bort noder från en viss nodtyp från ett kluster</span><span class="sxs-lookup"><span data-stu-id="3543a-125">Remove nodes from the specific node type from a cluster</span></span>

### [<span data-ttu-id="3543a-126">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="3543a-126">Remove-AzureRmServiceFabricNodeType</span></span>](Remove-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="3543a-127">Ta bort en nodtyp från ett kluster</span><span class="sxs-lookup"><span data-stu-id="3543a-127">Remove a node type from a cluster</span></span>

### [<span data-ttu-id="3543a-128">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="3543a-128">Remove-AzureRmServiceFabricSetting</span></span>](Remove-AzureRmServiceFabricSetting.md)
<span data-ttu-id="3543a-129">Ta bort en eller flera ServiceFabric-inställningar från klustret</span><span class="sxs-lookup"><span data-stu-id="3543a-129">Remove one or more ServiceFabric settings from the cluster</span></span>

### [<span data-ttu-id="3543a-130">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="3543a-130">Set-AzureRmServiceFabricSetting</span></span>](Set-AzureRmServiceFabricSetting.md)
<span data-ttu-id="3543a-131">Lägga till eller uppdatera en eller flera ServiceFabric-inställningar i klustret</span><span class="sxs-lookup"><span data-stu-id="3543a-131">Add or update one or more ServiceFabric settings to the cluster</span></span>

### [<span data-ttu-id="3543a-132">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="3543a-132">Set-AzureRmServiceFabricUpgradeType</span></span>](Set-AzureRmServiceFabricUpgradeType.md)
<span data-ttu-id="3543a-133">Ändra ServiceFabric uppgraderings typ för ett kluster</span><span class="sxs-lookup"><span data-stu-id="3543a-133">Change the ServiceFabric upgrade type of a cluster</span></span>

### [<span data-ttu-id="3543a-134">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="3543a-134">Update-AzureRmServiceFabricDurability</span></span>](Update-AzureRmServiceFabricDurability.md)
<span data-ttu-id="3543a-135">Ändra livs längden för ett kluster</span><span class="sxs-lookup"><span data-stu-id="3543a-135">Change the durability tier of a cluster</span></span>

### [<span data-ttu-id="3543a-136">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="3543a-136">Update-AzureRmServiceFabricReliability</span></span>](Update-AzureRmServiceFabricReliability.md)
<span data-ttu-id="3543a-137">Ändra Tillförlitlighets nivån för ett kluster</span><span class="sxs-lookup"><span data-stu-id="3543a-137">Change the reliability tier of a cluster</span></span>
