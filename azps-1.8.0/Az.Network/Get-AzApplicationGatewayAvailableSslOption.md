---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: 04a24ee5148782f4a15aa5b93ffb937ad312ccfb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748394"
---
# <span data-ttu-id="292c9-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="292c9-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="292c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="292c9-102">SYNOPSIS</span></span>
<span data-ttu-id="292c9-103">Hämtar alla tillgängliga SSL-alternativ för SSL-princip för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="292c9-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="292c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="292c9-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="292c9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="292c9-105">DESCRIPTION</span></span>
<span data-ttu-id="292c9-106">Cmdleten **Get-AzApplicationGatewayAvailableSslOption** får alla tillgängliga SSL-alternativ för SSL-princip</span><span class="sxs-lookup"><span data-stu-id="292c9-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="292c9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="292c9-107">EXAMPLES</span></span>

### <span data-ttu-id="292c9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="292c9-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="292c9-109">Det här kommandot returnerar alla tillgängliga SSL-alternativ för SSL-principen.</span><span class="sxs-lookup"><span data-stu-id="292c9-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="292c9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="292c9-110">PARAMETERS</span></span>

### <span data-ttu-id="292c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="292c9-111">-DefaultProfile</span></span>
<span data-ttu-id="292c9-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="292c9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="292c9-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="292c9-113">CommonParameters</span></span>
<span data-ttu-id="292c9-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="292c9-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="292c9-115">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="292c9-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="292c9-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="292c9-116">INPUTS</span></span>

### <span data-ttu-id="292c9-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="292c9-117">None</span></span>

## <span data-ttu-id="292c9-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="292c9-118">OUTPUTS</span></span>

### <span data-ttu-id="292c9-119">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="292c9-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="292c9-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="292c9-120">NOTES</span></span>

## <span data-ttu-id="292c9-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="292c9-121">RELATED LINKS</span></span>