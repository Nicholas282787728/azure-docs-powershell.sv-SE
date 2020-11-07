---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
ms.openlocfilehash: 4b6f253da0c2494db49883402be8f39f5ef80ae4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918773"
---
# <span data-ttu-id="15c4a-101">Get-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="15c4a-101">Get-AzDelegation</span></span>

## <span data-ttu-id="15c4a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="15c4a-102">SYNOPSIS</span></span>
<span data-ttu-id="15c4a-103">Få en delegering (eller alla delegeringarna) i ett givet undernät.</span><span class="sxs-lookup"><span data-stu-id="15c4a-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

## <span data-ttu-id="15c4a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="15c4a-104">SYNTAX</span></span>

```
Get-AzDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15c4a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="15c4a-105">DESCRIPTION</span></span>
<span data-ttu-id="15c4a-106">Cmdleten **Get-AzDelegation** hämtar den namngivna delegeringen från ett undernät.</span><span class="sxs-lookup"><span data-stu-id="15c4a-106">The **Get-AzDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="15c4a-107">Om ingen delegation heter returneras alla delegeringarna för det tillhandahållna under nätet.</span><span class="sxs-lookup"><span data-stu-id="15c4a-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="15c4a-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="15c4a-108">EXAMPLES</span></span>

### <span data-ttu-id="15c4a-109">1: Hämta en specifik delegering</span><span class="sxs-lookup"><span data-stu-id="15c4a-109">1: Retrieving a specific delegation</span></span>
```powershell
PS C:\> $subnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> Get-AzDelegation -Name "myDelegation" -Subnet $subnet

ProvisioningState : Succeeded
ServiceName       : Microsoft.Sql/servers
Actions           : {}
Name              : myDelegation
Etag              : "thisisaguid"
Id                : /subscriptions/subId/resourceGroups/rg/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/mySubnet/delegations/myDelegation
```

<span data-ttu-id="15c4a-110">Den första raden hämtar under nätet av intresse.</span><span class="sxs-lookup"><span data-stu-id="15c4a-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="15c4a-111">Den andra raden visar Delegerings information för delegeringen.</span><span class="sxs-lookup"><span data-stu-id="15c4a-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="15c4a-112">2: alla under nätverks delegeringar hämtas</span><span class="sxs-lookup"><span data-stu-id="15c4a-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzDelegation -Subnet $subnet
```

<span data-ttu-id="15c4a-113">Den första raden hämtar under nätet av intresse.</span><span class="sxs-lookup"><span data-stu-id="15c4a-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="15c4a-114">På den andra raden lagras en lista över alla delegeringar i mina _undernät_ i $delegations variabel.</span><span class="sxs-lookup"><span data-stu-id="15c4a-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="15c4a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="15c4a-115">PARAMETERS</span></span>

### <span data-ttu-id="15c4a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15c4a-116">-DefaultProfile</span></span>
<span data-ttu-id="15c4a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="15c4a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15c4a-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="15c4a-118">-Name</span></span>
<span data-ttu-id="15c4a-119">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="15c4a-119">The name of the delegation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15c4a-120">-Undernät</span><span class="sxs-lookup"><span data-stu-id="15c4a-120">-Subnet</span></span>
<span data-ttu-id="15c4a-121">Under nätet</span><span class="sxs-lookup"><span data-stu-id="15c4a-121">The subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15c4a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15c4a-122">CommonParameters</span></span>
<span data-ttu-id="15c4a-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15c4a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15c4a-124">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15c4a-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15c4a-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="15c4a-125">INPUTS</span></span>

### <span data-ttu-id="15c4a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="15c4a-126">System.String</span></span>

### <span data-ttu-id="15c4a-127">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="15c4a-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="15c4a-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="15c4a-128">OUTPUTS</span></span>

### <span data-ttu-id="15c4a-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="15c4a-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="15c4a-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="15c4a-130">NOTES</span></span>

## <span data-ttu-id="15c4a-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="15c4a-131">RELATED LINKS</span></span>

<span data-ttu-id="15c4a-132">[Add-AzDelegation](./Add-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="15c4a-132">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span></span>