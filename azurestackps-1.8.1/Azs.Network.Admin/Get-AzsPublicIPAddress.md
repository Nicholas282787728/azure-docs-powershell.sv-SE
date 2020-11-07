---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af3edc04e7db61fa43aa4b192d4bc29d0ec47640
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921821"
---
# <span data-ttu-id="d09ce-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="d09ce-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="d09ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d09ce-102">SYNOPSIS</span></span>
<span data-ttu-id="d09ce-103">Lista över offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="d09ce-103">List of public IP addresses.</span></span>

## <span data-ttu-id="d09ce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d09ce-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="d09ce-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d09ce-105">DESCRIPTION</span></span>
<span data-ttu-id="d09ce-106">Lista över offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="d09ce-106">List of public IP addresses.</span></span>

## <span data-ttu-id="d09ce-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d09ce-107">EXAMPLES</span></span>

### <span data-ttu-id="d09ce-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="d09ce-108">EXAMPLE 1</span></span>
```
Get-AzsPublicIPAddress
```

<span data-ttu-id="d09ce-109">Hämta listan med offentliga IP-adresser, antingen tilldelade eller inte tilldelade.</span><span class="sxs-lookup"><span data-stu-id="d09ce-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="d09ce-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d09ce-110">PARAMETERS</span></span>

### <span data-ttu-id="d09ce-111">-Filter</span><span class="sxs-lookup"><span data-stu-id="d09ce-111">-Filter</span></span>
<span data-ttu-id="d09ce-112">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="d09ce-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="d09ce-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="d09ce-113">-OrderBy</span></span>
<span data-ttu-id="d09ce-114">OData orderBy-parameter.</span><span class="sxs-lookup"><span data-stu-id="d09ce-114">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="d09ce-115">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="d09ce-115">-Skip</span></span>
<span data-ttu-id="d09ce-116">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="d09ce-116">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d09ce-117">-Överst</span><span class="sxs-lookup"><span data-stu-id="d09ce-117">-Top</span></span>
<span data-ttu-id="d09ce-118">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="d09ce-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="d09ce-119">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="d09ce-119">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d09ce-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="d09ce-120">-InlineCount</span></span>
<span data-ttu-id="d09ce-121">Parameter för OData-antal.</span><span class="sxs-lookup"><span data-stu-id="d09ce-121">OData inline count parameter.</span></span>

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

### <span data-ttu-id="d09ce-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d09ce-122">CommonParameters</span></span>
<span data-ttu-id="d09ce-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d09ce-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d09ce-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d09ce-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d09ce-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d09ce-125">INPUTS</span></span>

## <span data-ttu-id="d09ce-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d09ce-126">OUTPUTS</span></span>

### <span data-ttu-id="d09ce-127">Microsoft. AzureStack. Management. Network. admin. Models. PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d09ce-127">Microsoft.AzureStack.Management.Network.Admin.Models.PublicIpAddress</span></span>

## <span data-ttu-id="d09ce-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d09ce-128">NOTES</span></span>

## <span data-ttu-id="d09ce-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d09ce-129">RELATED LINKS</span></span>
