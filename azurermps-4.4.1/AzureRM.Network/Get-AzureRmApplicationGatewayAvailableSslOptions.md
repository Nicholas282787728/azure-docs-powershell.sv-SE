---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableSslOptions.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableSslOptions.md
ms.openlocfilehash: 60e380ffd046c61abb218395a838c6e0d5d785f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574614"
---
# <span data-ttu-id="4253a-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="4253a-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="4253a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4253a-102">SYNOPSIS</span></span>
<span data-ttu-id="4253a-103">Hämtar alla tillgängliga SSL-alternativ för SSL-princip för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4253a-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4253a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4253a-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableSslOptions [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4253a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4253a-105">DESCRIPTION</span></span>
<span data-ttu-id="4253a-106">Cmdleten **Get-AzureRmApplicationGatewayAvailableSslOptions** får alla tillgängliga SSL-alternativ för SSL-princip</span><span class="sxs-lookup"><span data-stu-id="4253a-106">The **Get-AzureRmApplicationGatewayAvailableSslOptions** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="4253a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4253a-107">EXAMPLES</span></span>

### <span data-ttu-id="4253a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4253a-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzureRmApplicationGatewayAvailableSslOptions
```

<span data-ttu-id="4253a-109">Det här kommandot returnerar alla tillgängliga SSL-alternativ för SSL-principen.</span><span class="sxs-lookup"><span data-stu-id="4253a-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="4253a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4253a-110">PARAMETERS</span></span>

### <span data-ttu-id="4253a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4253a-111">-DefaultProfile</span></span>
<span data-ttu-id="4253a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4253a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4253a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4253a-113">CommonParameters</span></span>
<span data-ttu-id="4253a-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4253a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4253a-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4253a-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4253a-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4253a-116">INPUTS</span></span>

### <span data-ttu-id="4253a-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="4253a-117">None</span></span>

## <span data-ttu-id="4253a-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4253a-118">OUTPUTS</span></span>

### <span data-ttu-id="4253a-119">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="4253a-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="4253a-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4253a-120">NOTES</span></span>

## <span data-ttu-id="4253a-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4253a-121">RELATED LINKS</span></span>

