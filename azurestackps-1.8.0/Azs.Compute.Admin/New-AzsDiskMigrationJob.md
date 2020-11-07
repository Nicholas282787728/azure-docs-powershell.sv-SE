---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: db6eff0b0b0e0698c42dd7905cd3e5f7879345e1
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921402"
---
# <span data-ttu-id="6a63b-101">New-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="6a63b-101">New-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="6a63b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6a63b-102">SYNOPSIS</span></span>
<span data-ttu-id="6a63b-103">Startar ett migreringsjobb med hanterade diskar för att migrera hanterade diskar till angiven mål resurs.</span><span class="sxs-lookup"><span data-stu-id="6a63b-103">Starts a managed disk migration job to migrate managed disks to the specified destination share.</span></span>

## <span data-ttu-id="6a63b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6a63b-104">SYNTAX</span></span>

```
New-AzsDiskMigrationJob [-Disks] <Disk[]> [-TargetShare] <String> [[-Location] <String>] [-Name] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="6a63b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6a63b-105">DESCRIPTION</span></span>
<span data-ttu-id="6a63b-106">Skapa ett migreringsjobb.</span><span class="sxs-lookup"><span data-stu-id="6a63b-106">Create a disk migration job.</span></span>

## <span data-ttu-id="6a63b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6a63b-107">EXAMPLES</span></span>

### <span data-ttu-id="6a63b-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6a63b-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsDiskMigrationJob -Name "MyMigrationJob" -Disks $disks -location local -TargetShare "\\SU1FileServer.azurestack.local\SU1_ObjStore"
```

<span data-ttu-id="6a63b-109">Starta ett migreringsarkiv för de första 20 diskarna</span><span class="sxs-lookup"><span data-stu-id="6a63b-109">Start a managed disk migration job for the first 20 disks</span></span>

## <span data-ttu-id="6a63b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6a63b-110">PARAMETERS</span></span>

### <span data-ttu-id="6a63b-111">-Diskar</span><span class="sxs-lookup"><span data-stu-id="6a63b-111">-Disks</span></span>
<span data-ttu-id="6a63b-112">Parametrar för disk lista.</span><span class="sxs-lookup"><span data-stu-id="6a63b-112">The parameters of disk list.</span></span>

```yaml
Type: Disk[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a63b-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="6a63b-113">-Location</span></span>
<span data-ttu-id="6a63b-114">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="6a63b-114">Location of the resource.</span></span>

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

### <span data-ttu-id="6a63b-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="6a63b-115">-Name</span></span>
<span data-ttu-id="6a63b-116">GUID-namnet för migreringen.</span><span class="sxs-lookup"><span data-stu-id="6a63b-116">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MigrationId

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a63b-117">-TargetShare</span><span class="sxs-lookup"><span data-stu-id="6a63b-117">-TargetShare</span></span>
<span data-ttu-id="6a63b-118">Namnet på mål resursen.</span><span class="sxs-lookup"><span data-stu-id="6a63b-118">The target share name.</span></span>

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

### <span data-ttu-id="6a63b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a63b-119">CommonParameters</span></span>
<span data-ttu-id="6a63b-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a63b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a63b-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a63b-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a63b-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6a63b-122">INPUTS</span></span>

## <span data-ttu-id="6a63b-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6a63b-123">OUTPUTS</span></span>

### <span data-ttu-id="6a63b-124">Microsoft. AzureStack. Management. Compute. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="6a63b-124">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="6a63b-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6a63b-125">NOTES</span></span>

## <span data-ttu-id="6a63b-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6a63b-126">RELATED LINKS</span></span>

