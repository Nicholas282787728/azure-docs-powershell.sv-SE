---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee1a9ae5a4d5ef7545ee9a3e071fcc06475034f4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921724"
---
# <span data-ttu-id="76a76-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="76a76-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="76a76-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="76a76-102">SYNOPSIS</span></span>
<span data-ttu-id="76a76-103">Avbryta ett migreringsarkiv för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="76a76-103">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="76a76-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="76a76-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob [[-Location] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="76a76-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="76a76-105">DESCRIPTION</span></span>
<span data-ttu-id="76a76-106">Avbryta ett migreringsjobb.</span><span class="sxs-lookup"><span data-stu-id="76a76-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="76a76-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="76a76-107">EXAMPLES</span></span>

### <span data-ttu-id="76a76-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="76a76-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsDiskMigrationJob -Location local -MigrationId $migration.MigrationId
```

<span data-ttu-id="76a76-109">Avbryta ett migreringsarkiv för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="76a76-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="76a76-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="76a76-110">PARAMETERS</span></span>

### <span data-ttu-id="76a76-111">-Plats</span><span class="sxs-lookup"><span data-stu-id="76a76-111">-Location</span></span>
<span data-ttu-id="76a76-112">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="76a76-112">Location of the resource.</span></span>

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

### <span data-ttu-id="76a76-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="76a76-113">-Name</span></span>
<span data-ttu-id="76a76-114">GUID-namnet för migreringen.</span><span class="sxs-lookup"><span data-stu-id="76a76-114">The migration job guid name.</span></span>

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

### <span data-ttu-id="76a76-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a76-115">CommonParameters</span></span>
<span data-ttu-id="76a76-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76a76-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a76-117">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76a76-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a76-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="76a76-118">INPUTS</span></span>

## <span data-ttu-id="76a76-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="76a76-119">OUTPUTS</span></span>

### <span data-ttu-id="76a76-120">Microsoft. AzureStack. Management. Compute. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="76a76-120">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="76a76-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="76a76-121">NOTES</span></span>

## <span data-ttu-id="76a76-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="76a76-122">RELATED LINKS</span></span>

