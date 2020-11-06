---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: 82e09e146999ce0bd320ba398ab2f196f1115688
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578667"
---
# <span data-ttu-id="98892-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="98892-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="98892-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="98892-102">SYNOPSIS</span></span>
<span data-ttu-id="98892-103">Skapar en distribution av API-hantering.</span><span class="sxs-lookup"><span data-stu-id="98892-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98892-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="98892-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98892-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="98892-105">DESCRIPTION</span></span>
<span data-ttu-id="98892-106">Cmdleten **New-AzureRmApiManagement** skapar en distribution av API-hantering i Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="98892-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="98892-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="98892-107">EXAMPLES</span></span>

### <span data-ttu-id="98892-108">Exempel 1: skapa en API-hanterings tjänst för en utvecklings nivå</span><span class="sxs-lookup"><span data-stu-id="98892-108">Example 1: Create a Developer tier API Management service</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="98892-109">Det här kommandot skapar en API-hanterings tjänst för utvecklings nivå.</span><span class="sxs-lookup"><span data-stu-id="98892-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="98892-110">Kommandot anger organisation och administratörs adress.</span><span class="sxs-lookup"><span data-stu-id="98892-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="98892-111">Kommandot anger inte parametern *SKU* .</span><span class="sxs-lookup"><span data-stu-id="98892-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="98892-112">Därför använder cmdleten standardvärdet för utvecklare.</span><span class="sxs-lookup"><span data-stu-id="98892-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="98892-113">Exempel 2: skapa en standard nivå tjänst med tre enheter</span><span class="sxs-lookup"><span data-stu-id="98892-113">Example 2: Create a Standard tier service that has three units</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="98892-114">Det här kommandot skapar en API-tjänst för standard nivå med tre enheter.</span><span class="sxs-lookup"><span data-stu-id="98892-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="98892-115">Exempel 3: skapa en API-hanterings tjänst för ett externt virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="98892-115">Example 3: Create an API Management service for an external virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="98892-116">Det här kommandot skapar en API-tjänst för Premium-nivå i ett Azure Virtual Network-undernät som har en extern Gateway slut punkt med ett huvud område i USA.</span><span class="sxs-lookup"><span data-stu-id="98892-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="98892-117">Exempel 4: skapa en API-hanterings tjänst för ett internt virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="98892-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="98892-118">Det här kommandot skapar en API-tjänst för Premium-nivå i ett Azure Virtual Network-undernät som har en intern Gateway slut punkt med ett huvud område i USA.</span><span class="sxs-lookup"><span data-stu-id="98892-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="98892-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="98892-119">PARAMETERS</span></span>

### <span data-ttu-id="98892-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="98892-120">-AdditionalRegions</span></span>
<span data-ttu-id="98892-121">Ytterligare distributions områden i Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="98892-121">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="98892-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="98892-122">-AdminEmail</span></span>
<span data-ttu-id="98892-123">Anger den ursprungliga e-postadressen för alla meddelanden som skickas av API-hanterings systemet.</span><span class="sxs-lookup"><span data-stu-id="98892-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="98892-124">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="98892-124">-Capacity</span></span>
<span data-ttu-id="98892-125">Anger SKU-kapaciteten för Azure API Management Service.</span><span class="sxs-lookup"><span data-stu-id="98892-125">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="98892-126">Standardvärdet är ett (1).</span><span class="sxs-lookup"><span data-stu-id="98892-126">The default is one (1).</span></span>

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

### <span data-ttu-id="98892-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="98892-127">-Location</span></span>
<span data-ttu-id="98892-128">Anger den plats där den här cmdleten skapar en distribution av API-hantering.</span><span class="sxs-lookup"><span data-stu-id="98892-128">Specifies the location in which this cmdlet creates an API Management deployment.</span></span>
<span data-ttu-id="98892-129">Använd cmdletarna Get-AzureLocation för att få giltiga platser.</span><span class="sxs-lookup"><span data-stu-id="98892-129">To obtain valid locations, use the Get-AzureLocation cmdlets.</span></span>

<span data-ttu-id="98892-130">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="98892-130">Valid values are:</span></span> 

- <span data-ttu-id="98892-131">Norra Central USA</span><span class="sxs-lookup"><span data-stu-id="98892-131">North Central US</span></span>
- <span data-ttu-id="98892-132">Södra centrala USA</span><span class="sxs-lookup"><span data-stu-id="98892-132">South Central US</span></span>
- <span data-ttu-id="98892-133">Central</span><span class="sxs-lookup"><span data-stu-id="98892-133">Central US</span></span>
- <span data-ttu-id="98892-134">Västeuropa</span><span class="sxs-lookup"><span data-stu-id="98892-134">West Europe</span></span>
- <span data-ttu-id="98892-135">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="98892-135">North Europe</span></span>
- <span data-ttu-id="98892-136">Västra USA</span><span class="sxs-lookup"><span data-stu-id="98892-136">West US</span></span>
- <span data-ttu-id="98892-137">Östra USA</span><span class="sxs-lookup"><span data-stu-id="98892-137">East US</span></span>
- <span data-ttu-id="98892-138">Östra USA 2</span><span class="sxs-lookup"><span data-stu-id="98892-138">East US 2</span></span>
- <span data-ttu-id="98892-139">Östra Japan</span><span class="sxs-lookup"><span data-stu-id="98892-139">Japan East</span></span>
- <span data-ttu-id="98892-140">Västra Japan</span><span class="sxs-lookup"><span data-stu-id="98892-140">Japan West</span></span>
- <span data-ttu-id="98892-141">Brasilien, Syd</span><span class="sxs-lookup"><span data-stu-id="98892-141">Brazil South</span></span>
- <span data-ttu-id="98892-142">Sydostasien</span><span class="sxs-lookup"><span data-stu-id="98892-142">Southeast Asia</span></span>
- <span data-ttu-id="98892-143">Östasien</span><span class="sxs-lookup"><span data-stu-id="98892-143">East Asia</span></span>
- <span data-ttu-id="98892-144">Östra Australien</span><span class="sxs-lookup"><span data-stu-id="98892-144">Australia East</span></span>
- <span data-ttu-id="98892-145">Australien, sydöst</span><span class="sxs-lookup"><span data-stu-id="98892-145">Australia Southeast</span></span>

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

