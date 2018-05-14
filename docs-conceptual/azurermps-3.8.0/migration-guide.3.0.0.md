# <a name="breaking-changes-for-microsoft-azure-powershell-300"></a>Större ändringar för Microsoft Azure PowerShell 3.0.0.

Det här dokumentet fungerar både som ett meddelande om större ändringar och som en migreringsguide för användare av Microsoft Azure PowerShell-cmdletar.  I varje avsnitt beskrivs både orsaken till den större ändringen och det enklaste migreringssättet.  Se den pull-begäran som är kopplad till varje ändring för en mer djupgående kontext.

## <a name="table-of-contents"></a>Innehållsförteckning
1. [Större ändringar i Data Lake Store-cmdletar](#breaking-changes-to-data-lake-store-cmdlets)
2. [Större ändringar i ApiManagement-cmdletar](#breaking-changes-to-apimanagement-cmdlets)
3. [Större ändringar i Network-cmdletar](#breaking-changes-to-network-cmdlets)

## <a name="breaking-changes-to-data-lake-store-cmdlets"></a>Större ändringar i Data Lake Store-cmdletar

Följande cmdletar påverkades av den här uppdateringen ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)):

**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**
- Den här cmdleten har tagits bort och ersatts av ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.
- Den gamla cmdleten returnerade ett komplext objekt som representerar åtkomstkontrollistan (ACL). Följande nya cmdletar returnerar en enkel lista över poster i den valda sökvägens åtkomstkontrollista.

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**
- Den här cmdleten ersätter den gamla cmdleten ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)``.
- Den här nya cmdleten returnerar en enkel lista över poster i den valda sökvägens åtkomstkontrollista, av typen ``DataLakeStoreItemAce[]``.
- Den här cmdletens utdata kan skickas till parametern ``-Acl`` för följande cmdletar:
   - ``Remove-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAclEntry``

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**
- De här cmdletarna godkänner nu ``DataLakeStoreItemAce[]`` för parametern ``-Acl``.
- ``DataLakeStoreItemAce[]`` returneras av ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.

```powershell
# Old
$acl = Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $acl

# New
$aclEntries = Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $aclEntries
```

## <a name="breaking-changes-to-apimanagement-cmdlets"></a>Större ändringar i ApiManagement-cmdletar

Följande cmdletar påverkades av den här uppdateringen ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)):

**New-AzureRmApiManagementVirtualNetwork**
- De parametrar som är obligatoriska för att referera till ett virtuellt nätverk har ändrats från att kräva SubnetName och VnetId till SubnetResourceId i formatet ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``

```powershell
# Old
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetName <String> -VnetId <Guid>

# New
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>

```

**Cmdleten Set-AzureRmApiManagementVirtualNetworks blir inaktuell**
- Cmdleten blir inaktuell eftersom det fanns fler än ett sätt att konfigurera virtuella nätverk som är kopplade till distribution av ApiManagement.

```powershell
# Old
$networksList = @()
$networksList += New-AzureRmApiManagementVirtualNetwork -Location $vnetLocation -VnetId $vnetId -SubnetName $subnetName
Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $networksList

# New
$masterRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $masterRegionVirtualNetwork
```

## <a name="breaking-changes-to-network-cmdlets"></a>Större ändringar i Network-cmdletar

Följande cmdletar påverkades av den här uppdateringen ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)):

**New-AzureRmVirtualNetworkGateway**
- En beskrivning av vad som har ändrats i ``:- Bool parameter:-ActiveActive`` tas bort och ``SwitchParameter:-EnableActiveActiveFeature`` läggs till för att aktivera funktionen aktiv-aktiv på en nyligen skapad virtuell nätverksgateway.

```powershell
# Old 
# Sample of how the cmdlet was previously called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -ActiveActive $true

# New
# Sample of how the cmdlet should now be called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -EnableActiveActiveFeature
```

Set-AzureRmVirtualNetworkGateway
- En beskrivning av vad som har ändrats i ``:- Bool parameter:-ActiveActive`` tas bort och två ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` läggs till för att aktivera och inaktivera funktionen aktiv-aktiv på en virtuell nätverksgateway.

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