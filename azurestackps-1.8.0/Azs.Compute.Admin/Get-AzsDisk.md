---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b639a09789960393ac26d035a80157069dbaaa
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921413"
---
# <span data-ttu-id="3f66d-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="3f66d-101">Get-AzsDisk</span></span>

## <span data-ttu-id="3f66d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f66d-102">SYNOPSIS</span></span>
<span data-ttu-id="3f66d-103">Returnerar listan med hanterade diskar som kan migreras i den angivna resursen.</span><span class="sxs-lookup"><span data-stu-id="3f66d-103">Returns the list of managed disks which can be migrated in the specified share.</span></span>

## <span data-ttu-id="3f66d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f66d-104">SYNTAX</span></span>

### <span data-ttu-id="3f66d-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="3f66d-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-Start <Int32>] [-SharePath <String>] [-Count <Int32>]
 [-UserSubscriptionId <String>] [-Status <String>] [<CommonParameters>]
```

### <span data-ttu-id="3f66d-106">ID</span><span class="sxs-lookup"><span data-stu-id="3f66d-106">ResourceId</span></span>
```
Get-AzsDisk -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="3f66d-107">Lära</span><span class="sxs-lookup"><span data-stu-id="3f66d-107">Get</span></span>
```
Get-AzsDisk [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="3f66d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f66d-108">DESCRIPTION</span></span>
<span data-ttu-id="3f66d-109">Returnerar en lista med diskar.</span><span class="sxs-lookup"><span data-stu-id="3f66d-109">Returns a list of disks.</span></span>

## <span data-ttu-id="3f66d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f66d-110">EXAMPLES</span></span>

### <span data-ttu-id="3f66d-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3f66d-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$disks = Get-AzsDisk -location local
```

<span data-ttu-id="3f66d-112">Returnerar en lista med hanterade diskar på lokal plats.</span><span class="sxs-lookup"><span data-stu-id="3f66d-112">Returns a list of managed disks at the location local.</span></span>
<span data-ttu-id="3f66d-113">Den första 100-disketterna</span><span class="sxs-lookup"><span data-stu-id="3f66d-113">By default, it will the first 100 disks</span></span>

### <span data-ttu-id="3f66d-114">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="3f66d-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$disk = Get-AzsDisk -location local -name $DiskId
```

<span data-ttu-id="3f66d-115">Skaffa en specifik hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="3f66d-115">Get a specific managed disk.</span></span>

## <span data-ttu-id="3f66d-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f66d-116">PARAMETERS</span></span>

### <span data-ttu-id="3f66d-117">-Antal</span><span class="sxs-lookup"><span data-stu-id="3f66d-117">-Count</span></span>
<span data-ttu-id="3f66d-118">Det högsta antalet diskar som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="3f66d-118">The maximum number of disks to return.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f66d-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="3f66d-119">-Location</span></span>
<span data-ttu-id="3f66d-120">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="3f66d-120">Location of the resource.</span></span>

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

### <span data-ttu-id="3f66d-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="3f66d-121">-Name</span></span>
<span data-ttu-id="3f66d-122">GUID som identitet.</span><span class="sxs-lookup"><span data-stu-id="3f66d-122">The disk guid as identity.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: DiskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f66d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f66d-123">-ResourceId</span></span>
<span data-ttu-id="3f66d-124">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="3f66d-124">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f66d-125">-SharePath</span><span class="sxs-lookup"><span data-stu-id="3f66d-125">-SharePath</span></span>
<span data-ttu-id="3f66d-126">Käll resursen som resursen tillhör.</span><span class="sxs-lookup"><span data-stu-id="3f66d-126">The source share which the resource belongs to.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f66d-127">-Start</span><span class="sxs-lookup"><span data-stu-id="3f66d-127">-Start</span></span>
<span data-ttu-id="3f66d-128">Start indexet för diskar i Query.</span><span class="sxs-lookup"><span data-stu-id="3f66d-128">The start index of disks in query.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f66d-129">-Status</span><span class="sxs-lookup"><span data-stu-id="3f66d-129">-Status</span></span>
<span data-ttu-id="3f66d-130">Parametrar för disk status.</span><span class="sxs-lookup"><span data-stu-id="3f66d-130">The parameters of disk state.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f66d-131">-UserSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f66d-131">-UserSubscriptionId</span></span>
<span data-ttu-id="3f66d-132">ID för klient organisations prenumeration som resursen tillhör.</span><span class="sxs-lookup"><span data-stu-id="3f66d-132">Tenant Subscription Id which the resource belongs to.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f66d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f66d-133">CommonParameters</span></span>
<span data-ttu-id="3f66d-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f66d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f66d-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f66d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f66d-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f66d-136">INPUTS</span></span>

## <span data-ttu-id="3f66d-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f66d-137">OUTPUTS</span></span>

### <span data-ttu-id="3f66d-138">Microsoft. AzureStack. Management. Compute. admin. Models. disk</span><span class="sxs-lookup"><span data-stu-id="3f66d-138">Microsoft.AzureStack.Management.Compute.Admin.Models.Disk</span></span>

## <span data-ttu-id="3f66d-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f66d-139">NOTES</span></span>

## <span data-ttu-id="3f66d-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f66d-140">RELATED LINKS</span></span>

