---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: 97ae2607484828350be67cff9c9311fc73f19b6f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922219"
---
# <span data-ttu-id="78842-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="78842-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="78842-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="78842-102">SYNOPSIS</span></span>
<span data-ttu-id="78842-103">Hämtar ett virtuellt nätverk i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="78842-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="78842-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="78842-104">SYNTAX</span></span>

### <span data-ttu-id="78842-105">Noexpandering</span><span class="sxs-lookup"><span data-stu-id="78842-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78842-106">Byggnad</span><span class="sxs-lookup"><span data-stu-id="78842-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78842-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="78842-107">DESCRIPTION</span></span>
<span data-ttu-id="78842-108">Cmdleten **Get-AzVirtualNetwork** får ett eller flera virtuella nätverk n en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="78842-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="78842-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="78842-109">EXAMPLES</span></span>

### <span data-ttu-id="78842-110">1: Hämta ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="78842-110">1: Retrieve a virtual network</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="78842-111">Det här kommandot får det virtuella nätverk som heter MyVirtualNetwork i resurs gruppen TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="78842-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="78842-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="78842-112">PARAMETERS</span></span>

### <span data-ttu-id="78842-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78842-113">-DefaultProfile</span></span>
<span data-ttu-id="78842-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="78842-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78842-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="78842-115">-ExpandResource</span></span>
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

### <span data-ttu-id="78842-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="78842-116">-Name</span></span>
<span data-ttu-id="78842-117">Anger namnet på det virtuella nätverk som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="78842-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="78842-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78842-118">-ResourceGroupName</span></span>
<span data-ttu-id="78842-119">Anger namnet på den resurs grupp som det virtuella nätverket tillhör.</span><span class="sxs-lookup"><span data-stu-id="78842-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="78842-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78842-120">CommonParameters</span></span>
<span data-ttu-id="78842-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78842-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78842-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78842-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78842-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="78842-123">INPUTS</span></span>

## <span data-ttu-id="78842-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="78842-124">OUTPUTS</span></span>

### <span data-ttu-id="78842-125">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="78842-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="78842-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="78842-126">NOTES</span></span>

## <span data-ttu-id="78842-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="78842-127">RELATED LINKS</span></span>

[<span data-ttu-id="78842-128">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="78842-128">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="78842-129">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="78842-129">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="78842-130">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="78842-130">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


