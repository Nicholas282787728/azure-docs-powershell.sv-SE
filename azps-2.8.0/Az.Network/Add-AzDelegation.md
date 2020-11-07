---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
ms.openlocfilehash: e7646ff4a52131aaf1468cf32534235f71e7bf7d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918845"
---
# <span data-ttu-id="5009a-101">Add-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="5009a-101">Add-AzDelegation</span></span>

## <span data-ttu-id="5009a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5009a-102">SYNOPSIS</span></span>
<span data-ttu-id="5009a-103">Lägger till en delegering till ett undernät.</span><span class="sxs-lookup"><span data-stu-id="5009a-103">Adds a delegation to a subnet.</span></span>

## <span data-ttu-id="5009a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5009a-104">SYNTAX</span></span>

```
Add-AzDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5009a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5009a-105">DESCRIPTION</span></span>
<span data-ttu-id="5009a-106">Cmdleten **Add-AzDelegation** lägger till en tjänst delegering till ett Azure-undernät.</span><span class="sxs-lookup"><span data-stu-id="5009a-106">The **Add-AzDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="5009a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5009a-107">EXAMPLES</span></span>

### <span data-ttu-id="5009a-108">1: lägga till en delegering</span><span class="sxs-lookup"><span data-stu-id="5009a-108">1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="5009a-109">Det första kommandot hämtar det virtuella nätverk som under nätet.</span><span class="sxs-lookup"><span data-stu-id="5009a-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="5009a-110">Det andra kommandot isolerar det intressanta under nätet-det du vill delegera.</span><span class="sxs-lookup"><span data-stu-id="5009a-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="5009a-111">Det tredje kommandot lägger till en delegering till under nätet.</span><span class="sxs-lookup"><span data-stu-id="5009a-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="5009a-112">Det här exemplet är användbart när du vill aktivera SQL för att skapa gränssnitts slut punkter i det här under nätet.</span><span class="sxs-lookup"><span data-stu-id="5009a-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="5009a-113">Det sista kommandot skickar det uppdaterade under nätet till servern som faktiskt uppdaterar ditt undernät.</span><span class="sxs-lookup"><span data-stu-id="5009a-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="5009a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5009a-114">PARAMETERS</span></span>

### <span data-ttu-id="5009a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5009a-115">-DefaultProfile</span></span>
<span data-ttu-id="5009a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5009a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5009a-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="5009a-117">-Name</span></span>
<span data-ttu-id="5009a-118">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="5009a-118">The name of the delegation</span></span>

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

### <span data-ttu-id="5009a-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5009a-119">-ServiceName</span></span>
<span data-ttu-id="5009a-120">Namnet på tjänsten som under nätet ska delegeras till</span><span class="sxs-lookup"><span data-stu-id="5009a-120">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="5009a-121">-Undernät</span><span class="sxs-lookup"><span data-stu-id="5009a-121">-Subnet</span></span>
<span data-ttu-id="5009a-122">Under nätet</span><span class="sxs-lookup"><span data-stu-id="5009a-122">The subnet</span></span>

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

### <span data-ttu-id="5009a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5009a-123">CommonParameters</span></span>
<span data-ttu-id="5009a-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5009a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5009a-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5009a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5009a-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5009a-126">INPUTS</span></span>

### <span data-ttu-id="5009a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5009a-127">System.String</span></span>

### <span data-ttu-id="5009a-128">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="5009a-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="5009a-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5009a-129">OUTPUTS</span></span>

### <span data-ttu-id="5009a-130">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="5009a-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="5009a-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5009a-131">NOTES</span></span>

## <span data-ttu-id="5009a-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5009a-132">RELATED LINKS</span></span>

<span data-ttu-id="5009a-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="5009a-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>