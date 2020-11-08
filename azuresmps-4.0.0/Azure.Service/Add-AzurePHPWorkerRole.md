---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FEFBF1EF-FBCE-45D8-8455-F3F8662F1F36
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ddf78f30cb6938571fc967d510e4ab99a0cfc80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099617"
---
# <span data-ttu-id="831a5-101">Add-AzurePHPWorkerRole</span><span class="sxs-lookup"><span data-stu-id="831a5-101">Add-AzurePHPWorkerRole</span></span>

## <span data-ttu-id="831a5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="831a5-102">SYNOPSIS</span></span>
<span data-ttu-id="831a5-103">Skapar nödvändiga filer och konfiguration för ett PHP-program som hanteras i Azure via php.exe.</span><span class="sxs-lookup"><span data-stu-id="831a5-103">Creates the required files and configuration for a PHP application that will be hosted in Azure through php.exe.</span></span>

## <span data-ttu-id="831a5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="831a5-104">SYNTAX</span></span>

```
Add-AzurePHPWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="831a5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="831a5-105">DESCRIPTION</span></span>
<span data-ttu-id="831a5-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="831a5-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="831a5-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="831a5-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="831a5-108">Skapar de filer och den konfiguration som krävs, som ibland kallas scaffolding, för ett PHP-program som hanteras i Azure via php.exe.</span><span class="sxs-lookup"><span data-stu-id="831a5-108">Creates the required files and configuration, sometimes referred to as scaffolding, for a PHP application that will be hosted in Azure through php.exe.</span></span>

## <span data-ttu-id="831a5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="831a5-109">EXAMPLES</span></span>

### <span data-ttu-id="831a5-110">Exempel 1: skapa en arbets roll med en enda instans</span><span class="sxs-lookup"><span data-stu-id="831a5-110">Example 1: Create a worker role with a single instance</span></span>
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole
```

<span data-ttu-id="831a5-111">I det här exemplet läggs nödvändiga filer och inställningar till i det aktuella programmet.</span><span class="sxs-lookup"><span data-stu-id="831a5-111">This example adds the required files and configuration for a single worker role named MyWorkerRole to the current application.</span></span>

### <span data-ttu-id="831a5-112">Exempel 2: skapa en arbets roll med flera instanser</span><span class="sxs-lookup"><span data-stu-id="831a5-112">Example 2: Create a worker role with multiple instances</span></span>
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="831a5-113">I det här exemplet läggs nödvändiga filer och inställningar till i det aktuella programmet med hjälp av namnet MyWorkerRole med en roll instans räkning på 2.</span><span class="sxs-lookup"><span data-stu-id="831a5-113">This example adds the required files and configuration for a new worker role to the current application, using the name MyWorkerRole with a role instance count of 2.</span></span>

## <span data-ttu-id="831a5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="831a5-114">PARAMETERS</span></span>

### <span data-ttu-id="831a5-115">-Instanser</span><span class="sxs-lookup"><span data-stu-id="831a5-115">-Instances</span></span>
<span data-ttu-id="831a5-116">Anger antalet roll instanser för denna arbets roll.</span><span class="sxs-lookup"><span data-stu-id="831a5-116">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="831a5-117">Standardvärdet är 1.</span><span class="sxs-lookup"><span data-stu-id="831a5-117">The default is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831a5-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="831a5-118">-Name</span></span>
<span data-ttu-id="831a5-119">Anger namnet på arbets rollen.</span><span class="sxs-lookup"><span data-stu-id="831a5-119">Specifies the name of the worker role.</span></span>
<span data-ttu-id="831a5-120">Namnet bestämmer mappnamnet som innehåller de filer och den konfiguration för PHP-tjänsten som finns i arbets rollen.</span><span class="sxs-lookup"><span data-stu-id="831a5-120">The name determines the folder name that contains the required files and configuration for the PHP service hosted in the worker role.</span></span>
<span data-ttu-id="831a5-121">Standardvärdet är WorkerRole1.</span><span class="sxs-lookup"><span data-stu-id="831a5-121">The default is WorkerRole1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831a5-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="831a5-122">-Profile</span></span>
<span data-ttu-id="831a5-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="831a5-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="831a5-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="831a5-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="831a5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="831a5-125">CommonParameters</span></span>
<span data-ttu-id="831a5-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="831a5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="831a5-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="831a5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="831a5-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="831a5-128">INPUTS</span></span>

## <span data-ttu-id="831a5-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="831a5-129">OUTPUTS</span></span>

## <span data-ttu-id="831a5-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="831a5-130">NOTES</span></span>

## <span data-ttu-id="831a5-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="831a5-131">RELATED LINKS</span></span>

[<span data-ttu-id="831a5-132">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="831a5-132">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="831a5-133">Add-AzurePHPWebRole</span><span class="sxs-lookup"><span data-stu-id="831a5-133">Add-AzurePHPWebRole</span></span>](./Add-AzurePHPWebRole.md)


