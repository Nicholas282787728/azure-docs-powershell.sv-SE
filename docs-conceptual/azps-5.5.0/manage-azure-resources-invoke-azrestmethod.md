---
title: Hantera Azure-resurser med Invoke-AzRestMethod
description: Så här använder du Azure PowerShell för att hantera resurser med cmdleten Invoke-AzRestMethod.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/24/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 5fdb8543630198d141d42626dc3a8b85f0bcdaa7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100012776"
---
# <a name="manage-azure-resources-with-invoke-azrestmethod"></a>Hantera Azure-resurser med Invoke-AzRestMethod

[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) är en Azure PowerShell-cmdlet som lanserades i version 4.4.0 av Az PowerShell-modulen. Med hjälp av den kan du göra anpassade HTTP-begäranden till ARM-slutpunkten (Azure Resource Management) med Az-kontexten.

Denna cmdlet är användbar när du vill hantera Azure-tjänster för funktioner som ännu inte är tillgängliga i Az PowerShell-modulen.

## <a name="how-to-use-invoke-azrestmethod"></a>Så här använder du Invoke-AzRestMethod

Du kan exempelvis tillåta åtkomst till Azure Container Registry (ACR) endast för vissa nätverk eller neka offentlig åtkomst. Från och med Az PowerShell-modul version 4.5.0 är funktionen är inte tillgänglig än i [Az.ContainerRegistry PowerShell-modulen](/powershell/module/Az.ContainerRegistry/). Men under tiden kan den hanteras med `Invoke-AzRestMethod`.

## <a name="using-invoke-azrestmethod-with-get-operations"></a>Använda Invoke-AzRestMethod med GET-åtgärder

Följande exempel visar hur du använder `Invoke-AzRestMethod`-cmdleten med en GET-åtgärd:

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

För maximal flexibilitet är de flesta av parametrarna för `Invoke-AzRestMethod` valfria.
Men när du hanterar resurser inom en resursgrupp behöver du förmodligen ange antingen det fullständiga ID:t för resursen eller parametrar som resursgrupp, resursprovider och resurstyp.

Parametrarna `ResourceType` och `Name` kan ta flera värden när de har resurser som kräver mer än ett namn som mål. Om du till exempel vill ändra en sparad sökning i en Log Analytics-arbetsyta ser parametrarna ut som i följande exempel: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.

Med hjälp av en mappning som baseras på positionen i matrisen skapar cmdleten följande resurs: `Id:'/workspaces/my-la/savedsearches/my-search'`.

Med parametern `APIVersion` kan du använda en specifik API-version, inklusive förhandsversioner. De API-versioner som stöds för Azure Resource-providers finns på GitHub-lagringsplatsen för [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs).

Du hittar definitionen för ACR-versionen 2019-12-01-preview på följande plats: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).

## <a name="using-invoke-azrestmethod-with-patch-operations"></a>Använda Invoke-AzRestMethod med PATCH-åtgärder

Du kan inaktivera offentlig åtkomst till det befintliga ACR:et med namnet `myacr` i resursgruppen `myresourcegroup` med hjälp av cmdleten `Invoke-AzRestMethod`.

Om du vill inaktivera offentlig nätverksåtkomst måste du göra ett **PATCH**-anrop till API:et som ändrar värdet för parametern `publicNetwokAccess` enligt följande exempel:

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

Egenskapen `Payload` är en JSON-sträng som visar sökvägen för den egenskap som ska ändras.

Alla parametrar för detta API beskrivs i filen **rest-api-spec** som är associerad med detta API.
Den specifika definitionen för parametern publicNetworkAccess finns i [containerregistrets JSON-fil](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) för API-versionen 2019-12-01-preview.

Om du bara vill tillåta åtkomst till registret från en viss IP-adress måste nyttolasten ändras på det sätt som visas i följande exempel:

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

## <a name="comparison-to-get-azresource-new-azresource-and-remove-azresource"></a>Jämförelse med Get-AzResource, New-AzResource och Remove-AzResource

Med `*-AzResource`-cmdletarna kan du anpassa REST API-anropet till Azure genom att ange resurstypen, API-versionen och de egenskaper som ska uppdateras. Men egenskaperna måste först skapas som ett `PSObject`. Den här processen medför ytterligare en nivå av komplexitet och kan enkelt bli komplicerad.

Med `Invoke-AzRestMethod` får du ett enkelt sätt att hantera Azure-resurser. Du kan skapa en JSON-sträng och använda den för att anpassa REST-API-anropet utan att du behöver skapa `PSObjects` i förväg (se föregående exempel).

Om du redan är van vid `*-AzResource`-cmdletarna kan du fortsätta att använda dem. Vi har inga planer på att sluta stöda dem. Med `Invoke-AzRestMethod` har vi lagt till en ny cmdlet i din verktygslåda.

## <a name="see-also"></a>Se även

* [Get-AzResource](/powershell/module/az.resources/get-azresource)
* [New-AzResource](/powershell/module/az.resources/new-azresource)
* [Remove-AzResource](/powershell/module/az.resources/remove-azresource)
