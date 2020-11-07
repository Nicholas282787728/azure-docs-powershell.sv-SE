---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4285a7423390f5d9b5384faa63f95c4206840d71
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921838"
---
# <span data-ttu-id="00aac-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="00aac-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="00aac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="00aac-102">SYNOPSIS</span></span>
<span data-ttu-id="00aac-103">Returnerar en lista över statusen för varje resurs under en tjänst.</span><span class="sxs-lookup"><span data-stu-id="00aac-103">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="00aac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="00aac-104">SYNTAX</span></span>

### <span data-ttu-id="00aac-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="00aac-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="00aac-106">Lära</span><span class="sxs-lookup"><span data-stu-id="00aac-106">Get</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> -ResourceRegistrationId <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="00aac-107">ID</span><span class="sxs-lookup"><span data-stu-id="00aac-107">ResourceId</span></span>
```
Get-AzsRegistrationHealth -ResourceId <String> [-Filter <String>] [<CommonParameters>]
```

## <span data-ttu-id="00aac-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="00aac-108">DESCRIPTION</span></span>
<span data-ttu-id="00aac-109">Returnerar en lista över statusen för varje resurs under en tjänst.</span><span class="sxs-lookup"><span data-stu-id="00aac-109">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="00aac-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="00aac-110">EXAMPLES</span></span>

### <span data-ttu-id="00aac-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="00aac-111">EXAMPLE 1</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="00aac-112">Returnerar en lista över statusen för varje resurs under en tjänst.</span><span class="sxs-lookup"><span data-stu-id="00aac-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="00aac-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="00aac-113">EXAMPLE 2</span></span>
```
Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationId $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="00aac-114">Returnerar hälso status under a för Microsoft. Fabric. admin.</span><span class="sxs-lookup"><span data-stu-id="00aac-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="00aac-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="00aac-115">PARAMETERS</span></span>

### <span data-ttu-id="00aac-116">-ServiceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="00aac-116">-ServiceRegistrationId</span></span>
<span data-ttu-id="00aac-117">Registrerings-ID för tjänst.</span><span class="sxs-lookup"><span data-stu-id="00aac-117">Service registration id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00aac-118">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="00aac-118">-ResourceRegistrationId</span></span>


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

### <span data-ttu-id="00aac-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="00aac-119">-Location</span></span>
<span data-ttu-id="00aac-120">Regionens namn</span><span class="sxs-lookup"><span data-stu-id="00aac-120">Name of the region</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00aac-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00aac-121">-ResourceGroupName</span></span>
<span data-ttu-id="00aac-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="00aac-122">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00aac-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00aac-123">-ResourceId</span></span>
<span data-ttu-id="00aac-124">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="00aac-124">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00aac-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="00aac-125">-Filter</span></span>
<span data-ttu-id="00aac-126">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="00aac-126">OData filter parameter.</span></span>

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

### <span data-ttu-id="00aac-127">-Överst</span><span class="sxs-lookup"><span data-stu-id="00aac-127">-Top</span></span>
<span data-ttu-id="00aac-128">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="00aac-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="00aac-129">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="00aac-129">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00aac-130">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="00aac-130">-Skip</span></span>
<span data-ttu-id="00aac-131">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="00aac-131">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00aac-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00aac-132">CommonParameters</span></span>
<span data-ttu-id="00aac-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00aac-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00aac-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00aac-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00aac-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="00aac-135">INPUTS</span></span>

## <span data-ttu-id="00aac-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="00aac-136">OUTPUTS</span></span>

### <span data-ttu-id="00aac-137">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. ResourceHealth</span><span class="sxs-lookup"><span data-stu-id="00aac-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ResourceHealth</span></span>

## <span data-ttu-id="00aac-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="00aac-138">NOTES</span></span>

## <span data-ttu-id="00aac-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="00aac-139">RELATED LINKS</span></span>
