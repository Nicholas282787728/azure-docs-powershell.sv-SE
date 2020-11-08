---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: DF12406D-894C-4732-95EE-D75524023B82
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2e6596c0de702175927f51bfd70fc5271b13bfd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099210"
---
# <span data-ttu-id="17cac-101">New-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="17cac-101">New-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="17cac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="17cac-102">SYNOPSIS</span></span>
<span data-ttu-id="17cac-103">Skapar en jobb samling i Schemaläggaren.</span><span class="sxs-lookup"><span data-stu-id="17cac-103">Creates a scheduler job collection.</span></span>

## <span data-ttu-id="17cac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="17cac-104">SYNTAX</span></span>

```
New-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="17cac-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="17cac-105">DESCRIPTION</span></span>
<span data-ttu-id="17cac-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="17cac-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="17cac-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="17cac-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="17cac-108">Cmdleten **New-AzureSchedulerJobCollection** skapar en jobb samling för schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="17cac-108">The **New-AzureSchedulerJobCollection** cmdlet creates a scheduler job collection.</span></span>
<span data-ttu-id="17cac-109">Om du inte anger ett värde för parametern *plan* skapar cmdleten en standard jobb samling.</span><span class="sxs-lookup"><span data-stu-id="17cac-109">If you do not specify a value for the *Plan* parameter, the cmdlet creates a standard job collection.</span></span>

## <span data-ttu-id="17cac-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="17cac-110">EXAMPLES</span></span>

### <span data-ttu-id="17cac-111">Exempel 1: skapa en jobb samling i Schemaläggaren som innehåller standardvärden</span><span class="sxs-lookup"><span data-stu-id="17cac-111">Example 1: Create a scheduler job collection that includes default values</span></span>
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection01" -Location "North Central US" -Plan "Standard"
```

<span data-ttu-id="17cac-112">Det här kommandot skapar en standard jobb samling med namnet JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="17cac-112">This command creates a standard scheduler job collection named JobCollection01.</span></span>
<span data-ttu-id="17cac-113">Den nya samlingen har ett standard jobb antal och Max återkommande värden för en standard jobb samling i Schemaläggaren.</span><span class="sxs-lookup"><span data-stu-id="17cac-113">The new collection has a default job count and maximum recurrence values for a standard scheduler job collection.</span></span>

