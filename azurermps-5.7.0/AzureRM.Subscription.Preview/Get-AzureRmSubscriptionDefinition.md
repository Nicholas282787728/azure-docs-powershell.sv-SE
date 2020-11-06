---
external help file: Microsoft.Azure.Commands.SubscriptionDefinition.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription.preview/get-azurermsubscriptiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/Get-AzureRmSubscriptionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/Get-AzureRmSubscriptionDefinition.md
ms.openlocfilehash: 8f9cfda051542327fdb6175da081c99e6b8b6b3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574125"
---
# <span data-ttu-id="a2a0a-101">Get-AzureRmSubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="a2a0a-101">Get-AzureRmSubscriptionDefinition</span></span>

## <span data-ttu-id="a2a0a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a2a0a-102">SYNOPSIS</span></span>
<span data-ttu-id="a2a0a-103">Skaffa en prenumerations definition.</span><span class="sxs-lookup"><span data-stu-id="a2a0a-103">Get a subscription definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2a0a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a2a0a-104">SYNTAX</span></span>

### <span data-ttu-id="a2a0a-105">Hämta abonnemangs definitioner.</span><span class="sxs-lookup"><span data-stu-id="a2a0a-105">Get subscription definitions.</span></span>
```
Get-AzureRmSubscriptionDefinition
```

## <span data-ttu-id="a2a0a-106">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a2a0a-106">EXAMPLES</span></span>

### <span data-ttu-id="a2a0a-107">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a2a0a-107">Example 1</span></span>
```
PS C:\> Get-AzureRmSubscriptionDefinition

Name                    : MyProdSubscription1
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MyProdSubscription1
OfferType               : MS-AZR-0017P

Name                    : MyProdSubscription2
SubscriptionId          : 368425df-b536-4f42-b1ba-64613cfcc4b5
SubscriptionDisplayName : MyProdSubscription2
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="a2a0a-108">Hämtar alla abonnemangs definitioner.</span><span class="sxs-lookup"><span data-stu-id="a2a0a-108">Gets all subscription definitions.</span></span>

### <span data-ttu-id="a2a0a-109">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a2a0a-109">Example 2</span></span>
```
PS C:\> Get-AzureRmSubscriptionDefinition -Name MyProdSubscription2

Name                    : MyProdSubscription2
SubscriptionId          : 368425df-b536-4f42-b1ba-64613cfcc4b5
SubscriptionDisplayName : MyProdSubscription2
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="a2a0a-110">Hämtar en prenumerations definition med namnet MyProdSubscription2.</span><span class="sxs-lookup"><span data-stu-id="a2a0a-110">Gets a subscription definition with the name MyProdSubscription2.</span></span>

## <span data-ttu-id="a2a0a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a2a0a-111">PARAMETERS</span></span>

### <span data-ttu-id="a2a0a-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="a2a0a-112">-Name</span></span>
<span data-ttu-id="a2a0a-113">Namnet på prenumerations definitionen som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="a2a0a-113">The name of the subscription definition to retrieve.</span></span>

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

### <span data-ttu-id="a2a0a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2a0a-114">CommonParameters</span></span>
<span data-ttu-id="a2a0a-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2a0a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2a0a-116">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2a0a-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2a0a-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a2a0a-117">INPUTS</span></span>

### <span data-ttu-id="a2a0a-118">Ingen</span><span class="sxs-lookup"><span data-stu-id="a2a0a-118">None</span></span>

## <span data-ttu-id="a2a0a-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a2a0a-119">OUTPUTS</span></span>

### <span data-ttu-id="a2a0a-120">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. SubscriptionDefinition. Models. PSSubscriptionDefinition, Microsoft. Azure. commands. SubscriptionDefinition, version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a2a0a-120">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.SubscriptionDefinition.Models.PSSubscriptionDefinition, Microsoft.Azure.Commands.SubscriptionDefinition, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a2a0a-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a2a0a-121">NOTES</span></span>

## <span data-ttu-id="a2a0a-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a2a0a-122">RELATED LINKS</span></span>

