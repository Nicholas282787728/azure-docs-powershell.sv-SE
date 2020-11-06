---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
ms.openlocfilehash: d955cb51d92d9d0f3c156900d847e903d642e9af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578380"
---
# <span data-ttu-id="38ef0-101">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="38ef0-101">Get-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="38ef0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="38ef0-102">SYNOPSIS</span></span>
<span data-ttu-id="38ef0-103">Hämtar ett virtuellt nätverk i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="38ef0-103">Gets a virtual network in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38ef0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="38ef0-104">SYNTAX</span></span>

### <span data-ttu-id="38ef0-105">Noexpandering</span><span class="sxs-lookup"><span data-stu-id="38ef0-105">NoExpand</span></span>
```
Get-AzureRmVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38ef0-106">Byggnad</span><span class="sxs-lookup"><span data-stu-id="38ef0-106">Expand</span></span>
```
Get-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38ef0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="38ef0-107">DESCRIPTION</span></span>
<span data-ttu-id="38ef0-108">Cmdleten **Get-AzureRmVirtualNetwork** får ett eller flera virtuella nätverk n en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="38ef0-108">The **Get-AzureRmVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="38ef0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="38ef0-109">EXAMPLES</span></span>

### <span data-ttu-id="38ef0-110">1: Hämta ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="38ef0-110">1: Retrieve a virtual network</span></span>
```
Get-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="38ef0-111">Det här kommandot får det virtuella nätverk som heter MyVirtualNetwork i resurs gruppen TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="38ef0-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="38ef0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="38ef0-112">PARAMETERS</span></span>

### <span data-ttu-id="38ef0-113">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="38ef0-113">-ExpandResource</span></span>
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

### <span data-ttu-id="38ef0-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="38ef0-114">-Name</span></span>
<span data-ttu-id="38ef0-115">Anger namnet på det virtuella nätverk som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="38ef0-115">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="38ef0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38ef0-116">-ResourceGroupName</span></span>
<span data-ttu-id="38ef0-117">Anger namnet på den resurs grupp som det virtuella nätverket tillhör.</span><span class="sxs-lookup"><span data-stu-id="38ef0-117">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="38ef0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38ef0-118">-DefaultProfile</span></span>
<span data-ttu-id="38ef0-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="38ef0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38ef0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38ef0-120">CommonParameters</span></span>
<span data-ttu-id="38ef0-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38ef0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38ef0-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38ef0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38ef0-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="38ef0-123">INPUTS</span></span>

## <span data-ttu-id="38ef0-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="38ef0-124">OUTPUTS</span></span>

### <span data-ttu-id="38ef0-125">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="38ef0-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="38ef0-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="38ef0-126">NOTES</span></span>

## <span data-ttu-id="38ef0-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="38ef0-127">RELATED LINKS</span></span>

[<span data-ttu-id="38ef0-128">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="38ef0-128">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="38ef0-129">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="38ef0-129">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="38ef0-130">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="38ef0-130">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


