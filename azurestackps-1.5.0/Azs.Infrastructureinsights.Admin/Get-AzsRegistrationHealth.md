---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d73e2db2f09ba504e9c6adbf15a0bbc2629452ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754955"
---
# <span data-ttu-id="81a63-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="81a63-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="81a63-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="81a63-102">SYNOPSIS</span></span>
<span data-ttu-id="81a63-103">Returnerar en lista över statusen för varje resurs under en tjänst.</span><span class="sxs-lookup"><span data-stu-id="81a63-103">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="81a63-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="81a63-104">SYNTAX</span></span>

### <span data-ttu-id="81a63-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="81a63-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="81a63-106">Lära</span><span class="sxs-lookup"><span data-stu-id="81a63-106">Get</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName <String> -Name <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="81a63-107">ID</span><span class="sxs-lookup"><span data-stu-id="81a63-107">ResourceId</span></span>
```
Get-AzsRegistrationHealth -ResourceId <String> [-Filter <String>] [<CommonParameters>]
```

## <span data-ttu-id="81a63-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="81a63-108">DESCRIPTION</span></span>
<span data-ttu-id="81a63-109">Returnerar en lista över statusen för varje resurs under en tjänst.</span><span class="sxs-lookup"><span data-stu-id="81a63-109">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="81a63-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="81a63-110">EXAMPLES</span></span>

### <span data-ttu-id="81a63-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="81a63-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="81a63-112">Returnerar en lista över statusen för varje resurs under en tjänst.</span><span class="sxs-lookup"><span data-stu-id="81a63-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="81a63-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="81a63-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationName $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="81a63-114">Returnerar hälso status under a för Microsoft. Fabric. admin.</span><span class="sxs-lookup"><span data-stu-id="81a63-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="81a63-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="81a63-115">PARAMETERS</span></span>

### <span data-ttu-id="81a63-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="81a63-116">-Filter</span></span>
<span data-ttu-id="81a63-117">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="81a63-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="81a63-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="81a63-118">-Location</span></span>
<span data-ttu-id="81a63-119">Regionens namn</span><span class="sxs-lookup"><span data-stu-id="81a63-119">Name of the region</span></span>

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

### <span data-ttu-id="81a63-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="81a63-120">-Name</span></span>
<span data-ttu-id="81a63-121">Resurs namn för hälso objekt som motsvarar resurs registrerings-ID: t.</span><span class="sxs-lookup"><span data-stu-id="81a63-121">The resource name of the health object which corresponds to the resource registration id.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ResourceRegistrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81a63-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81a63-122">-ResourceGroupName</span></span>
<span data-ttu-id="81a63-123">Resurs grupp namn som resursen finns.</span><span class="sxs-lookup"><span data-stu-id="81a63-123">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="81a63-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81a63-124">-ResourceId</span></span>
<span data-ttu-id="81a63-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="81a63-125">The resource id.</span></span>

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

### <span data-ttu-id="81a63-126">-ServiceRegistrationName</span><span class="sxs-lookup"><span data-stu-id="81a63-126">-ServiceRegistrationName</span></span>
<span data-ttu-id="81a63-127">Registrerings-ID för tjänst.</span><span class="sxs-lookup"><span data-stu-id="81a63-127">Service registration id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: ServiceRegistrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81a63-128">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="81a63-128">-Skip</span></span>
<span data-ttu-id="81a63-129">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="81a63-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="81a63-130">-Överst</span><span class="sxs-lookup"><span data-stu-id="81a63-130">-Top</span></span>
<span data-ttu-id="81a63-131">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="81a63-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="81a63-132">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="81a63-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="81a63-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a63-133">CommonParameters</span></span>
<span data-ttu-id="81a63-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81a63-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a63-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81a63-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a63-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="81a63-136">INPUTS</span></span>

## <span data-ttu-id="81a63-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="81a63-137">OUTPUTS</span></span>

### <span data-ttu-id="81a63-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. ResourceHealth</span><span class="sxs-lookup"><span data-stu-id="81a63-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ResourceHealth</span></span>

## <span data-ttu-id="81a63-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="81a63-139">NOTES</span></span>

## <span data-ttu-id="81a63-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="81a63-140">RELATED LINKS</span></span>

