---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: ebf95d8e809731bdca2f288bc09054fd14353686
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584488"
---
# <span data-ttu-id="9708f-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="9708f-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="9708f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9708f-102">SYNOPSIS</span></span>
<span data-ttu-id="9708f-103">Skapar en distribution av API-hantering.</span><span class="sxs-lookup"><span data-stu-id="9708f-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9708f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9708f-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9708f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9708f-105">DESCRIPTION</span></span>
<span data-ttu-id="9708f-106">Cmdleten **New-AzureRmApiManagement** skapar en distribution av API-hantering i Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="9708f-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="9708f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9708f-107">EXAMPLES</span></span>

### <span data-ttu-id="9708f-108">Exempel 1: skapa en API-hanterings tjänst för en utvecklings nivå</span><span class="sxs-lookup"><span data-stu-id="9708f-108">Example 1: Create a Developer tier API Management service</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="9708f-109">Det här kommandot skapar en API-hanterings tjänst för utvecklings nivå.</span><span class="sxs-lookup"><span data-stu-id="9708f-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="9708f-110">Kommandot anger organisation och administratörs adress.</span><span class="sxs-lookup"><span data-stu-id="9708f-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="9708f-111">Kommandot anger inte parametern *SKU* .</span><span class="sxs-lookup"><span data-stu-id="9708f-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="9708f-112">Därför använder cmdleten standardvärdet för utvecklare.</span><span class="sxs-lookup"><span data-stu-id="9708f-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="9708f-113">Exempel 2: skapa en standard nivå tjänst med tre enheter</span><span class="sxs-lookup"><span data-stu-id="9708f-113">Example 2: Create a Standard tier service that has three units</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="9708f-114">Det här kommandot skapar en API-tjänst för standard nivå med tre enheter.</span><span class="sxs-lookup"><span data-stu-id="9708f-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="9708f-115">Exempel 3: skapa en API-hanterings tjänst för ett externt virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="9708f-115">Example 3: Create an API Management service for an external virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="9708f-116">Det här kommandot skapar en API-tjänst för Premium-nivå i ett Azure Virtual Network-undernät som har en extern Gateway slut punkt med ett huvud område i USA.</span><span class="sxs-lookup"><span data-stu-id="9708f-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="9708f-117">Exempel 4: skapa en API-hanterings tjänst för ett internt virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="9708f-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="9708f-118">Det här kommandot skapar en API-tjänst för Premium-nivå i ett Azure Virtual Network-undernät som har en intern Gateway slut punkt med ett huvud område i USA.</span><span class="sxs-lookup"><span data-stu-id="9708f-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="9708f-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9708f-119">PARAMETERS</span></span>

### <span data-ttu-id="9708f-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="9708f-120">-AdditionalRegions</span></span>
<span data-ttu-id="9708f-121">Ytterligare distributions områden i Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="9708f-121">Additional deployment regions of Azure API Management.</span></span>

