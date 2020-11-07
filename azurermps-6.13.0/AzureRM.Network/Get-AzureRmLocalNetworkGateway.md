---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 522516df5d4500f55a17e769140149f021501210
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758327"
---
# <span data-ttu-id="47b51-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="47b51-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="47b51-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="47b51-102">SYNOPSIS</span></span>
<span data-ttu-id="47b51-103">Får en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="47b51-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47b51-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="47b51-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47b51-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="47b51-105">DESCRIPTION</span></span>
<span data-ttu-id="47b51-106">Den lokala Nätverksgatewayen är det objekt som representerar din privata VPN-enhet.</span><span class="sxs-lookup"><span data-stu-id="47b51-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="47b51-107">Cmdleten **Get-AzureRmLocalNetworkGateway** returnerar det objekt som representerar din lokala-gateway baserat på namn och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="47b51-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="47b51-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="47b51-108">EXAMPLES</span></span>

### <span data-ttu-id="47b51-109">1: skaffa en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="47b51-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="47b51-110">Returnerar objektet för den lokala Nätverksgatewayen med namnet "myLocalGW" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="47b51-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="47b51-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="47b51-111">PARAMETERS</span></span>

### <span data-ttu-id="47b51-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47b51-112">-DefaultProfile</span></span>
<span data-ttu-id="47b51-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="47b51-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47b51-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="47b51-114">-Name</span></span>
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

### <span data-ttu-id="47b51-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47b51-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="47b51-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b51-116">CommonParameters</span></span>
<span data-ttu-id="47b51-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47b51-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b51-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47b51-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b51-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="47b51-119">INPUTS</span></span>

### <span data-ttu-id="47b51-120">System. String</span><span class="sxs-lookup"><span data-stu-id="47b51-120">System.String</span></span>

## <span data-ttu-id="47b51-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="47b51-121">OUTPUTS</span></span>

### <span data-ttu-id="47b51-122">Microsoft. Azure. commands. Networks. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="47b51-122">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="47b51-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="47b51-123">NOTES</span></span>

## <span data-ttu-id="47b51-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="47b51-124">RELATED LINKS</span></span>
