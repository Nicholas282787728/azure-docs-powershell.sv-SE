---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmDelegation.md
ms.openlocfilehash: 0306d327bf7e93eedd040979912622b2dcbc09d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582616"
---
# <span data-ttu-id="cc039-101">Add-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="cc039-101">Add-AzureRmDelegation</span></span>

## <span data-ttu-id="cc039-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cc039-102">SYNOPSIS</span></span>
<span data-ttu-id="cc039-103">Lägger till en delegering till ett undernät.</span><span class="sxs-lookup"><span data-stu-id="cc039-103">Adds a delegation to a subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc039-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cc039-104">SYNTAX</span></span>

```
Add-AzureRmDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc039-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cc039-105">DESCRIPTION</span></span>
<span data-ttu-id="cc039-106">Cmdleten **Add-AzureRmDelegation** lägger till en tjänst delegering till ett Azure-undernät.</span><span class="sxs-lookup"><span data-stu-id="cc039-106">The **Add-AzureRmDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="cc039-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cc039-107">EXAMPLES</span></span>

### <span data-ttu-id="cc039-108">1: lägga till en delegering</span><span class="sxs-lookup"><span data-stu-id="cc039-108">1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="cc039-109">Det första kommandot hämtar det virtuella nätverk som under nätet.</span><span class="sxs-lookup"><span data-stu-id="cc039-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="cc039-110">Det andra kommandot isolerar det intressanta under nätet-det du vill delegera.</span><span class="sxs-lookup"><span data-stu-id="cc039-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="cc039-111">Det tredje kommandot lägger till en delegering till under nätet.</span><span class="sxs-lookup"><span data-stu-id="cc039-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="cc039-112">Det här exemplet är användbart när du vill aktivera SQL för att skapa gränssnitts slut punkter i det här under nätet.</span><span class="sxs-lookup"><span data-stu-id="cc039-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="cc039-113">Det sista kommandot skickar det uppdaterade under nätet till servern som faktiskt uppdaterar ditt undernät.</span><span class="sxs-lookup"><span data-stu-id="cc039-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="cc039-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cc039-114">PARAMETERS</span></span>

### <span data-ttu-id="cc039-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc039-115">-DefaultProfile</span></span>
<span data-ttu-id="cc039-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cc039-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc039-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="cc039-117">-Name</span></span>
<span data-ttu-id="cc039-118">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="cc039-118">The name of the delegation</span></span>

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

### <span data-ttu-id="cc039-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cc039-119">-ServiceName</span></span>
<span data-ttu-id="cc039-120">Namnet på tjänsten som under nätet ska delegeras till</span><span class="sxs-lookup"><span data-stu-id="cc039-120">The name of the service to which the subnet should be delegated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc039-121">-Undernät</span><span class="sxs-lookup"><span data-stu-id="cc039-121">-Subnet</span></span>
<span data-ttu-id="cc039-122">Under nätet</span><span class="sxs-lookup"><span data-stu-id="cc039-122">The subnet</span></span>

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

### <span data-ttu-id="cc039-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc039-123">CommonParameters</span></span>
<span data-ttu-id="cc039-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc039-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cc039-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc039-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc039-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cc039-126">INPUTS</span></span>

### <span data-ttu-id="cc039-127">System. String</span><span class="sxs-lookup"><span data-stu-id="cc039-127">System.String</span></span>

### <span data-ttu-id="cc039-128">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="cc039-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="cc039-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cc039-129">OUTPUTS</span></span>

### <span data-ttu-id="cc039-130">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="cc039-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="cc039-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cc039-131">NOTES</span></span>

## <span data-ttu-id="cc039-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cc039-132">RELATED LINKS</span></span>
<span data-ttu-id="cc039-133">[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="cc039-133">[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
