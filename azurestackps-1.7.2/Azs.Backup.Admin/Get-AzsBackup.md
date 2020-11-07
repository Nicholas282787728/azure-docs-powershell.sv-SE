---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 364b22c834ae7476e64f972b289e20d3caa5ba80
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920959"
---
# <span data-ttu-id="74507-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="74507-101">Get-AzsBackup</span></span>

## <span data-ttu-id="74507-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="74507-102">SYNOPSIS</span></span>
<span data-ttu-id="74507-103">Returnerar en säkerhets kopia från en plats baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="74507-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="74507-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="74507-104">SYNTAX</span></span>

### <span data-ttu-id="74507-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="74507-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="74507-106">Lära</span><span class="sxs-lookup"><span data-stu-id="74507-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="74507-107">ID</span><span class="sxs-lookup"><span data-stu-id="74507-107">ResourceId</span></span>
```
Get-AzsBackup -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="74507-108">ParentResource</span><span class="sxs-lookup"><span data-stu-id="74507-108">ParentResource</span></span>
```
Get-AzsBackup -ParentResource <BackupLocation> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="74507-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="74507-109">DESCRIPTION</span></span>
<span data-ttu-id="74507-110">Returnerar en säkerhets kopia från en plats baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="74507-110">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="74507-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="74507-111">EXAMPLES</span></span>

### <span data-ttu-id="74507-112">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="74507-112">EXAMPLE 1</span></span>
```
Get-AzsBackup
```

<span data-ttu-id="74507-113">Få information om alla säkerhets kopior av Azure-stacken.</span><span class="sxs-lookup"><span data-stu-id="74507-113">Get information about all Azure Stack backups.</span></span>

### <span data-ttu-id="74507-114">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="74507-114">EXAMPLE 2</span></span>
```
Get-AzsBackup -Name 'backupName'
```

<span data-ttu-id="74507-115">Få information för den angivna Azure-stacken.</span><span class="sxs-lookup"><span data-stu-id="74507-115">Get information for the specified Azure Stack backup.</span></span>

## <span data-ttu-id="74507-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="74507-116">PARAMETERS</span></span>

### <span data-ttu-id="74507-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="74507-117">-Location</span></span>
<span data-ttu-id="74507-118">Plats har säkerhetskopierats.</span><span class="sxs-lookup"><span data-stu-id="74507-118">Location backed up.</span></span>

```yaml
Type: System.String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74507-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="74507-119">-Name</span></span>
<span data-ttu-id="74507-120">Namn på säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="74507-120">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74507-121">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="74507-121">-ParentResource</span></span>
<span data-ttu-id="74507-122">Om du överför en plats för säkerhets kopior returneras listan över alla säkerhets kopior på den platsen.</span><span class="sxs-lookup"><span data-stu-id="74507-122">Passing a backup location will return the list of all backups at that backup location.</span></span>

```yaml
Type: Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation
Parameter Sets: ParentResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74507-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74507-123">-ResourceGroupName</span></span>
<span data-ttu-id="74507-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="74507-124">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74507-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74507-125">-ResourceId</span></span>
<span data-ttu-id="74507-126">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="74507-126">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74507-127">-Överst</span><span class="sxs-lookup"><span data-stu-id="74507-127">-Top</span></span>
<span data-ttu-id="74507-128">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="74507-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="74507-129">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="74507-129">Applies after the -Skip parameter.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, ParentResource
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74507-130">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="74507-130">-Skip</span></span>
<span data-ttu-id="74507-131">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="74507-131">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, ParentResource
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74507-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74507-132">CommonParameters</span></span>
<span data-ttu-id="74507-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74507-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74507-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74507-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74507-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="74507-135">INPUTS</span></span>

## <span data-ttu-id="74507-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="74507-136">OUTPUTS</span></span>

### <span data-ttu-id="74507-137">Microsoft. AzureStack. Management. backup. admin. Models. backup</span><span class="sxs-lookup"><span data-stu-id="74507-137">Microsoft.AzureStack.Management.Backup.Admin.Models.Backup</span></span>

## <span data-ttu-id="74507-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="74507-138">NOTES</span></span>

## <span data-ttu-id="74507-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="74507-139">RELATED LINKS</span></span>
