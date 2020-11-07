---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee1a9ae5a4d5ef7545ee9a3e071fcc06475034f4
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921390"
---
# <span data-ttu-id="6f6d9-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="6f6d9-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="6f6d9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f6d9-102">SYNOPSIS</span></span>
<span data-ttu-id="6f6d9-103">Avbryta ett migreringsarkiv för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="6f6d9-103">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="6f6d9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f6d9-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob [[-Location] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="6f6d9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f6d9-105">DESCRIPTION</span></span>
<span data-ttu-id="6f6d9-106">Avbryta ett migreringsjobb.</span><span class="sxs-lookup"><span data-stu-id="6f6d9-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="6f6d9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f6d9-107">EXAMPLES</span></span>

### <span data-ttu-id="6f6d9-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6f6d9-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsDiskMigrationJob -Location local -MigrationId $migration.MigrationId
```

<span data-ttu-id="6f6d9-109">Avbryta ett migreringsarkiv för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="6f6d9-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="6f6d9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f6d9-110">PARAMETERS</span></span>

### <span data-ttu-id="6f6d9-111">-Plats</span><span class="sxs-lookup"><span data-stu-id="6f6d9-111">-Location</span></span>
<span data-ttu-id="6f6d9-112">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="6f6d9-112">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6d9-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="6f6d9-113">-Name</span></span>
<span data-ttu-id="6f6d9-114">GUID-namnet för migreringen.</span><span class="sxs-lookup"><span data-stu-id="6f6d9-114">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MigrationId

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6d9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f6d9-115">CommonParameters</span></span>
<span data-ttu-id="6f6d9-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f6d9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f6d9-117">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f6d9-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f6d9-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f6d9-118">INPUTS</span></span>

## <span data-ttu-id="6f6d9-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f6d9-119">OUTPUTS</span></span>

### <span data-ttu-id="6f6d9-120">Microsoft. AzureStack. Management. Compute. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="6f6d9-120">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="6f6d9-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f6d9-121">NOTES</span></span>

## <span data-ttu-id="6f6d9-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f6d9-122">RELATED LINKS</span></span>

