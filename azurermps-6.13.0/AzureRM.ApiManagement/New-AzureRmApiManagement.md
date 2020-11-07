---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: 98e90b4c8275028ab3e62e7383505775271e8d09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756040"
---
# <span data-ttu-id="9bb13-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="9bb13-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="9bb13-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9bb13-102">SYNOPSIS</span></span>
<span data-ttu-id="9bb13-103">Skapar en distribution av API-hantering.</span><span class="sxs-lookup"><span data-stu-id="9bb13-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bb13-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9bb13-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bb13-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9bb13-105">DESCRIPTION</span></span>
<span data-ttu-id="9bb13-106">Cmdleten **New-AzureRmApiManagement** skapar en distribution av API-hantering i Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="9bb13-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="9bb13-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9bb13-107">EXAMPLES</span></span>

### <span data-ttu-id="9bb13-108">Exempel 1: skapa en API-hanterings tjänst för en utvecklings nivå</span><span class="sxs-lookup"><span data-stu-id="9bb13-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="9bb13-109">Det här kommandot skapar en API-hanterings tjänst för utvecklings nivå.</span><span class="sxs-lookup"><span data-stu-id="9bb13-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="9bb13-110">Kommandot anger organisation och administratörs adress.</span><span class="sxs-lookup"><span data-stu-id="9bb13-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="9bb13-111">Kommandot anger inte parametern *SKU* .</span><span class="sxs-lookup"><span data-stu-id="9bb13-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="9bb13-112">Därför använder cmdleten standardvärdet för utvecklare.</span><span class="sxs-lookup"><span data-stu-id="9bb13-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="9bb13-113">Exempel 2: skapa en standard nivå tjänst med tre enheter</span><span class="sxs-lookup"><span data-stu-id="9bb13-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="9bb13-114">Det här kommandot skapar en API-tjänst för standard nivå med tre enheter.</span><span class="sxs-lookup"><span data-stu-id="9bb13-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="9bb13-115">Exempel 3: skapa en API-hanterings tjänst för ett externt virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="9bb13-115">Example 3: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="9bb13-116">Det här kommandot skapar en API-tjänst för Premium-nivå i ett Azure Virtual Network-undernät som har en extern Gateway slut punkt med ett huvud område i USA.</span><span class="sxs-lookup"><span data-stu-id="9bb13-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="9bb13-117">Exempel 4: skapa en API-hanterings tjänst för ett internt virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="9bb13-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="9bb13-118">Det här kommandot skapar en API-tjänst för Premium-nivå i ett Azure Virtual Network-undernät som har en intern Gateway slut punkt med ett huvud område i USA.</span><span class="sxs-lookup"><span data-stu-id="9bb13-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="9bb13-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9bb13-119">PARAMETERS</span></span>

### <span data-ttu-id="9bb13-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="9bb13-120">-AdditionalRegions</span></span>
<span data-ttu-id="9bb13-121">Ytterligare distributions områden i Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="9bb13-121">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="9bb13-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="9bb13-122">-AdminEmail</span></span>
<span data-ttu-id="9bb13-123">Anger den ursprungliga e-postadressen för alla meddelanden som skickas av API-hanterings systemet.</span><span class="sxs-lookup"><span data-stu-id="9bb13-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="9bb13-124">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="9bb13-124">-AssignIdentity</span></span>
<span data-ttu-id="9bb13-125">Skapa och tilldela en Azure Active Directory-identitet för den här servern för användning med Key Management Services, till exempel Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="9bb13-125">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="9bb13-126">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="9bb13-126">-Capacity</span></span>
<span data-ttu-id="9bb13-127">Anger SKU-kapaciteten för Azure API Management Service.</span><span class="sxs-lookup"><span data-stu-id="9bb13-127">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="9bb13-128">Standardvärdet är ett (1).</span><span class="sxs-lookup"><span data-stu-id="9bb13-128">The default is one (1).</span></span>

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

### <span data-ttu-id="9bb13-129">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="9bb13-129">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="9bb13-130">Anpassade värd konfigurations inställningar.</span><span class="sxs-lookup"><span data-stu-id="9bb13-130">Custom hostname configurations.</span></span> <span data-ttu-id="9bb13-131">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="9bb13-131">Default value is $null.</span></span> <span data-ttu-id="9bb13-132">Om du skickar $null anges standard värd namnet.</span><span class="sxs-lookup"><span data-stu-id="9bb13-132">Passing $null will set the default hostname.</span></span>

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

