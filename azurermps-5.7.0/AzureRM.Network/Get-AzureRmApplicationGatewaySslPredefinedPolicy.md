---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 92c71163b922dacb7920fd842f3d662b18607a70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580364"
---
# <span data-ttu-id="5f624-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="5f624-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="5f624-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f624-102">SYNOPSIS</span></span>
<span data-ttu-id="5f624-103">Hämtar fördefinierade SSL-principer från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="5f624-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f624-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f624-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f624-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f624-105">DESCRIPTION</span></span>
<span data-ttu-id="5f624-106">Cmdleten **Get-AzureRmApplicationGatewaySslPredefinedPolicy** hämtar fördefinierade SSL-principer från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="5f624-106">The **Get-AzureRmApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="5f624-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f624-107">EXAMPLES</span></span>

### <span data-ttu-id="5f624-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5f624-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzureRmApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="5f624-109">Dessa kommandon returnerar alla fördefinierade SSL-principer.</span><span class="sxs-lookup"><span data-stu-id="5f624-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="5f624-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5f624-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzureRmApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="5f624-111">Det här kommandot returnerar en fördefinierad princip med namnet AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="5f624-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="5f624-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f624-112">PARAMETERS</span></span>

### <span data-ttu-id="5f624-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f624-113">-DefaultProfile</span></span>
<span data-ttu-id="5f624-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5f624-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f624-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="5f624-115">-Name</span></span>
<span data-ttu-id="5f624-116">Namn på den fördefinierade SSL-principen</span><span class="sxs-lookup"><span data-stu-id="5f624-116">Name of the ssl predefined policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f624-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f624-117">CommonParameters</span></span>
<span data-ttu-id="5f624-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f624-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f624-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f624-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f624-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f624-120">INPUTS</span></span>

### <span data-ttu-id="5f624-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="5f624-121">None</span></span>

## <span data-ttu-id="5f624-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f624-122">OUTPUTS</span></span>

### <span data-ttu-id="5f624-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="5f624-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>
<span data-ttu-id="5f624-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationGatewaySslPredefinedPolicy, Microsoft. Azure. commands. Network, version = 4.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5f624-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5f624-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f624-125">NOTES</span></span>

## <span data-ttu-id="5f624-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f624-126">RELATED LINKS</span></span>

