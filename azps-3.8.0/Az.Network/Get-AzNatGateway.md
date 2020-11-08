---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNatGateway.md
ms.openlocfilehash: 650ffdfd557780727a4f3bc4c69a7be6f2783cb3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091052"
---
# <span data-ttu-id="4b8ee-101">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4b8ee-101">Get-AzNatGateway</span></span>

## <span data-ttu-id="4b8ee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4b8ee-102">SYNOPSIS</span></span>
<span data-ttu-id="4b8ee-103">Hämtar en NAT-gatewayenhet i en resurs grupp efter namn eller NatGateway-ID eller alla NAT-gateway-resurser i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="4b8ee-103">Gets a Nat Gateway resource in a resource group by name or NatGateway Id  or all Nat Gateway resources in a resource group.</span></span>

## <span data-ttu-id="4b8ee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4b8ee-104">SYNTAX</span></span>

### <span data-ttu-id="4b8ee-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4b8ee-105">ListParameterSet (Default)</span></span>
```
Get-AzNatGateway [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b8ee-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b8ee-106">GetByNameParameterSet</span></span>
```
Get-AzNatGateway -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4b8ee-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b8ee-107">GetByResourceIdParameterSet</span></span>
```
Get-AzNatGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b8ee-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4b8ee-108">DESCRIPTION</span></span>
<span data-ttu-id="4b8ee-109">Hämtar en NAT-gatewayenhet i en resurs grupp efter namn eller NatGateway-ID eller alla NAT-gateway-resurser i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="4b8ee-109">Gets a Nat Gateway resource in a resource group by name OR NatGateway Id OR all Nat Gateway resources in a resource group.</span></span>

## <span data-ttu-id="4b8ee-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4b8ee-110">EXAMPLES</span></span>

### <span data-ttu-id="4b8ee-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4b8ee-111">Example 1</span></span>
```powershell
PS C:> Get-AzNatGateway -ResourceGroupName "natgateway_test"


IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : [
                          {
                            "Id": "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip"
                          }
                        ]
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : nat_gateway
Etag                  : W/"178470d2-7b86-4ddd-b954-e0cd3ab30a90"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway

IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : []
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : ng1
Etag                  : W/"bdf98e30-d6c6-4af2-8f62-10d1fdaa6e84"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/ng1


PS C:> Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"


IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : [
                          {
                            "Id": "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip"
                          }
                        ]
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : nat_gateway
Etag                  : W/"178470d2-7b86-4ddd-b954-e0cd3ab30a90"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway

PS C:> Get-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway"


IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : [
                          {
                            "Id": "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip"
                          }
                        ]
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : nat_gateway
Etag                  : W/"178470d2-7b86-4ddd-b954-e0cd3ab30a90"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway
```

## <span data-ttu-id="4b8ee-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4b8ee-112">PARAMETERS</span></span>

### <span data-ttu-id="4b8ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b8ee-113">-DefaultProfile</span></span>
<span data-ttu-id="4b8ee-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4b8ee-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b8ee-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="4b8ee-115">-Name</span></span>
<span data-ttu-id="4b8ee-116">Namnet på NAT-gatewayen.</span><span class="sxs-lookup"><span data-stu-id="4b8ee-116">The name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b8ee-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b8ee-117">-ResourceGroupName</span></span>
<span data-ttu-id="4b8ee-118">Namnet på den som heter NAT.</span><span class="sxs-lookup"><span data-stu-id="4b8ee-118">The resource group name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b8ee-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b8ee-119">-ResourceId</span></span>
<span data-ttu-id="4b8ee-120">ID för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="4b8ee-120">Nat Gateway Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b8ee-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b8ee-121">CommonParameters</span></span>
<span data-ttu-id="4b8ee-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b8ee-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b8ee-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b8ee-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b8ee-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4b8ee-124">INPUTS</span></span>

### <span data-ttu-id="4b8ee-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4b8ee-125">System.String</span></span>

## <span data-ttu-id="4b8ee-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4b8ee-126">OUTPUTS</span></span>

### <span data-ttu-id="4b8ee-127">Microsoft. Azure. commands. Networks. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="4b8ee-127">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="4b8ee-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4b8ee-128">NOTES</span></span>

## <span data-ttu-id="4b8ee-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4b8ee-129">RELATED LINKS</span></span>
