---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 88c17626da87608a1086331289cb99f8e7668e5a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922262"
---
# <span data-ttu-id="d6729-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d6729-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="d6729-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6729-102">SYNOPSIS</span></span>
<span data-ttu-id="d6729-103">Får en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="d6729-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="d6729-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6729-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6729-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6729-105">DESCRIPTION</span></span>
<span data-ttu-id="d6729-106">Den lokala Nätverksgatewayen är det objekt som representerar din privata VPN-enhet.</span><span class="sxs-lookup"><span data-stu-id="d6729-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="d6729-107">Cmdleten **Get-AzLocalNetworkGateway** returnerar det objekt som representerar din lokala-gateway baserat på namn och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="d6729-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="d6729-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6729-108">EXAMPLES</span></span>

### <span data-ttu-id="d6729-109">1: skaffa en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="d6729-109">1: Get a Local Network Gateway</span></span>
```
Get-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="d6729-110">Returnerar objektet för den lokala Nätverksgatewayen med namnet "myLocalGW" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="d6729-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="d6729-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6729-111">PARAMETERS</span></span>

### <span data-ttu-id="d6729-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6729-112">-DefaultProfile</span></span>
<span data-ttu-id="d6729-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d6729-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6729-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="d6729-114">-Name</span></span>
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

### <span data-ttu-id="d6729-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6729-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="d6729-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6729-116">CommonParameters</span></span>
<span data-ttu-id="d6729-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6729-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6729-118">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6729-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6729-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6729-119">INPUTS</span></span>

## <span data-ttu-id="d6729-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6729-120">OUTPUTS</span></span>

### <span data-ttu-id="d6729-121">Microsoft. Azure. commands. Networks. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d6729-121">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="d6729-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6729-122">NOTES</span></span>

## <span data-ttu-id="d6729-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6729-123">RELATED LINKS</span></span>

