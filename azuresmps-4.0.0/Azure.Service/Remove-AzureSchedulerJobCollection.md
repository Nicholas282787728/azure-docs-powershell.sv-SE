---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D4349562-1392-44B6-9353-6231F0CB5C51
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66618c0a684a8e54d41bbe4014ee1e6c893acdbf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099358"
---
# <span data-ttu-id="33f45-101">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="33f45-101">Remove-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="33f45-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="33f45-102">SYNOPSIS</span></span>
<span data-ttu-id="33f45-103">Tar bort en jobb samling i schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="33f45-103">Deletes a scheduler job collection.</span></span>

## <span data-ttu-id="33f45-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="33f45-104">SYNTAX</span></span>

```
Remove-AzureSchedulerJobCollection [-Force] [-Location <String>] -JobCollectionName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="33f45-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="33f45-105">DESCRIPTION</span></span>
<span data-ttu-id="33f45-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="33f45-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="33f45-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="33f45-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="33f45-108">Cmdleten **Remove-AzureSchedulerJobCollection** tar bort en jobb samling för Schemaläggaren och alla jobb under den samlingen.</span><span class="sxs-lookup"><span data-stu-id="33f45-108">The **Remove-AzureSchedulerJobCollection** cmdlet deletes a scheduler job collection and any jobs under that collection.</span></span>

## <span data-ttu-id="33f45-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="33f45-109">EXAMPLES</span></span>

### <span data-ttu-id="33f45-110">Exempel 1: ta bort en jobb samling för en plats</span><span class="sxs-lookup"><span data-stu-id="33f45-110">Example 1: Delete a job collection for a location</span></span>
```
PS C:\> Remove-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="33f45-111">Med det här kommandot tas jobb samlingen för Schemaläggaren bort med namnet JobCollection01 på platsen Central amerikanska.</span><span class="sxs-lookup"><span data-stu-id="33f45-111">This command deletes the scheduler job collection named JobCollection01 in the North Central US location.</span></span>
<span data-ttu-id="33f45-112">Kommandot tar också bort utskrifterna under JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="33f45-112">The command also deletes the jobs under JobCollection01.</span></span>

### <span data-ttu-id="33f45-113">Exempel 2: ta bort en jobb plats</span><span class="sxs-lookup"><span data-stu-id="33f45-113">Example 2: Delete a job location</span></span>
```
PS C:\> Remove-AzureSchedulerJobCollection -JobCollectionName "JobCollection02"
```

<span data-ttu-id="33f45-114">Det här kommandot tar bort jobb samlingen för Schemaläggaren med namnet JobCollection02.</span><span class="sxs-lookup"><span data-stu-id="33f45-114">This command deletes the scheduler job collection named JobCollection02.</span></span>
<span data-ttu-id="33f45-115">Kommandot tar också bort utskrifterna under JobCollection02.</span><span class="sxs-lookup"><span data-stu-id="33f45-115">The command also deletes the jobs under JobCollection02.</span></span>

## <span data-ttu-id="33f45-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="33f45-116">PARAMETERS</span></span>

### <span data-ttu-id="33f45-117">-Force</span><span class="sxs-lookup"><span data-stu-id="33f45-117">-Force</span></span>
<span data-ttu-id="33f45-118">Anger att denna cmdlet tar bort jobb samlingen i Schemaläggaren utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="33f45-118">Indicates that this cmdlet removes the scheduler job collection without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="33f45-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="33f45-119">-JobCollectionName</span></span>
<span data-ttu-id="33f45-120">Anger namnet på jobb samlingen i Schemaläggaren som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="33f45-120">Specifies the name of the scheduler job collection to delete.</span></span>

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

### <span data-ttu-id="33f45-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="33f45-121">-Location</span></span>
<span data-ttu-id="33f45-122">Anger namnet på platsen där moln tjänsten är värd.</span><span class="sxs-lookup"><span data-stu-id="33f45-122">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="33f45-123">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="33f45-123">Valid values are:</span></span> 

- <span data-ttu-id="33f45-124">Världen över</span><span class="sxs-lookup"><span data-stu-id="33f45-124">Anywhere Asia</span></span>
- <span data-ttu-id="33f45-125">Överallt i Europa</span><span class="sxs-lookup"><span data-stu-id="33f45-125">Anywhere Europe</span></span>
- <span data-ttu-id="33f45-126">Var du än är</span><span class="sxs-lookup"><span data-stu-id="33f45-126">Anywhere US</span></span>
- <span data-ttu-id="33f45-127">Östasien</span><span class="sxs-lookup"><span data-stu-id="33f45-127">East Asia</span></span>
- <span data-ttu-id="33f45-128">Östra USA</span><span class="sxs-lookup"><span data-stu-id="33f45-128">East US</span></span>
- <span data-ttu-id="33f45-129">Norra Central USA</span><span class="sxs-lookup"><span data-stu-id="33f45-129">North Central US</span></span>
- <span data-ttu-id="33f45-130">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="33f45-130">North Europe</span></span>
- <span data-ttu-id="33f45-131">Södra centrala USA</span><span class="sxs-lookup"><span data-stu-id="33f45-131">South Central US</span></span>
- <span data-ttu-id="33f45-132">Sydostasien</span><span class="sxs-lookup"><span data-stu-id="33f45-132">Southeast Asia</span></span>
- <span data-ttu-id="33f45-133">Västeuropa</span><span class="sxs-lookup"><span data-stu-id="33f45-133">West Europe</span></span>
- <span data-ttu-id="33f45-134">Västra USA</span><span class="sxs-lookup"><span data-stu-id="33f45-134">West US</span></span>

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

### <span data-ttu-id="33f45-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="33f45-135">-Profile</span></span>
<span data-ttu-id="33f45-136">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="33f45-136">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="33f45-137">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="33f45-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="33f45-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33f45-138">CommonParameters</span></span>
<span data-ttu-id="33f45-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33f45-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33f45-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33f45-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33f45-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="33f45-141">INPUTS</span></span>

## <span data-ttu-id="33f45-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="33f45-142">OUTPUTS</span></span>

## <span data-ttu-id="33f45-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="33f45-143">NOTES</span></span>

## <span data-ttu-id="33f45-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="33f45-144">RELATED LINKS</span></span>

[<span data-ttu-id="33f45-145">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="33f45-145">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="33f45-146">New-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="33f45-146">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="33f45-147">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="33f45-147">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


