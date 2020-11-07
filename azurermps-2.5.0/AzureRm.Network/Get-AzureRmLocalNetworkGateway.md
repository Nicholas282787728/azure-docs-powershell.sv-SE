---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 1a2a8aa8405be5dfc5275a07d253f06f1134e3e7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930193"
---
# <span data-ttu-id="b0f86-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b0f86-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="b0f86-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0f86-102">SYNOPSIS</span></span>
<span data-ttu-id="b0f86-103">Får en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="b0f86-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0f86-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0f86-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0f86-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0f86-105">DESCRIPTION</span></span>
<span data-ttu-id="b0f86-106">Den lokala Nätverksgatewayen är det objekt som representerar din privata VPN-enhet.</span><span class="sxs-lookup"><span data-stu-id="b0f86-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="b0f86-107">Cmdleten **Get-AzureRmLocalNetworkGateway** returnerar det objekt som representerar din lokala-gateway baserat på namn och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="b0f86-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="b0f86-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0f86-108">EXAMPLES</span></span>

### <span data-ttu-id="b0f86-109">1: skaffa en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="b0f86-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="b0f86-110">Returnerar objektet för den lokala Nätverksgatewayen med namnet "myLocalGW" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="b0f86-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="b0f86-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0f86-111">PARAMETERS</span></span>

### <span data-ttu-id="b0f86-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0f86-112">-DefaultProfile</span></span>
<span data-ttu-id="b0f86-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b0f86-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0f86-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="b0f86-114">-Name</span></span>
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

### <span data-ttu-id="b0f86-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0f86-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="b0f86-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0f86-116">CommonParameters</span></span>
<span data-ttu-id="b0f86-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0f86-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0f86-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0f86-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0f86-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0f86-119">INPUTS</span></span>

## <span data-ttu-id="b0f86-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0f86-120">OUTPUTS</span></span>

### <span data-ttu-id="b0f86-121">Microsoft. Azure. commands. Networks. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b0f86-121">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="b0f86-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0f86-122">NOTES</span></span>

## <span data-ttu-id="b0f86-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0f86-123">RELATED LINKS</span></span>

