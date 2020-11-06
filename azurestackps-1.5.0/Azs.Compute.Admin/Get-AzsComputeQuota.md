---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 30a1bc70b4e704d8dadf864dedf7173476909cf2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572060"
---
# <span data-ttu-id="038ff-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="038ff-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="038ff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="038ff-102">SYNOPSIS</span></span>
<span data-ttu-id="038ff-103">Returnerar kvoter som anger kvot gränser för beräkning av objekt.</span><span class="sxs-lookup"><span data-stu-id="038ff-103">Returns quotas specifying the quota limits for compute objects.</span></span>

## <span data-ttu-id="038ff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="038ff-104">SYNTAX</span></span>

### <span data-ttu-id="038ff-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="038ff-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="038ff-106">Lära</span><span class="sxs-lookup"><span data-stu-id="038ff-106">Get</span></span>
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="038ff-107">ID</span><span class="sxs-lookup"><span data-stu-id="038ff-107">ResourceId</span></span>
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="038ff-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="038ff-108">DESCRIPTION</span></span>
<span data-ttu-id="038ff-109">Få en lista över befintliga kvoter.</span><span class="sxs-lookup"><span data-stu-id="038ff-109">Get a list of existing quotas.</span></span>

## <span data-ttu-id="038ff-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="038ff-110">EXAMPLES</span></span>

### <span data-ttu-id="038ff-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="038ff-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsComputeQuota -Location 'local'
```

<span data-ttu-id="038ff-112">Hämta alla beräknings kvoter på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="038ff-112">Get all compute quotas at the specified location.</span></span>

### <span data-ttu-id="038ff-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="038ff-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsComputeQuota 'Default Quota'
```

<span data-ttu-id="038ff-114">Skaffa en specifik kvot.</span><span class="sxs-lookup"><span data-stu-id="038ff-114">Get a specific compute quota.</span></span>

## <span data-ttu-id="038ff-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="038ff-115">PARAMETERS</span></span>

### <span data-ttu-id="038ff-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="038ff-116">-Location</span></span>
<span data-ttu-id="038ff-117">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="038ff-117">Location of the resource.</span></span>

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

### <span data-ttu-id="038ff-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="038ff-118">-Name</span></span>
<span data-ttu-id="038ff-119">Namn på kvoten.</span><span class="sxs-lookup"><span data-stu-id="038ff-119">Name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="038ff-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="038ff-120">-ResourceId</span></span>
<span data-ttu-id="038ff-121">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="038ff-121">The resource id.</span></span>

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

### <span data-ttu-id="038ff-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="038ff-122">CommonParameters</span></span>
<span data-ttu-id="038ff-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="038ff-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="038ff-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="038ff-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="038ff-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="038ff-125">INPUTS</span></span>

## <span data-ttu-id="038ff-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="038ff-126">OUTPUTS</span></span>

### <span data-ttu-id="038ff-127">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="038ff-127">ComputeQuotaObject</span></span>

## <span data-ttu-id="038ff-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="038ff-128">NOTES</span></span>

## <span data-ttu-id="038ff-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="038ff-129">RELATED LINKS</span></span>

