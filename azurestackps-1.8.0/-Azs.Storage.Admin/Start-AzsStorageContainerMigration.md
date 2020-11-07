---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54016a200b4304c7e37777202a8450fc9ad10e1e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921417"
---
# <span data-ttu-id="fca69-101">Start-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="fca69-101">Start-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="fca69-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fca69-102">SYNOPSIS</span></span>
<span data-ttu-id="fca69-103">Startar ett migreringsjobb för container för att migrera behållare till angiven destinations delning.</span><span class="sxs-lookup"><span data-stu-id="fca69-103">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="fca69-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fca69-104">SYNTAX</span></span>

```
Start-AzsStorageContainerMigration [-StorageAccountName] <String> [-Name] <String> [-ShareName] <String>
 [[-ResourceGroupName] <String>] [-FarmName] <String> [-DestinationShareUncPath] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fca69-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fca69-105">DESCRIPTION</span></span>
<span data-ttu-id="fca69-106">Startar ett migreringsjobb för container för att migrera behållare till angiven destinations delning.</span><span class="sxs-lookup"><span data-stu-id="fca69-106">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="fca69-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fca69-107">EXAMPLES</span></span>

### <span data-ttu-id="fca69-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fca69-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsStorageContainerMigration -StorageAccountName "accountTest" -Name "containerTest" -ShareName "shareTest" -FarmName "10e8d576-d73c-454c-a40a-aee31a77a5f0" -DestinationShareUncPath "\\***.***.***.***\C$\Test"
```

<span data-ttu-id="fca69-109">Startar en container-migrering.</span><span class="sxs-lookup"><span data-stu-id="fca69-109">Starts a container migration.</span></span>

## <span data-ttu-id="fca69-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fca69-110">PARAMETERS</span></span>

### <span data-ttu-id="fca69-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fca69-111">-AsJob</span></span>
<span data-ttu-id="fca69-112">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="fca69-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="fca69-113">-DestinationShareUncPath</span><span class="sxs-lookup"><span data-stu-id="fca69-113">-DestinationShareUncPath</span></span>
<span data-ttu-id="fca69-114">UNC-sökvägen för mål resursen för migrering.</span><span class="sxs-lookup"><span data-stu-id="fca69-114">The UNC path of the destination share for migration.</span></span>

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

### <span data-ttu-id="fca69-115">-FarmName</span><span class="sxs-lookup"><span data-stu-id="fca69-115">-FarmName</span></span>
<span data-ttu-id="fca69-116">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="fca69-116">Farm Id.</span></span>

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

### <span data-ttu-id="fca69-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fca69-117">-Force</span></span>
<span data-ttu-id="fca69-118">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="fca69-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fca69-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="fca69-119">-Name</span></span>
<span data-ttu-id="fca69-120">Namnet på den behållare som ska migreras.</span><span class="sxs-lookup"><span data-stu-id="fca69-120">The name of the container to be migrated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fca69-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fca69-121">-ResourceGroupName</span></span>
<span data-ttu-id="fca69-122">Namnet på resurs gruppen där lagringsprovidern registrerades under.</span><span class="sxs-lookup"><span data-stu-id="fca69-122">The resource group name in which the storage resource provider was registered under.</span></span>

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

### <span data-ttu-id="fca69-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="fca69-123">-ShareName</span></span>
<span data-ttu-id="fca69-124">Namn på resursen som innehåller behållaren som angetts för migrering.</span><span class="sxs-lookup"><span data-stu-id="fca69-124">Name of the share containing the container specified for migration.</span></span>

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

### <span data-ttu-id="fca69-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fca69-125">-StorageAccountName</span></span>
<span data-ttu-id="fca69-126">Namnet på lagrings kontot där behållaren hittas.</span><span class="sxs-lookup"><span data-stu-id="fca69-126">The name of storage account where the container locates.</span></span>

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

### <span data-ttu-id="fca69-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fca69-127">-Confirm</span></span>
<span data-ttu-id="fca69-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fca69-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fca69-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fca69-129">-WhatIf</span></span>
<span data-ttu-id="fca69-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fca69-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fca69-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fca69-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fca69-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fca69-132">CommonParameters</span></span>
<span data-ttu-id="fca69-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fca69-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fca69-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fca69-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fca69-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fca69-135">INPUTS</span></span>

## <span data-ttu-id="fca69-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fca69-136">OUTPUTS</span></span>

## <span data-ttu-id="fca69-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fca69-137">NOTES</span></span>

## <span data-ttu-id="fca69-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fca69-138">RELATED LINKS</span></span>

