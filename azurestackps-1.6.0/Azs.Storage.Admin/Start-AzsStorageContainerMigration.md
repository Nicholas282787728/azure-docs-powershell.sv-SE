---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54016a200b4304c7e37777202a8450fc9ad10e1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743553"
---
# <span data-ttu-id="99fd9-101">Start-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="99fd9-101">Start-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="99fd9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="99fd9-102">SYNOPSIS</span></span>
<span data-ttu-id="99fd9-103">Startar ett migreringsjobb för container för att migrera behållare till angiven destinations delning.</span><span class="sxs-lookup"><span data-stu-id="99fd9-103">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="99fd9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="99fd9-104">SYNTAX</span></span>

```
Start-AzsStorageContainerMigration [-StorageAccountName] <String> [-Name] <String> [-ShareName] <String>
 [[-ResourceGroupName] <String>] [-FarmName] <String> [-DestinationShareUncPath] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99fd9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="99fd9-105">DESCRIPTION</span></span>
<span data-ttu-id="99fd9-106">Startar ett migreringsjobb för container för att migrera behållare till angiven destinations delning.</span><span class="sxs-lookup"><span data-stu-id="99fd9-106">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="99fd9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="99fd9-107">EXAMPLES</span></span>

### <span data-ttu-id="99fd9-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="99fd9-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsStorageContainerMigration -StorageAccountName "accountTest" -Name "containerTest" -ShareName "shareTest" -FarmName "10e8d576-d73c-454c-a40a-aee31a77a5f0" -DestinationShareUncPath "\\***.***.***.***\C$\Test"
```

<span data-ttu-id="99fd9-109">Startar en container-migrering.</span><span class="sxs-lookup"><span data-stu-id="99fd9-109">Starts a container migration.</span></span>

## <span data-ttu-id="99fd9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="99fd9-110">PARAMETERS</span></span>

### <span data-ttu-id="99fd9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99fd9-111">-AsJob</span></span>
<span data-ttu-id="99fd9-112">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="99fd9-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="99fd9-113">-DestinationShareUncPath</span><span class="sxs-lookup"><span data-stu-id="99fd9-113">-DestinationShareUncPath</span></span>
<span data-ttu-id="99fd9-114">UNC-sökvägen för mål resursen för migrering.</span><span class="sxs-lookup"><span data-stu-id="99fd9-114">The UNC path of the destination share for migration.</span></span>

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

### <span data-ttu-id="99fd9-115">-FarmName</span><span class="sxs-lookup"><span data-stu-id="99fd9-115">-FarmName</span></span>
<span data-ttu-id="99fd9-116">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="99fd9-116">Farm Id.</span></span>

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

### <span data-ttu-id="99fd9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="99fd9-117">-Force</span></span>
<span data-ttu-id="99fd9-118">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="99fd9-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="99fd9-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="99fd9-119">-Name</span></span>
<span data-ttu-id="99fd9-120">Namnet på den behållare som ska migreras.</span><span class="sxs-lookup"><span data-stu-id="99fd9-120">The name of the container to be migrated.</span></span>

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

### <span data-ttu-id="99fd9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99fd9-121">-ResourceGroupName</span></span>
<span data-ttu-id="99fd9-122">Namnet på resurs gruppen där lagringsprovidern registrerades under.</span><span class="sxs-lookup"><span data-stu-id="99fd9-122">The resource group name in which the storage resource provider was registered under.</span></span>

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

### <span data-ttu-id="99fd9-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="99fd9-123">-ShareName</span></span>
<span data-ttu-id="99fd9-124">Namn på resursen som innehåller behållaren som angetts för migrering.</span><span class="sxs-lookup"><span data-stu-id="99fd9-124">Name of the share containing the container specified for migration.</span></span>

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

### <span data-ttu-id="99fd9-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="99fd9-125">-StorageAccountName</span></span>
<span data-ttu-id="99fd9-126">Namnet på lagrings kontot där behållaren hittas.</span><span class="sxs-lookup"><span data-stu-id="99fd9-126">The name of storage account where the container locates.</span></span>

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

### <span data-ttu-id="99fd9-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="99fd9-127">-Confirm</span></span>
<span data-ttu-id="99fd9-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="99fd9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99fd9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99fd9-129">-WhatIf</span></span>
<span data-ttu-id="99fd9-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="99fd9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99fd9-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="99fd9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99fd9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99fd9-132">CommonParameters</span></span>
<span data-ttu-id="99fd9-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99fd9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99fd9-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99fd9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99fd9-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="99fd9-135">INPUTS</span></span>

## <span data-ttu-id="99fd9-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="99fd9-136">OUTPUTS</span></span>

## <span data-ttu-id="99fd9-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="99fd9-137">NOTES</span></span>

## <span data-ttu-id="99fd9-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="99fd9-138">RELATED LINKS</span></span>

