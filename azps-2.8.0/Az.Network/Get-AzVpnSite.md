---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
ms.openlocfilehash: 0c6ede26826547e525610c76f4a2883f9b738b33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918378"
---
# <span data-ttu-id="fc697-101">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="fc697-101">Get-AzVpnSite</span></span>

## <span data-ttu-id="fc697-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fc697-102">SYNOPSIS</span></span>
<span data-ttu-id="fc697-103">Hämtar en Azure VpnSite-resurs efter namn eller listar alla VpnSites i ett ResourceGroup eller SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="fc697-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="fc697-104">Det här är en RM-representation av kund grenar som laddas upp till Azure för S2S-anslutning med en cortex virtuellt hubb.</span><span class="sxs-lookup"><span data-stu-id="fc697-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="fc697-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fc697-105">SYNTAX</span></span>

### <span data-ttu-id="fc697-106">ListBySubscriptionId (standard)</span><span class="sxs-lookup"><span data-stu-id="fc697-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc697-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc697-107">ListByResourceGroupName</span></span>
```
Get-AzVpnSite [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc697-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fc697-108">DESCRIPTION</span></span>
<span data-ttu-id="fc697-109">Hämtar en Azure VpnSite-resurs efter namn eller listar alla VpnSites i ett ResourceGroup eller SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="fc697-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="fc697-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fc697-110">EXAMPLES</span></span>

### <span data-ttu-id="fc697-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fc697-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"

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

<span data-ttu-id="fc697-112">Ovanstående skapar en resurs grupp, virtuellt WAN i West-resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="fc697-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="fc697-113">Därefter skapas en VpnSite för att representera en kund gren och länkar den till den virtuella WAN-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="fc697-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="fc697-114">När webbplatsen har skapats får den webbplatsen med kommandot Get-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="fc697-114">Once the site is created, it gets the site using the Get-AzVpnSite command.</span></span>

### <span data-ttu-id="fc697-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="fc697-115">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnSite -Name test*

ResourceGroupName : testRG
Name              : testVpnSite1
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite1
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded

ResourceGroupName : testRG
Name              : testVpnSite2
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite2
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="fc697-116">Denna cmdlet får alla webbplatser som börjar med "test".</span><span class="sxs-lookup"><span data-stu-id="fc697-116">This cmdlet gets all Sites that start with "test".</span></span>

## <span data-ttu-id="fc697-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fc697-117">PARAMETERS</span></span>

### <span data-ttu-id="fc697-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc697-118">-DefaultProfile</span></span>
<span data-ttu-id="fc697-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fc697-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc697-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="fc697-120">-Name</span></span>
<span data-ttu-id="fc697-121">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="fc697-121">The resource name.</span></span>

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

### <span data-ttu-id="fc697-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc697-122">-ResourceGroupName</span></span>
<span data-ttu-id="fc697-123">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="fc697-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc697-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc697-124">CommonParameters</span></span>
<span data-ttu-id="fc697-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc697-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc697-126">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc697-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc697-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fc697-127">INPUTS</span></span>

### <span data-ttu-id="fc697-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="fc697-128">None</span></span>

## <span data-ttu-id="fc697-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fc697-129">OUTPUTS</span></span>

### <span data-ttu-id="fc697-130">Microsoft. Azure. commands. Networks. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="fc697-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="fc697-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fc697-131">NOTES</span></span>

## <span data-ttu-id="fc697-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fc697-132">RELATED LINKS</span></span>

[<span data-ttu-id="fc697-133">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="fc697-133">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="fc697-134">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="fc697-134">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="fc697-135">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="fc697-135">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
