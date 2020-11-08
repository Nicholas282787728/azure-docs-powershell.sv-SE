---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
ms.openlocfilehash: d6657c9402eff46d274d982170e167cd97a29a9a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091811"
---
# <span data-ttu-id="a52dd-101">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a52dd-101">Get-AzFirewall</span></span>

## <span data-ttu-id="a52dd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a52dd-102">SYNOPSIS</span></span>
<span data-ttu-id="a52dd-103">Får en Azure-brandvägg.</span><span class="sxs-lookup"><span data-stu-id="a52dd-103">Gets a Azure Firewall.</span></span>

## <span data-ttu-id="a52dd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a52dd-104">SYNTAX</span></span>

```
Get-AzFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a52dd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a52dd-105">DESCRIPTION</span></span>
<span data-ttu-id="a52dd-106">Cmdleten **Get-AzFirewall** hämtar en eller flera brand väggar i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a52dd-106">The **Get-AzFirewall** cmdlet gets one or more Firewalls in a resource group.</span></span>

## <span data-ttu-id="a52dd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a52dd-107">EXAMPLES</span></span>

### <span data-ttu-id="a52dd-108">1: Hämta alla brand väggar i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="a52dd-108">1:  Retrieve all Firewalls in a resource group</span></span>
```
Get-AzFirewall -ResourceGroupName rgName

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}

Name                       : azFw1
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw1
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw1/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="a52dd-109">I det här exemplet hämtas alla brand väggar i resurs gruppen "rgName".</span><span class="sxs-lookup"><span data-stu-id="a52dd-109">This example retrieves all Firewalls in resource group "rgName".</span></span>

### <span data-ttu-id="a52dd-110">2: Hämta en brand vägg efter namn</span><span class="sxs-lookup"><span data-stu-id="a52dd-110">2:  Retrieve a Firewall by name</span></span>
```
Get-AzFirewall -ResourceGroupName rgName -Name azFw

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="a52dd-111">I det här exemplet hämtas brand väggen med namnet "azFw" i resurs gruppen "rgName".</span><span class="sxs-lookup"><span data-stu-id="a52dd-111">This example retrieves Firewall named "azFw" in resource group "rgName".</span></span>

### <span data-ttu-id="a52dd-112">3: Hämta alla brand väggar med filtrering</span><span class="sxs-lookup"><span data-stu-id="a52dd-112">3:  Retrieve all Firewalls with filtering</span></span>
```
Get-AzFirewall -Name azFw*

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}

Name                       : azFw1
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw1
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw1/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="a52dd-113">I det här exemplet hämtas alla brand väggar som börjar med "azFw"</span><span class="sxs-lookup"><span data-stu-id="a52dd-113">This example retrieves all Firewalls that start with "azFw"</span></span>

### <span data-ttu-id="a52dd-114">4: Hämta en brand vägg och Lägg till en program regel samling i brand väggen</span><span class="sxs-lookup"><span data-stu-id="a52dd-114">4:  Retrieve a firewall and then add a application rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

<span data-ttu-id="a52dd-115">I det här exemplet hämtas en brand vägg och läggs sedan till i brand väggen genom att anropa metoden AddApplicationRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="a52dd-115">This example retrieves a firewall, then adds a application rule collection to the firewall by calling method AddApplicationRuleCollection.</span></span>

### <span data-ttu-id="a52dd-116">5: Hämta en brand vägg och Lägg sedan till en nätverks regel samling i brand väggen</span><span class="sxs-lookup"><span data-stu-id="a52dd-116">5:  Retrieve a firewall and then add a network rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "Udp" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

<span data-ttu-id="a52dd-117">I det här exemplet hämtas en brand vägg och en nätverks regel läggs till i brand väggen genom att anropa metoden AddNetworkRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="a52dd-117">This example retrieves a firewall, then adds a network rule collection to the firewall by calling method AddNetworkRuleCollection.</span></span>

