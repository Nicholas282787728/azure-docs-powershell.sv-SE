---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: f2175583aaaf3af04120e22e32db79d7b20f1e30
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091309"
---
# <span data-ttu-id="a618c-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="a618c-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="a618c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a618c-102">SYNOPSIS</span></span>
<span data-ttu-id="a618c-103">Hämtar alla tillgängliga SSL-alternativ för SSL-princip för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a618c-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="a618c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a618c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a618c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a618c-105">DESCRIPTION</span></span>
<span data-ttu-id="a618c-106">Cmdleten **Get-AzApplicationGatewayAvailableSslOption** får alla tillgängliga SSL-alternativ för SSL-princip</span><span class="sxs-lookup"><span data-stu-id="a618c-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="a618c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a618c-107">EXAMPLES</span></span>

### <span data-ttu-id="a618c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a618c-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="a618c-109">Det här kommandot returnerar alla tillgängliga SSL-alternativ för SSL-principen.</span><span class="sxs-lookup"><span data-stu-id="a618c-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="a618c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a618c-110">PARAMETERS</span></span>

### <span data-ttu-id="a618c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a618c-111">-DefaultProfile</span></span>
<span data-ttu-id="a618c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a618c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a618c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a618c-113">CommonParameters</span></span>
<span data-ttu-id="a618c-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a618c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a618c-115">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a618c-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a618c-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a618c-116">INPUTS</span></span>

### <span data-ttu-id="a618c-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="a618c-117">None</span></span>

## <span data-ttu-id="a618c-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a618c-118">OUTPUTS</span></span>

### <span data-ttu-id="a618c-119">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="a618c-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="a618c-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a618c-120">NOTES</span></span>

## <span data-ttu-id="a618c-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a618c-121">RELATED LINKS</span></span>