---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee1a9ae5a4d5ef7545ee9a3e071fcc06475034f4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100009"
---
# <span data-ttu-id="e5527-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="e5527-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="e5527-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e5527-102">SYNOPSIS</span></span>
<span data-ttu-id="e5527-103">Avbryta ett migreringsarkiv för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="e5527-103">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="e5527-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e5527-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob [[-Location] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="e5527-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e5527-105">DESCRIPTION</span></span>
<span data-ttu-id="e5527-106">Avbryta ett migreringsjobb.</span><span class="sxs-lookup"><span data-stu-id="e5527-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="e5527-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e5527-107">EXAMPLES</span></span>

### <span data-ttu-id="e5527-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e5527-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsDiskMigrationJob -Location local -MigrationId $migration.MigrationId
```

<span data-ttu-id="e5527-109">Avbryta ett migreringsarkiv för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="e5527-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="e5527-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e5527-110">PARAMETERS</span></span>

### <span data-ttu-id="e5527-111">-Plats</span><span class="sxs-lookup"><span data-stu-id="e5527-111">-Location</span></span>
<span data-ttu-id="e5527-112">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="e5527-112">Location of the resource.</span></span>

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

### <span data-ttu-id="e5527-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="e5527-113">-Name</span></span>
<span data-ttu-id="e5527-114">GUID-namnet för migreringen.</span><span class="sxs-lookup"><span data-stu-id="e5527-114">The migration job guid name.</span></span>

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

### <span data-ttu-id="e5527-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5527-115">CommonParameters</span></span>
<span data-ttu-id="e5527-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5527-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5527-117">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5527-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5527-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e5527-118">INPUTS</span></span>

## <span data-ttu-id="e5527-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e5527-119">OUTPUTS</span></span>

### <span data-ttu-id="e5527-120">Microsoft. AzureStack. Management. Compute. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="e5527-120">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="e5527-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e5527-121">NOTES</span></span>

## <span data-ttu-id="e5527-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e5527-122">RELATED LINKS</span></span>