### <span data-ttu-id="17cac-114">Exempel 2: skapa en jobb samling i Schemaläggaren med angivna värden</span><span class="sxs-lookup"><span data-stu-id="17cac-114">Example 2: Create a scheduler job collection with specified values</span></span>
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection02" -Location "North Central US" -Frequency "Hour" -Interval 12 -MaxJobCount 30 -Plan "Standard"
```

<span data-ttu-id="17cac-115">Det här kommandot skapar en standard jobb samling med namnet JobCollection02.</span><span class="sxs-lookup"><span data-stu-id="17cac-115">This command creates a standard scheduler job collection named JobCollection02.</span></span>
<span data-ttu-id="17cac-116">Den nya samlingen har ett maximalt antal jobb om 30 och en maximal återkomst på 12 per timme.</span><span class="sxs-lookup"><span data-stu-id="17cac-116">The new collection has a maximum job count of 30 and a maximum recurrence of 12 per hour.</span></span>

## <span data-ttu-id="17cac-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="17cac-117">PARAMETERS</span></span>

### <span data-ttu-id="17cac-118">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="17cac-118">-Frequency</span></span>
<span data-ttu-id="17cac-119">Anger den maximala frekvens som kan anges för alla jobb i jobb samlingen i Schemaläggaren.</span><span class="sxs-lookup"><span data-stu-id="17cac-119">Specifies the maximum frequency that can be specified on any job in this scheduler job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17cac-120">-Intervall</span><span class="sxs-lookup"><span data-stu-id="17cac-120">-Interval</span></span>
<span data-ttu-id="17cac-121">Anger upprepnings intervallet för frekvensen som anges med hjälp av parametern *frekvens* .</span><span class="sxs-lookup"><span data-stu-id="17cac-121">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17cac-122">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="17cac-122">-JobCollectionName</span></span>
<span data-ttu-id="17cac-123">Anger namnet på den nya jobb samlingen i Schemaläggaren.</span><span class="sxs-lookup"><span data-stu-id="17cac-123">Specifies the name for the new scheduler job collection.</span></span>

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

### <span data-ttu-id="17cac-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="17cac-124">-Location</span></span>
<span data-ttu-id="17cac-125">Anger namnet på platsen där moln tjänsten är värd.</span><span class="sxs-lookup"><span data-stu-id="17cac-125">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="17cac-126">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="17cac-126">Valid values are:</span></span> 

- <span data-ttu-id="17cac-127">Världen över</span><span class="sxs-lookup"><span data-stu-id="17cac-127">Anywhere Asia</span></span>
- <span data-ttu-id="17cac-128">Överallt i Europa</span><span class="sxs-lookup"><span data-stu-id="17cac-128">Anywhere Europe</span></span>
- <span data-ttu-id="17cac-129">Var du än är</span><span class="sxs-lookup"><span data-stu-id="17cac-129">Anywhere US</span></span>
- <span data-ttu-id="17cac-130">Östasien</span><span class="sxs-lookup"><span data-stu-id="17cac-130">East Asia</span></span>
- <span data-ttu-id="17cac-131">Östra USA</span><span class="sxs-lookup"><span data-stu-id="17cac-131">East US</span></span>
- <span data-ttu-id="17cac-132">Norra Central USA</span><span class="sxs-lookup"><span data-stu-id="17cac-132">North Central US</span></span>
- <span data-ttu-id="17cac-133">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="17cac-133">North Europe</span></span>
- <span data-ttu-id="17cac-134">Södra centrala USA</span><span class="sxs-lookup"><span data-stu-id="17cac-134">South Central US</span></span>
- <span data-ttu-id="17cac-135">Sydostasien</span><span class="sxs-lookup"><span data-stu-id="17cac-135">Southeast Asia</span></span>
- <span data-ttu-id="17cac-136">Västeuropa</span><span class="sxs-lookup"><span data-stu-id="17cac-136">West Europe</span></span>
- <span data-ttu-id="17cac-137">Västra USA</span><span class="sxs-lookup"><span data-stu-id="17cac-137">West US</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17cac-138">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="17cac-138">-MaxJobCount</span></span>
<span data-ttu-id="17cac-139">Anger maximalt antal jobb som kan skapas i jobb samlingen i schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="17cac-139">Specifies the maximum number of jobs that can be created in the scheduler job collection.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17cac-140">-Planera</span><span class="sxs-lookup"><span data-stu-id="17cac-140">-Plan</span></span>
<span data-ttu-id="17cac-141">Anger Schemaläggaren jobb samlings plan.</span><span class="sxs-lookup"><span data-stu-id="17cac-141">Specifies the scheduler job collection plan.</span></span>

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

### <span data-ttu-id="17cac-142">-Profil</span><span class="sxs-lookup"><span data-stu-id="17cac-142">-Profile</span></span>
<span data-ttu-id="17cac-143">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="17cac-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="17cac-144">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="17cac-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="17cac-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17cac-145">CommonParameters</span></span>
<span data-ttu-id="17cac-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17cac-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17cac-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17cac-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17cac-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="17cac-148">INPUTS</span></span>

## <span data-ttu-id="17cac-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="17cac-149">OUTPUTS</span></span>

## <span data-ttu-id="17cac-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="17cac-150">NOTES</span></span>

## <span data-ttu-id="17cac-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="17cac-151">RELATED LINKS</span></span>

[<span data-ttu-id="17cac-152">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="17cac-152">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="17cac-153">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="17cac-153">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)

[<span data-ttu-id="17cac-154">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="17cac-154">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


