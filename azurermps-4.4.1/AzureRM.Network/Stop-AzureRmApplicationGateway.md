---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
ms.openlocfilehash: 6c2de883a797c445105edddfc562bc2d494fd234
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574566"
---
# <span data-ttu-id="f4b4c-101">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4b4c-101">Stop-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="f4b4c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f4b4c-102">SYNOPSIS</span></span>
<span data-ttu-id="f4b4c-103">Stoppa en Programgateway</span><span class="sxs-lookup"><span data-stu-id="f4b4c-103">Stops an application gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4b4c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f4b4c-104">SYNTAX</span></span>

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4b4c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f4b4c-105">DESCRIPTION</span></span>
<span data-ttu-id="f4b4c-106">Cmdleten **Stop-AzureRmApplicationGateway** stoppar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-106">The **Stop-AzureRmApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="f4b4c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f4b4c-107">EXAMPLES</span></span>

### <span data-ttu-id="f4b4c-108">Exempel 1: stoppa en Programgateway</span><span class="sxs-lookup"><span data-stu-id="f4b4c-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="f4b4c-109">Det här kommandot stoppar programgatewayen som lagras i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="f4b4c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f4b4c-110">PARAMETERS</span></span>

### <span data-ttu-id="f4b4c-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4b4c-111">-ApplicationGateway</span></span>
<span data-ttu-id="f4b4c-112">Anger den Programgateway som denna cmdlet slutar.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-112">Specifies the application gateway that this cmdlet stops.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4b4c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4b4c-113">-DefaultProfile</span></span>
<span data-ttu-id="f4b4c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4b4c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4b4c-115">CommonParameters</span></span>
<span data-ttu-id="f4b4c-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4b4c-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4b4c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4b4c-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f4b4c-118">INPUTS</span></span>

### <span data-ttu-id="f4b4c-119">System. String</span><span class="sxs-lookup"><span data-stu-id="f4b4c-119">System.String</span></span>

## <span data-ttu-id="f4b4c-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f4b4c-120">OUTPUTS</span></span>

### <span data-ttu-id="f4b4c-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4b4c-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f4b4c-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f4b4c-122">NOTES</span></span>

## <span data-ttu-id="f4b4c-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f4b4c-123">RELATED LINKS</span></span>

[<span data-ttu-id="f4b4c-124">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4b4c-124">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="f4b4c-125">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4b4c-125">New-AzureRmApplicationGateway</span></span>](./New-AzureRmApplicationGateway.md)

[<span data-ttu-id="f4b4c-126">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4b4c-126">Remove-AzureRmApplicationGateway</span></span>](./Remove-AzureRmApplicationGateway.md)

[<span data-ttu-id="f4b4c-127">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4b4c-127">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)

[<span data-ttu-id="f4b4c-128">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4b4c-128">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