### <span data-ttu-id="a52dd-118">6: Hämta en brand vägg och hämta en samling med program regler efter namn från brand väggen</span><span class="sxs-lookup"><span data-stu-id="a52dd-118">6:  Retrieve a firewall and then retrieve a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="a52dd-119">I det här exemplet hämtas en brand vägg och sedan får regel samlingen ett namn som anropar metod GetApplicationRuleCollectionByName på brand Väggs objekt.</span><span class="sxs-lookup"><span data-stu-id="a52dd-119">This example retrieves a firewall and then gets a rule collection by name, calling method GetApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="a52dd-120">Namnet på regel samlingen för metod GetApplicationRuleCollectionByName är Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="a52dd-120">The rule collection name for method GetApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="a52dd-121">7: Hämta en brand vägg och hämta en nätverks regel samling efter namn från brand väggen</span><span class="sxs-lookup"><span data-stu-id="a52dd-121">7:  Retrieve a firewall and then retrieve a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="a52dd-122">I det här exemplet hämtas en brand vägg och sedan får regel samlingen ett namn som anropar metod GetNetworkRuleCollectionByName på brand Väggs objekt.</span><span class="sxs-lookup"><span data-stu-id="a52dd-122">This example retrieves a firewall and then gets a rule collection by name, calling method GetNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="a52dd-123">Namnet på regel samlingen för metod GetNetworkRuleCollectionByName är Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="a52dd-123">The rule collection name for method GetNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="a52dd-124">8: Hämta en brand vägg och ta sedan bort en samling med program regler efter namn från brand väggen</span><span class="sxs-lookup"><span data-stu-id="a52dd-124">8:  Retrieve a firewall and then remove a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="a52dd-125">I det här exemplet hämtas en brand vägg och sedan tas en regel samling bort från namn, metod RemoveApplicationRuleCollectionByName på brand Väggs objekt.</span><span class="sxs-lookup"><span data-stu-id="a52dd-125">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="a52dd-126">Namnet på regel samlingen för metod RemoveApplicationRuleCollectionByName är Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="a52dd-126">The rule collection name for method RemoveApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="a52dd-127">9: Hämta en brand vägg och ta sedan bort en nätverks regel samling efter namn från brand väggen</span><span class="sxs-lookup"><span data-stu-id="a52dd-127">9:  Retrieve a firewall and then remove a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="a52dd-128">I det här exemplet hämtas en brand vägg och sedan tas en regel samling bort från namn, metod RemoveNetworkRuleCollectionByName på brand Väggs objekt.</span><span class="sxs-lookup"><span data-stu-id="a52dd-128">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="a52dd-129">Namnet på regel samlingen för metod RemoveNetworkRuleCollectionByName är Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="a52dd-129">The rule collection name for method RemoveNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="a52dd-130">10: Hämta en brand vägg och koppla sedan brand väggen</span><span class="sxs-lookup"><span data-stu-id="a52dd-130">10:  Retrieve a firewall and then allocate the firewall</span></span>
```
$vnet=Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

<span data-ttu-id="a52dd-131">I det här exemplet hämtas en brand vägg och samtal för att starta brand Väggs tjänsten med den konfiguration (program-och nätverks regel samlingar) som är kopplade till brand väggen.</span><span class="sxs-lookup"><span data-stu-id="a52dd-131">This example retrieves a firewall and calls Allocate on the firewall to start the firewall service using the configuration (application and network rule collections) associated with the firewall.</span></span>

## <span data-ttu-id="a52dd-132">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a52dd-132">PARAMETERS</span></span>

### <span data-ttu-id="a52dd-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a52dd-133">-DefaultProfile</span></span>
<span data-ttu-id="a52dd-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a52dd-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a52dd-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="a52dd-135">-Name</span></span>
<span data-ttu-id="a52dd-136">Anger namnet på den brand vägg som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="a52dd-136">Specifies the name of the Firewall that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a52dd-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a52dd-137">-ResourceGroupName</span></span>
<span data-ttu-id="a52dd-138">Anger namnet på den resurs grupp som brand väggen tillhör.</span><span class="sxs-lookup"><span data-stu-id="a52dd-138">Specifies the name of the resource group that Firewall belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a52dd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a52dd-139">CommonParameters</span></span>
<span data-ttu-id="a52dd-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a52dd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a52dd-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a52dd-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a52dd-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a52dd-142">INPUTS</span></span>

### <span data-ttu-id="a52dd-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a52dd-143">System.String</span></span>

## <span data-ttu-id="a52dd-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a52dd-144">OUTPUTS</span></span>

### <span data-ttu-id="a52dd-145">Microsoft. Azure. commands. Networks. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="a52dd-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="a52dd-146">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. Network. Models. PSAzureFirewall, Microsoft. Azure. PowerShell. cmdletar. Network, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a52dd-146">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a52dd-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a52dd-147">NOTES</span></span>

## <span data-ttu-id="a52dd-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a52dd-148">RELATED LINKS</span></span>

[<span data-ttu-id="a52dd-149">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a52dd-149">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="a52dd-150">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a52dd-150">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="a52dd-151">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a52dd-151">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
