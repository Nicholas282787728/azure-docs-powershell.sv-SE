---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: ed57a1832e3581d4d49b285fa9e61c93b17be02c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578376"
---
# <span data-ttu-id="fe5c2-101">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fe5c2-101">Get-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="fe5c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe5c2-102">SYNOPSIS</span></span>
<span data-ttu-id="fe5c2-103">Hämtar en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="fe5c2-103">Gets a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe5c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe5c2-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe5c2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe5c2-105">DESCRIPTION</span></span>
<span data-ttu-id="fe5c2-106">Den virtuella Nätverksgatewayen är det objekt som representerar din gateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="fe5c2-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="fe5c2-107">Cmdleten **Get-AzureRmVirtualNetworkGateway** returnerar gatewayens objekt i Azure baserat på namn-och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="fe5c2-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="fe5c2-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe5c2-108">EXAMPLES</span></span>

### <span data-ttu-id="fe5c2-109">1: skaffa en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="fe5c2-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="fe5c2-110">Returnerar objektet för den virtuella Nätverksgatewayen med namnet "Gateway" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="fe5c2-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="fe5c2-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe5c2-111">PARAMETERS</span></span>

### <span data-ttu-id="fe5c2-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="fe5c2-112">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe5c2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe5c2-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="fe5c2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe5c2-114">-DefaultProfile</span></span>
<span data-ttu-id="fe5c2-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fe5c2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe5c2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe5c2-116">CommonParameters</span></span>
<span data-ttu-id="fe5c2-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe5c2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe5c2-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe5c2-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe5c2-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe5c2-119">INPUTS</span></span>

## <span data-ttu-id="fe5c2-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe5c2-120">OUTPUTS</span></span>

### <span data-ttu-id="fe5c2-121">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fe5c2-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="fe5c2-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe5c2-122">NOTES</span></span>

## <span data-ttu-id="fe5c2-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe5c2-123">RELATED LINKS</span></span>
