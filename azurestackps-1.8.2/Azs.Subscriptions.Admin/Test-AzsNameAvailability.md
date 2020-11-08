---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4bd00dc1709a3060da9777ab4755ae1c6a28ec4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099942"
---
# <span data-ttu-id="9b0ff-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="9b0ff-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="9b0ff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b0ff-102">SYNOPSIS</span></span>
<span data-ttu-id="9b0ff-103">Returnerar avaialbility för angiven prenumerations resurs typ och namn</span><span class="sxs-lookup"><span data-stu-id="9b0ff-103">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="9b0ff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b0ff-104">SYNTAX</span></span>

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## <span data-ttu-id="9b0ff-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b0ff-105">DESCRIPTION</span></span>
<span data-ttu-id="9b0ff-106">Returnerar avaialbility för angiven prenumerations resurs typ och namn</span><span class="sxs-lookup"><span data-stu-id="9b0ff-106">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="9b0ff-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b0ff-107">EXAMPLES</span></span>

### <span data-ttu-id="9b0ff-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9b0ff-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

<span data-ttu-id="9b0ff-109">Returnerar avaialbility för angiven prenumerations resurs typ och namn</span><span class="sxs-lookup"><span data-stu-id="9b0ff-109">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="9b0ff-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b0ff-110">PARAMETERS</span></span>

### <span data-ttu-id="9b0ff-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="9b0ff-111">-Name</span></span>
<span data-ttu-id="9b0ff-112">Resurs namn som ska verifieras.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-112">The resource name to verify.</span></span>

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

### <span data-ttu-id="9b0ff-113">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9b0ff-113">-ResourceType</span></span>
<span data-ttu-id="9b0ff-114">Resurs typen för att verifiera.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-114">The resource type to verify.</span></span>

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

### <span data-ttu-id="9b0ff-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b0ff-115">CommonParameters</span></span>
<span data-ttu-id="9b0ff-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b0ff-117">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b0ff-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b0ff-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b0ff-118">INPUTS</span></span>

## <span data-ttu-id="9b0ff-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b0ff-119">OUTPUTS</span></span>

### <span data-ttu-id="9b0ff-120">Microsoft. AzureStack. Management. abonnemang. admin. Models. CheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="9b0ff-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.CheckNameAvailabilityResponse</span></span>

## <span data-ttu-id="9b0ff-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b0ff-121">NOTES</span></span>

## <span data-ttu-id="9b0ff-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b0ff-122">RELATED LINKS</span></span>

