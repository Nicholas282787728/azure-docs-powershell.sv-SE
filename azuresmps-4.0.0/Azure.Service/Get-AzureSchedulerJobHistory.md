---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2BF5BDF8-3743-46FC-8E04-1A4EA920A2AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77b4d184ffbdb1d054f3d14aa3c51c8d2afc928b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099540"
---
# <span data-ttu-id="198a9-101">Get-AzureSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="198a9-101">Get-AzureSchedulerJobHistory</span></span>

## <span data-ttu-id="198a9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="198a9-102">SYNOPSIS</span></span>
<span data-ttu-id="198a9-103">Hämtar historik för ett jobb i schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="198a9-103">Gets history for a scheduler job.</span></span>

## <span data-ttu-id="198a9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="198a9-104">SYNTAX</span></span>

```
Get-AzureSchedulerJobHistory -Location <String> -JobCollectionName <String> -JobName <String>
 [-JobStatus <String>] [-Profile <AzureSMProfile>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="198a9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="198a9-105">DESCRIPTION</span></span>
<span data-ttu-id="198a9-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="198a9-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="198a9-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="198a9-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="198a9-108">Cmdleten **Get-AzureSchedulerJobHistory** hämtar historiken för ett jobb i Schemaläggaren.</span><span class="sxs-lookup"><span data-stu-id="198a9-108">The **Get-AzureSchedulerJobHistory** cmdlet gets the history for a scheduler job.</span></span>

## <span data-ttu-id="198a9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="198a9-109">EXAMPLES</span></span>

### <span data-ttu-id="198a9-110">Exempel 1: Hämta historik för ett jobb med dess namn</span><span class="sxs-lookup"><span data-stu-id="198a9-110">Example 1: Get history for a job by using its name</span></span>
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

<span data-ttu-id="198a9-111">Det här kommandot får historiken för jobbet som heter Job01.</span><span class="sxs-lookup"><span data-stu-id="198a9-111">This command gets the history of the job named Job01.</span></span>
<span data-ttu-id="198a9-112">Jobbet tillhör jobbet JobCollection01 på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="198a9-112">That job belongs to the job collection named JobCollection01 in the specified location.</span></span>

### <span data-ttu-id="198a9-113">Exempel 2: Hämta historik för ett misslyckat jobb med dess namn</span><span class="sxs-lookup"><span data-stu-id="198a9-113">Example 2: Get history for a failed job by using its name</span></span>
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job12" -JobStatus "Failed"
```

<span data-ttu-id="198a9-114">Det här kommandot får historiken för jobbet med namnet Job12 som har statusen Misslyckad.</span><span class="sxs-lookup"><span data-stu-id="198a9-114">This command gets the history of the job named Job12 that has a status of Failed.</span></span>
<span data-ttu-id="198a9-115">Jobbet tillhör jobbet JobCollection01 på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="198a9-115">That job belongs to the job collection named JobCollection01 in the specified location.</span></span>

## <span data-ttu-id="198a9-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="198a9-116">PARAMETERS</span></span>

### <span data-ttu-id="198a9-117">-Först</span><span class="sxs-lookup"><span data-stu-id="198a9-117">-First</span></span>
<span data-ttu-id="198a9-118">Hämtar bara angivet antal objekt.</span><span class="sxs-lookup"><span data-stu-id="198a9-118">Gets only the specified number of objects.</span></span>
<span data-ttu-id="198a9-119">Ange antalet objekt som ska visas.</span><span class="sxs-lookup"><span data-stu-id="198a9-119">Enter the number of objects to get.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="198a9-120">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="198a9-120">-IncludeTotalCount</span></span>
<span data-ttu-id="198a9-121">Rapporterar totalt antal objekt i data uppsättningen (ett heltal) följt av de markerade objekten.</span><span class="sxs-lookup"><span data-stu-id="198a9-121">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="198a9-122">Om cmdleten inte kan bestämma det totala antalet visar den "okänt antal".</span><span class="sxs-lookup"><span data-stu-id="198a9-122">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="198a9-123">Heltalet har en egenskap för exakthet som anger tillförlitligheten hos det totala värdet.</span><span class="sxs-lookup"><span data-stu-id="198a9-123">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="198a9-124">Värdet för precisions intervall från 0,0 till 1,0 där 0,0 innebär att cmdleten inte kan räkna antalet objekt, ger 1,0 att antalet är exakt och ett värde mellan 0,0 och 1,0 tyder på en allt tillförlitlig uppskattning.</span><span class="sxs-lookup"><span data-stu-id="198a9-124">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="198a9-125">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="198a9-125">-JobCollectionName</span></span>
<span data-ttu-id="198a9-126">Anger namnet på en jobb samling i Schemaläggaren.</span><span class="sxs-lookup"><span data-stu-id="198a9-126">Specifies the name of a scheduler job collection.</span></span>
<span data-ttu-id="198a9-127">Denna cmdlet hämtar historiken för ett jobb som tillhör samlingen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="198a9-127">This cmdlet gets the history for a job that belongs to the collection that this parameter specifies.</span></span>

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

