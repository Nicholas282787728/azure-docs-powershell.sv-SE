---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 03d47278681cbba23895c00b124cc3a2fc2cc6e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758388"
---
# <span data-ttu-id="73048-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="73048-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="73048-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="73048-102">SYNOPSIS</span></span>
<span data-ttu-id="73048-103">Hämtar fördefinierade SSL-principer från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="73048-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73048-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="73048-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73048-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="73048-105">DESCRIPTION</span></span>
<span data-ttu-id="73048-106">Cmdleten **Get-AzureRmApplicationGatewaySslPredefinedPolicy** hämtar fördefinierade SSL-principer från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="73048-106">The **Get-AzureRmApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="73048-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="73048-107">EXAMPLES</span></span>

### <span data-ttu-id="73048-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="73048-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzureRmApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="73048-109">Dessa kommandon returnerar alla fördefinierade SSL-principer.</span><span class="sxs-lookup"><span data-stu-id="73048-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="73048-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="73048-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzureRmApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="73048-111">Det här kommandot returnerar en fördefinierad princip med namnet AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="73048-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="73048-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="73048-112">PARAMETERS</span></span>

### <span data-ttu-id="73048-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="73048-113">-Name</span></span>
<span data-ttu-id="73048-114">Namn på den fördefinierade SSL-principen</span><span class="sxs-lookup"><span data-stu-id="73048-114">Name of the ssl predefined policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73048-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73048-115">-DefaultProfile</span></span>
<span data-ttu-id="73048-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="73048-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73048-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73048-117">CommonParameters</span></span>
<span data-ttu-id="73048-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73048-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73048-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73048-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73048-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="73048-120">INPUTS</span></span>

### <span data-ttu-id="73048-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="73048-121">None</span></span>

## <span data-ttu-id="73048-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="73048-122">OUTPUTS</span></span>

### <span data-ttu-id="73048-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="73048-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>
<span data-ttu-id="73048-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationGatewaySslPredefinedPolicy, Microsoft. Azure. commands. Network, version = 4.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="73048-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="73048-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="73048-125">NOTES</span></span>

## <span data-ttu-id="73048-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="73048-126">RELATED LINKS</span></span>

