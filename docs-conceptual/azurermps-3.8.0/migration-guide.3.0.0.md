# <a name="breaking-changes-for-microsoft-azure-powershell-300"></a><span data-ttu-id="2368c-101">Större ändringar för Microsoft Azure PowerShell 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="2368c-101">Breaking changes for Microsoft Azure PowerShell 3.0.0.</span></span>

<span data-ttu-id="2368c-102">Det här dokumentet fungerar både som ett meddelande om större ändringar och som en migreringsguide för användare av Microsoft Azure PowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="2368c-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="2368c-103">I varje avsnitt beskrivs både orsaken till den större ändringen och det enklaste migreringssättet.</span><span class="sxs-lookup"><span data-stu-id="2368c-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span>  <span data-ttu-id="2368c-104">Se den pull-begäran som är kopplad till varje ändring för en mer djupgående kontext.</span><span class="sxs-lookup"><span data-stu-id="2368c-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="2368c-105">Innehållsförteckning</span><span class="sxs-lookup"><span data-stu-id="2368c-105">Table of Contents</span></span>
1. [<span data-ttu-id="2368c-106">Större ändringar i Data Lake Store-cmdletar</span><span class="sxs-lookup"><span data-stu-id="2368c-106">Breaking changes to Data Lake Store cmdlets</span></span>](#breaking-changes-to-data-lake-store-cmdlets)
2. [<span data-ttu-id="2368c-107">Större ändringar i ApiManagement-cmdletar</span><span class="sxs-lookup"><span data-stu-id="2368c-107">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
3. [<span data-ttu-id="2368c-108">Större ändringar i Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="2368c-108">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)

## <a name="breaking-changes-to-data-lake-store-cmdlets"></a><span data-ttu-id="2368c-109">Större ändringar i Data Lake Store-cmdletar</span><span class="sxs-lookup"><span data-stu-id="2368c-109">Breaking changes to Data Lake Store cmdlets</span></span>

<span data-ttu-id="2368c-110">Följande cmdletar påverkades av den här uppdateringen ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)):</span><span class="sxs-lookup"><span data-stu-id="2368c-110">The following cmdlets were affected this release ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)):</span></span>

<span data-ttu-id="2368c-111">**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**</span><span class="sxs-lookup"><span data-stu-id="2368c-111">**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**</span></span>
- <span data-ttu-id="2368c-112">Den här cmdleten har tagits bort och ersatts av ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span><span class="sxs-lookup"><span data-stu-id="2368c-112">This cmdlet was removed and replaced with ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span></span>
- <span data-ttu-id="2368c-113">Den gamla cmdleten returnerade ett komplext objekt som representerar åtkomstkontrollistan (ACL).</span><span class="sxs-lookup"><span data-stu-id="2368c-113">The old cmdlet returned a complex object representing the access control list (ACL).</span></span> <span data-ttu-id="2368c-114">Följande nya cmdletar returnerar en enkel lista över poster i den valda sökvägens åtkomstkontrollista.</span><span class="sxs-lookup"><span data-stu-id="2368c-114">The new cmdlet returns a simple list of entries in the chosen path's ACL.</span></span>

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

<span data-ttu-id="2368c-115">**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**</span><span class="sxs-lookup"><span data-stu-id="2368c-115">**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**</span></span>
- <span data-ttu-id="2368c-116">Den här cmdleten ersätter den gamla cmdleten ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)``.</span><span class="sxs-lookup"><span data-stu-id="2368c-116">This cmdlet replaces the old cmdlet ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)``.</span></span>
- <span data-ttu-id="2368c-117">Den här nya cmdleten returnerar en enkel lista över poster i den valda sökvägens åtkomstkontrollista, av typen ``DataLakeStoreItemAce[]``.</span><span class="sxs-lookup"><span data-stu-id="2368c-117">This new cmdlet returns a simple list of entries in the chosen path's ACL, with type ``DataLakeStoreItemAce[]``.</span></span>
- <span data-ttu-id="2368c-118">Den här cmdletens utdata kan skickas till parametern ``-Acl`` för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="2368c-118">The output of this cmdlet can be passed in to the ``-Acl`` parameter of the following cmdlets:</span></span>
   - ``Remove-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAclEntry``

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

