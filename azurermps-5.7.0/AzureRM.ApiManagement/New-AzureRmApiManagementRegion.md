---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
ms.openlocfilehash: dc51caee3a0cb8d5571a5a316c2018c30abbe239
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586444"
---
# <span data-ttu-id="edfcd-101">New-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="edfcd-101">New-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="edfcd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="edfcd-102">SYNOPSIS</span></span>
<span data-ttu-id="edfcd-103">Skapar en instans av PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="edfcd-103">Creates an instance of PsApiManagementRegion.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edfcd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="edfcd-104">SYNTAX</span></span>

```
New-AzureRmApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="edfcd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="edfcd-105">DESCRIPTION</span></span>
<span data-ttu-id="edfcd-106">Kommandot hjälp för att skapa en instans av PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="edfcd-106">Helper command to create an instance of PsApiManagementRegion.</span></span>
<span data-ttu-id="edfcd-107">Kommandot ska användas med kommandot New-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="edfcd-107">This command is to be used with New-AzureRmApiManagement command.</span></span>

## <span data-ttu-id="edfcd-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="edfcd-108">EXAMPLES</span></span>

### <span data-ttu-id="edfcd-109">--------------------------Exempel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="edfcd-109">--------------------------  Example 1  --------------------------</span></span>
```
$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### <span data-ttu-id="edfcd-110">--------------------------Exempel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="edfcd-110">--------------------------  Example 2  --------------------------</span></span>
```
$apimRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="edfcd-111">Skapar en ApiManagement-tjänst för extern VpnType i västra USA-regionen, med ytterligare en region i Central USA.</span><span class="sxs-lookup"><span data-stu-id="edfcd-111">Creates an ApiManagement service of External VpnType in West US Region, with an Additional Region in Central US.</span></span>

## <span data-ttu-id="edfcd-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="edfcd-112">PARAMETERS</span></span>

### <span data-ttu-id="edfcd-113">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="edfcd-113">-Capacity</span></span>
<span data-ttu-id="edfcd-114">SKU-kapacitet för Azure API Management Service ytterligare region.</span><span class="sxs-lookup"><span data-stu-id="edfcd-114">Sku capacity of the Azure API Management service additional region.</span></span>
<span data-ttu-id="edfcd-115">Standardvärdet är 1.</span><span class="sxs-lookup"><span data-stu-id="edfcd-115">Default value is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edfcd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edfcd-116">-DefaultProfile</span></span>
<span data-ttu-id="edfcd-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="edfcd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="edfcd-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="edfcd-118">-Location</span></span>
<span data-ttu-id="edfcd-119">Anger platsen för det nya distributions området bland de regioner som stöds för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="edfcd-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="edfcd-120">För att få giltiga platser, Använd cmdleten Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | där {$ _. ResourceTypes [0]. ResourceTypeName-EQ "tjänst"} | Select-Object platser</span><span class="sxs-lookup"><span data-stu-id="edfcd-120">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edfcd-121">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="edfcd-121">-VirtualNetwork</span></span>
<span data-ttu-id="edfcd-122">Konfigurations region för Azure API Management med virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="edfcd-122">Virtual Network Configuration of Azure API Management deployment region.</span></span>
<span data-ttu-id="edfcd-123">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="edfcd-123">Default value is $null.</span></span>

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

### <span data-ttu-id="edfcd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edfcd-124">CommonParameters</span></span>
<span data-ttu-id="edfcd-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edfcd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edfcd-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edfcd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edfcd-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="edfcd-127">INPUTS</span></span>

### <span data-ttu-id="edfcd-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="edfcd-128">None</span></span>
<span data-ttu-id="edfcd-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="edfcd-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="edfcd-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="edfcd-130">OUTPUTS</span></span>

### <span data-ttu-id="edfcd-131">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="edfcd-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span></span>

## <span data-ttu-id="edfcd-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="edfcd-132">NOTES</span></span>

## <span data-ttu-id="edfcd-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="edfcd-133">RELATED LINKS</span></span>

