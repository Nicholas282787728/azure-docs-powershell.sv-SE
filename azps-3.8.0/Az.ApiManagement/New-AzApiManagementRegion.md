---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
ms.openlocfilehash: 2259990c568dbf6fd5b7bc6f8bff34c464a082ec
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089945"
---
# <span data-ttu-id="1c599-101">New-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="1c599-101">New-AzApiManagementRegion</span></span>

## <span data-ttu-id="1c599-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c599-102">SYNOPSIS</span></span>
<span data-ttu-id="1c599-103">Skapar en instans av PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="1c599-103">Creates an instance of PsApiManagementRegion.</span></span>

## <span data-ttu-id="1c599-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c599-104">SYNTAX</span></span>

```
New-AzApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c599-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c599-105">DESCRIPTION</span></span>
<span data-ttu-id="1c599-106">Kommandot hjälp för att skapa en instans av PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="1c599-106">Helper command to create an instance of PsApiManagementRegion.</span></span>
<span data-ttu-id="1c599-107">Kommandot ska användas med kommandot New-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="1c599-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="1c599-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c599-108">EXAMPLES</span></span>

### <span data-ttu-id="1c599-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1c599-109">Example 1</span></span>
```
$apimRegion = New-AzApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### <span data-ttu-id="1c599-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1c599-110">Example 2</span></span>
```
$apimRegionVirtualNetwork = New-AzApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="1c599-111">Skapar en ApiManagement-tjänst för extern VpnType i västra USA-regionen, med ytterligare en region i Central USA.</span><span class="sxs-lookup"><span data-stu-id="1c599-111">Creates an ApiManagement service of External VpnType in West US Region, with an Additional Region in Central US.</span></span>

## <span data-ttu-id="1c599-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c599-112">PARAMETERS</span></span>

### <span data-ttu-id="1c599-113">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="1c599-113">-Capacity</span></span>
<span data-ttu-id="1c599-114">SKU-kapacitet för Azure API Management Service ytterligare region.</span><span class="sxs-lookup"><span data-stu-id="1c599-114">Sku capacity of the Azure API Management service additional region.</span></span>
<span data-ttu-id="1c599-115">Standardvärdet är 1.</span><span class="sxs-lookup"><span data-stu-id="1c599-115">Default value is 1.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c599-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c599-116">-DefaultProfile</span></span>
<span data-ttu-id="1c599-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1c599-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c599-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="1c599-118">-Location</span></span>
<span data-ttu-id="1c599-119">Anger platsen för det nya distributions området bland de regioner som stöds för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1c599-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="1c599-120">För att få giltiga platser, Använd cmdleten Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | där {$ _. ResourceTypes [0]. ResourceTypeName-EQ "tjänst"} | Select-Object platser</span><span class="sxs-lookup"><span data-stu-id="1c599-120">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c599-121">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1c599-121">-VirtualNetwork</span></span>
<span data-ttu-id="1c599-122">Konfigurations region för Azure API Management med virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="1c599-122">Virtual Network Configuration of Azure API Management deployment region.</span></span>
<span data-ttu-id="1c599-123">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="1c599-123">Default value is $null.</span></span>

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

### <span data-ttu-id="1c599-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c599-124">CommonParameters</span></span>
<span data-ttu-id="1c599-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c599-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c599-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c599-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c599-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c599-127">INPUTS</span></span>

### <span data-ttu-id="1c599-128">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1c599-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="1c599-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c599-129">OUTPUTS</span></span>

### <span data-ttu-id="1c599-130">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="1c599-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span></span>

## <span data-ttu-id="1c599-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c599-131">NOTES</span></span>

## <span data-ttu-id="1c599-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c599-132">RELATED LINKS</span></span>