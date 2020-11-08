---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 641017c75243a253a6b9eb0054df7737a674f671
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100244"
---
# <span data-ttu-id="29537-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="29537-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="29537-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29537-102">SYNOPSIS</span></span>
<span data-ttu-id="29537-103">Skapa eller uppdatera en befintlig lagrings kvot.</span><span class="sxs-lookup"><span data-stu-id="29537-103">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="29537-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29537-104">SYNTAX</span></span>

### <span data-ttu-id="29537-105">Uppdatering (standard)</span><span class="sxs-lookup"><span data-stu-id="29537-105">Update (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>]
 [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29537-106">ID</span><span class="sxs-lookup"><span data-stu-id="29537-106">ResourceId</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -ResourceId <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29537-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="29537-107">InputObject</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -InputObject <StorageQuota>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29537-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29537-108">DESCRIPTION</span></span>
<span data-ttu-id="29537-109">Skapa eller uppdatera en befintlig lagrings kvot.</span><span class="sxs-lookup"><span data-stu-id="29537-109">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="29537-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29537-110">EXAMPLES</span></span>

### <span data-ttu-id="29537-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="29537-111">EXAMPLE 1</span></span>
```
Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -CapacityInGb 123 -NumberOfStorageAccounts 10
```

<span data-ttu-id="29537-112">Uppdatera en befintlig lagrings kvot.</span><span class="sxs-lookup"><span data-stu-id="29537-112">Update an existing storage quota.</span></span>

## <span data-ttu-id="29537-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29537-113">PARAMETERS</span></span>

### <span data-ttu-id="29537-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="29537-114">-Name</span></span>
<span data-ttu-id="29537-115">Namnet på lagrings kvoten.</span><span class="sxs-lookup"><span data-stu-id="29537-115">The name of the storage quota.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29537-116">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="29537-116">-CapacityInGb</span></span>
<span data-ttu-id="29537-117">Maxium kapacitet (GB).</span><span class="sxs-lookup"><span data-stu-id="29537-117">Maxium capacity (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29537-118">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="29537-118">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="29537-119">Totalt antal lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="29537-119">Total number of storage accounts.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29537-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="29537-120">-Location</span></span>
<span data-ttu-id="29537-121">Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="29537-121">Resource location.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29537-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29537-122">-ResourceId</span></span>
<span data-ttu-id="29537-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="29537-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29537-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29537-124">-InputObject</span></span>
<span data-ttu-id="29537-125">Posbbily ändrade lagrings kvot som returneras av Get-AzsStorageQuota.</span><span class="sxs-lookup"><span data-stu-id="29537-125">Posbbily modified storage quota returned by Get-AzsStorageQuota.</span></span>

```yaml
Type: StorageQuota
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29537-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29537-126">-WhatIf</span></span>
<span data-ttu-id="29537-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="29537-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29537-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="29537-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29537-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="29537-129">-Confirm</span></span>
<span data-ttu-id="29537-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="29537-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29537-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29537-131">CommonParameters</span></span>
<span data-ttu-id="29537-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29537-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29537-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29537-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29537-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29537-134">INPUTS</span></span>

## <span data-ttu-id="29537-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29537-135">OUTPUTS</span></span>

### <span data-ttu-id="29537-136">Microsoft. AzureStack. Management. Storage. admin. Models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="29537-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="29537-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29537-137">NOTES</span></span>

## <span data-ttu-id="29537-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29537-138">RELATED LINKS</span></span>
