---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
ms.openlocfilehash: 489df2abd46f3ec198422991c2627804f6dc140b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745806"
---
# <span data-ttu-id="c0127-101">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c0127-101">New-AzApiManagement</span></span>

## <span data-ttu-id="c0127-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0127-102">SYNOPSIS</span></span>
<span data-ttu-id="c0127-103">Skapar en distribution av API-hantering.</span><span class="sxs-lookup"><span data-stu-id="c0127-103">Creates an API Management deployment.</span></span>

## <span data-ttu-id="c0127-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0127-104">SYNTAX</span></span>

```
New-AzApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>]
 [-SslSetting <PsApiManagementSslSetting>] [-AssignIdentity] [-EnableClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0127-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0127-105">DESCRIPTION</span></span>
<span data-ttu-id="c0127-106">Cmdleten **New-AzApiManagement** skapar en distribution av API-hantering i Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="c0127-106">The **New-AzApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="c0127-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0127-107">EXAMPLES</span></span>

### <span data-ttu-id="c0127-108">Exempel 1: skapa en API-hanterings tjänst för en utvecklings nivå</span><span class="sxs-lookup"><span data-stu-id="c0127-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="c0127-109">Det här kommandot skapar en API-hanterings tjänst för utvecklings nivå.</span><span class="sxs-lookup"><span data-stu-id="c0127-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="c0127-110">Kommandot anger organisation och administratörs adress.</span><span class="sxs-lookup"><span data-stu-id="c0127-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="c0127-111">Kommandot anger inte parametern *SKU* .</span><span class="sxs-lookup"><span data-stu-id="c0127-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="c0127-112">Därför använder cmdleten standardvärdet för utvecklare.</span><span class="sxs-lookup"><span data-stu-id="c0127-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="c0127-113">Exempel 2: skapa en standard nivå tjänst med tre enheter</span><span class="sxs-lookup"><span data-stu-id="c0127-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="c0127-114">Det här kommandot skapar en API-tjänst för standard nivå med tre enheter.</span><span class="sxs-lookup"><span data-stu-id="c0127-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="c0127-115">Exempel 3: skapa en tjänst på förbruknings nivå</span><span class="sxs-lookup"><span data-stu-id="c0127-115">Example 3: Create a Consumption tier service</span></span>
```powershell
PS D:\github\azure-powershell> New-AzApiManagement -ResourceGroupName Api-Default-North-Europe -Name consumptionskuservice -Location 'West Europe' -Sku Consumption -Organization microsoft -AdminEmail contoso@contoso.com -AssignIdentity -EnableClientCertificate

