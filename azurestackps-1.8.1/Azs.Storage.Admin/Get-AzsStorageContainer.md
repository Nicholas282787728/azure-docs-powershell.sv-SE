---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 34d5c967154f08526a0002f187b8cb869d933d39
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921896"
---
# <span data-ttu-id="db8f3-101">Get-AzsStorageContainer</span><span class="sxs-lookup"><span data-stu-id="db8f3-101">Get-AzsStorageContainer</span></span>

## <span data-ttu-id="db8f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db8f3-102">SYNOPSIS</span></span>
<span data-ttu-id="db8f3-103">Returnerar listan med behållare som kan migreras i den angivna resursen.</span><span class="sxs-lookup"><span data-stu-id="db8f3-103">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="db8f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db8f3-104">SYNTAX</span></span>

```
Get-AzsStorageContainer [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-MaxCount] <Int32>] [[-StartIndex] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="db8f3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db8f3-105">DESCRIPTION</span></span>
<span data-ttu-id="db8f3-106">Returnerar listan med behållare som kan migreras i den angivna resursen.</span><span class="sxs-lookup"><span data-stu-id="db8f3-106">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="db8f3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db8f3-107">EXAMPLES</span></span>

### <span data-ttu-id="db8f3-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="db8f3-108">EXAMPLE 1</span></span>
```
Get-AzsStorageContainer -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="db8f3-109">Få en lista med behållare som kan migreras på den angivna resursen.</span><span class="sxs-lookup"><span data-stu-id="db8f3-109">Get a list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="db8f3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db8f3-110">PARAMETERS</span></span>

### <span data-ttu-id="db8f3-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="db8f3-111">-FarmName</span></span>
<span data-ttu-id="db8f3-112">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="db8f3-112">Farm Id.</span></span>

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

### <span data-ttu-id="db8f3-113">-ShareName</span><span class="sxs-lookup"><span data-stu-id="db8f3-113">-ShareName</span></span>
<span data-ttu-id="db8f3-114">Resurs namn som innehåller lagrings behållarna.</span><span class="sxs-lookup"><span data-stu-id="db8f3-114">Share name which holds the storage containers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db8f3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db8f3-115">-ResourceGroupName</span></span>
<span data-ttu-id="db8f3-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="db8f3-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db8f3-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="db8f3-117">-MaxCount</span></span>
<span data-ttu-id="db8f3-118">Det högsta antalet containrar.</span><span class="sxs-lookup"><span data-stu-id="db8f3-118">The max count of containers.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: 100000000
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db8f3-119">-Start index</span><span class="sxs-lookup"><span data-stu-id="db8f3-119">-StartIndex</span></span>
<span data-ttu-id="db8f3-120">Start indexet för behållare.</span><span class="sxs-lookup"><span data-stu-id="db8f3-120">The start index of get containers.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db8f3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db8f3-121">CommonParameters</span></span>
<span data-ttu-id="db8f3-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db8f3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db8f3-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db8f3-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db8f3-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db8f3-124">INPUTS</span></span>

## <span data-ttu-id="db8f3-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db8f3-125">OUTPUTS</span></span>

## <span data-ttu-id="db8f3-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db8f3-126">NOTES</span></span>

## <span data-ttu-id="db8f3-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db8f3-127">RELATED LINKS</span></span>
