---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
ms.openlocfilehash: 11a0b65118fc9b580a885510f1e5ffa337b1d2e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258283"
---
# <span data-ttu-id="f5842-101">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5842-101">Get-AzPrivateEndpoint</span></span>

## <span data-ttu-id="f5842-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f5842-102">SYNOPSIS</span></span>
<span data-ttu-id="f5842-103">Skaffa en privat slut punkt</span><span class="sxs-lookup"><span data-stu-id="f5842-103">Get a private endpoint</span></span>

## <span data-ttu-id="f5842-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f5842-104">SYNTAX</span></span>

### <span data-ttu-id="f5842-105">Noexpandering (standard)</span><span class="sxs-lookup"><span data-stu-id="f5842-105">NoExpand (Default)</span></span>
```
Get-AzPrivateEndpoint [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f5842-106">Byggnad</span><span class="sxs-lookup"><span data-stu-id="f5842-106">Expand</span></span>
```
Get-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5842-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f5842-107">DESCRIPTION</span></span>
<span data-ttu-id="f5842-108">Cmdleten **Get-AzPrivateEndpoint** hämtar en eller flera privata slut punkter.</span><span class="sxs-lookup"><span data-stu-id="f5842-108">The **Get-AzPrivateEndpoint** cmdlet gets one or more private endpoints.</span></span>

## <span data-ttu-id="f5842-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f5842-109">EXAMPLES</span></span>

### <span data-ttu-id="f5842-110">Exempel 1: Hämta en privat slut punkt</span><span class="sxs-lookup"><span data-stu-id="f5842-110">Example 1: Retrieve a private endpoint</span></span>
```powershell
Get-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup

Name                                : MyPrivateEndpoint1
ResourceGroupName                   : TestResourceGroup
Location                            : eastus2euap
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/provi
                                      ders/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1
Etag                                : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                   : Succeeded
Subnet                              : {
                                        "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1/subnets/backendSubnet",
                                      }
NetworkInterfaces                   : [
                                        {

                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/MyNic1",
                                        }
                                      ]
PrivateLinkServiceConnections       : []
ManualPrivateLinkServiceConnections : [
                                        {
                                          "Name": "MyPrivateLinkServiceConnection",
                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1/manualPrivateLinkServi
                                      ceConnections/MyPrivateLinkServiceConnection",
                                          "PrivateLinkServiceId": "/subscriptions/00000000-0000-0000-0000-000000000000/
                                      resourceGroups/TestResourceGroup/providers/Microsoft.Network/priv
                                      ateLinkServices/MyPrivateLinkService",
                                          "PrivateLinkServiceConnectionState": {
                                            "Status": "Pending",
                                            "Description": "Awaiting approval"
                                          }
                                        }
                                      ]
```

<span data-ttu-id="f5842-111">Det här kommandot får den privata slut punkten som heter MyPrivateEndpoint1 i resurs gruppen TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f5842-111">This command gets the private endpoint named MyPrivateEndpoint1 in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="f5842-112">Exempel 2: lista alla privata slut punkter i ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f5842-112">Example 2: List all private endpoints in ResourceGroup</span></span>
```powershell
Get-AzPrivateEndpoint -ResourceGroupName TestResourceGroup

Name                                : MyPrivateEndpoint1
ResourceGroupName                   : TestResourceGroup
Location                            : eastus2euap
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/provi
                                      ders/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1
Etag                                : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                   : Succeeded
Subnet                              : {
                                        "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1/subnets/backendSubnet",
                                      }
NetworkInterfaces                   : [
                                        {

                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/MyNic1",
                                        }
                                      ]
PrivateLinkServiceConnections       : []
ManualPrivateLinkServiceConnections : [
                                        {
                                          "Name": "MyPrivateLinkServiceConnection",
                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1/manualPrivateLinkServi
                                      ceConnections/MyPrivateLinkServiceConnection",
                                          "PrivateLinkServiceId": "/subscriptions/00000000-0000-0000-0000-000000000000/
                                      resourceGroups/TestResourceGroup/providers/Microsoft.Network/priv
                                      ateLinkServices/MyPrivateLinkService",
                                          "PrivateLinkServiceConnectionState": {
                                            "Status": "Pending",
                                            "Description": "Awaiting approval"
                                          }
                                        }
                                      ]
```

<span data-ttu-id="f5842-113">Det här kommandot får alla privata slut punkter i resurs gruppen TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f5842-113">This command gets all of private end points in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="f5842-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f5842-114">PARAMETERS</span></span>

### <span data-ttu-id="f5842-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5842-115">-DefaultProfile</span></span>
<span data-ttu-id="f5842-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f5842-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5842-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="f5842-117">-ExpandResource</span></span>
<span data-ttu-id="f5842-118">Resurs referensen som ska expanderas.</span><span class="sxs-lookup"><span data-stu-id="f5842-118">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5842-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="f5842-119">-Name</span></span>
<span data-ttu-id="f5842-120">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="f5842-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5842-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5842-121">-ResourceGroupName</span></span>
<span data-ttu-id="f5842-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="f5842-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5842-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5842-123">CommonParameters</span></span>
<span data-ttu-id="f5842-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5842-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5842-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5842-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5842-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f5842-126">INPUTS</span></span>

### <span data-ttu-id="f5842-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f5842-127">System.String</span></span>

## <span data-ttu-id="f5842-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f5842-128">OUTPUTS</span></span>

### <span data-ttu-id="f5842-129">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f5842-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="f5842-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f5842-130">NOTES</span></span>

## <span data-ttu-id="f5842-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f5842-131">RELATED LINKS</span></span>

[<span data-ttu-id="f5842-132">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5842-132">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="f5842-133">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5842-133">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)