---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 267a5bf4c3f864c987c0bc747eefce9dd3ffe6b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920925"
---
# <span data-ttu-id="e81c3-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="e81c3-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="e81c3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e81c3-102">SYNOPSIS</span></span>
<span data-ttu-id="e81c3-103">Returnerar avaialbility för angiven prenumerations resurs typ och namn</span><span class="sxs-lookup"><span data-stu-id="e81c3-103">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="e81c3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e81c3-104">SYNTAX</span></span>

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## <span data-ttu-id="e81c3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e81c3-105">DESCRIPTION</span></span>
<span data-ttu-id="e81c3-106">Returnerar avaialbility för angiven prenumerations resurs typ och namn</span><span class="sxs-lookup"><span data-stu-id="e81c3-106">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="e81c3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e81c3-107">EXAMPLES</span></span>

### <span data-ttu-id="e81c3-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e81c3-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

<span data-ttu-id="e81c3-109">Returnerar avaialbility för angiven prenumerations resurs typ och namn</span><span class="sxs-lookup"><span data-stu-id="e81c3-109">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="e81c3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e81c3-110">PARAMETERS</span></span>

### <span data-ttu-id="e81c3-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="e81c3-111">-Name</span></span>
<span data-ttu-id="e81c3-112">Resurs namn som ska verifieras.</span><span class="sxs-lookup"><span data-stu-id="e81c3-112">The resource name to verify.</span></span>

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

### <span data-ttu-id="e81c3-113">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e81c3-113">-ResourceType</span></span>
<span data-ttu-id="e81c3-114">Resurs typen för att verifiera.</span><span class="sxs-lookup"><span data-stu-id="e81c3-114">The resource type to verify.</span></span>

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

### <span data-ttu-id="e81c3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e81c3-115">CommonParameters</span></span>
<span data-ttu-id="e81c3-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e81c3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e81c3-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e81c3-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e81c3-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e81c3-118">INPUTS</span></span>

## <span data-ttu-id="e81c3-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e81c3-119">OUTPUTS</span></span>

### <span data-ttu-id="e81c3-120">Microsoft. AzureStack. Management. abonnemang. admin. Models. CheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="e81c3-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.CheckNameAvailabilityResponse</span></span>

## <span data-ttu-id="e81c3-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e81c3-121">NOTES</span></span>

## <span data-ttu-id="e81c3-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e81c3-122">RELATED LINKS</span></span>

