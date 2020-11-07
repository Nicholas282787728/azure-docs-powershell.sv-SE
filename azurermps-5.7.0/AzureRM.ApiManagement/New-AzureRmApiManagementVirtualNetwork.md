---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: 30a237f0f87286be8f6cd18e804d80850df7a8be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586440"
---
# <span data-ttu-id="1a009-101">New-AzureRmApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1a009-101">New-AzureRmApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="1a009-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1a009-102">SYNOPSIS</span></span>
<span data-ttu-id="1a009-103">Skapar en instans av PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="1a009-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a009-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1a009-104">SYNTAX</span></span>

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a009-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1a009-105">DESCRIPTION</span></span>
<span data-ttu-id="1a009-106">**New-AzureRmApiManagementVirtualNetwork** cmdlet är ett hjälp kommando för att skapa en instans av **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="1a009-106">The **New-AzureRmApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="1a009-107">Det här kommandot används med **Update-AzureRmApiManagementDeployment** cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a009-107">This command is used with **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="1a009-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1a009-108">EXAMPLES</span></span>

### <span data-ttu-id="1a009-109">Exempel 1: skapa ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="1a009-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$vnetName = "myvnet"
PS C:\>$subnetName = "default"
PS C:\>$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.1.0/24
PS C:\>$vnet = New-AzureRmvirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix 10.0.0.0/16 -Subnet $subnet

# Create a Virtual Network Object
PS C:\>$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location $location -SubnetResourceId $vnet.Subnets[0].Id

# Get the service
PS C:\>$service = Get-AzureRmApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName    
PS C:\>$service.VirtualNetwork = $virtualNetwork
PS C:\>$service.VpnType = "External"

# Update the Deployment with Virtual Network
PS C:\>Update-AzureRmApiManagementDeployment -ApiManagement $service
```

<span data-ttu-id="1a009-110">I det här exemplet skapas ett virtuellt nätverk och sedan anropas cmdleten **Update-AzureRmApiManagementDeployment** .</span><span class="sxs-lookup"><span data-stu-id="1a009-110">This example creates a virtual network and then calls the **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="1a009-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1a009-111">PARAMETERS</span></span>

### <span data-ttu-id="1a009-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a009-112">-DefaultProfile</span></span>
<span data-ttu-id="1a009-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1a009-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="1a009-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="1a009-114">-Location</span></span>
<span data-ttu-id="1a009-115">Anger platsen för den region som stöds för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1a009-115">Specifies the location amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="1a009-116">För att få giltiga platser, Använd cmdleten Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | där {$ _. ResourceTypes [0]. ResourceTypeName-EQ "tjänst"} | Select-Object platser</span><span class="sxs-lookup"><span data-stu-id="1a009-116">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="1a009-117">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="1a009-117">-SubnetResourceId</span></span>
<span data-ttu-id="1a009-118">Anger det virtuella nätverkets ID för under nätet.</span><span class="sxs-lookup"><span data-stu-id="1a009-118">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="1a009-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a009-119">CommonParameters</span></span>
<span data-ttu-id="1a009-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a009-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a009-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a009-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a009-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1a009-122">INPUTS</span></span>

### <span data-ttu-id="1a009-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="1a009-123">None</span></span>
<span data-ttu-id="1a009-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="1a009-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1a009-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1a009-125">OUTPUTS</span></span>

### <span data-ttu-id="1a009-126">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1a009-126">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="1a009-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1a009-127">NOTES</span></span>

## <span data-ttu-id="1a009-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1a009-128">RELATED LINKS</span></span>

[<span data-ttu-id="1a009-129">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="1a009-129">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)
