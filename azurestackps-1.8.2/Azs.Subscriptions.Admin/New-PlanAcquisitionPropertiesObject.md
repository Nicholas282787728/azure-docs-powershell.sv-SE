---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 199d9fb2ce88c149965d488b55bce669f364a615
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099931"
---
# <span data-ttu-id="19b1d-101">New-PlanAcquisitionPropertiesObject</span><span class="sxs-lookup"><span data-stu-id="19b1d-101">New-PlanAcquisitionPropertiesObject</span></span>

## <span data-ttu-id="19b1d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="19b1d-102">SYNOPSIS</span></span>
<span data-ttu-id="19b1d-103">Representerar anskaffning av ett tilläggs abonnemang för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="19b1d-103">Represents the acquisition of an add-on plan for a subscription.</span></span>

## <span data-ttu-id="19b1d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="19b1d-104">SYNTAX</span></span>

```
New-PlanAcquisitionPropertiesObject [[-ProvisioningState] <String>] [[-AcquisitionTime] <String>]
 [[-Id] <String>] [[-PlanId] <String>] [[-AcquisitionId] <String>] [[-ExternalReferenceId] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="19b1d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="19b1d-105">DESCRIPTION</span></span>
<span data-ttu-id="19b1d-106">Representerar anskaffning av ett tilläggs abonnemang för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="19b1d-106">Represents the acquisition of an add-on plan for a subscription.</span></span>

## <span data-ttu-id="19b1d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="19b1d-107">EXAMPLES</span></span>

### <span data-ttu-id="19b1d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="19b1d-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="19b1d-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="19b1d-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="19b1d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="19b1d-110">PARAMETERS</span></span>

### <span data-ttu-id="19b1d-111">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="19b1d-111">-AcquisitionId</span></span>
<span data-ttu-id="19b1d-112">Anskaffnings-ID.</span><span class="sxs-lookup"><span data-stu-id="19b1d-112">Acquisition identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19b1d-113">-AcquisitionTime</span><span class="sxs-lookup"><span data-stu-id="19b1d-113">-AcquisitionTime</span></span>
<span data-ttu-id="19b1d-114">Anskaffnings tid.</span><span class="sxs-lookup"><span data-stu-id="19b1d-114">Acquisition time.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19b1d-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="19b1d-115">-ExternalReferenceId</span></span>
<span data-ttu-id="19b1d-116">Extern referens-ID.</span><span class="sxs-lookup"><span data-stu-id="19b1d-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19b1d-117">-ID</span><span class="sxs-lookup"><span data-stu-id="19b1d-117">-Id</span></span>
<span data-ttu-id="19b1d-118">Identifierare i kontexten för klient organisations prenumeration.</span><span class="sxs-lookup"><span data-stu-id="19b1d-118">Identifier in the tenant subscription context.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19b1d-119">-PlanId</span><span class="sxs-lookup"><span data-stu-id="19b1d-119">-PlanId</span></span>
<span data-ttu-id="19b1d-120">Plan identifierare i kontexten för klient organisations prenumeration.</span><span class="sxs-lookup"><span data-stu-id="19b1d-120">Plan identifier in the tenant subscription context.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19b1d-121">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="19b1d-121">-ProvisioningState</span></span>
<span data-ttu-id="19b1d-122">Tillstånd för etableringen.</span><span class="sxs-lookup"><span data-stu-id="19b1d-122">State of the provisioning.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19b1d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19b1d-123">CommonParameters</span></span>
<span data-ttu-id="19b1d-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19b1d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19b1d-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19b1d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19b1d-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="19b1d-126">INPUTS</span></span>

## <span data-ttu-id="19b1d-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="19b1d-127">OUTPUTS</span></span>

## <span data-ttu-id="19b1d-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="19b1d-128">NOTES</span></span>

## <span data-ttu-id="19b1d-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="19b1d-129">RELATED LINKS</span></span>

