---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2eec56d9fc157da994521a5b258cd28132344c52
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920895"
---
# <span data-ttu-id="dfba5-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="dfba5-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="dfba5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dfba5-102">SYNOPSIS</span></span>
<span data-ttu-id="dfba5-103">Skapa eller uppdatera en befintlig lagrings kvot.</span><span class="sxs-lookup"><span data-stu-id="dfba5-103">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="dfba5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dfba5-104">SYNTAX</span></span>

### <span data-ttu-id="dfba5-105">Uppdatering (standard)</span><span class="sxs-lookup"><span data-stu-id="dfba5-105">Update (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>]
 [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfba5-106">ID</span><span class="sxs-lookup"><span data-stu-id="dfba5-106">ResourceId</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -ResourceId <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfba5-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="dfba5-107">InputObject</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -InputObject <StorageQuota>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfba5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dfba5-108">DESCRIPTION</span></span>
<span data-ttu-id="dfba5-109">Skapa eller uppdatera en befintlig lagrings kvot.</span><span class="sxs-lookup"><span data-stu-id="dfba5-109">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="dfba5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dfba5-110">EXAMPLES</span></span>

### <span data-ttu-id="dfba5-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="dfba5-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -CapacityInGb 123 -NumberOfStorageAccounts 10
```

<span data-ttu-id="dfba5-112">Uppdatera en befintlig lagrings kvot.</span><span class="sxs-lookup"><span data-stu-id="dfba5-112">Update an existing storage quota.</span></span>

## <span data-ttu-id="dfba5-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dfba5-113">PARAMETERS</span></span>

### <span data-ttu-id="dfba5-114">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="dfba5-114">-CapacityInGb</span></span>
<span data-ttu-id="dfba5-115">Maxium kapacitet (GB).</span><span class="sxs-lookup"><span data-stu-id="dfba5-115">Maxium capacity (GB).</span></span>

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

### <span data-ttu-id="dfba5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfba5-116">-InputObject</span></span>
<span data-ttu-id="dfba5-117">Posbbily ändrade lagrings kvot som returneras av Get-AzsStorageQuota.</span><span class="sxs-lookup"><span data-stu-id="dfba5-117">Posbbily modified storage quota returned by Get-AzsStorageQuota.</span></span>

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

### <span data-ttu-id="dfba5-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="dfba5-118">-Location</span></span>
<span data-ttu-id="dfba5-119">Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="dfba5-119">Resource location.</span></span>

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

### <span data-ttu-id="dfba5-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="dfba5-120">-Name</span></span>
<span data-ttu-id="dfba5-121">Namnet på lagrings kvoten.</span><span class="sxs-lookup"><span data-stu-id="dfba5-121">The name of the storage quota.</span></span>

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

### <span data-ttu-id="dfba5-122">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="dfba5-122">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="dfba5-123">Totalt antal lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="dfba5-123">Total number of storage accounts.</span></span>

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

### <span data-ttu-id="dfba5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dfba5-124">-ResourceId</span></span>
<span data-ttu-id="dfba5-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="dfba5-125">The resource id.</span></span>

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

### <span data-ttu-id="dfba5-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dfba5-126">-Confirm</span></span>
<span data-ttu-id="dfba5-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dfba5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfba5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfba5-128">-WhatIf</span></span>
<span data-ttu-id="dfba5-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dfba5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfba5-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dfba5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfba5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfba5-131">CommonParameters</span></span>
<span data-ttu-id="dfba5-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfba5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfba5-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfba5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfba5-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dfba5-134">INPUTS</span></span>

## <span data-ttu-id="dfba5-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dfba5-135">OUTPUTS</span></span>

### <span data-ttu-id="dfba5-136">Microsoft. AzureStack. Management. Storage. admin. Models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="dfba5-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="dfba5-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dfba5-137">NOTES</span></span>

## <span data-ttu-id="dfba5-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dfba5-138">RELATED LINKS</span></span>

