---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
ms.openlocfilehash: 3a5cd755718536170c3e6fb1f6dd5410e1acffc7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586327"
---
# <span data-ttu-id="2a15c-101">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2a15c-101">Get-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="2a15c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a15c-102">SYNOPSIS</span></span>
<span data-ttu-id="2a15c-103">Hämtar ett virtuellt nätverk i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="2a15c-103">Gets a virtual network in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a15c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a15c-104">SYNTAX</span></span>

### <span data-ttu-id="2a15c-105">Noexpandering</span><span class="sxs-lookup"><span data-stu-id="2a15c-105">NoExpand</span></span>
```
Get-AzureRmVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a15c-106">Byggnad</span><span class="sxs-lookup"><span data-stu-id="2a15c-106">Expand</span></span>
```
Get-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a15c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a15c-107">DESCRIPTION</span></span>
<span data-ttu-id="2a15c-108">Cmdleten **Get-AzureRmVirtualNetwork** får ett eller flera virtuella nätverk n en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="2a15c-108">The **Get-AzureRmVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="2a15c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a15c-109">EXAMPLES</span></span>

### <span data-ttu-id="2a15c-110">1: Hämta ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="2a15c-110">1: Retrieve a virtual network</span></span>
```
Get-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="2a15c-111">Det här kommandot får det virtuella nätverk som heter MyVirtualNetwork i resurs gruppen TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2a15c-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="2a15c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a15c-112">PARAMETERS</span></span>

### <span data-ttu-id="2a15c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a15c-113">-DefaultProfile</span></span>
<span data-ttu-id="2a15c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2a15c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a15c-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="2a15c-115">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a15c-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="2a15c-116">-Name</span></span>
<span data-ttu-id="2a15c-117">Anger namnet på det virtuella nätverk som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="2a15c-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a15c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a15c-118">-ResourceGroupName</span></span>
<span data-ttu-id="2a15c-119">Anger namnet på den resurs grupp som det virtuella nätverket tillhör.</span><span class="sxs-lookup"><span data-stu-id="2a15c-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a15c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a15c-120">CommonParameters</span></span>
<span data-ttu-id="2a15c-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a15c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a15c-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a15c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a15c-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a15c-123">INPUTS</span></span>

### <span data-ttu-id="2a15c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="2a15c-124">System.String</span></span>

## <span data-ttu-id="2a15c-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a15c-125">OUTPUTS</span></span>

### <span data-ttu-id="2a15c-126">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2a15c-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="2a15c-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a15c-127">NOTES</span></span>

## <span data-ttu-id="2a15c-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a15c-128">RELATED LINKS</span></span>

[<span data-ttu-id="2a15c-129">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2a15c-129">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="2a15c-130">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2a15c-130">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="2a15c-131">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2a15c-131">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


