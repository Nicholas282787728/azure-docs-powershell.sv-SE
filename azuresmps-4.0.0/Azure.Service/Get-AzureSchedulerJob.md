---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8EED9813-5106-4D6C-B869-97BCBD7845AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67e354616161ad7f2d2467a37b92c355c7c8c39e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099541"
---
# <span data-ttu-id="15270-101">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="15270-101">Get-AzureSchedulerJob</span></span>

## <span data-ttu-id="15270-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="15270-102">SYNOPSIS</span></span>
<span data-ttu-id="15270-103">Hämtar en lista över jobb i schemaläggare eller ett visst jobb i Schemaläggaren.</span><span class="sxs-lookup"><span data-stu-id="15270-103">Gets a list of scheduler jobs or a particular scheduler job.</span></span>

## <span data-ttu-id="15270-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="15270-104">SYNTAX</span></span>

```
Get-AzureSchedulerJob -Location <String> -JobCollectionName <String> [-JobName <String>] [-JobState <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="15270-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="15270-105">DESCRIPTION</span></span>
<span data-ttu-id="15270-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="15270-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="15270-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="15270-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="15270-108">Cmdleten **Get-AzureSchedulerJobCollection** hämtar en lista över jobb i schemaläggare eller ett visst jobb i Schemaläggaren.</span><span class="sxs-lookup"><span data-stu-id="15270-108">The **Get-AzureSchedulerJobCollection** cmdlet gets a list of scheduler jobs or a particular scheduler job.</span></span>

## <span data-ttu-id="15270-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="15270-109">EXAMPLES</span></span>

### <span data-ttu-id="15270-110">Exempel 1: Hämta alla jobb i en samling</span><span class="sxs-lookup"><span data-stu-id="15270-110">Example 1: Get all jobs in a collection</span></span>
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="15270-111">Det här kommandot hämtar schema jobb som är en del av jobb samlingen med namnet JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="15270-111">This command gets scheduler jobs that are part of the job collection named JobCollection01.</span></span>

### <span data-ttu-id="15270-112">Exempel 2: Hämta ett namngivet jobb</span><span class="sxs-lookup"><span data-stu-id="15270-112">Example 2: Get a named job</span></span>
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

<span data-ttu-id="15270-113">Det här kommandot får jobbet med namnet Job01 från samlingen med namnet JobCollection01 på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="15270-113">This command gets the job named Job01 from the collection named JobCollection01 in the specified location.</span></span>

### <span data-ttu-id="15270-114">Exempel 3: komma igång med jobb i en samling</span><span class="sxs-lookup"><span data-stu-id="15270-114">Example 3: Get disabled jobs in a collection</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -JobState "Disabled"
```

<span data-ttu-id="15270-115">Det här kommandot får alla inaktiverade schemaläggnings jobb som ingår i JobCollection01 på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="15270-115">This command gets all disabled scheduler jobs that are part of JobCollection01 in the specified location.</span></span>

## <span data-ttu-id="15270-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="15270-116">PARAMETERS</span></span>

### <span data-ttu-id="15270-117">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="15270-117">-JobCollectionName</span></span>
<span data-ttu-id="15270-118">Anger namnet på den mängd som innehåller Schemaläggaren-jobbet som ska visas.</span><span class="sxs-lookup"><span data-stu-id="15270-118">Specifies the name of the collection that contains the scheduler job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15270-119">-JobName</span><span class="sxs-lookup"><span data-stu-id="15270-119">-JobName</span></span>
<span data-ttu-id="15270-120">Anger namnet på ett jobb i Schemaläggaren som ska visas.</span><span class="sxs-lookup"><span data-stu-id="15270-120">Specifies the name of a scheduler job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15270-121">-JobState</span><span class="sxs-lookup"><span data-stu-id="15270-121">-JobState</span></span>
<span data-ttu-id="15270-122">Anger tillståndet för de jobb du vill få.</span><span class="sxs-lookup"><span data-stu-id="15270-122">Specifies the state of scheduler jobs to get.</span></span>
<span data-ttu-id="15270-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="15270-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="15270-124">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="15270-124">Enabled</span></span>
- <span data-ttu-id="15270-125">Aktiv</span><span class="sxs-lookup"><span data-stu-id="15270-125">Disabled</span></span>
- <span data-ttu-id="15270-126">Fel</span><span class="sxs-lookup"><span data-stu-id="15270-126">Faulted</span></span>
- <span data-ttu-id="15270-127">Rätta</span><span class="sxs-lookup"><span data-stu-id="15270-127">Completed</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15270-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="15270-128">-Location</span></span>
<span data-ttu-id="15270-129">Anger namnet på platsen där moln tjänsten är värd.</span><span class="sxs-lookup"><span data-stu-id="15270-129">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="15270-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="15270-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="15270-131">Världen över</span><span class="sxs-lookup"><span data-stu-id="15270-131">Anywhere Asia</span></span>
- <span data-ttu-id="15270-132">Överallt i Europa</span><span class="sxs-lookup"><span data-stu-id="15270-132">Anywhere Europe</span></span>
- <span data-ttu-id="15270-133">Var du än är</span><span class="sxs-lookup"><span data-stu-id="15270-133">Anywhere US</span></span>
- <span data-ttu-id="15270-134">Östasien</span><span class="sxs-lookup"><span data-stu-id="15270-134">East Asia</span></span>
- <span data-ttu-id="15270-135">Östra USA</span><span class="sxs-lookup"><span data-stu-id="15270-135">East US</span></span>
- <span data-ttu-id="15270-136">Norra Central USA</span><span class="sxs-lookup"><span data-stu-id="15270-136">North Central US</span></span>
- <span data-ttu-id="15270-137">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="15270-137">North Europe</span></span>
- <span data-ttu-id="15270-138">Södra centrala USA</span><span class="sxs-lookup"><span data-stu-id="15270-138">South Central US</span></span>
- <span data-ttu-id="15270-139">Sydostasien</span><span class="sxs-lookup"><span data-stu-id="15270-139">Southeast Asia</span></span>
- <span data-ttu-id="15270-140">Västeuropa</span><span class="sxs-lookup"><span data-stu-id="15270-140">West Europe</span></span>
- <span data-ttu-id="15270-141">Västra USA</span><span class="sxs-lookup"><span data-stu-id="15270-141">West US</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15270-142">-Profil</span><span class="sxs-lookup"><span data-stu-id="15270-142">-Profile</span></span>
<span data-ttu-id="15270-143">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="15270-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="15270-144">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="15270-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15270-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15270-145">CommonParameters</span></span>
<span data-ttu-id="15270-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15270-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15270-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15270-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15270-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="15270-148">INPUTS</span></span>

## <span data-ttu-id="15270-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="15270-149">OUTPUTS</span></span>

## <span data-ttu-id="15270-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="15270-150">NOTES</span></span>

## <span data-ttu-id="15270-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="15270-151">RELATED LINKS</span></span>

[<span data-ttu-id="15270-152">Remove-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="15270-152">Remove-AzureSchedulerJob</span></span>](./Remove-AzureSchedulerJob.md)


