---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af9c5d2c5ebb547a6e09d2e4f4302ed2da470a39
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921759"
---
# <span data-ttu-id="20b1e-101">Start-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="20b1e-101">Start-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="20b1e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20b1e-102">SYNOPSIS</span></span>
<span data-ttu-id="20b1e-103">Startar ett migreringsjobb för container för att migrera behållare till angiven destinations delning.</span><span class="sxs-lookup"><span data-stu-id="20b1e-103">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="20b1e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20b1e-104">SYNTAX</span></span>

```
Start-AzsStorageContainerMigration [-StorageAccountName] <String> [-ContainerName] <String>
 [-ShareName] <String> [[-ResourceGroupName] <String>] [-FarmName] <String> [-DestinationShareUncPath] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20b1e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20b1e-105">DESCRIPTION</span></span>
<span data-ttu-id="20b1e-106">Startar ett migreringsjobb för container för att migrera behållare till angiven destinations delning.</span><span class="sxs-lookup"><span data-stu-id="20b1e-106">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="20b1e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20b1e-107">EXAMPLES</span></span>

### <span data-ttu-id="20b1e-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="20b1e-108">EXAMPLE 1</span></span>
```
Start-AzsStorageContainerMigration -StorageAccountName "accountTest" -ContainerName "containerTest" -ShareName "shareTest" -FarmName "10e8d576-d73c-454c-a40a-aee31a77a5f0" -DestinationShareUncPath "\\***.***.***.***\C$\Test"
```

<span data-ttu-id="20b1e-109">Startar en container-migrering.</span><span class="sxs-lookup"><span data-stu-id="20b1e-109">Starts a container migration.</span></span>

## <span data-ttu-id="20b1e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20b1e-110">PARAMETERS</span></span>

### <span data-ttu-id="20b1e-111">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="20b1e-111">-StorageAccountName</span></span>
<span data-ttu-id="20b1e-112">Namnet på lagrings kontot där behållaren hittas.</span><span class="sxs-lookup"><span data-stu-id="20b1e-112">The name of storage account where the container locates.</span></span>

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

### <span data-ttu-id="20b1e-113">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="20b1e-113">-ContainerName</span></span>
<span data-ttu-id="20b1e-114">Namnet på den behållare som ska migreras.</span><span class="sxs-lookup"><span data-stu-id="20b1e-114">The name of the container to be migrated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20b1e-115">-ShareName</span><span class="sxs-lookup"><span data-stu-id="20b1e-115">-ShareName</span></span>
<span data-ttu-id="20b1e-116">Namn på resursen som innehåller behållaren som angetts för migrering.</span><span class="sxs-lookup"><span data-stu-id="20b1e-116">Name of the share containing the container specified for migration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20b1e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20b1e-117">-ResourceGroupName</span></span>
<span data-ttu-id="20b1e-118">Namnet på resurs gruppen där lagringsprovidern registrerades under.</span><span class="sxs-lookup"><span data-stu-id="20b1e-118">The resource group name in which the storage resource provider was registered under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20b1e-119">-FarmName</span><span class="sxs-lookup"><span data-stu-id="20b1e-119">-FarmName</span></span>
<span data-ttu-id="20b1e-120">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="20b1e-120">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20b1e-121">-DestinationShareUncPath</span><span class="sxs-lookup"><span data-stu-id="20b1e-121">-DestinationShareUncPath</span></span>
<span data-ttu-id="20b1e-122">UNC-sökvägen för mål resursen för migrering.</span><span class="sxs-lookup"><span data-stu-id="20b1e-122">The UNC path of the destination share for migration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20b1e-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20b1e-123">-AsJob</span></span>
<span data-ttu-id="20b1e-124">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="20b1e-124">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20b1e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="20b1e-125">-Force</span></span>
<span data-ttu-id="20b1e-126">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="20b1e-126">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20b1e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20b1e-127">-WhatIf</span></span>
<span data-ttu-id="20b1e-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="20b1e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20b1e-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="20b1e-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20b1e-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="20b1e-130">-Confirm</span></span>
<span data-ttu-id="20b1e-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="20b1e-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20b1e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20b1e-132">CommonParameters</span></span>
<span data-ttu-id="20b1e-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20b1e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20b1e-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20b1e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20b1e-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20b1e-135">INPUTS</span></span>

## <span data-ttu-id="20b1e-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20b1e-136">OUTPUTS</span></span>

## <span data-ttu-id="20b1e-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20b1e-137">NOTES</span></span>

## <span data-ttu-id="20b1e-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20b1e-138">RELATED LINKS</span></span>
