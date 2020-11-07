---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d38e4bd949a6118f55ce0096a8ca56d08137bb2a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921280"
---
# <span data-ttu-id="4371b-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="4371b-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="4371b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4371b-102">SYNOPSIS</span></span>
<span data-ttu-id="4371b-103">Avbryta ett migreringsarkiv för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="4371b-103">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="4371b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4371b-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob [[-Location] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="4371b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4371b-105">DESCRIPTION</span></span>
<span data-ttu-id="4371b-106">Avbryta ett migreringsjobb.</span><span class="sxs-lookup"><span data-stu-id="4371b-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="4371b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4371b-107">EXAMPLES</span></span>

### <span data-ttu-id="4371b-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4371b-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsDiskMigrationJob -Location local -MigrationId $migration.MigrationId
```

<span data-ttu-id="4371b-109">Avbryta ett migreringsarkiv för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="4371b-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="4371b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4371b-110">PARAMETERS</span></span>

### <span data-ttu-id="4371b-111">-Plats</span><span class="sxs-lookup"><span data-stu-id="4371b-111">-Location</span></span>
<span data-ttu-id="4371b-112">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="4371b-112">Location of the resource.</span></span>

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

### <span data-ttu-id="4371b-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="4371b-113">-Name</span></span>
<span data-ttu-id="4371b-114">GUID-namnet för migreringen.</span><span class="sxs-lookup"><span data-stu-id="4371b-114">The migration job guid name.</span></span>

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

### <span data-ttu-id="4371b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4371b-115">CommonParameters</span></span>
<span data-ttu-id="4371b-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4371b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4371b-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4371b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4371b-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4371b-118">INPUTS</span></span>

## <span data-ttu-id="4371b-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4371b-119">OUTPUTS</span></span>

### <span data-ttu-id="4371b-120">Microsoft. AzureStack. Management. Compute. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="4371b-120">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="4371b-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4371b-121">NOTES</span></span>

## <span data-ttu-id="4371b-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4371b-122">RELATED LINKS</span></span>