### <span data-ttu-id="98892-146">-Namn</span><span class="sxs-lookup"><span data-stu-id="98892-146">-Name</span></span>
<span data-ttu-id="98892-147">Anger ett namn på distributionen av API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="98892-147">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="98892-148">-Organisation</span><span class="sxs-lookup"><span data-stu-id="98892-148">-Organization</span></span>
<span data-ttu-id="98892-149">Anger namnet på en organisation.</span><span class="sxs-lookup"><span data-stu-id="98892-149">Specifies the name of an organization.</span></span>
<span data-ttu-id="98892-150">Med API-hantering används den här adressen i utvecklings portalen i e-postaviseringar.</span><span class="sxs-lookup"><span data-stu-id="98892-150">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="98892-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98892-151">-ResourceGroupName</span></span>
<span data-ttu-id="98892-152">Anger namnet på den resurs grupp under vilken denna cmdlet skapar en distribution av API-hantering.</span><span class="sxs-lookup"><span data-stu-id="98892-152">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="98892-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="98892-153">-Sku</span></span>
<span data-ttu-id="98892-154">Anger nivån för API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="98892-154">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="98892-155">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="98892-155">Valid values are:</span></span> 

- <span data-ttu-id="98892-156">Utvecklar</span><span class="sxs-lookup"><span data-stu-id="98892-156">Developer</span></span> 
- <span data-ttu-id="98892-157">Standar</span><span class="sxs-lookup"><span data-stu-id="98892-157">Standard</span></span> 
- <span data-ttu-id="98892-158">Beta</span><span class="sxs-lookup"><span data-stu-id="98892-158">Premium</span></span> 

<span data-ttu-id="98892-159">Standardvärdet är utvecklare.</span><span class="sxs-lookup"><span data-stu-id="98892-159">The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98892-160">-Taggar</span><span class="sxs-lookup"><span data-stu-id="98892-160">-Tags</span></span>
<span data-ttu-id="98892-161">Anger en ord lista med taggar.</span><span class="sxs-lookup"><span data-stu-id="98892-161">Specifies a dictionary of tags.</span></span>

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

### <span data-ttu-id="98892-162">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="98892-162">-VirtualNetwork</span></span>
<span data-ttu-id="98892-163">Konfigurations region för huvud nätverk för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="98892-163">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="98892-164">-VpnType</span><span class="sxs-lookup"><span data-stu-id="98892-164">-VpnType</span></span>
<span data-ttu-id="98892-165">Virtuell nätverks typ för distributionen av ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="98892-165">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="98892-166">Giltiga värden är</span><span class="sxs-lookup"><span data-stu-id="98892-166">Valid Values are</span></span> 
- <span data-ttu-id="98892-167">"Inget" (standardvärde.</span><span class="sxs-lookup"><span data-stu-id="98892-167">"None" (Default Value.</span></span> <span data-ttu-id="98892-168">ApiManagement ingår inte i något virtuellt nätverk ")</span><span class="sxs-lookup"><span data-stu-id="98892-168">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="98892-169">"Extern" (ApiManagement Deployment är konfigurerat i ett virtuellt nätverk med en slut punkt på Internet)</span><span class="sxs-lookup"><span data-stu-id="98892-169">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="98892-170">"Intern" (ApiManagement distributionen är konfigurerat i ett virtuellt nätverk som har en slut punkt för intranätet)</span><span class="sxs-lookup"><span data-stu-id="98892-170">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="98892-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98892-171">-DefaultProfile</span></span>
<span data-ttu-id="98892-172">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="98892-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98892-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98892-173">CommonParameters</span></span>
<span data-ttu-id="98892-174">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98892-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98892-175">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98892-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98892-176">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="98892-176">INPUTS</span></span>

## <span data-ttu-id="98892-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="98892-177">OUTPUTS</span></span>

### <span data-ttu-id="98892-178">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="98892-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="98892-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="98892-179">NOTES</span></span>

## <span data-ttu-id="98892-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="98892-180">RELATED LINKS</span></span>

[<span data-ttu-id="98892-181">Säkerhets kopiering-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="98892-181">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="98892-182">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="98892-182">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="98892-183">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="98892-183">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="98892-184">Återställ-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="98892-184">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


