---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnSite.md
ms.openlocfilehash: 0277e61a6b1b180691908b2e86c0050eb8d62b1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576213"
---
# <span data-ttu-id="82a95-101">Get-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="82a95-101">Get-AzureRmVpnSite</span></span>

## <span data-ttu-id="82a95-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82a95-102">SYNOPSIS</span></span>
<span data-ttu-id="82a95-103">Hämtar en Azure VpnSite-resurs efter namn eller listar alla VpnSites i ett ResourceGroup eller SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="82a95-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="82a95-104">Det här är en RM-representation av kund grenar som laddas upp till Azure för S2S-anslutning med en cortex virtuellt hubb.</span><span class="sxs-lookup"><span data-stu-id="82a95-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82a95-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82a95-105">SYNTAX</span></span>

### <span data-ttu-id="82a95-106">ListBySubscriptionId (standard)</span><span class="sxs-lookup"><span data-stu-id="82a95-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82a95-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82a95-107">ListByResourceGroupName</span></span>
```
Get-AzureRmVpnSite -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="82a95-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82a95-108">DESCRIPTION</span></span>
<span data-ttu-id="82a95-109">Hämtar en Azure VpnSite-resurs efter namn eller listar alla VpnSites i ett ResourceGroup eller SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="82a95-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="82a95-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82a95-110">EXAMPLES</span></span>

### <span data-ttu-id="82a95-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="82a95-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="82a95-112">Ovanstående skapar en resurs grupp, virtuellt WAN i West-resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="82a95-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="82a95-113">Därefter skapas en VpnSite för att representera en kund gren och länkar den till den virtuella WAN-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="82a95-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="82a95-114">När webbplatsen har skapats får den webbplatsen med kommandot Get-AzureRmVpnSite.</span><span class="sxs-lookup"><span data-stu-id="82a95-114">Once the site is created, it gets the site using the Get-AzureRmVpnSite command.</span></span>

## <span data-ttu-id="82a95-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82a95-115">PARAMETERS</span></span>

### <span data-ttu-id="82a95-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82a95-116">-DefaultProfile</span></span>
<span data-ttu-id="82a95-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="82a95-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82a95-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="82a95-118">-Name</span></span>
<span data-ttu-id="82a95-119">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="82a95-119">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnSiteName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82a95-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82a95-120">-ResourceGroupName</span></span>
<span data-ttu-id="82a95-121">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="82a95-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82a95-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82a95-122">CommonParameters</span></span>
<span data-ttu-id="82a95-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82a95-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82a95-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82a95-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82a95-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82a95-125">INPUTS</span></span>

### <span data-ttu-id="82a95-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="82a95-126">None</span></span>

## <span data-ttu-id="82a95-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82a95-127">OUTPUTS</span></span>

### <span data-ttu-id="82a95-128">Microsoft. Azure. commands. Networks. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="82a95-128">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="82a95-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82a95-129">NOTES</span></span>

## <span data-ttu-id="82a95-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82a95-130">RELATED LINKS</span></span>
