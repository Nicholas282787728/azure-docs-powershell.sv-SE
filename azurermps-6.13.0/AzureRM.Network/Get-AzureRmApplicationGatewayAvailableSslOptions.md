---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablessloptions
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableSslOptions.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableSslOptions.md
ms.openlocfilehash: 157093dc382b4f56ac7759a9b32b42c8b2488d90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758170"
---
# <span data-ttu-id="a4bf1-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="a4bf1-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="a4bf1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4bf1-102">SYNOPSIS</span></span>
<span data-ttu-id="a4bf1-103">Hämtar alla tillgängliga SSL-alternativ för SSL-princip för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a4bf1-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4bf1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4bf1-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableSslOptions [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4bf1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4bf1-105">DESCRIPTION</span></span>
<span data-ttu-id="a4bf1-106">Cmdleten **Get-AzureRmApplicationGatewayAvailableSslOptions** får alla tillgängliga SSL-alternativ för SSL-princip</span><span class="sxs-lookup"><span data-stu-id="a4bf1-106">The **Get-AzureRmApplicationGatewayAvailableSslOptions** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="a4bf1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4bf1-107">EXAMPLES</span></span>

### <span data-ttu-id="a4bf1-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a4bf1-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzureRmApplicationGatewayAvailableSslOptions
```

<span data-ttu-id="a4bf1-109">Det här kommandot returnerar alla tillgängliga SSL-alternativ för SSL-principen.</span><span class="sxs-lookup"><span data-stu-id="a4bf1-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="a4bf1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4bf1-110">PARAMETERS</span></span>

### <span data-ttu-id="a4bf1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4bf1-111">-DefaultProfile</span></span>
<span data-ttu-id="a4bf1-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a4bf1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4bf1-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4bf1-113">CommonParameters</span></span>
<span data-ttu-id="a4bf1-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4bf1-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4bf1-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4bf1-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4bf1-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4bf1-116">INPUTS</span></span>

### <span data-ttu-id="a4bf1-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="a4bf1-117">None</span></span>

## <span data-ttu-id="a4bf1-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4bf1-118">OUTPUTS</span></span>

### <span data-ttu-id="a4bf1-119">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="a4bf1-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="a4bf1-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4bf1-120">NOTES</span></span>

## <span data-ttu-id="a4bf1-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4bf1-121">RELATED LINKS</span></span>
