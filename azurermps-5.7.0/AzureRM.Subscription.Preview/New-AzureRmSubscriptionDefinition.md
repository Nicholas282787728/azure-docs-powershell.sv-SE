---
external help file: Microsoft.Azure.Commands.SubscriptionDefinition.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription.preview/new-azurermsubscriptiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
ms.openlocfilehash: 7acaca4977114a1a57f88f5050f658753a9b6214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581895"
---
# <span data-ttu-id="f48d6-101">New-AzureRmSubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="f48d6-101">New-AzureRmSubscriptionDefinition</span></span>

## <span data-ttu-id="f48d6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f48d6-102">SYNOPSIS</span></span>
<span data-ttu-id="f48d6-103">Skapar en prenumerations definition.</span><span class="sxs-lookup"><span data-stu-id="f48d6-103">Creates a subscription definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f48d6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f48d6-104">SYNTAX</span></span>

### <span data-ttu-id="f48d6-105">Skapa abonnemangs definition</span><span class="sxs-lookup"><span data-stu-id="f48d6-105">Create subscription definition</span></span>
```
New-AzureRmSubscriptionDefinition -Name <String> -OfferType <String> [-SubscriptionDisplayName <String>]
```

## <span data-ttu-id="f48d6-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f48d6-106">DESCRIPTION</span></span>
<span data-ttu-id="f48d6-107">Cmdleten **New-AzureRmSubscriptionDefinition** skapar en prenumerations definition.</span><span class="sxs-lookup"><span data-stu-id="f48d6-107">The **New-AzureRmSubscriptionDefinition** cmdlet creates a subscription definition.</span></span>

## <span data-ttu-id="f48d6-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f48d6-108">EXAMPLES</span></span>

### <span data-ttu-id="f48d6-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f48d6-109">Example 1</span></span>
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MySubDef
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="f48d6-110">Skapar en prenumerations definition med ett förvalt visnings namn för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="f48d6-110">Creates a subscription definition with a default subscription display name.</span></span>

### <span data-ttu-id="f48d6-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f48d6-111">Example 2</span></span>
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P -SubscriptionDisplayName MyPaygoSub

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MyPaygoSub
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="f48d6-112">Skapar en prenumerations definition med ett anpassat abonnemangs visnings namn.</span><span class="sxs-lookup"><span data-stu-id="f48d6-112">Creates a subscription definition with a custom subscription display name.</span></span>

## <span data-ttu-id="f48d6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f48d6-113">PARAMETERS</span></span>

### <span data-ttu-id="f48d6-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="f48d6-114">-Name</span></span>
<span data-ttu-id="f48d6-115">Namnet på den prenumerations definition som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="f48d6-115">The name of the subscription definition to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f48d6-116">-OfferType</span><span class="sxs-lookup"><span data-stu-id="f48d6-116">-OfferType</span></span>
<span data-ttu-id="f48d6-117">Den typ av erbjudande som ska användas när det underliggande abonnemanget skapas.</span><span class="sxs-lookup"><span data-stu-id="f48d6-117">The type of offer to use when creating the underlying subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f48d6-118">-SubscriptionDisplayName</span><span class="sxs-lookup"><span data-stu-id="f48d6-118">-SubscriptionDisplayName</span></span>
<span data-ttu-id="f48d6-119">Visnings namnet som ska användas när prenumerations definitionen för ett underliggande abonnemang skapas.</span><span class="sxs-lookup"><span data-stu-id="f48d6-119">The display name to use when creating the subscription definition's underlying subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f48d6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f48d6-120">CommonParameters</span></span>
<span data-ttu-id="f48d6-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f48d6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f48d6-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f48d6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f48d6-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f48d6-123">INPUTS</span></span>

### <span data-ttu-id="f48d6-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="f48d6-124">None</span></span>

## <span data-ttu-id="f48d6-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f48d6-125">OUTPUTS</span></span>

### <span data-ttu-id="f48d6-126">Microsoft. Azure. commands. SubscriptionDefinition. Models. PSSubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="f48d6-126">Microsoft.Azure.Commands.SubscriptionDefinition.Models.PSSubscriptionDefinition</span></span>

## <span data-ttu-id="f48d6-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f48d6-127">NOTES</span></span>

## <span data-ttu-id="f48d6-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f48d6-128">RELATED LINKS</span></span>

