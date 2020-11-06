---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: abfcbec55ba3f53986a63a8c0964320c10fc91ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581827"
---
# <span data-ttu-id="fa1c0-101">New-AzureRmApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fa1c0-101">New-AzureRmApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="fa1c0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fa1c0-102">SYNOPSIS</span></span>
<span data-ttu-id="fa1c0-103">Skapar en instans av PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="fa1c0-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa1c0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fa1c0-104">SYNTAX</span></span>

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa1c0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fa1c0-105">DESCRIPTION</span></span>
<span data-ttu-id="fa1c0-106">**New-AzureRmApiManagementVirtualNetwork** cmdlet är ett hjälp kommando för att skapa en instans av **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="fa1c0-106">The **New-AzureRmApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="fa1c0-107">Det här kommandot används med **Update-AzureRmApiManagementDeployment** cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa1c0-107">This command is used with **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="fa1c0-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fa1c0-108">EXAMPLES</span></span>

### <span data-ttu-id="fa1c0-109">Exempel 1: skapa ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="fa1c0-109">Example 1: Create a virtual network</span></span>
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

<span data-ttu-id="fa1c0-110">I det här exemplet skapas ett virtuellt nätverk och sedan anropas cmdleten **Update-AzureRmApiManagementDeployment** .</span><span class="sxs-lookup"><span data-stu-id="fa1c0-110">This example creates a virtual network and then calls the **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="fa1c0-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fa1c0-111">PARAMETERS</span></span>

### <span data-ttu-id="fa1c0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa1c0-112">-DefaultProfile</span></span>
<span data-ttu-id="fa1c0-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fa1c0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa1c0-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="fa1c0-114">-Location</span></span>
<span data-ttu-id="fa1c0-115">Anger platsen för den region som stöds för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="fa1c0-115">Specifies the location amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="fa1c0-116">För att få giltiga platser, Använd cmdleten Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | där {$ _. ResourceTypes [0]. ResourceTypeName-EQ "tjänst"} | Select-Object platser</span><span class="sxs-lookup"><span data-stu-id="fa1c0-116">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="fa1c0-117">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="fa1c0-117">-SubnetResourceId</span></span>
<span data-ttu-id="fa1c0-118">Anger det virtuella nätverkets ID för under nätet.</span><span class="sxs-lookup"><span data-stu-id="fa1c0-118">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="fa1c0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa1c0-119">CommonParameters</span></span>
<span data-ttu-id="fa1c0-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa1c0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa1c0-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa1c0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa1c0-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fa1c0-122">INPUTS</span></span>

### <span data-ttu-id="fa1c0-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="fa1c0-123">None</span></span>

## <span data-ttu-id="fa1c0-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fa1c0-124">OUTPUTS</span></span>

### <span data-ttu-id="fa1c0-125">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fa1c0-125">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="fa1c0-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fa1c0-126">NOTES</span></span>

## <span data-ttu-id="fa1c0-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fa1c0-127">RELATED LINKS</span></span>

[<span data-ttu-id="fa1c0-128">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="fa1c0-128">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)

