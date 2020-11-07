---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablessloptions
schema: 2.0.0
ms.openlocfilehash: 023b2a43114fe47b50956e7f4626a75706e914f5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929833"
---
# <span data-ttu-id="99bd6-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="99bd6-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="99bd6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="99bd6-102">SYNOPSIS</span></span>
<span data-ttu-id="99bd6-103">Hämtar alla tillgängliga SSL-alternativ för SSL-princip för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="99bd6-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99bd6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="99bd6-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableSslOptions [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99bd6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="99bd6-105">DESCRIPTION</span></span>
<span data-ttu-id="99bd6-106">Cmdleten **Get-AzureRmApplicationGatewayAvailableSslOptions** får alla tillgängliga SSL-alternativ för SSL-princip</span><span class="sxs-lookup"><span data-stu-id="99bd6-106">The **Get-AzureRmApplicationGatewayAvailableSslOptions** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="99bd6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="99bd6-107">EXAMPLES</span></span>

### <span data-ttu-id="99bd6-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="99bd6-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzureRmApplicationGatewayAvailableSslOptions
```

<span data-ttu-id="99bd6-109">Det här kommandot returnerar alla tillgängliga SSL-alternativ för SSL-principen.</span><span class="sxs-lookup"><span data-stu-id="99bd6-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="99bd6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="99bd6-110">PARAMETERS</span></span>

### <span data-ttu-id="99bd6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99bd6-111">-DefaultProfile</span></span>
<span data-ttu-id="99bd6-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="99bd6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99bd6-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99bd6-113">CommonParameters</span></span>
<span data-ttu-id="99bd6-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99bd6-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99bd6-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99bd6-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99bd6-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="99bd6-116">INPUTS</span></span>

### <span data-ttu-id="99bd6-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="99bd6-117">None</span></span>

## <span data-ttu-id="99bd6-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="99bd6-118">OUTPUTS</span></span>

### <span data-ttu-id="99bd6-119">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="99bd6-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="99bd6-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="99bd6-120">NOTES</span></span>

## <span data-ttu-id="99bd6-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="99bd6-121">RELATED LINKS</span></span>

