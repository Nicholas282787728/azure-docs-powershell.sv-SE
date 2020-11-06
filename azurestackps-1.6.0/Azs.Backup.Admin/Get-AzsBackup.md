---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb306ed03cb9ab1f06209345474b2ef196d9e1d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572287"
---
# <span data-ttu-id="45fa6-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="45fa6-101">Get-AzsBackup</span></span>

## <span data-ttu-id="45fa6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45fa6-102">SYNOPSIS</span></span>
<span data-ttu-id="45fa6-103">Returnerar en säkerhets kopia från en plats baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="45fa6-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="45fa6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45fa6-104">SYNTAX</span></span>

### <span data-ttu-id="45fa6-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="45fa6-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="45fa6-106">Lära</span><span class="sxs-lookup"><span data-stu-id="45fa6-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="45fa6-107">ID</span><span class="sxs-lookup"><span data-stu-id="45fa6-107">ResourceId</span></span>
```
Get-AzsBackup -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="45fa6-108">ParentResource</span><span class="sxs-lookup"><span data-stu-id="45fa6-108">ParentResource</span></span>
```
Get-AzsBackup -ParentResource <BackupLocation> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="45fa6-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45fa6-109">DESCRIPTION</span></span>
<span data-ttu-id="45fa6-110">Returnerar en säkerhets kopia från en plats baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="45fa6-110">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="45fa6-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45fa6-111">EXAMPLES</span></span>

### <span data-ttu-id="45fa6-112">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="45fa6-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackup
```

<span data-ttu-id="45fa6-113">Få information om alla säkerhets kopior av Azure-stacken.</span><span class="sxs-lookup"><span data-stu-id="45fa6-113">Get information about all Azure Stack backups.</span></span>

### <span data-ttu-id="45fa6-114">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="45fa6-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsBackup -Name 'backupName'
```

<span data-ttu-id="45fa6-115">Få information för den angivna Azure-stacken.</span><span class="sxs-lookup"><span data-stu-id="45fa6-115">Get information for the specified Azure Stack backup.</span></span>

## <span data-ttu-id="45fa6-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45fa6-116">PARAMETERS</span></span>

### <span data-ttu-id="45fa6-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="45fa6-117">-Location</span></span>
<span data-ttu-id="45fa6-118">Plats har säkerhetskopierats.</span><span class="sxs-lookup"><span data-stu-id="45fa6-118">Location backed up.</span></span>

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

### <span data-ttu-id="45fa6-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="45fa6-119">-Name</span></span>
<span data-ttu-id="45fa6-120">Namn på säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="45fa6-120">Name of the backup.</span></span>

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

### <span data-ttu-id="45fa6-121">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="45fa6-121">-ParentResource</span></span>
<span data-ttu-id="45fa6-122">Om du överför en plats för säkerhets kopior returneras listan över alla säkerhets kopior på den platsen.</span><span class="sxs-lookup"><span data-stu-id="45fa6-122">Passing a backup location will return the list of all backups at that backup location.</span></span>

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

### <span data-ttu-id="45fa6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45fa6-123">-ResourceGroupName</span></span>
<span data-ttu-id="45fa6-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="45fa6-124">Name of the resource group.</span></span>

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

### <span data-ttu-id="45fa6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45fa6-125">-ResourceId</span></span>
<span data-ttu-id="45fa6-126">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="45fa6-126">The resource id.</span></span>

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

### <span data-ttu-id="45fa6-127">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="45fa6-127">-Skip</span></span>
<span data-ttu-id="45fa6-128">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="45fa6-128">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="45fa6-129">-Överst</span><span class="sxs-lookup"><span data-stu-id="45fa6-129">-Top</span></span>
<span data-ttu-id="45fa6-130">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="45fa6-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="45fa6-131">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="45fa6-131">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="45fa6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45fa6-132">CommonParameters</span></span>
<span data-ttu-id="45fa6-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45fa6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45fa6-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45fa6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45fa6-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45fa6-135">INPUTS</span></span>

## <span data-ttu-id="45fa6-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45fa6-136">OUTPUTS</span></span>

### <span data-ttu-id="45fa6-137">Microsoft. AzureStack. Management. backup. admin. Models. backup</span><span class="sxs-lookup"><span data-stu-id="45fa6-137">Microsoft.AzureStack.Management.Backup.Admin.Models.Backup</span></span>

## <span data-ttu-id="45fa6-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45fa6-138">NOTES</span></span>

## <span data-ttu-id="45fa6-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45fa6-139">RELATED LINKS</span></span>

