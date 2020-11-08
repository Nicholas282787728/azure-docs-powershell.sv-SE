---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 62c174a3aec5034b230954922f6aab5078fe4bac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919846"
---
# <span data-ttu-id="be9b2-101">Get-AzsQueueService</span><span class="sxs-lookup"><span data-stu-id="be9b2-101">Get-AzsQueueService</span></span>

## <span data-ttu-id="be9b2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="be9b2-102">SYNOPSIS</span></span>
<span data-ttu-id="be9b2-103">Returnerar kötjänsten.</span><span class="sxs-lookup"><span data-stu-id="be9b2-103">Returns the queue service.</span></span>

## <span data-ttu-id="be9b2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="be9b2-104">SYNTAX</span></span>

```
Get-AzsQueueService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="be9b2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="be9b2-105">DESCRIPTION</span></span>
<span data-ttu-id="be9b2-106">Returnerar kötjänsten.</span><span class="sxs-lookup"><span data-stu-id="be9b2-106">Returns the queue service.</span></span>

## <span data-ttu-id="be9b2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="be9b2-107">EXAMPLES</span></span>

### <span data-ttu-id="be9b2-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="be9b2-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsQueueService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="be9b2-109">Skaffa kötjänsten.</span><span class="sxs-lookup"><span data-stu-id="be9b2-109">Get the queue service.</span></span>

## <span data-ttu-id="be9b2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="be9b2-110">PARAMETERS</span></span>

### <span data-ttu-id="be9b2-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="be9b2-111">-FarmName</span></span>
<span data-ttu-id="be9b2-112">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="be9b2-112">Farm Id.</span></span>

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

### <span data-ttu-id="be9b2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be9b2-113">-ResourceGroupName</span></span>
<span data-ttu-id="be9b2-114">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="be9b2-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be9b2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be9b2-115">CommonParameters</span></span>
<span data-ttu-id="be9b2-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be9b2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be9b2-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be9b2-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be9b2-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="be9b2-118">INPUTS</span></span>

## <span data-ttu-id="be9b2-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="be9b2-119">OUTPUTS</span></span>

### <span data-ttu-id="be9b2-120">Microsoft. AzureStack. Management. Storage. admin. Models. QueueService</span><span class="sxs-lookup"><span data-stu-id="be9b2-120">Microsoft.AzureStack.Management.Storage.Admin.Models.QueueService</span></span>

## <span data-ttu-id="be9b2-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="be9b2-121">NOTES</span></span>

## <span data-ttu-id="be9b2-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="be9b2-122">RELATED LINKS</span></span>
