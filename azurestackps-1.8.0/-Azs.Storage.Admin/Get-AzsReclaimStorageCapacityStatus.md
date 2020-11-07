---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dbd8de47397e86f2aed9f774b555a587cf69976a
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921578"
---
# <span data-ttu-id="3fdb0-101">Get-AzsReclaimStorageCapacityStatus</span><span class="sxs-lookup"><span data-stu-id="3fdb0-101">Get-AzsReclaimStorageCapacityStatus</span></span>

## <span data-ttu-id="3fdb0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3fdb0-102">SYNOPSIS</span></span>
<span data-ttu-id="3fdb0-103">Returnerar tillståndet för skräp insamlings jobbet.</span><span class="sxs-lookup"><span data-stu-id="3fdb0-103">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="3fdb0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3fdb0-104">SYNTAX</span></span>

```
Get-AzsReclaimStorageCapacityStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="3fdb0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3fdb0-105">DESCRIPTION</span></span>
<span data-ttu-id="3fdb0-106">Returnerar tillståndet för skräp insamlings jobbet.</span><span class="sxs-lookup"><span data-stu-id="3fdb0-106">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="3fdb0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3fdb0-107">EXAMPLES</span></span>

### <span data-ttu-id="3fdb0-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3fdb0-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsReclaimStorageCapacityStatus -FarmName "6ddbfe6e-8781-4a3d-b370-4a8b20a494d8" -JobId "92360f29-cd21-429d-a20b-9b11ab5902a0"
```

<span data-ttu-id="3fdb0-109">Returnera information om skräp insamling statusen.</span><span class="sxs-lookup"><span data-stu-id="3fdb0-109">Return information about the status of garbage collection.</span></span>

## <span data-ttu-id="3fdb0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3fdb0-110">PARAMETERS</span></span>

### <span data-ttu-id="3fdb0-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="3fdb0-111">-FarmName</span></span>
<span data-ttu-id="3fdb0-112">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="3fdb0-112">Farm Id.</span></span>

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

### <span data-ttu-id="3fdb0-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="3fdb0-113">-JobId</span></span>
<span data-ttu-id="3fdb0-114">Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="3fdb0-114">Operation Id.</span></span>

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

### <span data-ttu-id="3fdb0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fdb0-115">-ResourceGroupName</span></span>
<span data-ttu-id="3fdb0-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="3fdb0-116">Resource group name.</span></span>

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

### <span data-ttu-id="3fdb0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fdb0-117">CommonParameters</span></span>
<span data-ttu-id="3fdb0-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fdb0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fdb0-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fdb0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fdb0-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3fdb0-120">INPUTS</span></span>

## <span data-ttu-id="3fdb0-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3fdb0-121">OUTPUTS</span></span>

## <span data-ttu-id="3fdb0-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3fdb0-122">NOTES</span></span>

## <span data-ttu-id="3fdb0-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3fdb0-123">RELATED LINKS</span></span>