### <span data-ttu-id="9bb13-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bb13-133">-DefaultProfile</span></span>
<span data-ttu-id="9bb13-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9bb13-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bb13-135">-Plats</span><span class="sxs-lookup"><span data-stu-id="9bb13-135">-Location</span></span>
<span data-ttu-id="9bb13-136">Anger platsen där API-hanteringskonsolen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="9bb13-136">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="9bb13-137">För att få giltiga platser, Använd cmdleten Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | där {$ _. ResourceTypes [0]. ResourceTypeName-EQ "tjänst"} | Select-Object platser</span><span class="sxs-lookup"><span data-stu-id="9bb13-137">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="9bb13-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="9bb13-138">-Name</span></span>
<span data-ttu-id="9bb13-139">Anger ett namn på distributionen av API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="9bb13-139">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="9bb13-140">-Organisation</span><span class="sxs-lookup"><span data-stu-id="9bb13-140">-Organization</span></span>
<span data-ttu-id="9bb13-141">Anger namnet på en organisation.</span><span class="sxs-lookup"><span data-stu-id="9bb13-141">Specifies the name of an organization.</span></span>
<span data-ttu-id="9bb13-142">Med API-hantering används den här adressen i utvecklings portalen i e-postaviseringar.</span><span class="sxs-lookup"><span data-stu-id="9bb13-142">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="9bb13-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bb13-143">-ResourceGroupName</span></span>
<span data-ttu-id="9bb13-144">Anger namnet på den resurs grupp under vilken denna cmdlet skapar en distribution av API-hantering.</span><span class="sxs-lookup"><span data-stu-id="9bb13-144">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="9bb13-145">-SKU</span><span class="sxs-lookup"><span data-stu-id="9bb13-145">-Sku</span></span>
<span data-ttu-id="9bb13-146">Anger nivån för API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="9bb13-146">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="9bb13-147">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="9bb13-147">Valid values are:</span></span> 
- <span data-ttu-id="9bb13-148">Utvecklar</span><span class="sxs-lookup"><span data-stu-id="9bb13-148">Developer</span></span> 
- <span data-ttu-id="9bb13-149">Standar</span><span class="sxs-lookup"><span data-stu-id="9bb13-149">Standard</span></span> 
- <span data-ttu-id="9bb13-150">Premium standard är utvecklare.</span><span class="sxs-lookup"><span data-stu-id="9bb13-150">Premium The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bb13-151">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="9bb13-151">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="9bb13-152">Certifikat som utfärdas av intern CA för att installeras på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9bb13-152">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="9bb13-153">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="9bb13-153">Default value is $null.</span></span>

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

### <span data-ttu-id="9bb13-154">-Tagg</span><span class="sxs-lookup"><span data-stu-id="9bb13-154">-Tag</span></span>
<span data-ttu-id="9bb13-155">Ord lista med märkord.</span><span class="sxs-lookup"><span data-stu-id="9bb13-155">Tags dictionary.</span></span>

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

### <span data-ttu-id="9bb13-156">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9bb13-156">-VirtualNetwork</span></span>
<span data-ttu-id="9bb13-157">Konfigurations region för huvud nätverk för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="9bb13-157">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="9bb13-158">-VpnType</span><span class="sxs-lookup"><span data-stu-id="9bb13-158">-VpnType</span></span>
<span data-ttu-id="9bb13-159">Virtuell nätverks typ för distributionen av ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="9bb13-159">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="9bb13-160">Giltiga värden är</span><span class="sxs-lookup"><span data-stu-id="9bb13-160">Valid Values are</span></span> 
- <span data-ttu-id="9bb13-161">"Inget" (standardvärde.</span><span class="sxs-lookup"><span data-stu-id="9bb13-161">"None" (Default Value.</span></span> <span data-ttu-id="9bb13-162">ApiManagement ingår inte i något virtuellt nätverk ")</span><span class="sxs-lookup"><span data-stu-id="9bb13-162">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="9bb13-163">"Extern" (ApiManagement Deployment är konfigurerat i ett virtuellt nätverk med en slut punkt på Internet)</span><span class="sxs-lookup"><span data-stu-id="9bb13-163">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="9bb13-164">"Intern" (ApiManagement distributionen är konfigurerat i ett virtuellt nätverk som har en slut punkt för intranätet)</span><span class="sxs-lookup"><span data-stu-id="9bb13-164">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="9bb13-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bb13-165">CommonParameters</span></span>
<span data-ttu-id="9bb13-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bb13-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bb13-167">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bb13-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bb13-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9bb13-168">INPUTS</span></span>

### <span data-ttu-id="9bb13-169">System. String</span><span class="sxs-lookup"><span data-stu-id="9bb13-169">System.String</span></span>

### <span data-ttu-id="9bb13-170">System. Nullable ' 1 [[Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementSku, Microsoft. Azure. commands. ApiManagement, version = 6.1.2.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9bb13-170">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.Commands.ApiManagement, Version=6.1.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="9bb13-171">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9bb13-171">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="9bb13-172">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9bb13-172">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="9bb13-173">System. Collections. Generic. ordbok ' 2 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089], [system. String, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9bb13-173">System.Collections.Generic.Dictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="9bb13-174">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementRegion []</span><span class="sxs-lookup"><span data-stu-id="9bb13-174">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="9bb13-175">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementCustomHostNameConfiguration []</span><span class="sxs-lookup"><span data-stu-id="9bb13-175">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="9bb13-176">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementSystemCertificate []</span><span class="sxs-lookup"><span data-stu-id="9bb13-176">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="9bb13-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9bb13-177">OUTPUTS</span></span>

### <span data-ttu-id="9bb13-178">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9bb13-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="9bb13-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9bb13-179">NOTES</span></span>

## <span data-ttu-id="9bb13-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9bb13-180">RELATED LINKS</span></span>

[<span data-ttu-id="9bb13-181">Säkerhets kopiering-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="9bb13-181">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="9bb13-182">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="9bb13-182">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="9bb13-183">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="9bb13-183">Set-AzureRmApiManagement</span></span>](./Set-AzureRmApiManagement.md)

[<span data-ttu-id="9bb13-184">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="9bb13-184">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="9bb13-185">Återställ-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="9bb13-185">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


