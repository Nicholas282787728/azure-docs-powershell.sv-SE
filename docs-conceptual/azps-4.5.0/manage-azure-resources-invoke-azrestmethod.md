---
title: Hantera Azure-resurser med Invoke-AzRestMethod
description: Så här använder du Azure PowerShell för att hantera resurser med cmdleten Invoke-AzRestMethod.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.openlocfilehash: 380fd818a3af2474ce192c7a1da8a6798795cf21
ms.sourcegitcommit: bd7edc4d48b6a8a8bec864edc876e16af0a49505
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/18/2020
ms.locfileid: "88513009"
---
# <a name="manage-azure-resources-with-invoke-azrestmethod"></a>Hantera Azure-resurser med Invoke-AzRestMethod

[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) är en Azure PowerShell-cmdlet som lanserades i version 4.4.0 av Az PowerShell-modulen. Med hjälp av den kan du göra anpassade HTTP-begäranden till ARM-slutpunkten (Azure Resource Management) med Az-kontexten.

Denna cmdlet är användbar när du vill hantera Azure-tjänster för funktioner som ännu inte är tillgängliga i Az PowerShell-modulen.

## <a name="how-to-use-invoke-azrestmethod"></a>Så här använder du Invoke-AzRestMethod

Du kan exempelvis tillåta åtkomst till Azure Container Registry (ACR) endast för vissa nätverk eller neka offentlig åtkomst. Den här funktionen är inte tillgänglig än i [Az.ContainerRegistry PowerShell-modulen](/powershell/module/Az.ContainerRegistry/).
Men under tiden kan den hanteras med `Invoke-AzRestMethod`.

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

Du kan inaktivera offentlig åtkomst till det befintliga ACR:et med namnet `myacr` i resursgruppen `myresourcegroup` med hjälp av cmdleten Invoke-AzRestMethod.

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

Med `*-AzResource`-cmdletarna kan du anpassa REST API-anropet till Azure genom att ange resurstypen, API-versionen och de egenskaper som ska uppdateras. Egenskaperna måste ändå vara ett `PSObject` som lätt blir krångligt att skapa.

Med `Invoke-AzRestMethod` får du ett enklare sätt att hantera Azure-resurser. Du kan se att nyttolasten är en JSON-sträng i det föregående exemplet. Du behöver inte kämpa med konverteringen mellan JSON och `PSObjects`.

Om du redan är van vid `*-AzResource`-cmdletarna kan du fortsätta att använda dem. Vi har inga planer på att sluta stöda dem. Med `Invoke-AzRestMethod` har vi lagt till en ny cmdlet i familjen.

## <a name="see-also"></a>Se även

* [Get-AzResource](/powershell/module/az.resources/get-azresource)
* [New-AzResource](/powershell/module/az.resources/new-azresource)
* [Remove-AzResource](/powershell/module/az.resources/remove-azresource)
