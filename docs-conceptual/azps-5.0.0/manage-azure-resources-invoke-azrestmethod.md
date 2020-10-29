---
title: Hantera Azure-resurser med Invoke-AzRestMethod
description: Så här använder du Azure PowerShell för att hantera resurser med cmdleten Invoke-AzRestMethod.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/24/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 55d7cc06178257a9288e2d27f810d1180369ddc4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92753969"
---
# <a name="manage-azure-resources-with-invoke-azrestmethod"></a><span data-ttu-id="0fafd-103">Hantera Azure-resurser med Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="0fafd-103">Manage Azure resources with Invoke-AzRestMethod</span></span>

<span data-ttu-id="0fafd-104">[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) är en Azure PowerShell-cmdlet som lanserades i version 4.4.0 av Az PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="0fafd-104">[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) is an Azure PowerShell cmdlet that was introduced in Az PowerShell module version 4.4.0.</span></span> <span data-ttu-id="0fafd-105">Med hjälp av den kan du göra anpassade HTTP-begäranden till ARM-slutpunkten (Azure Resource Management) med Az-kontexten.</span><span class="sxs-lookup"><span data-stu-id="0fafd-105">It allows you to make custom HTTP requests to the Azure Resource Management (ARM) endpoint using the Az context.</span></span>

<span data-ttu-id="0fafd-106">Denna cmdlet är användbar när du vill hantera Azure-tjänster för funktioner som ännu inte är tillgängliga i Az PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="0fafd-106">This cmdlet is useful when you want to manage Azure services for features that aren't yet available in the Az PowerShell module.</span></span>

## <a name="how-to-use-invoke-azrestmethod"></a><span data-ttu-id="0fafd-107">Så här använder du Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="0fafd-107">How to use Invoke-AzRestMethod</span></span>

<span data-ttu-id="0fafd-108">Du kan exempelvis tillåta åtkomst till Azure Container Registry (ACR) endast för vissa nätverk eller neka offentlig åtkomst.</span><span class="sxs-lookup"><span data-stu-id="0fafd-108">As an example, you can allow access to Azure Container Registry (ACR) only for specific networks or deny public access.</span></span> <span data-ttu-id="0fafd-109">Från och med Az PowerShell-modul version 4.5.0 är funktionen är inte tillgänglig än i [Az.ContainerRegistry PowerShell-modulen](/powershell/module/Az.ContainerRegistry/).</span><span class="sxs-lookup"><span data-stu-id="0fafd-109">As of Az PowerShell module version 4.5.0, that feature isn't available yet in the [Az.ContainerRegistry PowerShell module](/powershell/module/Az.ContainerRegistry/).</span></span> <span data-ttu-id="0fafd-110">Men under tiden kan den hanteras med `Invoke-AzRestMethod`.</span><span class="sxs-lookup"><span data-stu-id="0fafd-110">However, it can be managed in the interim with `Invoke-AzRestMethod`.</span></span>

## <a name="using-invoke-azrestmethod-with-get-operations"></a><span data-ttu-id="0fafd-111">Använda Invoke-AzRestMethod med GET-åtgärder</span><span class="sxs-lookup"><span data-stu-id="0fafd-111">Using Invoke-AzRestMethod with GET operations</span></span>

<span data-ttu-id="0fafd-112">Följande exempel visar hur du använder `Invoke-AzRestMethod`-cmdleten med en GET-åtgärd:</span><span class="sxs-lookup"><span data-stu-id="0fafd-112">The following example demonstrates how to use the `Invoke-AzRestMethod` cmdlet with a GET operation:</span></span>

```azurepowershell-interactive
$getParams = @{
  ResourceGroupName = 'myresourcegroup'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  Name = 'myacr'
  ApiVersion = '2019-12-01-preview'
  Method = 'GET'
}
Invoke-AzRestMethod @getParams
```

<span data-ttu-id="0fafd-113">För maximal flexibilitet är de flesta av parametrarna för `Invoke-AzRestMethod` valfria.</span><span class="sxs-lookup"><span data-stu-id="0fafd-113">To allow maximum flexibility, most of the parameters for `Invoke-AzRestMethod` are optional.</span></span>
<span data-ttu-id="0fafd-114">Men när du hanterar resurser inom en resursgrupp behöver du förmodligen ange antingen det fullständiga ID:t för resursen eller parametrar som resursgrupp, resursprovider och resurstyp.</span><span class="sxs-lookup"><span data-stu-id="0fafd-114">However, when you're managing resources within a resource group, you'll most likely need to provide either the full ID to the resource or parameters like resource group, resource provider, and resource type.</span></span>