### <span data-ttu-id="198a9-128">-JobName</span><span class="sxs-lookup"><span data-stu-id="198a9-128">-JobName</span></span>
<span data-ttu-id="198a9-129">Anger namnet på ett jobb i Schemaläggaren där historiken ska visas.</span><span class="sxs-lookup"><span data-stu-id="198a9-129">Specifies the name of a scheduler job for which to get the history.</span></span>

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

### <span data-ttu-id="198a9-130">-JobStatus</span><span class="sxs-lookup"><span data-stu-id="198a9-130">-JobStatus</span></span>
<span data-ttu-id="198a9-131">Anger statusen för Schemaläggaren-jobbet som du vill hämta historik för.</span><span class="sxs-lookup"><span data-stu-id="198a9-131">Specifies the status of scheduler job for which to get the history.</span></span>
<span data-ttu-id="198a9-132">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="198a9-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="198a9-133">Rätta</span><span class="sxs-lookup"><span data-stu-id="198a9-133">Completed</span></span>
- <span data-ttu-id="198a9-134">Startade</span><span class="sxs-lookup"><span data-stu-id="198a9-134">Failed</span></span>

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

### <span data-ttu-id="198a9-135">-Plats</span><span class="sxs-lookup"><span data-stu-id="198a9-135">-Location</span></span>
<span data-ttu-id="198a9-136">Anger namnet på platsen där moln tjänsten är värd.</span><span class="sxs-lookup"><span data-stu-id="198a9-136">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="198a9-137">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="198a9-137">Valid values are:</span></span> 

- <span data-ttu-id="198a9-138">Världen över</span><span class="sxs-lookup"><span data-stu-id="198a9-138">Anywhere Asia</span></span>
- <span data-ttu-id="198a9-139">Överallt i Europa</span><span class="sxs-lookup"><span data-stu-id="198a9-139">Anywhere Europe</span></span>
- <span data-ttu-id="198a9-140">Var du än är</span><span class="sxs-lookup"><span data-stu-id="198a9-140">Anywhere US</span></span>
- <span data-ttu-id="198a9-141">Östasien</span><span class="sxs-lookup"><span data-stu-id="198a9-141">East Asia</span></span>
- <span data-ttu-id="198a9-142">Östra USA</span><span class="sxs-lookup"><span data-stu-id="198a9-142">East US</span></span>
- <span data-ttu-id="198a9-143">Norra Central USA</span><span class="sxs-lookup"><span data-stu-id="198a9-143">North Central US</span></span>
- <span data-ttu-id="198a9-144">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="198a9-144">North Europe</span></span>
- <span data-ttu-id="198a9-145">Södra centrala USA</span><span class="sxs-lookup"><span data-stu-id="198a9-145">South Central US</span></span>
- <span data-ttu-id="198a9-146">Sydostasien</span><span class="sxs-lookup"><span data-stu-id="198a9-146">Southeast Asia</span></span>
- <span data-ttu-id="198a9-147">Västeuropa</span><span class="sxs-lookup"><span data-stu-id="198a9-147">West Europe</span></span>
- <span data-ttu-id="198a9-148">Västra USA</span><span class="sxs-lookup"><span data-stu-id="198a9-148">West US</span></span>

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

### <span data-ttu-id="198a9-149">-Profil</span><span class="sxs-lookup"><span data-stu-id="198a9-149">-Profile</span></span>
<span data-ttu-id="198a9-150">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="198a9-150">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="198a9-151">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="198a9-151">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="198a9-152">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="198a9-152">-Skip</span></span>
<span data-ttu-id="198a9-153">Ignorerar angivet antal objekt och hämtar sedan återstående objekt.</span><span class="sxs-lookup"><span data-stu-id="198a9-153">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="198a9-154">Ange antalet objekt som ska hoppas över.</span><span class="sxs-lookup"><span data-stu-id="198a9-154">Enter the number of objects to skip.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="198a9-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="198a9-155">CommonParameters</span></span>
<span data-ttu-id="198a9-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="198a9-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="198a9-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="198a9-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="198a9-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="198a9-158">INPUTS</span></span>

## <span data-ttu-id="198a9-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="198a9-159">OUTPUTS</span></span>

## <span data-ttu-id="198a9-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="198a9-160">NOTES</span></span>

## <span data-ttu-id="198a9-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="198a9-161">RELATED LINKS</span></span>

[<span data-ttu-id="198a9-162">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="198a9-162">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)

[<span data-ttu-id="198a9-163">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="198a9-163">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)


