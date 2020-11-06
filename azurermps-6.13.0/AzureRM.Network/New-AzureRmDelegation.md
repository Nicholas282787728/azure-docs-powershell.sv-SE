---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDelegation.md
ms.openlocfilehash: 9912d41cd9e2600c55d378fbb88510a0defaaa85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580772"
---
# <span data-ttu-id="66627-101">New-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="66627-101">New-AzureRmDelegation</span></span>

## <span data-ttu-id="66627-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66627-102">SYNOPSIS</span></span>
<span data-ttu-id="66627-103">Skapar en tjänst delegering.</span><span class="sxs-lookup"><span data-stu-id="66627-103">Creates a service delegation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66627-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66627-104">SYNTAX</span></span>

```
New-AzureRmDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="66627-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66627-105">DESCRIPTION</span></span>
<span data-ttu-id="66627-106">Cmdleten **New-AzureRmDelegation** skapar en tjänst delegering som kan läggas till i ett undernät.</span><span class="sxs-lookup"><span data-stu-id="66627-106">The **New-AzureRmDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="66627-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66627-107">EXAMPLES</span></span>

### <span data-ttu-id="66627-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="66627-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="66627-109">Den första cmdleten skapar en delegering som kan läggas till i ett undernät och det lagrar den i $delegation variabeln.</span><span class="sxs-lookup"><span data-stu-id="66627-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="66627-110">Den andra och tredje cmdleten hämtar under nätet som ska delegeras.</span><span class="sxs-lookup"><span data-stu-id="66627-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="66627-111">Den fjärde cmdleten lägger till den skapade delegeringen till under nätet av intresse och den sista cmdleten skickar den uppdaterade konfigurationen till servern.</span><span class="sxs-lookup"><span data-stu-id="66627-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="66627-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66627-112">PARAMETERS</span></span>

### <span data-ttu-id="66627-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66627-113">-DefaultProfile</span></span>
<span data-ttu-id="66627-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="66627-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66627-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="66627-115">-Name</span></span>
<span data-ttu-id="66627-116">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="66627-116">The name of the delegation</span></span>

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

### <span data-ttu-id="66627-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="66627-117">-ServiceName</span></span>
<span data-ttu-id="66627-118">Namnet på tjänsten som under nätet ska delegeras till</span><span class="sxs-lookup"><span data-stu-id="66627-118">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="66627-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66627-119">CommonParameters</span></span>
<span data-ttu-id="66627-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66627-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="66627-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66627-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66627-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66627-122">INPUTS</span></span>

### <span data-ttu-id="66627-123">System. String</span><span class="sxs-lookup"><span data-stu-id="66627-123">System.String</span></span>

## <span data-ttu-id="66627-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66627-124">OUTPUTS</span></span>

### <span data-ttu-id="66627-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="66627-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="66627-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66627-126">NOTES</span></span>

## <span data-ttu-id="66627-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66627-127">RELATED LINKS</span></span>
<span data-ttu-id="66627-128">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [Get-AzureRmDelegation](./Get-AzureRmDelegation.md) 
 [Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="66627-128">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