<span data-ttu-id="0fafd-115">Parametrarna `ResourceType` och `Name` kan ta flera värden när de har resurser som kräver mer än ett namn som mål.</span><span class="sxs-lookup"><span data-stu-id="0fafd-115">The `ResourceType` and `Name` parameters can take multiple values when targeting resources that require more than one name.</span></span> <span data-ttu-id="0fafd-116">Om du till exempel vill ändra en sparad sökning i en Log Analytics-arbetsyta ser parametrarna ut som i följande exempel: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.</span><span class="sxs-lookup"><span data-stu-id="0fafd-116">For example, to manipulate a saved search in a Log Analytics workspace, the parameters look like the following example: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.</span></span>

<span data-ttu-id="0fafd-117">Med hjälp av en mappning som baseras på positionen i matrisen skapar cmdleten följande resurs: `Id:'/workspaces/my-la/savedsearches/my-search'`.</span><span class="sxs-lookup"><span data-stu-id="0fafd-117">Using a mapping based on the position in the array, the cmdlet constructs the following resource: `Id:'/workspaces/my-la/savedsearches/my-search'`.</span></span>

<span data-ttu-id="0fafd-118">Med parametern `APIVersion` kan du använda en specifik API-version, inklusive förhandsversioner.</span><span class="sxs-lookup"><span data-stu-id="0fafd-118">The `APIVersion` parameter allows you to use a specific API version, including preview ones.</span></span> <span data-ttu-id="0fafd-119">De API-versioner som stöds för Azure Resource-providers finns på GitHub-lagringsplatsen för [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs).</span><span class="sxs-lookup"><span data-stu-id="0fafd-119">The supported API versions for Azure Resource providers can be found in the [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs) GitHub repository.</span></span>

<span data-ttu-id="0fafd-120">Du hittar definitionen för ACR-versionen 2019-12-01-preview på följande plats: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).</span><span class="sxs-lookup"><span data-stu-id="0fafd-120">You can find the definition for the 2019-12-01-preview version of ACR in the following location: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).</span></span>

## <a name="using-invoke-azrestmethod-with-patch-operations"></a><span data-ttu-id="0fafd-121">Använda Invoke-AzRestMethod med PATCH-åtgärder</span><span class="sxs-lookup"><span data-stu-id="0fafd-121">Using Invoke-AzRestMethod with PATCH operations</span></span>

<span data-ttu-id="0fafd-122">Du kan inaktivera offentlig åtkomst till det befintliga ACR:et med namnet `myacr` i resursgruppen `myresourcegroup` med hjälp av cmdleten `Invoke-AzRestMethod`.</span><span class="sxs-lookup"><span data-stu-id="0fafd-122">You can disable public access to the existing ACR named `myacr` in the `myresourcegroup` resource group using the `Invoke-AzRestMethod` cmdlet.</span></span>

<span data-ttu-id="0fafd-123">Om du vill inaktivera offentlig nätverksåtkomst måste du göra ett **PATCH** -anrop till API:et som ändrar värdet för parametern `publicNetwokAccess` enligt följande exempel:</span><span class="sxs-lookup"><span data-stu-id="0fafd-123">To disable the public network access, you need to make a **PATCH** call to the API that changes the value of the `publicNetwokAccess` parameter as shown in the following example:</span></span>

```azurepowershell-interactive
$patchParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
     "publicNetworkAccess": "Disabled"
     } }'
  Method = 'PATCH'
}
Invoke-AzRestMethod @patchParams
```

<span data-ttu-id="0fafd-124">Egenskapen `Payload` är en JSON-sträng som visar sökvägen för den egenskap som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="0fafd-124">The `Payload` property is a JSON string that shows the path of the property to be modified.</span></span>

