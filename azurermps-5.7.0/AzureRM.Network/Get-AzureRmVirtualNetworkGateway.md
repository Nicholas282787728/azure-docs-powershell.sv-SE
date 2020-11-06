---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 29d5ad86d9df7bddec8be600d8b7c680c7bcd7fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574905"
---
# <span data-ttu-id="fc15a-101">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fc15a-101">Get-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="fc15a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fc15a-102">SYNOPSIS</span></span>
<span data-ttu-id="fc15a-103">Hämtar en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="fc15a-103">Gets a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc15a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fc15a-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc15a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fc15a-105">DESCRIPTION</span></span>
<span data-ttu-id="fc15a-106">Den virtuella Nätverksgatewayen är det objekt som representerar din gateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="fc15a-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="fc15a-107">Cmdleten **Get-AzureRmVirtualNetworkGateway** returnerar gatewayens objekt i Azure baserat på namn-och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="fc15a-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="fc15a-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fc15a-108">EXAMPLES</span></span>

### <span data-ttu-id="fc15a-109">1: skaffa en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="fc15a-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="fc15a-110">Returnerar objektet för den virtuella Nätverksgatewayen med namnet "Gateway" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="fc15a-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="fc15a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fc15a-111">PARAMETERS</span></span>

### <span data-ttu-id="fc15a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc15a-112">-DefaultProfile</span></span>
<span data-ttu-id="fc15a-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fc15a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc15a-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="fc15a-114">-Name</span></span>
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

### <span data-ttu-id="fc15a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc15a-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="fc15a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc15a-116">CommonParameters</span></span>
<span data-ttu-id="fc15a-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc15a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc15a-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc15a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc15a-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fc15a-119">INPUTS</span></span>

### <span data-ttu-id="fc15a-120">Ingen</span><span class="sxs-lookup"><span data-stu-id="fc15a-120">None</span></span>
<span data-ttu-id="fc15a-121">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="fc15a-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fc15a-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fc15a-122">OUTPUTS</span></span>

### <span data-ttu-id="fc15a-123">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fc15a-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="fc15a-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fc15a-124">NOTES</span></span>

## <span data-ttu-id="fc15a-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fc15a-125">RELATED LINKS</span></span>

