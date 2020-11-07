---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cf36bf232ae48891b28562313fa2063e14a2be8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920660"
---
# <span data-ttu-id="426bd-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="426bd-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="426bd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="426bd-102">SYNOPSIS</span></span>
<span data-ttu-id="426bd-103">Returnerar listan med hanterade Migreringsverktyg för diskar.</span><span class="sxs-lookup"><span data-stu-id="426bd-103">Returns the list of managed disk migration jobs.</span></span>

## <span data-ttu-id="426bd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="426bd-104">SYNTAX</span></span>

### <span data-ttu-id="426bd-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="426bd-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="426bd-106">ID</span><span class="sxs-lookup"><span data-stu-id="426bd-106">ResourceId</span></span>
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="426bd-107">Lära</span><span class="sxs-lookup"><span data-stu-id="426bd-107">Get</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="426bd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="426bd-108">DESCRIPTION</span></span>
<span data-ttu-id="426bd-109">Returnerar en lista med migreringsjobb.</span><span class="sxs-lookup"><span data-stu-id="426bd-109">Returns a list of disk migration jobs.</span></span>

## <span data-ttu-id="426bd-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="426bd-110">EXAMPLES</span></span>

### <span data-ttu-id="426bd-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="426bd-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

<span data-ttu-id="426bd-112">Hämta ett specifikt jobb för hanterad migrering.</span><span class="sxs-lookup"><span data-stu-id="426bd-112">Get a specific managed disk migration job.</span></span>

### <span data-ttu-id="426bd-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="426bd-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local
```

<span data-ttu-id="426bd-114">Returnerar en lista med hanterade diskallokering på platsen lokal.</span><span class="sxs-lookup"><span data-stu-id="426bd-114">Returns a list of managed disk migration jobs at the location local.</span></span>

## <span data-ttu-id="426bd-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="426bd-115">PARAMETERS</span></span>

### <span data-ttu-id="426bd-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="426bd-116">-Location</span></span>
<span data-ttu-id="426bd-117">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="426bd-117">Location of the resource.</span></span>

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

### <span data-ttu-id="426bd-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="426bd-118">-Name</span></span>
<span data-ttu-id="426bd-119">GUID-namnet för migreringen.</span><span class="sxs-lookup"><span data-stu-id="426bd-119">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="426bd-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="426bd-120">-ResourceId</span></span>
<span data-ttu-id="426bd-121">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="426bd-121">The resource id.</span></span>

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

### <span data-ttu-id="426bd-122">-Status</span><span class="sxs-lookup"><span data-stu-id="426bd-122">-Status</span></span>
<span data-ttu-id="426bd-123">Parametrarna för jobb status för diskallokering.</span><span class="sxs-lookup"><span data-stu-id="426bd-123">The parameters of disk migration job status.</span></span>

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

### <span data-ttu-id="426bd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="426bd-124">CommonParameters</span></span>
<span data-ttu-id="426bd-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="426bd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="426bd-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="426bd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="426bd-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="426bd-127">INPUTS</span></span>

## <span data-ttu-id="426bd-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="426bd-128">OUTPUTS</span></span>

### <span data-ttu-id="426bd-129">Microsoft. AzureStack. Management. Compute. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="426bd-129">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="426bd-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="426bd-130">NOTES</span></span>

## <span data-ttu-id="426bd-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="426bd-131">RELATED LINKS</span></span>

