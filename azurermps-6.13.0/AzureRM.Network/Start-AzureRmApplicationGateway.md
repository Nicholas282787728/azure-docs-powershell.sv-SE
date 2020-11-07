---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
ms.openlocfilehash: 88ca18eca50f1e68eab8599ad79f902ff1fd2551
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756020"
---
# <span data-ttu-id="204a1-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="204a1-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="204a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="204a1-102">SYNOPSIS</span></span>
<span data-ttu-id="204a1-103">Startar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="204a1-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="204a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="204a1-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="204a1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="204a1-105">DESCRIPTION</span></span>
<span data-ttu-id="204a1-106">Cmdleten **Start-AzureRmApplicationGateway** startar en Azure Application Gateway</span><span class="sxs-lookup"><span data-stu-id="204a1-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="204a1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="204a1-107">EXAMPLES</span></span>

### <span data-ttu-id="204a1-108">Example1: starta en Programgateway</span><span class="sxs-lookup"><span data-stu-id="204a1-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="204a1-109">Det här kommandot startar den Programgateway som lagras i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="204a1-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="204a1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="204a1-110">PARAMETERS</span></span>

### <span data-ttu-id="204a1-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="204a1-111">-ApplicationGateway</span></span>
<span data-ttu-id="204a1-112">Anger den Programgateway som den här cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="204a1-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="204a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="204a1-113">-DefaultProfile</span></span>
<span data-ttu-id="204a1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="204a1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="204a1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="204a1-115">CommonParameters</span></span>
<span data-ttu-id="204a1-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="204a1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="204a1-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="204a1-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="204a1-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="204a1-118">INPUTS</span></span>

### <span data-ttu-id="204a1-119">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="204a1-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="204a1-120">Parametrar: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="204a1-120">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="204a1-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="204a1-121">OUTPUTS</span></span>

### <span data-ttu-id="204a1-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="204a1-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="204a1-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="204a1-123">NOTES</span></span>

## <span data-ttu-id="204a1-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="204a1-124">RELATED LINKS</span></span>

[<span data-ttu-id="204a1-125">Stopp-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="204a1-125">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


