---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: ca23e58b173ee67917099f2743dac7dbd3d1bc4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586051"
---
# <span data-ttu-id="29432-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="29432-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="29432-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29432-102">SYNOPSIS</span></span>
<span data-ttu-id="29432-103">Får en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="29432-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29432-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29432-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29432-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29432-105">DESCRIPTION</span></span>
<span data-ttu-id="29432-106">Den lokala Nätverksgatewayen är det objekt som representerar din privata VPN-enhet.</span><span class="sxs-lookup"><span data-stu-id="29432-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="29432-107">Cmdleten **Get-AzureRmLocalNetworkGateway** returnerar det objekt som representerar din lokala-gateway baserat på namn och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="29432-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="29432-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29432-108">EXAMPLES</span></span>

### <span data-ttu-id="29432-109">1: skaffa en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="29432-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="29432-110">Returnerar objektet för den lokala Nätverksgatewayen med namnet "myLocalGW" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="29432-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="29432-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29432-111">PARAMETERS</span></span>

### <span data-ttu-id="29432-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29432-112">-DefaultProfile</span></span>
<span data-ttu-id="29432-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="29432-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29432-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="29432-114">-Name</span></span>
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

### <span data-ttu-id="29432-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29432-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="29432-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29432-116">CommonParameters</span></span>
<span data-ttu-id="29432-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29432-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29432-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29432-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29432-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29432-119">INPUTS</span></span>

### <span data-ttu-id="29432-120">Ingen</span><span class="sxs-lookup"><span data-stu-id="29432-120">None</span></span>
<span data-ttu-id="29432-121">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="29432-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="29432-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29432-122">OUTPUTS</span></span>

### <span data-ttu-id="29432-123">Microsoft. Azure. commands. Networks. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="29432-123">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="29432-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29432-124">NOTES</span></span>

## <span data-ttu-id="29432-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29432-125">RELATED LINKS</span></span>

