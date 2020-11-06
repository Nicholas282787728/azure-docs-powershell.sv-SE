---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 47ac85406955592cba566df505900e6c42befb7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571524"
---
# <span data-ttu-id="3f099-101">Get-AzsStorageDestinationShare</span><span class="sxs-lookup"><span data-stu-id="3f099-101">Get-AzsStorageDestinationShare</span></span>

## <span data-ttu-id="3f099-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f099-102">SYNOPSIS</span></span>
<span data-ttu-id="3f099-103">Returnerar en lista med mål resurser som systemet anser som bästa kandidater för migrering.</span><span class="sxs-lookup"><span data-stu-id="3f099-103">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="3f099-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f099-104">SYNTAX</span></span>

```
Get-AzsStorageDestinationShare [-SourceShareName] <String> [-FarmName] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f099-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f099-105">DESCRIPTION</span></span>
<span data-ttu-id="3f099-106">Returnerar en lista med mål resurser som systemet anser som bästa kandidater för migrering.</span><span class="sxs-lookup"><span data-stu-id="3f099-106">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="3f099-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f099-107">EXAMPLES</span></span>

### <span data-ttu-id="3f099-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3f099-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageDestinationShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -SourceShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="3f099-109">Få en lista över mål delar som systemet anser som bästa kandidater för migrering.</span><span class="sxs-lookup"><span data-stu-id="3f099-109">Get a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="3f099-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f099-110">PARAMETERS</span></span>

### <span data-ttu-id="3f099-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="3f099-111">-FarmName</span></span>
<span data-ttu-id="3f099-112">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="3f099-112">Farm Id.</span></span>

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

### <span data-ttu-id="3f099-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f099-113">-ResourceGroupName</span></span>
<span data-ttu-id="3f099-114">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="3f099-114">Resource group name.</span></span>

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

### <span data-ttu-id="3f099-115">-SourceShareName</span><span class="sxs-lookup"><span data-stu-id="3f099-115">-SourceShareName</span></span>
<span data-ttu-id="3f099-116">Namn på resursen som innehåller behållare som ska migreras.</span><span class="sxs-lookup"><span data-stu-id="3f099-116">Name of the share which holds containers to be migrated.</span></span>

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

### <span data-ttu-id="3f099-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f099-117">CommonParameters</span></span>
<span data-ttu-id="3f099-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f099-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f099-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f099-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f099-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f099-120">INPUTS</span></span>

## <span data-ttu-id="3f099-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f099-121">OUTPUTS</span></span>

## <span data-ttu-id="3f099-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f099-122">NOTES</span></span>

## <span data-ttu-id="3f099-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f099-123">RELATED LINKS</span></span>

