---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4cc08220a92dce5a49544cf958db79d7243b9ebb
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921876"
---
# <span data-ttu-id="7a479-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="7a479-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="7a479-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7a479-102">SYNOPSIS</span></span>
<span data-ttu-id="7a479-103">Skapa en ny lagrings kvot.</span><span class="sxs-lookup"><span data-stu-id="7a479-103">Create a new storage quota.</span></span>

## <span data-ttu-id="7a479-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7a479-104">SYNTAX</span></span>

```
New-AzsStorageQuota [-Name] <String> [[-CapacityInGb] <Int32>] [[-NumberOfStorageAccounts] <Int32>]
 [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a479-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7a479-105">DESCRIPTION</span></span>
<span data-ttu-id="7a479-106">Skapa en ny lagrings kvot.</span><span class="sxs-lookup"><span data-stu-id="7a479-106">Create a new storage quota.</span></span>

## <span data-ttu-id="7a479-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7a479-107">EXAMPLES</span></span>

### <span data-ttu-id="7a479-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="7a479-108">EXAMPLE 1</span></span>
```
New-AzsStorageQuota -CapacityInGb 1000 -NumberOfStorageAccounts 100 -Name 'TestCreateStorageQuota'
```

<span data-ttu-id="7a479-109">Skapa en ny lagrings kvot med angivna värden.</span><span class="sxs-lookup"><span data-stu-id="7a479-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="7a479-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7a479-110">PARAMETERS</span></span>

### <span data-ttu-id="7a479-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="7a479-111">-Name</span></span>
<span data-ttu-id="7a479-112">Namnet på lagrings kvoten.</span><span class="sxs-lookup"><span data-stu-id="7a479-112">The name of the storage quota.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a479-113">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="7a479-113">-CapacityInGb</span></span>
<span data-ttu-id="7a479-114">Maxium kapacitet (GB).</span><span class="sxs-lookup"><span data-stu-id="7a479-114">Maxium capacity (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: 500
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a479-115">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="7a479-115">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="7a479-116">Totalt antal lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="7a479-116">Total number of storage accounts.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: 20
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a479-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="7a479-117">-Location</span></span>
<span data-ttu-id="7a479-118">Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="7a479-118">Resource location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a479-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a479-119">-WhatIf</span></span>
<span data-ttu-id="7a479-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7a479-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a479-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7a479-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a479-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7a479-122">-Confirm</span></span>
<span data-ttu-id="7a479-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7a479-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a479-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a479-124">CommonParameters</span></span>
<span data-ttu-id="7a479-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a479-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a479-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a479-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a479-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7a479-127">INPUTS</span></span>

## <span data-ttu-id="7a479-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7a479-128">OUTPUTS</span></span>

### <span data-ttu-id="7a479-129">Microsoft. AzureStack. Management. Storage. admin. Models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="7a479-129">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="7a479-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7a479-130">NOTES</span></span>

## <span data-ttu-id="7a479-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7a479-131">RELATED LINKS</span></span>
