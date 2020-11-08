---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22DBB3DD-B02D-4288-89CB-550EBECC2E79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4373e4eed8524db1dd5311778b3e297e766c74dd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093169"
---
# <span data-ttu-id="59de7-101">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="59de7-101">Set-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="59de7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59de7-102">SYNOPSIS</span></span>
<span data-ttu-id="59de7-103">Uppdaterar en jobb samling i schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="59de7-103">Updates a scheduler job collection.</span></span>

## <span data-ttu-id="59de7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59de7-104">SYNTAX</span></span>

```
Set-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="59de7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59de7-105">DESCRIPTION</span></span>
<span data-ttu-id="59de7-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="59de7-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="59de7-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="59de7-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="59de7-108">Cmdleten **set-AzureSchedulerJobCollection** uppdaterar en jobb samling i Schemaläggaren.</span><span class="sxs-lookup"><span data-stu-id="59de7-108">The **Set-AzureSchedulerJobCollection** cmdlet updates a scheduler job collection.</span></span>

## <span data-ttu-id="59de7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59de7-109">EXAMPLES</span></span>

### <span data-ttu-id="59de7-110">Exempel 1: ändra det maximala antalet jobb för en samling</span><span class="sxs-lookup"><span data-stu-id="59de7-110">Example 1: Change the maximum job count for a collection</span></span>
```
PS C:\> Set-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -MaxJobCount 30
```

<span data-ttu-id="59de7-111">Det här kommandot ändrar det maximala antalet jobb till 30 för den befintliga jobb samlingen i Schemaläggaren med namnet JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="59de7-111">This command changes the maximum job count to 30 on the existing scheduler job collection named JobCollection01.</span></span>

## <span data-ttu-id="59de7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59de7-112">PARAMETERS</span></span>

### <span data-ttu-id="59de7-113">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="59de7-113">-Frequency</span></span>
<span data-ttu-id="59de7-114">Anger den maximala frekvens som kan anges för alla jobb i jobb samlingen i Schemaläggaren.</span><span class="sxs-lookup"><span data-stu-id="59de7-114">Specifies the maximum frequency that can be specified on any job in this scheduler job collection.</span></span>
<span data-ttu-id="59de7-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="59de7-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="59de7-116">Minut</span><span class="sxs-lookup"><span data-stu-id="59de7-116">Minute</span></span>
- <span data-ttu-id="59de7-117">Timme</span><span class="sxs-lookup"><span data-stu-id="59de7-117">Hour</span></span>
- <span data-ttu-id="59de7-118">Day</span><span class="sxs-lookup"><span data-stu-id="59de7-118">Day</span></span>
- <span data-ttu-id="59de7-119">Fjorton</span><span class="sxs-lookup"><span data-stu-id="59de7-119">Week</span></span>
- <span data-ttu-id="59de7-120">Månad</span><span class="sxs-lookup"><span data-stu-id="59de7-120">Month</span></span>
- <span data-ttu-id="59de7-121">Vinåret</span><span class="sxs-lookup"><span data-stu-id="59de7-121">Year</span></span>

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

### <span data-ttu-id="59de7-122">-Intervall</span><span class="sxs-lookup"><span data-stu-id="59de7-122">-Interval</span></span>
<span data-ttu-id="59de7-123">Anger upprepnings intervallet för frekvensen som anges med hjälp av parametern *frekvens* .</span><span class="sxs-lookup"><span data-stu-id="59de7-123">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="59de7-124">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="59de7-124">-JobCollectionName</span></span>
<span data-ttu-id="59de7-125">Anger namnet på jobb samlingen för Schemaläggaren som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="59de7-125">Specifies the name of scheduler job collection to update.</span></span>

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

### <span data-ttu-id="59de7-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="59de7-126">-Location</span></span>
<span data-ttu-id="59de7-127">Anger namnet på platsen där moln tjänsten är värd.</span><span class="sxs-lookup"><span data-stu-id="59de7-127">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="59de7-128">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="59de7-128">Valid values are:</span></span> 

- <span data-ttu-id="59de7-129">Världen över</span><span class="sxs-lookup"><span data-stu-id="59de7-129">Anywhere Asia</span></span>
- <span data-ttu-id="59de7-130">Överallt i Europa</span><span class="sxs-lookup"><span data-stu-id="59de7-130">Anywhere Europe</span></span>
- <span data-ttu-id="59de7-131">Var du än är</span><span class="sxs-lookup"><span data-stu-id="59de7-131">Anywhere US</span></span>
- <span data-ttu-id="59de7-132">Östasien</span><span class="sxs-lookup"><span data-stu-id="59de7-132">East Asia</span></span>
- <span data-ttu-id="59de7-133">Östra USA</span><span class="sxs-lookup"><span data-stu-id="59de7-133">East US</span></span>
- <span data-ttu-id="59de7-134">Norra Central USA</span><span class="sxs-lookup"><span data-stu-id="59de7-134">North Central US</span></span>
- <span data-ttu-id="59de7-135">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="59de7-135">North Europe</span></span>
- <span data-ttu-id="59de7-136">Södra centrala USA</span><span class="sxs-lookup"><span data-stu-id="59de7-136">South Central US</span></span>
- <span data-ttu-id="59de7-137">Sydostasien</span><span class="sxs-lookup"><span data-stu-id="59de7-137">Southeast Asia</span></span>
- <span data-ttu-id="59de7-138">Västeuropa</span><span class="sxs-lookup"><span data-stu-id="59de7-138">West Europe</span></span>
- <span data-ttu-id="59de7-139">Västra USA</span><span class="sxs-lookup"><span data-stu-id="59de7-139">West US</span></span>

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

### <span data-ttu-id="59de7-140">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="59de7-140">-MaxJobCount</span></span>
<span data-ttu-id="59de7-141">Anger maximalt antal jobb som kan skapas i jobb samlingen i schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="59de7-141">Specifies the maximum number of jobs that can be created in the scheduler job collection.</span></span>

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

### <span data-ttu-id="59de7-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59de7-142">-PassThru</span></span>
<span data-ttu-id="59de7-143">Anger att den här cmdleten returnerar ett objekt som representerar det objekt som den körs på.</span><span class="sxs-lookup"><span data-stu-id="59de7-143">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="59de7-144">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="59de7-144">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59de7-145">-Planera</span><span class="sxs-lookup"><span data-stu-id="59de7-145">-Plan</span></span>
<span data-ttu-id="59de7-146">Anger Schemaläggaren jobb samlings plan.</span><span class="sxs-lookup"><span data-stu-id="59de7-146">Specifies the scheduler job collection plan.</span></span>

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

### <span data-ttu-id="59de7-147">-Profil</span><span class="sxs-lookup"><span data-stu-id="59de7-147">-Profile</span></span>
<span data-ttu-id="59de7-148">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="59de7-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="59de7-149">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="59de7-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="59de7-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59de7-150">CommonParameters</span></span>
<span data-ttu-id="59de7-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59de7-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59de7-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59de7-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59de7-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59de7-153">INPUTS</span></span>

## <span data-ttu-id="59de7-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59de7-154">OUTPUTS</span></span>

## <span data-ttu-id="59de7-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59de7-155">NOTES</span></span>

## <span data-ttu-id="59de7-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59de7-156">RELATED LINKS</span></span>

[<span data-ttu-id="59de7-157">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="59de7-157">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="59de7-158">New-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="59de7-158">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="59de7-159">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="59de7-159">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)