PublicIPAddresses                     :
PrivateIPAddresses                    :
Id                                    : /subscriptions/subid/resourceGroups/Api-Default-North-Europe/providers/Microsoft.ApiManagement/service/consumptionskuservice
Name                                  : consumptionskuservice
Location                              : West Europe
Sku                                   : Consumption
Capacity                              : 0
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://consumptionskuservice.azure-api.net
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {consumptionskuservice.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity
EnableClientCertificate               : True
ResourceGroupName                     : Api-Default-North-Europe
```

<span data-ttu-id="c0127-116">Det här kommandot skapar en API-tjänst för förbruknings nivå med klient certifikat aktiverat i Västeuropa, Europa.</span><span class="sxs-lookup"><span data-stu-id="c0127-116">This command creates a consumption tier API Management service with Client Certificate enabled in west Europe.</span></span>

### <span data-ttu-id="c0127-117">Exempel 4: skapa en API-hanterings tjänst för ett externt virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="c0127-117">Example 4: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="c0127-118">Det här kommandot skapar en API-tjänst för Premium-nivå i ett Azure Virtual Network-undernät som har en extern Gateway slut punkt med ett huvud område i USA.</span><span class="sxs-lookup"><span data-stu-id="c0127-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="c0127-119">Exempel 5: skapa en API-hanterings tjänst för ett internt virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="c0127-119">Example 5: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="c0127-120">Det här kommandot skapar en API-tjänst för Premium-nivå i ett Azure Virtual Network-undernät som har en intern Gateway slut punkt med ett huvud område i USA.</span><span class="sxs-lookup"><span data-stu-id="c0127-120">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="c0127-121">Exempel 6: skapa en API-hanterings tjänst och Aktivera TLS 1,0-protokollet</span><span class="sxs-lookup"><span data-stu-id="c0127-121">Example 6: Create an API Management service and Enable TLS 1.0 protocol</span></span>
```powershell
PS C:\> $enableTls=@{"Tls10" = "True"}
PS C:\> $sslSetting = New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls
PS C:\> New-AzApiManagement -ResourceGroupName Api-Default-CentralUS -Name "testtlspowershell" -Sku Standard -Location "CentralUS" -Organization "Microsoft" -AdminEmail "bar@contoso.com" -SslSetting $sslSetting

PublicIPAddresses                     : {23.99.140.18}
PrivateIPAddresses                    :
Id                                    : /subscriptions/subid/resourceGroups/Api-Default-CentralUS/providers/Microsoft.ApiManagement/service/testtlspowershell
Name                                  : testtlspowershell
Location                              : Central US
Sku                                   : Standard
Capacity                              : 1
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://testtlspowershell.azure-api.net
RuntimeRegionalUrl                    : https://testtlspowershell-centralus-01.regional.azure-api.net
PortalUrl                             : https://testtlspowershell.portal.azure-api.net
ManagementApiUrl                      : https://testtlspowershell.management.azure-api.net
ScmUrl                                : https://testtlspowershell.scm.azure-api.net
PublisherEmail                        : bar@contoso.com
OrganizationName                      : Microsoft
NotificationSenderEmail               : apimgmt-noreply@mail.windowsazure.com
VirtualNetwork                        :
VpnType                               : None
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {testtlspowershell.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              :
EnableClientCertificate               :
ResourceGroupName                     : Api-Default-CentralUS
```

<span data-ttu-id="c0127-122">Det här kommandot skapar en standard tjänst för API-hantering för SKU och aktiverar TLS 1,0 på klient delen av klienten till ApiManagement gateway-och backend-klient mellan ApiManagement gateway och Server del.</span><span class="sxs-lookup"><span data-stu-id="c0127-122">This command creates a Standard SKU Api Management service and Enable TLS 1.0 on Frontend client to ApiManagement Gateway and Backend client between ApiManagement Gateway and Backend.</span></span>

## <span data-ttu-id="c0127-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0127-123">PARAMETERS</span></span>

### <span data-ttu-id="c0127-124">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="c0127-124">-AdditionalRegions</span></span>
<span data-ttu-id="c0127-125">Ytterligare distributions områden i Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="c0127-125">Additional deployment regions of Azure API Management.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0127-126">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="c0127-126">-AdminEmail</span></span>
<span data-ttu-id="c0127-127">Anger den ursprungliga e-postadressen för alla meddelanden som skickas av API-hanterings systemet.</span><span class="sxs-lookup"><span data-stu-id="c0127-127">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0127-128">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c0127-128">-AssignIdentity</span></span>
<span data-ttu-id="c0127-129">Skapa och tilldela en Azure Active Directory-identitet för den här servern för användning med Key Management Services, till exempel Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="c0127-129">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0127-130">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="c0127-130">-Capacity</span></span>
<span data-ttu-id="c0127-131">Anger SKU-kapaciteten för Azure API Management Service.</span><span class="sxs-lookup"><span data-stu-id="c0127-131">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="c0127-132">Standardvärdet är ett (1).</span><span class="sxs-lookup"><span data-stu-id="c0127-132">The default is one (1).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0127-133">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0127-133">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="c0127-134">Anpassade värd konfigurations inställningar.</span><span class="sxs-lookup"><span data-stu-id="c0127-134">Custom hostname configurations.</span></span> <span data-ttu-id="c0127-135">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="c0127-135">Default value is $null.</span></span> <span data-ttu-id="c0127-136">Om du skickar $null anges standard värd namnet.</span><span class="sxs-lookup"><span data-stu-id="c0127-136">Passing $null will set the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0127-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0127-137">-DefaultProfile</span></span>
<span data-ttu-id="c0127-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c0127-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0127-139">-EnableClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c0127-139">-EnableClientCertificate</span></span>
<span data-ttu-id="c0127-140">Flagg endast avsedda att användas för förbruknings-SKU ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c0127-140">Flag only meant to be used for Consumption SKU ApiManagement Service.</span></span> <span data-ttu-id="c0127-141">Detta tillämpar att ett klient certifikat visas för varje begäran till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="c0127-141">This enforces a client certificate to be presented on each request to the gateway.</span></span> <span data-ttu-id="c0127-142">Det gör det också möjligt att autentisera certifikatet i principen för gatewayen.</span><span class="sxs-lookup"><span data-stu-id="c0127-142">This also enables the ability to authenticate the certificate in the policy on the gateway.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0127-143">-Plats</span><span class="sxs-lookup"><span data-stu-id="c0127-143">-Location</span></span>
<span data-ttu-id="c0127-144">Anger platsen där API-hanteringskonsolen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="c0127-144">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="c0127-145">För att få giltiga platser, Använd cmdleten Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | där {$ _. ResourceTypes [0]. ResourceTypeName-EQ "tjänst"} | Select-Object platser</span><span class="sxs-lookup"><span data-stu-id="c0127-145">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0127-146">-Namn</span><span class="sxs-lookup"><span data-stu-id="c0127-146">-Name</span></span>
<span data-ttu-id="c0127-147">Anger ett namn på distributionen av API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="c0127-147">Specifies a name for the API Management deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0127-148">-Organisation</span><span class="sxs-lookup"><span data-stu-id="c0127-148">-Organization</span></span>
<span data-ttu-id="c0127-149">Anger namnet på en organisation.</span><span class="sxs-lookup"><span data-stu-id="c0127-149">Specifies the name of an organization.</span></span>
<span data-ttu-id="c0127-150">Med API-hantering används den här adressen i utvecklings portalen i e-postaviseringar.</span><span class="sxs-lookup"><span data-stu-id="c0127-150">API Management uses this address in the developer portal in email notifications.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0127-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0127-151">-ResourceGroupName</span></span>
<span data-ttu-id="c0127-152">Anger namnet på den resurs grupp under vilken denna cmdlet skapar en distribution av API-hantering.</span><span class="sxs-lookup"><span data-stu-id="c0127-152">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0127-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="c0127-153">-Sku</span></span>
<span data-ttu-id="c0127-154">Anger nivån för API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="c0127-154">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="c0127-155">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="c0127-155">Valid values are:</span></span> 
- <span data-ttu-id="c0127-156">Utvecklar</span><span class="sxs-lookup"><span data-stu-id="c0127-156">Developer</span></span> 
- <span data-ttu-id="c0127-157">Standar</span><span class="sxs-lookup"><span data-stu-id="c0127-157">Standard</span></span> 
- <span data-ttu-id="c0127-158">Premium standard är utvecklare.</span><span class="sxs-lookup"><span data-stu-id="c0127-158">Premium The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Basic, Standard, Premium, Consumption

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0127-159">-SslSetting</span><span class="sxs-lookup"><span data-stu-id="c0127-159">-SslSetting</span></span>
<span data-ttu-id="c0127-160">SSL-inställningen för ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c0127-160">The Ssl Setting of the ApiManagement Service.</span></span> <span data-ttu-id="c0127-161">Standardvärdet är $null</span><span class="sxs-lookup"><span data-stu-id="c0127-161">Default value is $null</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0127-162">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0127-162">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="c0127-163">Certifikat som utfärdas av intern CA för att installeras på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c0127-163">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="c0127-164">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="c0127-164">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0127-165">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c0127-165">-Tag</span></span>
<span data-ttu-id="c0127-166">Ord lista med märkord.</span><span class="sxs-lookup"><span data-stu-id="c0127-166">Tags dictionary.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0127-167">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c0127-167">-VirtualNetwork</span></span>
<span data-ttu-id="c0127-168">Konfigurations region för huvud nätverk för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="c0127-168">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0127-169">-VpnType</span><span class="sxs-lookup"><span data-stu-id="c0127-169">-VpnType</span></span>
<span data-ttu-id="c0127-170">Virtuell nätverks typ för distributionen av ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="c0127-170">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="c0127-171">Giltiga värden är</span><span class="sxs-lookup"><span data-stu-id="c0127-171">Valid Values are</span></span> 
- <span data-ttu-id="c0127-172">"Inget" (standardvärde.</span><span class="sxs-lookup"><span data-stu-id="c0127-172">"None" (Default Value.</span></span> <span data-ttu-id="c0127-173">ApiManagement ingår inte i något virtuellt nätverk ")</span><span class="sxs-lookup"><span data-stu-id="c0127-173">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="c0127-174">"Extern" (ApiManagement Deployment är konfigurerat i ett virtuellt nätverk med en slut punkt på Internet)</span><span class="sxs-lookup"><span data-stu-id="c0127-174">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="c0127-175">"Intern" (ApiManagement distributionen är konfigurerat i ett virtuellt nätverk som har en slut punkt för intranätet)</span><span class="sxs-lookup"><span data-stu-id="c0127-175">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: (All)
Aliases:
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0127-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0127-176">CommonParameters</span></span>
<span data-ttu-id="c0127-177">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0127-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0127-178">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0127-178">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0127-179">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0127-179">INPUTS</span></span>

### <span data-ttu-id="c0127-180">System. String</span><span class="sxs-lookup"><span data-stu-id="c0127-180">System.String</span></span>

### <span data-ttu-id="c0127-181">System. Nullable ' 1 [[Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementSku, Microsoft. Azure. PowerShell. cmdletar. ApiManagement, version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c0127-181">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="c0127-182">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c0127-182">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c0127-183">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c0127-183">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="c0127-184">System. Collections. Generic. ordbok ' 2 [[system. String, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e], [system. String, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c0127-184">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c0127-185">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementRegion []</span><span class="sxs-lookup"><span data-stu-id="c0127-185">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="c0127-186">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementCustomHostNameConfiguration []</span><span class="sxs-lookup"><span data-stu-id="c0127-186">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="c0127-187">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementSystemCertificate []</span><span class="sxs-lookup"><span data-stu-id="c0127-187">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="c0127-188">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0127-188">OUTPUTS</span></span>

### <span data-ttu-id="c0127-189">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="c0127-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="c0127-190">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0127-190">NOTES</span></span>

## <span data-ttu-id="c0127-191">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0127-191">RELATED LINKS</span></span>

[<span data-ttu-id="c0127-192">Säkerhets kopiering-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c0127-192">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="c0127-193">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c0127-193">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="c0127-194">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c0127-194">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

[<span data-ttu-id="c0127-195">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c0127-195">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="c0127-196">Återställ-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c0127-196">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)

