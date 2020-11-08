---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22DEC693-32BA-4048-8912-D1626DD511E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c95fb7f79cdb160bf2dd2014cad49d1bc96eb3b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099359"
---
# <span data-ttu-id="8dc75-101">Remove-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="8dc75-101">Remove-AzureSchedulerJob</span></span>

## <span data-ttu-id="8dc75-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8dc75-102">SYNOPSIS</span></span>
<span data-ttu-id="8dc75-103">Tar bort ett jobb i schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="8dc75-103">Deletes a scheduler job.</span></span>

## <span data-ttu-id="8dc75-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8dc75-104">SYNTAX</span></span>

```
Remove-AzureSchedulerJob [-Force] [-Location <String>] -JobCollectionName <String> -JobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8dc75-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8dc75-105">DESCRIPTION</span></span>
<span data-ttu-id="8dc75-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="8dc75-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8dc75-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="8dc75-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="8dc75-108">Cmdleten **Remove-AzureSchedulerJob** tar bort ett jobb för schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="8dc75-108">The **Remove-AzureSchedulerJob** cmdlet deletes a scheduler job.</span></span>

## <span data-ttu-id="8dc75-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8dc75-109">EXAMPLES</span></span>

### <span data-ttu-id="8dc75-110">Exempel 1: ta bort ett jobb i schemaläggare</span><span class="sxs-lookup"><span data-stu-id="8dc75-110">Example 1: Delete a scheduler job</span></span>
```
PS C:\> Remove-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job17"
```

<span data-ttu-id="8dc75-111">Det här kommandot tar bort jobbet som heter Job17.</span><span class="sxs-lookup"><span data-stu-id="8dc75-111">This command deletes the job named Job17.</span></span>
<span data-ttu-id="8dc75-112">Jobbet ingår i jobb samlingen med namnet JobCollection01 och finns i den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="8dc75-112">That job is part of the job collection named JobCollection01 and is in of the specified location.</span></span>

## <span data-ttu-id="8dc75-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8dc75-113">PARAMETERS</span></span>

### <span data-ttu-id="8dc75-114">-Force</span><span class="sxs-lookup"><span data-stu-id="8dc75-114">-Force</span></span>
<span data-ttu-id="8dc75-115">Anger att denna cmdlet tar bort jobbet schemaläggare utan att du uppmanas att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="8dc75-115">Indicates that this cmdlet removes the scheduler job without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="8dc75-116">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="8dc75-116">-JobCollectionName</span></span>
<span data-ttu-id="8dc75-117">Anger namnet på den mängd som innehåller schemaläggnings jobbet som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="8dc75-117">Specifies the name of the collection that contains the scheduler job to delete.</span></span>

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

### <span data-ttu-id="8dc75-118">-JobName</span><span class="sxs-lookup"><span data-stu-id="8dc75-118">-JobName</span></span>
<span data-ttu-id="8dc75-119">Anger namnet på ett schema jobb som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="8dc75-119">Specifies the name of a scheduler job to delete.</span></span>

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

### <span data-ttu-id="8dc75-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="8dc75-120">-Location</span></span>
<span data-ttu-id="8dc75-121">Anger namnet på platsen där moln tjänsten är värd.</span><span class="sxs-lookup"><span data-stu-id="8dc75-121">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="8dc75-122">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="8dc75-122">Valid values are:</span></span> 

- <span data-ttu-id="8dc75-123">Världen över</span><span class="sxs-lookup"><span data-stu-id="8dc75-123">Anywhere Asia</span></span>
- <span data-ttu-id="8dc75-124">Överallt i Europa</span><span class="sxs-lookup"><span data-stu-id="8dc75-124">Anywhere Europe</span></span>
- <span data-ttu-id="8dc75-125">Var du än är</span><span class="sxs-lookup"><span data-stu-id="8dc75-125">Anywhere US</span></span>
- <span data-ttu-id="8dc75-126">Östasien</span><span class="sxs-lookup"><span data-stu-id="8dc75-126">East Asia</span></span>
- <span data-ttu-id="8dc75-127">Östra USA</span><span class="sxs-lookup"><span data-stu-id="8dc75-127">East US</span></span>
- <span data-ttu-id="8dc75-128">Norra Central USA</span><span class="sxs-lookup"><span data-stu-id="8dc75-128">North Central US</span></span>
- <span data-ttu-id="8dc75-129">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="8dc75-129">North Europe</span></span>
- <span data-ttu-id="8dc75-130">Södra centrala USA</span><span class="sxs-lookup"><span data-stu-id="8dc75-130">South Central US</span></span>
- <span data-ttu-id="8dc75-131">Sydostasien</span><span class="sxs-lookup"><span data-stu-id="8dc75-131">Southeast Asia</span></span>
- <span data-ttu-id="8dc75-132">Västeuropa</span><span class="sxs-lookup"><span data-stu-id="8dc75-132">West Europe</span></span>
- <span data-ttu-id="8dc75-133">Västra USA</span><span class="sxs-lookup"><span data-stu-id="8dc75-133">West US</span></span>

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

### <span data-ttu-id="8dc75-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="8dc75-134">-Profile</span></span>
<span data-ttu-id="8dc75-135">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="8dc75-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8dc75-136">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="8dc75-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8dc75-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dc75-137">CommonParameters</span></span>
<span data-ttu-id="8dc75-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dc75-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dc75-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dc75-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dc75-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8dc75-140">INPUTS</span></span>

## <span data-ttu-id="8dc75-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8dc75-141">OUTPUTS</span></span>

## <span data-ttu-id="8dc75-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8dc75-142">NOTES</span></span>

## <span data-ttu-id="8dc75-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8dc75-143">RELATED LINKS</span></span>

[<span data-ttu-id="8dc75-144">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="8dc75-144">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)


