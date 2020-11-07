---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b51280387ad3eb29f05bee8876765a621e0d07c4
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921549"
---
# <span data-ttu-id="e0742-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="e0742-101">Get-AzsBackup</span></span>

## <span data-ttu-id="e0742-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0742-102">SYNOPSIS</span></span>
<span data-ttu-id="e0742-103">Returnerar en säkerhets kopia från en plats baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="e0742-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="e0742-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0742-104">SYNTAX</span></span>

### <span data-ttu-id="e0742-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="e0742-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0742-106">Lära</span><span class="sxs-lookup"><span data-stu-id="e0742-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="e0742-107">ID</span><span class="sxs-lookup"><span data-stu-id="e0742-107">ResourceId</span></span>
```
Get-AzsBackup -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="e0742-108">ParentResource</span><span class="sxs-lookup"><span data-stu-id="e0742-108">ParentResource</span></span>
```
Get-AzsBackup -ParentResource <BackupLocation> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="e0742-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0742-109">DESCRIPTION</span></span>
<span data-ttu-id="e0742-110">Returnerar en säkerhets kopia från en plats baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="e0742-110">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="e0742-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0742-111">EXAMPLES</span></span>

### <span data-ttu-id="e0742-112">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e0742-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackup
```

<span data-ttu-id="e0742-113">Få information sbout alla säkerhets kopior av Azure-stacken.</span><span class="sxs-lookup"><span data-stu-id="e0742-113">Get information sbout all Azure Stack backups.</span></span>

### <span data-ttu-id="e0742-114">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e0742-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsBackup -Name 'backupName'
```

<span data-ttu-id="e0742-115">Få information för den angivna Azure-stacken.</span><span class="sxs-lookup"><span data-stu-id="e0742-115">Get information for the the specified Azure Stack backup.</span></span>

## <span data-ttu-id="e0742-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0742-116">PARAMETERS</span></span>

### <span data-ttu-id="e0742-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="e0742-117">-Location</span></span>
<span data-ttu-id="e0742-118">Plats har säkerhetskopierats.</span><span class="sxs-lookup"><span data-stu-id="e0742-118">Location backed up.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0742-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="e0742-119">-Name</span></span>
<span data-ttu-id="e0742-120">Namn på säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="e0742-120">Name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0742-121">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="e0742-121">-ParentResource</span></span>
<span data-ttu-id="e0742-122">Om du överför en plats för säkerhets kopior returneras listan över alla säkerhets kopior på den platsen.</span><span class="sxs-lookup"><span data-stu-id="e0742-122">Passing a backup location will return the list of all backups at that backup location.</span></span>

```yaml
Type: BackupLocation
Parameter Sets: ParentResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0742-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0742-123">-ResourceGroupName</span></span>
<span data-ttu-id="e0742-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e0742-124">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0742-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0742-125">-ResourceId</span></span>
<span data-ttu-id="e0742-126">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="e0742-126">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0742-127">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="e0742-127">-Skip</span></span>
<span data-ttu-id="e0742-128">{{Fill Skip Description}}</span><span class="sxs-lookup"><span data-stu-id="e0742-128">{{Fill Skip Description}}</span></span>

```yaml
Type: Int32
Parameter Sets: List, ParentResource
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0742-129">-Överst</span><span class="sxs-lookup"><span data-stu-id="e0742-129">-Top</span></span>
<span data-ttu-id="e0742-130">{{Fill Top Description}}</span><span class="sxs-lookup"><span data-stu-id="e0742-130">{{Fill Top Description}}</span></span>

```yaml
Type: Int32
Parameter Sets: List, ParentResource
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0742-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0742-131">CommonParameters</span></span>
<span data-ttu-id="e0742-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0742-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0742-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0742-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0742-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0742-134">INPUTS</span></span>

## <span data-ttu-id="e0742-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0742-135">OUTPUTS</span></span>

### <span data-ttu-id="e0742-136">Microsoft. AzureStack. Management. backup. admin. Models. backup</span><span class="sxs-lookup"><span data-stu-id="e0742-136">Microsoft.AzureStack.Management.Backup.Admin.Models.Backup</span></span>

## <span data-ttu-id="e0742-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0742-137">NOTES</span></span>

## <span data-ttu-id="e0742-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0742-138">RELATED LINKS</span></span>