```yaml
Type: PsApiManagementRegion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9708f-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="9708f-122">-AdminEmail</span></span>
<span data-ttu-id="9708f-123">Anger den ursprungliga e-postadressen för alla meddelanden som skickas av API-hanterings systemet.</span><span class="sxs-lookup"><span data-stu-id="9708f-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9708f-124">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="9708f-124">-Capacity</span></span>
<span data-ttu-id="9708f-125">Anger SKU-kapaciteten för Azure API Management Service.</span><span class="sxs-lookup"><span data-stu-id="9708f-125">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="9708f-126">Standardvärdet är ett (1).</span><span class="sxs-lookup"><span data-stu-id="9708f-126">The default is one (1).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9708f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9708f-127">-DefaultProfile</span></span>
<span data-ttu-id="9708f-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9708f-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9708f-129">-Plats</span><span class="sxs-lookup"><span data-stu-id="9708f-129">-Location</span></span>
<span data-ttu-id="9708f-130">Anger platsen där API-hanteringskonsolen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="9708f-130">Specifies the location to create the Api Management service.</span></span>

<span data-ttu-id="9708f-131">För att få giltiga platser, Använd cmdleten Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | där {$ _. ResourceTypes [0]. ResourceTypeName-EQ "tjänst"} | Select-Object platser</span><span class="sxs-lookup"><span data-stu-id="9708f-131">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9708f-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="9708f-132">-Name</span></span>
<span data-ttu-id="9708f-133">Anger ett namn på distributionen av API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="9708f-133">Specifies a name for the API Management deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9708f-134">-Organisation</span><span class="sxs-lookup"><span data-stu-id="9708f-134">-Organization</span></span>
<span data-ttu-id="9708f-135">Anger namnet på en organisation.</span><span class="sxs-lookup"><span data-stu-id="9708f-135">Specifies the name of an organization.</span></span>
<span data-ttu-id="9708f-136">Med API-hantering används den här adressen i utvecklings portalen i e-postaviseringar.</span><span class="sxs-lookup"><span data-stu-id="9708f-136">API Management uses this address in the developer portal in email notifications.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9708f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9708f-137">-ResourceGroupName</span></span>
<span data-ttu-id="9708f-138">Anger namnet på den resurs grupp under vilken denna cmdlet skapar en distribution av API-hantering.</span><span class="sxs-lookup"><span data-stu-id="9708f-138">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9708f-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="9708f-139">-Sku</span></span>
<span data-ttu-id="9708f-140">Anger nivån för API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="9708f-140">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="9708f-141">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="9708f-141">Valid values are:</span></span> 

- <span data-ttu-id="9708f-142">Utvecklar</span><span class="sxs-lookup"><span data-stu-id="9708f-142">Developer</span></span> 
- <span data-ttu-id="9708f-143">Standar</span><span class="sxs-lookup"><span data-stu-id="9708f-143">Standard</span></span> 
- <span data-ttu-id="9708f-144">Beta</span><span class="sxs-lookup"><span data-stu-id="9708f-144">Premium</span></span> 

<span data-ttu-id="9708f-145">Standardvärdet är utvecklare.</span><span class="sxs-lookup"><span data-stu-id="9708f-145">The default is Developer.</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9708f-146">-Tagg</span><span class="sxs-lookup"><span data-stu-id="9708f-146">-Tag</span></span>
<span data-ttu-id="9708f-147">Ord lista med märkord.</span><span class="sxs-lookup"><span data-stu-id="9708f-147">Tags dictionary.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9708f-148">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9708f-148">-VirtualNetwork</span></span>
<span data-ttu-id="9708f-149">Konfigurations region för huvud nätverk för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="9708f-149">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9708f-150">-VpnType</span><span class="sxs-lookup"><span data-stu-id="9708f-150">-VpnType</span></span>
<span data-ttu-id="9708f-151">Virtuell nätverks typ för distributionen av ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="9708f-151">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="9708f-152">Giltiga värden är</span><span class="sxs-lookup"><span data-stu-id="9708f-152">Valid Values are</span></span> 
- <span data-ttu-id="9708f-153">"Inget" (standardvärde.</span><span class="sxs-lookup"><span data-stu-id="9708f-153">"None" (Default Value.</span></span> <span data-ttu-id="9708f-154">ApiManagement ingår inte i något virtuellt nätverk ")</span><span class="sxs-lookup"><span data-stu-id="9708f-154">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="9708f-155">"Extern" (ApiManagement Deployment är konfigurerat i ett virtuellt nätverk med en slut punkt på Internet)</span><span class="sxs-lookup"><span data-stu-id="9708f-155">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="9708f-156">"Intern" (ApiManagement distributionen är konfigurerat i ett virtuellt nätverk som har en slut punkt för intranätet)</span><span class="sxs-lookup"><span data-stu-id="9708f-156">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

```yaml
Type: PsApiManagementVpnType
Parameter Sets: (All)
Aliases:
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9708f-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9708f-157">CommonParameters</span></span>
<span data-ttu-id="9708f-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9708f-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9708f-159">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9708f-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9708f-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9708f-160">INPUTS</span></span>

### <span data-ttu-id="9708f-161">Ingen</span><span class="sxs-lookup"><span data-stu-id="9708f-161">None</span></span>
<span data-ttu-id="9708f-162">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="9708f-162">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9708f-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9708f-163">OUTPUTS</span></span>

### <span data-ttu-id="9708f-164">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9708f-164">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="9708f-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9708f-165">NOTES</span></span>

## <span data-ttu-id="9708f-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9708f-166">RELATED LINKS</span></span>

[<span data-ttu-id="9708f-167">Säkerhets kopiering-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="9708f-167">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="9708f-168">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="9708f-168">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="9708f-169">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="9708f-169">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="9708f-170">Återställ-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="9708f-170">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


