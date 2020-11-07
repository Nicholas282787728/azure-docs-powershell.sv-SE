---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 74b8664a9b57089fd116620779354515ea984c79
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929266"
---
# <span data-ttu-id="6f8b1-101">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f8b1-101">Stop-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="6f8b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f8b1-102">SYNOPSIS</span></span>
<span data-ttu-id="6f8b1-103">Stoppa en Programgateway</span><span class="sxs-lookup"><span data-stu-id="6f8b1-103">Stops an application gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f8b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f8b1-104">SYNTAX</span></span>

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f8b1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f8b1-105">DESCRIPTION</span></span>
<span data-ttu-id="6f8b1-106">Cmdleten **Stop-AzureRmApplicationGateway** stoppar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="6f8b1-106">The **Stop-AzureRmApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="6f8b1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f8b1-107">EXAMPLES</span></span>

### <span data-ttu-id="6f8b1-108">Exempel 1: stoppa en Programgateway</span><span class="sxs-lookup"><span data-stu-id="6f8b1-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="6f8b1-109">Det här kommandot stoppar programgatewayen som lagras i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="6f8b1-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="6f8b1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f8b1-110">PARAMETERS</span></span>

### <span data-ttu-id="6f8b1-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f8b1-111">-ApplicationGateway</span></span>
<span data-ttu-id="6f8b1-112">Anger den Programgateway som denna cmdlet slutar.</span><span class="sxs-lookup"><span data-stu-id="6f8b1-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="6f8b1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f8b1-113">-AsJob</span></span>
<span data-ttu-id="6f8b1-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6f8b1-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8b1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f8b1-115">-DefaultProfile</span></span>
<span data-ttu-id="6f8b1-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6f8b1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f8b1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f8b1-117">CommonParameters</span></span>
<span data-ttu-id="6f8b1-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f8b1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f8b1-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f8b1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f8b1-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f8b1-120">INPUTS</span></span>

### <span data-ttu-id="6f8b1-121">System. String</span><span class="sxs-lookup"><span data-stu-id="6f8b1-121">System.String</span></span>

## <span data-ttu-id="6f8b1-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f8b1-122">OUTPUTS</span></span>

### <span data-ttu-id="6f8b1-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f8b1-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6f8b1-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f8b1-124">NOTES</span></span>

## <span data-ttu-id="6f8b1-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f8b1-125">RELATED LINKS</span></span>

[<span data-ttu-id="6f8b1-126">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f8b1-126">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="6f8b1-127">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f8b1-127">New-AzureRmApplicationGateway</span></span>](./New-AzureRmApplicationGateway.md)

[<span data-ttu-id="6f8b1-128">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f8b1-128">Remove-AzureRmApplicationGateway</span></span>](./Remove-AzureRmApplicationGateway.md)

[<span data-ttu-id="6f8b1-129">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f8b1-129">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)

[<span data-ttu-id="6f8b1-130">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f8b1-130">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


