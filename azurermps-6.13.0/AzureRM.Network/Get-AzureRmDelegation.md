---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDelegation.md
ms.openlocfilehash: f3e8ef97ab618df37ba7d5adae107d65676ed29f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581704"
---
# <span data-ttu-id="af9d2-101">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="af9d2-101">Get-AzureRmDelegation</span></span>

## <span data-ttu-id="af9d2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af9d2-102">SYNOPSIS</span></span>
<span data-ttu-id="af9d2-103">Få en delegering (eller alla delegeringarna) i ett givet undernät.</span><span class="sxs-lookup"><span data-stu-id="af9d2-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af9d2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af9d2-104">SYNTAX</span></span>

```
Get-AzureRmDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af9d2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af9d2-105">DESCRIPTION</span></span>
<span data-ttu-id="af9d2-106">Cmdleten **Get-AzureRmDelegation** hämtar den namngivna delegeringen från ett undernät.</span><span class="sxs-lookup"><span data-stu-id="af9d2-106">The **Get-AzureRmDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="af9d2-107">Om ingen delegation heter returneras alla delegeringarna för det tillhandahållna under nätet.</span><span class="sxs-lookup"><span data-stu-id="af9d2-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="af9d2-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af9d2-108">EXAMPLES</span></span>

### <span data-ttu-id="af9d2-109">1: Hämta en specifik delegering</span><span class="sxs-lookup"><span data-stu-id="af9d2-109">1: Retrieving a specific delegation</span></span>
```powershell
PS C:\> $subnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> Get-AzureRmDelegation -Name "myDelegation" -Subnet $subnet

ProvisioningState : Succeeded
ServiceName       : Microsoft.Sql/servers
Actions           : {}
Name              : myDelegation
Etag              : "thisisaguid"
Id                : /subscriptions/subId/resourceGroups/rg/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/mySubnet/delegations/myDelegation
```

<span data-ttu-id="af9d2-110">Den första raden hämtar under nätet av intresse.</span><span class="sxs-lookup"><span data-stu-id="af9d2-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="af9d2-111">Den andra raden visar Delegerings information för delegeringen.</span><span class="sxs-lookup"><span data-stu-id="af9d2-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="af9d2-112">2: alla under nätverks delegeringar hämtas</span><span class="sxs-lookup"><span data-stu-id="af9d2-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzureRmDelegation -Subnet $subnet
```

<span data-ttu-id="af9d2-113">Den första raden hämtar under nätet av intresse.</span><span class="sxs-lookup"><span data-stu-id="af9d2-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="af9d2-114">På den andra raden lagras en lista över alla delegeringar i mina _undernät_ i $delegations variabel.</span><span class="sxs-lookup"><span data-stu-id="af9d2-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="af9d2-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af9d2-115">PARAMETERS</span></span>

### <span data-ttu-id="af9d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af9d2-116">-DefaultProfile</span></span>
<span data-ttu-id="af9d2-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="af9d2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af9d2-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="af9d2-118">-Name</span></span>
<span data-ttu-id="af9d2-119">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="af9d2-119">The name of the delegation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af9d2-120">-Undernät</span><span class="sxs-lookup"><span data-stu-id="af9d2-120">-Subnet</span></span>
<span data-ttu-id="af9d2-121">Under nätet</span><span class="sxs-lookup"><span data-stu-id="af9d2-121">The subnet</span></span>

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af9d2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af9d2-122">CommonParameters</span></span>
<span data-ttu-id="af9d2-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af9d2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="af9d2-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af9d2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af9d2-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af9d2-125">INPUTS</span></span>

### <span data-ttu-id="af9d2-126">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="af9d2-126">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="af9d2-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af9d2-127">OUTPUTS</span></span>

### <span data-ttu-id="af9d2-128">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="af9d2-128">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="af9d2-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af9d2-129">NOTES</span></span>

## <span data-ttu-id="af9d2-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af9d2-130">RELATED LINKS</span></span>
<span data-ttu-id="af9d2-131">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [New-AzureRmDelegation](./New-AzureRmDelegation.md) 
 [Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="af9d2-131">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)</span></span>
