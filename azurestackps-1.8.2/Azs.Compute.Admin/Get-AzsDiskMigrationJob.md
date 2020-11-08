---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06f2d231754fc422115cf800ef66189378e0cd4d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100135"
---
# <span data-ttu-id="b9b7a-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="b9b7a-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="b9b7a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b9b7a-102">SYNOPSIS</span></span>
<span data-ttu-id="b9b7a-103">Returnerar listan med hanterade Migreringsverktyg för diskar.</span><span class="sxs-lookup"><span data-stu-id="b9b7a-103">Returns the list of managed disk migration jobs.</span></span>

## <span data-ttu-id="b9b7a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b9b7a-104">SYNTAX</span></span>

### <span data-ttu-id="b9b7a-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="b9b7a-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="b9b7a-106">ID</span><span class="sxs-lookup"><span data-stu-id="b9b7a-106">ResourceId</span></span>
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="b9b7a-107">Lära</span><span class="sxs-lookup"><span data-stu-id="b9b7a-107">Get</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="b9b7a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b9b7a-108">DESCRIPTION</span></span>
<span data-ttu-id="b9b7a-109">Returnerar en lista med migreringsjobb.</span><span class="sxs-lookup"><span data-stu-id="b9b7a-109">Returns a list of disk migration jobs.</span></span>

## <span data-ttu-id="b9b7a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b9b7a-110">EXAMPLES</span></span>

### <span data-ttu-id="b9b7a-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b9b7a-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

<span data-ttu-id="b9b7a-112">Hämta ett specifikt jobb för hanterad migrering.</span><span class="sxs-lookup"><span data-stu-id="b9b7a-112">Get a specific managed disk migration job.</span></span>

### <span data-ttu-id="b9b7a-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b9b7a-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local
```

<span data-ttu-id="b9b7a-114">Returnerar en lista med hanterade diskallokering på platsen lokal.</span><span class="sxs-lookup"><span data-stu-id="b9b7a-114">Returns a list of managed disk migration jobs at the location local.</span></span>

## <span data-ttu-id="b9b7a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b9b7a-115">PARAMETERS</span></span>

### <span data-ttu-id="b9b7a-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="b9b7a-116">-Location</span></span>
<span data-ttu-id="b9b7a-117">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="b9b7a-117">Location of the resource.</span></span>

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

### <span data-ttu-id="b9b7a-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="b9b7a-118">-Name</span></span>
<span data-ttu-id="b9b7a-119">GUID-namnet för migreringen.</span><span class="sxs-lookup"><span data-stu-id="b9b7a-119">The migration job guid name.</span></span>

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

### <span data-ttu-id="b9b7a-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9b7a-120">-ResourceId</span></span>
<span data-ttu-id="b9b7a-121">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b9b7a-121">The resource id.</span></span>

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

### <span data-ttu-id="b9b7a-122">-Status</span><span class="sxs-lookup"><span data-stu-id="b9b7a-122">-Status</span></span>
<span data-ttu-id="b9b7a-123">Parametrarna för jobb status för diskallokering.</span><span class="sxs-lookup"><span data-stu-id="b9b7a-123">The parameters of disk migration job status.</span></span>

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

### <span data-ttu-id="b9b7a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9b7a-124">CommonParameters</span></span>
<span data-ttu-id="b9b7a-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9b7a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9b7a-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9b7a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9b7a-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b9b7a-127">INPUTS</span></span>

## <span data-ttu-id="b9b7a-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b9b7a-128">OUTPUTS</span></span>

### <span data-ttu-id="b9b7a-129">Microsoft. AzureStack. Management. Compute. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="b9b7a-129">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="b9b7a-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b9b7a-130">NOTES</span></span>

## <span data-ttu-id="b9b7a-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b9b7a-131">RELATED LINKS</span></span>

