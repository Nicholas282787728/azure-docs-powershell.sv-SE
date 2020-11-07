---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 641017c75243a253a6b9eb0054df7737a674f671
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921861"
---
# <span data-ttu-id="b6548-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="b6548-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="b6548-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6548-102">SYNOPSIS</span></span>
<span data-ttu-id="b6548-103">Skapa eller uppdatera en befintlig lagrings kvot.</span><span class="sxs-lookup"><span data-stu-id="b6548-103">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="b6548-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6548-104">SYNTAX</span></span>

### <span data-ttu-id="b6548-105">Uppdatering (standard)</span><span class="sxs-lookup"><span data-stu-id="b6548-105">Update (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>]
 [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6548-106">ID</span><span class="sxs-lookup"><span data-stu-id="b6548-106">ResourceId</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -ResourceId <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6548-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b6548-107">InputObject</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -InputObject <StorageQuota>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6548-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6548-108">DESCRIPTION</span></span>
<span data-ttu-id="b6548-109">Skapa eller uppdatera en befintlig lagrings kvot.</span><span class="sxs-lookup"><span data-stu-id="b6548-109">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="b6548-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6548-110">EXAMPLES</span></span>

### <span data-ttu-id="b6548-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="b6548-111">EXAMPLE 1</span></span>
```
Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -CapacityInGb 123 -NumberOfStorageAccounts 10
```

<span data-ttu-id="b6548-112">Uppdatera en befintlig lagrings kvot.</span><span class="sxs-lookup"><span data-stu-id="b6548-112">Update an existing storage quota.</span></span>

## <span data-ttu-id="b6548-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6548-113">PARAMETERS</span></span>

### <span data-ttu-id="b6548-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="b6548-114">-Name</span></span>
<span data-ttu-id="b6548-115">Namnet på lagrings kvoten.</span><span class="sxs-lookup"><span data-stu-id="b6548-115">The name of the storage quota.</span></span>

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

### <span data-ttu-id="b6548-116">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="b6548-116">-CapacityInGb</span></span>
<span data-ttu-id="b6548-117">Maxium kapacitet (GB).</span><span class="sxs-lookup"><span data-stu-id="b6548-117">Maxium capacity (GB).</span></span>

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

### <span data-ttu-id="b6548-118">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="b6548-118">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="b6548-119">Totalt antal lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="b6548-119">Total number of storage accounts.</span></span>

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

### <span data-ttu-id="b6548-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="b6548-120">-Location</span></span>
<span data-ttu-id="b6548-121">Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="b6548-121">Resource location.</span></span>

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

### <span data-ttu-id="b6548-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6548-122">-ResourceId</span></span>
<span data-ttu-id="b6548-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b6548-123">The resource id.</span></span>

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

### <span data-ttu-id="b6548-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6548-124">-InputObject</span></span>
<span data-ttu-id="b6548-125">Posbbily ändrade lagrings kvot som returneras av Get-AzsStorageQuota.</span><span class="sxs-lookup"><span data-stu-id="b6548-125">Posbbily modified storage quota returned by Get-AzsStorageQuota.</span></span>

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

### <span data-ttu-id="b6548-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6548-126">-WhatIf</span></span>
<span data-ttu-id="b6548-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b6548-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6548-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b6548-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6548-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b6548-129">-Confirm</span></span>
<span data-ttu-id="b6548-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b6548-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6548-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6548-131">CommonParameters</span></span>
<span data-ttu-id="b6548-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6548-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6548-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6548-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6548-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6548-134">INPUTS</span></span>

## <span data-ttu-id="b6548-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6548-135">OUTPUTS</span></span>

### <span data-ttu-id="b6548-136">Microsoft. AzureStack. Management. Storage. admin. Models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="b6548-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="b6548-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6548-137">NOTES</span></span>

## <span data-ttu-id="b6548-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6548-138">RELATED LINKS</span></span>
