---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDelegation.md
ms.openlocfilehash: 1daa68e021646d91a2ab1b45382b137771411325
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757568"
---
# <span data-ttu-id="cc68f-101">Remove-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="cc68f-101">Remove-AzureRmDelegation</span></span>

## <span data-ttu-id="cc68f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cc68f-102">SYNOPSIS</span></span>
<span data-ttu-id="cc68f-103">Tar bort en tjänst delegering från det tillhandahållna nätet.</span><span class="sxs-lookup"><span data-stu-id="cc68f-103">Removes a service delegation from the provided subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc68f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cc68f-104">SYNTAX</span></span>

```
Remove-AzureRmDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc68f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cc68f-105">DESCRIPTION</span></span>
<span data-ttu-id="cc68f-106">Cmdleten **Remove-AzureRmDelegation** tar i ett undernät med delegeringar och tar bort den namngivna delegeringen från det under nätet.</span><span class="sxs-lookup"><span data-stu-id="cc68f-106">The **Remove-AzureRmDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="cc68f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cc68f-107">EXAMPLES</span></span>

### <span data-ttu-id="cc68f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cc68f-108">Example 1</span></span>
```powershell
# Add a delegation to an existing subnet
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet

# Remove the delegation
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Remove-AzureRmDelegation -Name "myDelegation" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="cc68f-109">I det här exemplet är den första halvan (finns under _"Lägg till en delegering till ett befintligt undernät"_ ) identiskt med [Add-AzureRmDelegation](./Add-AzureRmDelegation.md).</span><span class="sxs-lookup"><span data-stu-id="cc68f-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_ ) is identical to [Add-AzureRmDelegation](./Add-AzureRmDelegation.md).</span></span> <span data-ttu-id="cc68f-110">I den andra halvan hämtar de två första cmdletarna av intresse, vilket uppdaterar den lokala kopian med vad som finns på servern.</span><span class="sxs-lookup"><span data-stu-id="cc68f-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="cc68f-111">Den tredje cmdleten tar bort den delegering som skapades i första halvan från mina _undernät_ och lagrar det uppdaterade under nätet i _$Subnet_.</span><span class="sxs-lookup"><span data-stu-id="cc68f-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="cc68f-112">Den sista cmdleten uppdaterar servern med den borttagna delegeringen.</span><span class="sxs-lookup"><span data-stu-id="cc68f-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="cc68f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cc68f-113">PARAMETERS</span></span>

### <span data-ttu-id="cc68f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc68f-114">-DefaultProfile</span></span>
<span data-ttu-id="cc68f-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cc68f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc68f-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="cc68f-116">-Name</span></span>
<span data-ttu-id="cc68f-117">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="cc68f-117">The name of the delegation</span></span>

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

### <span data-ttu-id="cc68f-118">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cc68f-118">-ServiceName</span></span>
<span data-ttu-id="cc68f-119">Namnet på tjänsten som under nätet ska delegeras till</span><span class="sxs-lookup"><span data-stu-id="cc68f-119">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="cc68f-120">-Undernät</span><span class="sxs-lookup"><span data-stu-id="cc68f-120">-Subnet</span></span>
<span data-ttu-id="cc68f-121">Det undernät som du vill ta bort delegeringen från</span><span class="sxs-lookup"><span data-stu-id="cc68f-121">The subnet from which to remove the delegation</span></span>

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

### <span data-ttu-id="cc68f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc68f-122">CommonParameters</span></span>
<span data-ttu-id="cc68f-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc68f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc68f-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc68f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc68f-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cc68f-125">INPUTS</span></span>

### <span data-ttu-id="cc68f-126">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="cc68f-126">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>
### <span data-ttu-id="cc68f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="cc68f-127">System.String</span></span>
## <span data-ttu-id="cc68f-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cc68f-128">OUTPUTS</span></span>

### <span data-ttu-id="cc68f-129">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="cc68f-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>
## <span data-ttu-id="cc68f-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cc68f-130">NOTES</span></span>

## <span data-ttu-id="cc68f-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cc68f-131">RELATED LINKS</span></span>

<span data-ttu-id="cc68f-132">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [Get-AzureRmDelegation](./Get-AzureRmDelegation.md) 
 [New-AzureRmDelegation](./New-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="cc68f-132">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