<span data-ttu-id="0fafd-125">Alla parametrar för detta API beskrivs i filen **rest-api-spec** som är associerad med detta API.</span><span class="sxs-lookup"><span data-stu-id="0fafd-125">All the parameters for this API are described in the **rest-api-spec** file associated with this API.</span></span>
<span data-ttu-id="0fafd-126">Den specifika definitionen för parametern publicNetworkAccess finns i [containerregistrets JSON-fil](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) för API-versionen 2019-12-01-preview.</span><span class="sxs-lookup"><span data-stu-id="0fafd-126">The specific definition for the publicNetworkAccess parameter can be found in the [container registry JSON file](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) for the 2019-12-01 preview version of the API.</span></span>

<span data-ttu-id="0fafd-127">Om du bara vill tillåta åtkomst till registret från en viss IP-adress måste nyttolasten ändras på det sätt som visas i följande exempel:</span><span class="sxs-lookup"><span data-stu-id="0fafd-127">To only allow access to the registry from a specific IP address, the payload needs to be modified as shown in the following example:</span></span>

```azurepowershell-interactive
$specificIpParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
      "networkRuleSet": {
      "defaultAction": "Deny",
      "ipRules": [ {
         "action": "Allow",
         "value": "24.22.123.123"
         } ]
      }
  } }'
  -Method = 'PATCH'
}
Invoke-AzRestMethod @specificIpParams
```

## <a name="comparison-to-get-azresource-new-azresource-and-remove-azresource"></a><span data-ttu-id="0fafd-128">Jämförelse med Get-AzResource, New-AzResource och Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="0fafd-128">Comparison to Get-AzResource, New-AzResource, and Remove-AzResource</span></span>

<span data-ttu-id="0fafd-129">Med `*-AzResource`-cmdletarna kan du anpassa REST API-anropet till Azure genom att ange resurstypen, API-versionen och de egenskaper som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="0fafd-129">The `*-AzResource` cmdlets allow you to customize the REST API call to Azure by specifying the resource type, the API version, and the properties to be updated.</span></span> <span data-ttu-id="0fafd-130">Men egenskaperna måste först skapas som ett `PSObject`.</span><span class="sxs-lookup"><span data-stu-id="0fafd-130">However, the properties need to be created first as a `PSObject`.</span></span> <span data-ttu-id="0fafd-131">Den här processen medför ytterligare en nivå av komplexitet och kan enkelt bli komplicerad.</span><span class="sxs-lookup"><span data-stu-id="0fafd-131">This process adds an additional level of complexity and can easily become complicated.</span></span>

<span data-ttu-id="0fafd-132">Med `Invoke-AzRestMethod` får du ett enkelt sätt att hantera Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="0fafd-132">`Invoke-AzRestMethod` offers a simple way to manage Azure resources.</span></span> <span data-ttu-id="0fafd-133">Du kan skapa en JSON-sträng och använda den för att anpassa REST-API-anropet utan att du behöver skapa `PSObjects` i förväg (se föregående exempel).</span><span class="sxs-lookup"><span data-stu-id="0fafd-133">As shown in the previous example, you can build a JSON string and use it to customize the REST API call without having to precreate any `PSObjects`.</span></span>

<span data-ttu-id="0fafd-134">Om du redan är van vid `*-AzResource`-cmdletarna kan du fortsätta att använda dem.</span><span class="sxs-lookup"><span data-stu-id="0fafd-134">If you're already familiar with the `*-AzResource` cmdlets, you can continue using them.</span></span> <span data-ttu-id="0fafd-135">Vi har inga planer på att sluta stöda dem.</span><span class="sxs-lookup"><span data-stu-id="0fafd-135">We have no plans to stop supporting them.</span></span> <span data-ttu-id="0fafd-136">Med `Invoke-AzRestMethod` har vi lagt till en ny cmdlet i din verktygslåda.</span><span class="sxs-lookup"><span data-stu-id="0fafd-136">With `Invoke-AzRestMethod`, we have added a new cmdlet to your toolkit.</span></span>

## <a name="see-also"></a><span data-ttu-id="0fafd-137">Se även</span><span class="sxs-lookup"><span data-stu-id="0fafd-137">See Also</span></span>

* [<span data-ttu-id="0fafd-138">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="0fafd-138">Get-AzResource</span></span>](/powershell/module/az.resources/get-azresource)
* [<span data-ttu-id="0fafd-139">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="0fafd-139">New-AzResource</span></span>](/powershell/module/az.resources/new-azresource)
* [<span data-ttu-id="0fafd-140">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="0fafd-140">Remove-AzResource</span></span>](/powershell/module/az.resources/remove-azresource)
