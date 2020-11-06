---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
ms.openlocfilehash: 1745e3a87d91917e762c9b0e441110b4b6945601
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574907"
---
# <span data-ttu-id="5f7e7-101">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5f7e7-101">Get-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="5f7e7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f7e7-102">SYNOPSIS</span></span>
<span data-ttu-id="5f7e7-103">Hämtar ett virtuellt nätverk i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="5f7e7-103">Gets a virtual network in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f7e7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f7e7-104">SYNTAX</span></span>

### <span data-ttu-id="5f7e7-105">Noexpandering</span><span class="sxs-lookup"><span data-stu-id="5f7e7-105">NoExpand</span></span>
```
Get-AzureRmVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f7e7-106">Byggnad</span><span class="sxs-lookup"><span data-stu-id="5f7e7-106">Expand</span></span>
```
Get-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f7e7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f7e7-107">DESCRIPTION</span></span>
<span data-ttu-id="5f7e7-108">Cmdleten **Get-AzureRmVirtualNetwork** får ett eller flera virtuella nätverk n en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="5f7e7-108">The **Get-AzureRmVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="5f7e7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f7e7-109">EXAMPLES</span></span>

### <span data-ttu-id="5f7e7-110">1: Hämta ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="5f7e7-110">1: Retrieve a virtual network</span></span>
```
Get-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="5f7e7-111">Det här kommandot får det virtuella nätverk som heter MyVirtualNetwork i resurs gruppen TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5f7e7-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="5f7e7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f7e7-112">PARAMETERS</span></span>

### <span data-ttu-id="5f7e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f7e7-113">-DefaultProfile</span></span>
<span data-ttu-id="5f7e7-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5f7e7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f7e7-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="5f7e7-115">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f7e7-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="5f7e7-116">-Name</span></span>
<span data-ttu-id="5f7e7-117">Anger namnet på det virtuella nätverk som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="5f7e7-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f7e7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f7e7-118">-ResourceGroupName</span></span>
<span data-ttu-id="5f7e7-119">Anger namnet på den resurs grupp som det virtuella nätverket tillhör.</span><span class="sxs-lookup"><span data-stu-id="5f7e7-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f7e7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f7e7-120">CommonParameters</span></span>
<span data-ttu-id="5f7e7-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f7e7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f7e7-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f7e7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f7e7-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f7e7-123">INPUTS</span></span>

### <span data-ttu-id="5f7e7-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="5f7e7-124">None</span></span>
<span data-ttu-id="5f7e7-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="5f7e7-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5f7e7-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f7e7-126">OUTPUTS</span></span>

### <span data-ttu-id="5f7e7-127">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5f7e7-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="5f7e7-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f7e7-128">NOTES</span></span>

## <span data-ttu-id="5f7e7-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f7e7-129">RELATED LINKS</span></span>

[<span data-ttu-id="5f7e7-130">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5f7e7-130">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="5f7e7-131">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5f7e7-131">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="5f7e7-132">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5f7e7-132">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


