---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
ms.openlocfilehash: fdbb023c6796a780bfe9e6474191185a58489c91
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091028"
---
# <span data-ttu-id="0391a-101">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0391a-101">Get-AzPrivateLinkService</span></span>

## <span data-ttu-id="0391a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0391a-102">SYNOPSIS</span></span>
<span data-ttu-id="0391a-103">Får tjänsten Private Link</span><span class="sxs-lookup"><span data-stu-id="0391a-103">Gets private link service</span></span>

## <span data-ttu-id="0391a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0391a-104">SYNTAX</span></span>

### <span data-ttu-id="0391a-105">Noexpandering (standard)</span><span class="sxs-lookup"><span data-stu-id="0391a-105">NoExpand (Default)</span></span>
```
Get-AzPrivateLinkService [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0391a-106">Byggnad</span><span class="sxs-lookup"><span data-stu-id="0391a-106">Expand</span></span>
```
Get-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0391a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0391a-107">DESCRIPTION</span></span>
<span data-ttu-id="0391a-108">Cmdleten **Get-AzPrivateLinkService** får en eller flera privata länk tjänster.</span><span class="sxs-lookup"><span data-stu-id="0391a-108">The **Get-AzPrivateLinkService** cmdlet gets one or more private link services.</span></span>

## <span data-ttu-id="0391a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0391a-109">EXAMPLES</span></span>

### <span data-ttu-id="0391a-110">Exempel</span><span class="sxs-lookup"><span data-stu-id="0391a-110">Example</span></span>
```
Get-AzPrivateLinkService -Name MyPLS -ResourceGroupName TestResourceGroup

Name                                 : MyPLS
ResourceGroupName                    : TestResourceGroup
Id                                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/prov
                                       iders/Microsoft.Network/privateLinkServices/MyPLS
Location                             : eastus2euap
Type                                 : Microsoft.Network/privateLinkServices
Etag                                 : W/"00000000-0000-0000-0000-000000000000"
Tag                                  : {}
ProvisioningState                    : Succeeded
Visibility                           : 
AutoApproval                         : 
Alias                                :
LoadBalancerFrontendIpConfigurations : []
IpConfigurations                     : [
                                         {
                                           "PrivateIPAddress": "10.0.2.5",
                                           "PrivateIPAllocationMethod": "Static",
                                           "ProvisioningState": "Failed",
                                           "PrivateIPAddressVersion": "IPv4",
                                           "Name": "IP-Config",
                                           "Subnet": {
                                             "Delegations": [],
                                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/
                                       TestResourceGroup/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/backendSubne
                                       t",
                                             "ServiceAssociationLinks": []
                                           }
                                         }
                                       ]
PrivateEndpointConnections           : []
NetworkInterfaces                    : [
                                         {
                                           "TapConfigurations": [],
                                           "HostedWorkloads": [],
                                           "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/mytestinterface"
                                         }
                                       ]
```

<span data-ttu-id="0391a-111">Denna cmdleten får en privat länk tjänst i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0391a-111">This commandlet gets a private link service in the resource group.</span></span>

## <span data-ttu-id="0391a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0391a-112">PARAMETERS</span></span>

### <span data-ttu-id="0391a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0391a-113">-DefaultProfile</span></span>
<span data-ttu-id="0391a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0391a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0391a-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="0391a-115">-ExpandResource</span></span>
<span data-ttu-id="0391a-116">Resurs referensen som ska expanderas.</span><span class="sxs-lookup"><span data-stu-id="0391a-116">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="0391a-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="0391a-117">-Name</span></span>
<span data-ttu-id="0391a-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="0391a-118">The resource name.</span></span>

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

### <span data-ttu-id="0391a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0391a-119">-ResourceGroupName</span></span>
<span data-ttu-id="0391a-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="0391a-120">The resource group name.</span></span>

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

### <span data-ttu-id="0391a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0391a-121">CommonParameters</span></span>
<span data-ttu-id="0391a-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0391a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0391a-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0391a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0391a-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0391a-124">INPUTS</span></span>

### <span data-ttu-id="0391a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0391a-125">System.String</span></span>

## <span data-ttu-id="0391a-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0391a-126">OUTPUTS</span></span>

### <span data-ttu-id="0391a-127">Microsoft. Azure. commands. Networks. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0391a-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="0391a-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0391a-128">NOTES</span></span>

## <span data-ttu-id="0391a-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0391a-129">RELATED LINKS</span></span>
