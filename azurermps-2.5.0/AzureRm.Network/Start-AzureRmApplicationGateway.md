---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 382c4cd1b189e0dc95edd4824dec58a280dbb889
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930498"
---
# <span data-ttu-id="b074f-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b074f-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="b074f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b074f-102">SYNOPSIS</span></span>
<span data-ttu-id="b074f-103">Startar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="b074f-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b074f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b074f-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b074f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b074f-105">DESCRIPTION</span></span>
<span data-ttu-id="b074f-106">Cmdleten **Start-AzureRmApplicationGateway** startar en Azure Application Gateway</span><span class="sxs-lookup"><span data-stu-id="b074f-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="b074f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b074f-107">EXAMPLES</span></span>

### <span data-ttu-id="b074f-108">Example1: starta en Programgateway</span><span class="sxs-lookup"><span data-stu-id="b074f-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="b074f-109">Det här kommandot startar den Programgateway som lagras i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="b074f-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="b074f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b074f-110">PARAMETERS</span></span>

### <span data-ttu-id="b074f-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b074f-111">-ApplicationGateway</span></span>
<span data-ttu-id="b074f-112">Anger den Programgateway som den här cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="b074f-112">Specifies the application gateway that this cmdlet starts.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b074f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b074f-113">-DefaultProfile</span></span>
<span data-ttu-id="b074f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b074f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b074f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b074f-115">CommonParameters</span></span>
<span data-ttu-id="b074f-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b074f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b074f-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b074f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b074f-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b074f-118">INPUTS</span></span>

### <span data-ttu-id="b074f-119">System. String</span><span class="sxs-lookup"><span data-stu-id="b074f-119">System.String</span></span>

## <span data-ttu-id="b074f-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b074f-120">OUTPUTS</span></span>

### <span data-ttu-id="b074f-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b074f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b074f-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b074f-122">NOTES</span></span>

## <span data-ttu-id="b074f-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b074f-123">RELATED LINKS</span></span>

[<span data-ttu-id="b074f-124">Stopp-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b074f-124">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


