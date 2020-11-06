---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
ms.openlocfilehash: 4714b97773583197807d6ca54152ee25ab520909
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576438"
---
# <span data-ttu-id="70377-101">Get-AzureRmReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="70377-101">Get-AzureRmReservationCatalog</span></span>

## <span data-ttu-id="70377-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70377-102">SYNOPSIS</span></span>
<span data-ttu-id="70377-103">Hämta katalogen med tillgängliga reservationer</span><span class="sxs-lookup"><span data-stu-id="70377-103">Get the catalog of available reservation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70377-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70377-104">SYNTAX</span></span>

```
Get-AzureRmReservationCatalog [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="70377-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70377-105">DESCRIPTION</span></span>
<span data-ttu-id="70377-106">Skaffa de regioner och SKU: er som är tillgängliga för reserverade instans köp för det angivna Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="70377-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="70377-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70377-107">EXAMPLES</span></span>

### <span data-ttu-id="70377-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="70377-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationCatalog
```

<span data-ttu-id="70377-109">Hämta katalogen för standard abonnemanget</span><span class="sxs-lookup"><span data-stu-id="70377-109">Get the catalog for the default subscription</span></span>

### <span data-ttu-id="70377-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="70377-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="70377-111">Hämta katalogen för det angivna abonnemanget</span><span class="sxs-lookup"><span data-stu-id="70377-111">Get the catalog for the specified subscription</span></span>

## <span data-ttu-id="70377-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70377-112">PARAMETERS</span></span>

### <span data-ttu-id="70377-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="70377-113">-SubscriptionId</span></span>
<span data-ttu-id="70377-114">ID för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="70377-114">Id of the subscription</span></span>

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

### <span data-ttu-id="70377-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70377-115">CommonParameters</span></span>
<span data-ttu-id="70377-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70377-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70377-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70377-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70377-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70377-118">INPUTS</span></span>

### <span data-ttu-id="70377-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="70377-119">None</span></span>

## <span data-ttu-id="70377-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70377-120">OUTPUTS</span></span>

### <span data-ttu-id="70377-121">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. reservations. Models. PSCatalog, Microsoft. Azure. commands. reservations, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="70377-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSCatalog, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="70377-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70377-122">NOTES</span></span>

## <span data-ttu-id="70377-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70377-123">RELATED LINKS</span></span>

