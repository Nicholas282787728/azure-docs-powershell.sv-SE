---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: c881232c065f8494b962a0e010865cbefe8bc0eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580548"
---
# <span data-ttu-id="cf846-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cf846-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="cf846-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cf846-102">SYNOPSIS</span></span>
<span data-ttu-id="cf846-103">Får en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="cf846-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf846-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cf846-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf846-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cf846-105">DESCRIPTION</span></span>
<span data-ttu-id="cf846-106">Den lokala Nätverksgatewayen är det objekt som representerar din privata VPN-enhet.</span><span class="sxs-lookup"><span data-stu-id="cf846-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="cf846-107">Cmdleten **Get-AzureRmLocalNetworkGateway** returnerar det objekt som representerar din lokala-gateway baserat på namn och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="cf846-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="cf846-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cf846-108">EXAMPLES</span></span>

### <span data-ttu-id="cf846-109">1: skaffa en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="cf846-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="cf846-110">Returnerar objektet för den lokala Nätverksgatewayen med namnet "myLocalGW" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="cf846-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="cf846-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cf846-111">PARAMETERS</span></span>

### <span data-ttu-id="cf846-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="cf846-112">-Name</span></span>
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

### <span data-ttu-id="cf846-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf846-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="cf846-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf846-114">-DefaultProfile</span></span>
<span data-ttu-id="cf846-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cf846-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf846-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf846-116">CommonParameters</span></span>
<span data-ttu-id="cf846-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf846-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf846-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf846-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf846-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cf846-119">INPUTS</span></span>

## <span data-ttu-id="cf846-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cf846-120">OUTPUTS</span></span>

### <span data-ttu-id="cf846-121">Microsoft. Azure. commands. Networks. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cf846-121">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="cf846-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cf846-122">NOTES</span></span>

## <span data-ttu-id="cf846-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cf846-123">RELATED LINKS</span></span>