<span data-ttu-id="2368c-119">**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**</span><span class="sxs-lookup"><span data-stu-id="2368c-119">**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**</span></span>
- <span data-ttu-id="2368c-120">De här cmdletarna godkänner nu ``DataLakeStoreItemAce[]`` för parametern ``-Acl``.</span><span class="sxs-lookup"><span data-stu-id="2368c-120">These cmdlets now accept ``DataLakeStoreItemAce[]`` for the ``-Acl`` parameter.</span></span>
- <span data-ttu-id="2368c-121">``DataLakeStoreItemAce[]`` returneras av ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span><span class="sxs-lookup"><span data-stu-id="2368c-121">``DataLakeStoreItemAce[]`` is returned by ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span></span>

```powershell
# Old
$acl = Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $acl

# New
$aclEntries = Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $aclEntries
```

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="2368c-122">Större ändringar i ApiManagement-cmdletar</span><span class="sxs-lookup"><span data-stu-id="2368c-122">Breaking changes to ApiManagement cmdlets</span></span>

<span data-ttu-id="2368c-123">Följande cmdletar påverkades av den här uppdateringen ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)):</span><span class="sxs-lookup"><span data-stu-id="2368c-123">The following cmdlets were affected this release ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)):</span></span>

<span data-ttu-id="2368c-124">**New-AzureRmApiManagementVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="2368c-124">**New-AzureRmApiManagementVirtualNetwork**</span></span>
- <span data-ttu-id="2368c-125">De parametrar som är obligatoriska för att referera till ett virtuellt nätverk har ändrats från att kräva SubnetName och VnetId till SubnetResourceId i formatet ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``</span><span class="sxs-lookup"><span data-stu-id="2368c-125">The required parameters to reference a virtual network changed from requiring SubnetName and VnetId to SubnetResourceId in format ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``</span></span>

```powershell
# Old
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetName <String> -VnetId <Guid>

# New
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>

```

<span data-ttu-id="2368c-126">**Cmdleten Set-AzureRmApiManagementVirtualNetworks blir inaktuell**</span><span class="sxs-lookup"><span data-stu-id="2368c-126">**Deprecating Cmdlet Set-AzureRmApiManagementVirtualNetworks**</span></span>
- <span data-ttu-id="2368c-127">Cmdleten blir inaktuell eftersom det fanns fler än ett sätt att konfigurera virtuella nätverk som är kopplade till distribution av ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2368c-127">The Cmdlet is getting deprecated as there was more than one way to Set Virtual Network associated to ApiManagement deployment.</span></span>

```powershell
# Old
$networksList = @()
$networksList += New-AzureRmApiManagementVirtualNetwork -Location $vnetLocation -VnetId $vnetId -SubnetName $subnetName
Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $networksList

# New
$masterRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $masterRegionVirtualNetwork
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="2368c-128">Större ändringar i Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="2368c-128">Breaking changes to Network cmdlets</span></span>

<span data-ttu-id="2368c-129">Följande cmdletar påverkades av den här uppdateringen ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)):</span><span class="sxs-lookup"><span data-stu-id="2368c-129">The following cmdlets were affected this release ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)):</span></span>

<span data-ttu-id="2368c-130">**New-AzureRmVirtualNetworkGateway**</span><span class="sxs-lookup"><span data-stu-id="2368c-130">**New-AzureRmVirtualNetworkGateway**</span></span>
- <span data-ttu-id="2368c-131">En beskrivning av vad som har ändrats i ``:- Bool parameter:-ActiveActive`` tas bort och ``SwitchParameter:-EnableActiveActiveFeature`` läggs till för att aktivera funktionen aktiv-aktiv på en nyligen skapad virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="2368c-131">Description of what has changed ``:- Bool parameter:-ActiveActive`` is removed and ``SwitchParameter:-EnableActiveActiveFeature`` is added for enabling Active-Active feature on newly creating virtual network gateway.</span></span>

```powershell
# Old 
# Sample of how the cmdlet was previously called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -ActiveActive $true

# New
# Sample of how the cmdlet should now be called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -EnableActiveActiveFeature
```

<span data-ttu-id="2368c-132">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2368c-132">Set-AzureRmVirtualNetworkGateway</span></span>
- <span data-ttu-id="2368c-133">En beskrivning av vad som har ändrats i ``:- Bool parameter:-ActiveActive`` tas bort och två ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` läggs till för att aktivera och inaktivera funktionen aktiv-aktiv på en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="2368c-133">Description of what has changed ``:- Bool parameter:-ActiveActive`` is removed and 2 ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` are added for enabling and disabling Active-Active feature on virtual network gateway.</span></span>

```powershell
# Old
# Sample of how the cmdlet was previously called
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -ActiveActive $true
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -ActiveActive $false  

# New
# Sample of how the cmdlet should now be called
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -EnableActiveActiveFeature
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -DisableActiveActiveFeature
```