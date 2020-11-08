---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 89B28B7C-CA61-4CAB-A4DD-69363AB48A65
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a33739cfad37269fc2f91654e82d6ea36eb2336
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093338"
---
# <span data-ttu-id="ed38a-101">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ed38a-101">Get-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="ed38a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed38a-102">SYNOPSIS</span></span>
<span data-ttu-id="ed38a-103">Hämtar jobb samlingar för schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="ed38a-103">Gets scheduler job collections.</span></span>

## <span data-ttu-id="ed38a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed38a-104">SYNTAX</span></span>

```
Get-AzureSchedulerJobCollection [-Location <String>] [-JobCollectionName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed38a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed38a-105">DESCRIPTION</span></span>
<span data-ttu-id="ed38a-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="ed38a-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ed38a-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ed38a-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ed38a-108">Cmdleten **Get-AzureSchedulerJobCollection** får en eller flera jobb samlingar för schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="ed38a-108">The **Get-AzureSchedulerJobCollection** cmdlet gets one or more scheduler job collections.</span></span>

## <span data-ttu-id="ed38a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed38a-109">EXAMPLES</span></span>

### <span data-ttu-id="ed38a-110">Exempel 1: Hämta alla samlingar</span><span class="sxs-lookup"><span data-stu-id="ed38a-110">Example 1: Get all collections</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection
```

<span data-ttu-id="ed38a-111">Det här kommandot får alla jobb samlingar för schemaläggare på alla platser i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="ed38a-111">This command gets all scheduler job collections across all locations in the current subscription.</span></span>

### <span data-ttu-id="ed38a-112">Exempel 2: Hämta alla samlingar för en plats</span><span class="sxs-lookup"><span data-stu-id="ed38a-112">Example 2: Get all collections for a location</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US"
```

<span data-ttu-id="ed38a-113">Det här kommandot får alla jobb samlingar i Schemaläggaren på platsen norra Central oss.</span><span class="sxs-lookup"><span data-stu-id="ed38a-113">This command gets all scheduler job collections in the location named North Central US.</span></span>

### <span data-ttu-id="ed38a-114">Exempel 3: Hämta en samling med hjälp av ett namn</span><span class="sxs-lookup"><span data-stu-id="ed38a-114">Example 3: Get a collection by using a name</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="ed38a-115">Det här kommandot får jobb samlingen Schemaläggaren med namnet JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="ed38a-115">This command gets the scheduler job collection named JobCollection01.</span></span>

## <span data-ttu-id="ed38a-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed38a-116">PARAMETERS</span></span>

### <span data-ttu-id="ed38a-117">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="ed38a-117">-JobCollectionName</span></span>
<span data-ttu-id="ed38a-118">Anger namnet på jobb samlingen i Schemaläggaren som ska visas.</span><span class="sxs-lookup"><span data-stu-id="ed38a-118">Specifies the name of the scheduler job collection to get.</span></span>

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

### <span data-ttu-id="ed38a-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="ed38a-119">-Location</span></span>
<span data-ttu-id="ed38a-120">Anger namnet på platsen där moln tjänsten är värd.</span><span class="sxs-lookup"><span data-stu-id="ed38a-120">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="ed38a-121">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="ed38a-121">Valid values are:</span></span> 

- <span data-ttu-id="ed38a-122">Världen över</span><span class="sxs-lookup"><span data-stu-id="ed38a-122">Anywhere Asia</span></span>
- <span data-ttu-id="ed38a-123">Överallt i Europa</span><span class="sxs-lookup"><span data-stu-id="ed38a-123">Anywhere Europe</span></span>
- <span data-ttu-id="ed38a-124">Var du än är</span><span class="sxs-lookup"><span data-stu-id="ed38a-124">Anywhere US</span></span>
- <span data-ttu-id="ed38a-125">Östasien</span><span class="sxs-lookup"><span data-stu-id="ed38a-125">East Asia</span></span>
- <span data-ttu-id="ed38a-126">Östra USA</span><span class="sxs-lookup"><span data-stu-id="ed38a-126">East US</span></span>
- <span data-ttu-id="ed38a-127">Norra Central USA</span><span class="sxs-lookup"><span data-stu-id="ed38a-127">North Central US</span></span>
- <span data-ttu-id="ed38a-128">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="ed38a-128">North Europe</span></span>
- <span data-ttu-id="ed38a-129">Södra centrala USA</span><span class="sxs-lookup"><span data-stu-id="ed38a-129">South Central US</span></span>
- <span data-ttu-id="ed38a-130">Sydostasien</span><span class="sxs-lookup"><span data-stu-id="ed38a-130">Southeast Asia</span></span>
- <span data-ttu-id="ed38a-131">Västeuropa</span><span class="sxs-lookup"><span data-stu-id="ed38a-131">West Europe</span></span>
- <span data-ttu-id="ed38a-132">Västra USA</span><span class="sxs-lookup"><span data-stu-id="ed38a-132">West US</span></span>

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

### <span data-ttu-id="ed38a-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="ed38a-133">-Profile</span></span>
<span data-ttu-id="ed38a-134">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="ed38a-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ed38a-135">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="ed38a-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ed38a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed38a-136">CommonParameters</span></span>
<span data-ttu-id="ed38a-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed38a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed38a-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed38a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed38a-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed38a-139">INPUTS</span></span>

## <span data-ttu-id="ed38a-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed38a-140">OUTPUTS</span></span>

## <span data-ttu-id="ed38a-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed38a-141">NOTES</span></span>

## <span data-ttu-id="ed38a-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed38a-142">RELATED LINKS</span></span>

[<span data-ttu-id="ed38a-143">New-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ed38a-143">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="ed38a-144">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ed38a-144">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)

[<span data-ttu-id="ed38a-145">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ed38a-145">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


