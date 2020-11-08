---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
ms.openlocfilehash: 9d5f7960bb8f47a1f0d617cd4ba43db565ae2c79
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091806"
---
# <span data-ttu-id="afb01-101">Remove-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="afb01-101">Remove-AzDelegation</span></span>

## <span data-ttu-id="afb01-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="afb01-102">SYNOPSIS</span></span>
<span data-ttu-id="afb01-103">Tar bort en tjänst delegering från det tillhandahållna nätet.</span><span class="sxs-lookup"><span data-stu-id="afb01-103">Removes a service delegation from the provided subnet.</span></span>

## <span data-ttu-id="afb01-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="afb01-104">SYNTAX</span></span>

```
Remove-AzDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="afb01-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="afb01-105">DESCRIPTION</span></span>
<span data-ttu-id="afb01-106">Cmdleten **Remove-AzDelegation** tar i ett undernät med delegeringar och tar bort den namngivna delegeringen från det under nätet.</span><span class="sxs-lookup"><span data-stu-id="afb01-106">The **Remove-AzDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="afb01-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="afb01-107">EXAMPLES</span></span>

### <span data-ttu-id="afb01-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="afb01-108">Example 1</span></span>
```powershell
# Add a delegation to an existing subnet
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet

# Remove the delegation
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Remove-AzDelegation -Name "myDelegation" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="afb01-109">I det här exemplet är den första halvan (finns under _"Lägg till en delegering till ett befintligt undernät"_ ) identiskt med [Add-AzDelegation](./Add-AzDelegation.md).</span><span class="sxs-lookup"><span data-stu-id="afb01-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_ ) is identical to [Add-AzDelegation](./Add-AzDelegation.md).</span></span> <span data-ttu-id="afb01-110">I den andra halvan hämtar de två första cmdletarna av intresse, vilket uppdaterar den lokala kopian med vad som finns på servern.</span><span class="sxs-lookup"><span data-stu-id="afb01-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="afb01-111">Den tredje cmdleten tar bort den delegering som skapades i första halvan från mina _undernät_ och lagrar det uppdaterade under nätet i _$Subnet_.</span><span class="sxs-lookup"><span data-stu-id="afb01-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="afb01-112">Den sista cmdleten uppdaterar servern med den borttagna delegeringen.</span><span class="sxs-lookup"><span data-stu-id="afb01-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="afb01-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="afb01-113">PARAMETERS</span></span>

### <span data-ttu-id="afb01-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afb01-114">-DefaultProfile</span></span>
<span data-ttu-id="afb01-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="afb01-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afb01-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="afb01-116">-Name</span></span>
<span data-ttu-id="afb01-117">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="afb01-117">The name of the delegation</span></span>

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

### <span data-ttu-id="afb01-118">-Undernät</span><span class="sxs-lookup"><span data-stu-id="afb01-118">-Subnet</span></span>
<span data-ttu-id="afb01-119">Det undernät som du vill ta bort delegeringen från</span><span class="sxs-lookup"><span data-stu-id="afb01-119">The subnet from which to remove the delegation</span></span>

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

### <span data-ttu-id="afb01-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afb01-120">CommonParameters</span></span>
<span data-ttu-id="afb01-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afb01-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afb01-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afb01-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afb01-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="afb01-123">INPUTS</span></span>

### <span data-ttu-id="afb01-124">System. String</span><span class="sxs-lookup"><span data-stu-id="afb01-124">System.String</span></span>

### <span data-ttu-id="afb01-125">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="afb01-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="afb01-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="afb01-126">OUTPUTS</span></span>

### <span data-ttu-id="afb01-127">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="afb01-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="afb01-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="afb01-128">NOTES</span></span>

## <span data-ttu-id="afb01-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="afb01-129">RELATED LINKS</span></span>

<span data-ttu-id="afb01-130">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="afb01-130">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>