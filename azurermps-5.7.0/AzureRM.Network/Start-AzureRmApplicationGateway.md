---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
ms.openlocfilehash: 2faa1b245a38a5ef66bb5131f79000218c39d55c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582043"
---
# <span data-ttu-id="e5af5-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5af5-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="e5af5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e5af5-102">SYNOPSIS</span></span>
<span data-ttu-id="e5af5-103">Startar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="e5af5-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5af5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e5af5-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5af5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e5af5-105">DESCRIPTION</span></span>
<span data-ttu-id="e5af5-106">Cmdleten **Start-AzureRmApplicationGateway** startar en Azure Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e5af5-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="e5af5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e5af5-107">EXAMPLES</span></span>

### <span data-ttu-id="e5af5-108">Example1: starta en Programgateway</span><span class="sxs-lookup"><span data-stu-id="e5af5-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="e5af5-109">Det här kommandot startar den Programgateway som lagras i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="e5af5-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="e5af5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e5af5-110">PARAMETERS</span></span>

### <span data-ttu-id="e5af5-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5af5-111">-ApplicationGateway</span></span>
<span data-ttu-id="e5af5-112">Anger den Programgateway som den här cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="e5af5-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="e5af5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5af5-113">-DefaultProfile</span></span>
<span data-ttu-id="e5af5-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e5af5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5af5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5af5-115">CommonParameters</span></span>
<span data-ttu-id="e5af5-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5af5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5af5-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5af5-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5af5-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e5af5-118">INPUTS</span></span>

### <span data-ttu-id="e5af5-119">System. String</span><span class="sxs-lookup"><span data-stu-id="e5af5-119">System.String</span></span>

## <span data-ttu-id="e5af5-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e5af5-120">OUTPUTS</span></span>

### <span data-ttu-id="e5af5-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5af5-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e5af5-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e5af5-122">NOTES</span></span>

## <span data-ttu-id="e5af5-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e5af5-123">RELATED LINKS</span></span>

[<span data-ttu-id="e5af5-124">Stopp-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5af5-124">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


