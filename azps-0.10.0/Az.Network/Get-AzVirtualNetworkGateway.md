---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: 490e61142bdbc0bcdd64f18aeeb2fa527e5180b9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922217"
---
# <span data-ttu-id="c128b-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c128b-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="c128b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c128b-102">SYNOPSIS</span></span>
<span data-ttu-id="c128b-103">Hämtar en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="c128b-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="c128b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c128b-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c128b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c128b-105">DESCRIPTION</span></span>
<span data-ttu-id="c128b-106">Den virtuella Nätverksgatewayen är det objekt som representerar din gateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="c128b-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="c128b-107">Cmdleten **Get-AzVirtualNetworkGateway** returnerar gatewayens objekt i Azure baserat på namn-och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="c128b-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="c128b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c128b-108">EXAMPLES</span></span>

### <span data-ttu-id="c128b-109">1: skaffa en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="c128b-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="c128b-110">Returnerar objektet för den virtuella Nätverksgatewayen med namnet "Gateway" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="c128b-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="c128b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c128b-111">PARAMETERS</span></span>

### <span data-ttu-id="c128b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c128b-112">-DefaultProfile</span></span>
<span data-ttu-id="c128b-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c128b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c128b-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="c128b-114">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c128b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c128b-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="c128b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c128b-116">CommonParameters</span></span>
<span data-ttu-id="c128b-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c128b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c128b-118">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c128b-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c128b-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c128b-119">INPUTS</span></span>

## <span data-ttu-id="c128b-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c128b-120">OUTPUTS</span></span>

### <span data-ttu-id="c128b-121">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c128b-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="c128b-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c128b-122">NOTES</span></span>

## <span data-ttu-id="c128b-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c128b-123">RELATED LINKS</span></span>

