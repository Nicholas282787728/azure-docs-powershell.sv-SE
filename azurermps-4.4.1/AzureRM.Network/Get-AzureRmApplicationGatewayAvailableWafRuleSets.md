---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
ms.openlocfilehash: 27e5715f32b631fff3f185f0925d0b2a85967ac5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574612"
---
# <span data-ttu-id="19b5a-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span><span class="sxs-lookup"><span data-stu-id="19b5a-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span></span>

## <span data-ttu-id="19b5a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="19b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="19b5a-103">Hämtar alla tillgängliga regel uppsättningar för webb programs brand väggar.</span><span class="sxs-lookup"><span data-stu-id="19b5a-103">Gets all available web application firewall rule sets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19b5a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="19b5a-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableWafRuleSets [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="19b5a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="19b5a-105">DESCRIPTION</span></span>
<span data-ttu-id="19b5a-106">Cmdleten **Get-AzureRmApplicationGatewayAvailableWafRuleSets** hämtar alla tillgängliga regel uppsättningar för webb program brand väggar.</span><span class="sxs-lookup"><span data-stu-id="19b5a-106">The **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="19b5a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="19b5a-107">EXAMPLES</span></span>

### <span data-ttu-id="19b5a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="19b5a-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzureRmApplicationGatewayAvailableWafRuleSets
```

<span data-ttu-id="19b5a-109">Det här kommandot returnerar alla tillgängliga regel uppsättningar för webb program brand väggar.</span><span class="sxs-lookup"><span data-stu-id="19b5a-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="19b5a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="19b5a-110">PARAMETERS</span></span>

### <span data-ttu-id="19b5a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19b5a-111">-DefaultProfile</span></span>
<span data-ttu-id="19b5a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="19b5a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19b5a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19b5a-113">CommonParameters</span></span>
<span data-ttu-id="19b5a-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19b5a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19b5a-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19b5a-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19b5a-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="19b5a-116">INPUTS</span></span>

### <span data-ttu-id="19b5a-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="19b5a-117">None</span></span>

## <span data-ttu-id="19b5a-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="19b5a-118">OUTPUTS</span></span>

### <span data-ttu-id="19b5a-119">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="19b5a-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="19b5a-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="19b5a-120">NOTES</span></span>
<span data-ttu-id="19b5a-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** är ett alias för cmdleten **Get-AzureRmApplicationGatewayAvailableWafRuleSets** .</span><span class="sxs-lookup"><span data-stu-id="19b5a-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet.</span></span>

## <span data-ttu-id="19b5a-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="19b5a-122">RELATED LINKS</span></span>

