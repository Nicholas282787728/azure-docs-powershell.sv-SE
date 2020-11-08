---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
ms.openlocfilehash: ee140a968741269b8bebebeb7b179f8ad74e35c8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258288"
---
# <span data-ttu-id="29cd2-101">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="29cd2-101">Get-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="29cd2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29cd2-102">SYNOPSIS</span></span>
<span data-ttu-id="29cd2-103">Hämtar en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="29cd2-103">Gets a network security group.</span></span>

## <span data-ttu-id="29cd2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29cd2-104">SYNTAX</span></span>

### <span data-ttu-id="29cd2-105">Noexpandering</span><span class="sxs-lookup"><span data-stu-id="29cd2-105">NoExpand</span></span>
```
Get-AzNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29cd2-106">Byggnad</span><span class="sxs-lookup"><span data-stu-id="29cd2-106">Expand</span></span>
```
Get-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29cd2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29cd2-107">DESCRIPTION</span></span>
<span data-ttu-id="29cd2-108">Cmdleten **Get-AzNetworkSecurityGroup** får en Azure Network Security-grupp.</span><span class="sxs-lookup"><span data-stu-id="29cd2-108">The **Get-AzNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="29cd2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29cd2-109">EXAMPLES</span></span>

### <span data-ttu-id="29cd2-110">Exempel 1: Hämta en befintlig nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="29cd2-110">Example 1: Retrieve an existing network security group</span></span>
```powershell
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName "rg1"

Name                        : nsg1
ResourceGroupName           : rg1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provider
                              s/Microsoft.Network/networkSecurityGroups/nsg1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
SecurityRules               : []
DefaultSecurityRules        : [
                                {
                                  "Name": "AllowVnetInBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowVnetInBound",
                                  "Description": "Allow inbound traffic from all VMs in VNET",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65000,
                                  "Direction": "Inbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "AllowAzureLoadBalancerInBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowAzureLoadBalancerInBou
                              nd",
                                  "Description": "Allow inbound traffic from azure load balancer",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "AzureLoadBalancer"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "*"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65001,
                                  "Direction": "Inbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "DenyAllInBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/DenyAllInBound",
                                  "Description": "Deny all inbound traffic",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "*"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "*"
                                  ],
                                  "Access": "Deny",
                                  "Priority": 65500,
                                  "Direction": "Inbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "AllowVnetOutBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowVnetOutBound",
                                  "Description": "Allow outbound traffic from all VMs to all VMs in VNET",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65000,
                                  "Direction": "Outbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "AllowInternetOutBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowInternetOutBound",
                                  "Description": "Allow outbound traffic from all VMs to Internet",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "*"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "Internet"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65001,
                                  "Direction": "Outbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "DenyAllOutBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/DenyAllOutBound",
                                  "Description": "Deny all outbound traffic",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "*"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "*"
                                  ],
                                  "Access": "Deny",
                                  "Priority": 65500,
                                  "Direction": "Outbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                }
                              ]
NetworkInterfaces           : []
Subnets                     : []
```

<span data-ttu-id="29cd2-111">Det här kommandot returnerar innehållet i Azure nätverks säkerhets gruppen "nsg1" i resurs gruppen "RG1"</span><span class="sxs-lookup"><span data-stu-id="29cd2-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="29cd2-112">Exempel 2: Visa en lista över befintliga nätverks säkerhets grupper med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="29cd2-112">Example 2: List existing network security groups using filtering</span></span>
```powershell
Get-AzNetworkSecurityGroup -Name nsg*

Name                        : nsg1
ResourceGroupName           : rg1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provider
                              s/Microsoft.Network/networkSecurityGroups/nsg1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
SecurityRules               : []
DefaultSecurityRules        : [
                                {
                                  "Name": "AllowVnetInBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowVnetInBound",
                                  "Description": "Allow inbound traffic from all VMs in VNET",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65000,
                                  "Direction": "Inbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "AllowAzureLoadBalancerInBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowAzureLoadBalancerInBou
                              nd",
                                  "Description": "Allow inbound traffic from azure load balancer",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "AzureLoadBalancer"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "*"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65001,
                                  "Direction": "Inbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "DenyAllInBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/DenyAllInBound",
                                  "Description": "Deny all inbound traffic",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "*"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "*"
                                  ],
                                  "Access": "Deny",
                                  "Priority": 65500,
                                  "Direction": "Inbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "AllowVnetOutBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowVnetOutBound",
                                  "Description": "Allow outbound traffic from all VMs to all VMs in VNET",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65000,
                                  "Direction": "Outbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "AllowInternetOutBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowInternetOutBound",
                                  "Description": "Allow outbound traffic from all VMs to Internet",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "*"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "Internet"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65001,
                                  "Direction": "Outbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "DenyAllOutBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/DenyAllOutBound",
                                  "Description": "Deny all outbound traffic",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "*"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "*"
                                  ],
                                  "Access": "Deny",
                                  "Priority": 65500,
                                  "Direction": "Outbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                }
                              ]
NetworkInterfaces           : []
Subnets                     : []
```

<span data-ttu-id="29cd2-113">Det här kommandot returnerar innehållet i Azure Network Security Groups som börjar med "NSG"</span><span class="sxs-lookup"><span data-stu-id="29cd2-113">This command returns contents of Azure network security groups that start with "nsg"</span></span>

## <span data-ttu-id="29cd2-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29cd2-114">PARAMETERS</span></span>

### <span data-ttu-id="29cd2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29cd2-115">-DefaultProfile</span></span>
<span data-ttu-id="29cd2-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="29cd2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29cd2-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="29cd2-117">-ExpandResource</span></span>
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

### <span data-ttu-id="29cd2-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="29cd2-118">-Name</span></span>
<span data-ttu-id="29cd2-119">Anger namnet på den nätverks säkerhets grupp som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="29cd2-119">Specifies the name of the network security group that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="29cd2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29cd2-120">-ResourceGroupName</span></span>
<span data-ttu-id="29cd2-121">Anger namnet på den resurs grupp som nätverks säkerhets gruppen tillhör.</span><span class="sxs-lookup"><span data-stu-id="29cd2-121">Specifies the name of the resource group that the network security group belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="29cd2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29cd2-122">CommonParameters</span></span>
<span data-ttu-id="29cd2-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29cd2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29cd2-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29cd2-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29cd2-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29cd2-125">INPUTS</span></span>

### <span data-ttu-id="29cd2-126">System. String</span><span class="sxs-lookup"><span data-stu-id="29cd2-126">System.String</span></span>

## <span data-ttu-id="29cd2-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29cd2-127">OUTPUTS</span></span>

### <span data-ttu-id="29cd2-128">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="29cd2-128">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="29cd2-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29cd2-129">NOTES</span></span>

## <span data-ttu-id="29cd2-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29cd2-130">RELATED LINKS</span></span>

[<span data-ttu-id="29cd2-131">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="29cd2-131">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="29cd2-132">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="29cd2-132">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="29cd2-133">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="29cd2-133">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


