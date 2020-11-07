---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 2c55da6b7193d02de51e273df4626152d6d088fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922303"
---
# <span data-ttu-id="7126a-101">Get-AzApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="7126a-101">Get-AzApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="7126a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7126a-102">SYNOPSIS</span></span>
<span data-ttu-id="7126a-103">Hämtar fördefinierade SSL-principer från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7126a-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="7126a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7126a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7126a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7126a-105">DESCRIPTION</span></span>
<span data-ttu-id="7126a-106">Cmdleten **Get-AzApplicationGatewaySslPredefinedPolicy** hämtar fördefinierade SSL-principer från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7126a-106">The **Get-AzApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="7126a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7126a-107">EXAMPLES</span></span>

### <span data-ttu-id="7126a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7126a-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="7126a-109">Dessa kommandon returnerar alla fördefinierade SSL-principer.</span><span class="sxs-lookup"><span data-stu-id="7126a-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="7126a-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7126a-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="7126a-111">Det här kommandot returnerar en fördefinierad princip med namnet AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="7126a-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="7126a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7126a-112">PARAMETERS</span></span>

### <span data-ttu-id="7126a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7126a-113">-DefaultProfile</span></span>
<span data-ttu-id="7126a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7126a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7126a-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="7126a-115">-Name</span></span>
<span data-ttu-id="7126a-116">Namn på den fördefinierade SSL-principen</span><span class="sxs-lookup"><span data-stu-id="7126a-116">Name of the ssl predefined policy</span></span>

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

### <span data-ttu-id="7126a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7126a-117">CommonParameters</span></span>
<span data-ttu-id="7126a-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7126a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7126a-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7126a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7126a-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7126a-120">INPUTS</span></span>

### <span data-ttu-id="7126a-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="7126a-121">None</span></span>

## <span data-ttu-id="7126a-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7126a-122">OUTPUTS</span></span>

### <span data-ttu-id="7126a-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="7126a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>
<span data-ttu-id="7126a-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationGatewaySslPredefinedPolicy, Microsoft. Azure. commands. Network, version = 4.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7126a-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7126a-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7126a-125">NOTES</span></span>

## <span data-ttu-id="7126a-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7126a-126">RELATED LINKS</span></span>

