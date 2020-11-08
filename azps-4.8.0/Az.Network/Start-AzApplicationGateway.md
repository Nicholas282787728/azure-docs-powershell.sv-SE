---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: 974e30d9a287d18293515c019b0032bf36f15b51
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258143"
---
# <span data-ttu-id="9ecf3-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ecf3-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="9ecf3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9ecf3-102">SYNOPSIS</span></span>
<span data-ttu-id="9ecf3-103">Startar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="9ecf3-103">Starts an application gateway.</span></span>

## <span data-ttu-id="9ecf3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9ecf3-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ecf3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9ecf3-105">DESCRIPTION</span></span>
<span data-ttu-id="9ecf3-106">Cmdleten **Start-AzApplicationGateway** startar en Azure Application Gateway</span><span class="sxs-lookup"><span data-stu-id="9ecf3-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="9ecf3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9ecf3-107">EXAMPLES</span></span>

### <span data-ttu-id="9ecf3-108">Example1: starta en Programgateway</span><span class="sxs-lookup"><span data-stu-id="9ecf3-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="9ecf3-109">Det här kommandot startar den Programgateway som lagras i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="9ecf3-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="9ecf3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9ecf3-110">PARAMETERS</span></span>

### <span data-ttu-id="9ecf3-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ecf3-111">-ApplicationGateway</span></span>
<span data-ttu-id="9ecf3-112">Anger den Programgateway som den här cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="9ecf3-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="9ecf3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ecf3-113">-DefaultProfile</span></span>
<span data-ttu-id="9ecf3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9ecf3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ecf3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ecf3-115">CommonParameters</span></span>
<span data-ttu-id="9ecf3-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ecf3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ecf3-117">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ecf3-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ecf3-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9ecf3-118">INPUTS</span></span>

### <span data-ttu-id="9ecf3-119">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ecf3-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9ecf3-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9ecf3-120">OUTPUTS</span></span>

### <span data-ttu-id="9ecf3-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ecf3-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9ecf3-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9ecf3-122">NOTES</span></span>

## <span data-ttu-id="9ecf3-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9ecf3-123">RELATED LINKS</span></span>

[<span data-ttu-id="9ecf3-124">Stopp-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ecf3-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


