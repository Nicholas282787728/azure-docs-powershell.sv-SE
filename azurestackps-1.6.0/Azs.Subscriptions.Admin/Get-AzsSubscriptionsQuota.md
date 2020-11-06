---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 503661f4e50ddd7575cc9c98ef4c19e2028ddf83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572100"
---
# <span data-ttu-id="b9982-101">Get-AzsSubscriptionsQuota</span><span class="sxs-lookup"><span data-stu-id="b9982-101">Get-AzsSubscriptionsQuota</span></span>

## <span data-ttu-id="b9982-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b9982-102">SYNOPSIS</span></span>
<span data-ttu-id="b9982-103">Hämta listan med abonnemangs resurs leverantörs kvoter på en plats.</span><span class="sxs-lookup"><span data-stu-id="b9982-103">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="b9982-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b9982-104">SYNTAX</span></span>

### <span data-ttu-id="b9982-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="b9982-105">List (Default)</span></span>
```
Get-AzsSubscriptionsQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="b9982-106">Lära</span><span class="sxs-lookup"><span data-stu-id="b9982-106">Get</span></span>
```
Get-AzsSubscriptionsQuota -Name <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="b9982-107">ID</span><span class="sxs-lookup"><span data-stu-id="b9982-107">ResourceId</span></span>
```
Get-AzsSubscriptionsQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b9982-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b9982-108">DESCRIPTION</span></span>
<span data-ttu-id="b9982-109">Hämta listan med kvoter på en plats.</span><span class="sxs-lookup"><span data-stu-id="b9982-109">Get the list of quotas at a location.</span></span>

## <span data-ttu-id="b9982-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b9982-110">EXAMPLES</span></span>

### <span data-ttu-id="b9982-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b9982-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionsQuota
```

<span data-ttu-id="b9982-112">Hämta listan med abonnemangs resurs leverantörs kvoter på en plats.</span><span class="sxs-lookup"><span data-stu-id="b9982-112">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="b9982-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b9982-113">PARAMETERS</span></span>

### <span data-ttu-id="b9982-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="b9982-114">-Location</span></span>
<span data-ttu-id="b9982-115">AzureStack-platsen.</span><span class="sxs-lookup"><span data-stu-id="b9982-115">The AzureStack location.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9982-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="b9982-116">-Name</span></span>
<span data-ttu-id="b9982-117">Namn på kvoten.</span><span class="sxs-lookup"><span data-stu-id="b9982-117">Name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9982-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9982-118">-ResourceId</span></span>
<span data-ttu-id="b9982-119">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b9982-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9982-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9982-120">CommonParameters</span></span>
<span data-ttu-id="b9982-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9982-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9982-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9982-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9982-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b9982-123">INPUTS</span></span>

## <span data-ttu-id="b9982-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b9982-124">OUTPUTS</span></span>

### <span data-ttu-id="b9982-125">Microsoft. AzureStack. Management. abonnemang. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="b9982-125">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Quota</span></span>

## <span data-ttu-id="b9982-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b9982-126">NOTES</span></span>

## <span data-ttu-id="b9982-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b9982-127">RELATED LINKS</span></span>

