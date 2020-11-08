---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E499868E-A745-4CA4-A717-C33C3B94A2C8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b80071bb82ebbb960be5b5b4fcc854dc47c9ed9d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099222"
---
# <span data-ttu-id="47d05-101">New-AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="47d05-101">New-AzureRoleTemplate</span></span>

## <span data-ttu-id="47d05-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="47d05-102">SYNOPSIS</span></span>
<span data-ttu-id="47d05-103">Skapar roller för webb och arbetare.</span><span class="sxs-lookup"><span data-stu-id="47d05-103">Creates web and worker role templates.</span></span>

## <span data-ttu-id="47d05-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="47d05-104">SYNTAX</span></span>

### <span data-ttu-id="47d05-105">Webroll</span><span class="sxs-lookup"><span data-stu-id="47d05-105">WebRole</span></span>
```
New-AzureRoleTemplate [-Web] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="47d05-106">WorkerRole</span><span class="sxs-lookup"><span data-stu-id="47d05-106">WorkerRole</span></span>
```
New-AzureRoleTemplate [-Worker] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="47d05-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="47d05-107">DESCRIPTION</span></span>
<span data-ttu-id="47d05-108">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="47d05-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="47d05-109">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="47d05-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="47d05-110">Cmdleten **New-AzureRoleTemplate** skapar roller för webb och arbetare.</span><span class="sxs-lookup"><span data-stu-id="47d05-110">The **New-AzureRoleTemplate** cmdlet creates web and worker role templates.</span></span>

## <span data-ttu-id="47d05-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="47d05-111">EXAMPLES</span></span>

### <span data-ttu-id="47d05-112">Exempel 1: skapa en mall för webb roller</span><span class="sxs-lookup"><span data-stu-id="47d05-112">Example 1: Create a web role template</span></span>
```
PS C:\> New-AzureRoleTemplate -Web
```

<span data-ttu-id="47d05-113">I det här exemplet skapas en ny mall för webb roller i en mapp med namnet WebRoleTemplate i den aktuella katalogen.</span><span class="sxs-lookup"><span data-stu-id="47d05-113">This example creates a new web role template in a folder named WebRoleTemplate in the current directory.</span></span>

### <span data-ttu-id="47d05-114">Exempel 2: skapa en mall för arbets tagare</span><span class="sxs-lookup"><span data-stu-id="47d05-114">Example 2: Create a worker role template</span></span>
```
PS C:\> New-AzureRoleTemplate -Worker
```

<span data-ttu-id="47d05-115">I det här exemplet skapas en ny roll mal len i en mapp med namnet WebRoleTemplate i den aktuella katalogen.</span><span class="sxs-lookup"><span data-stu-id="47d05-115">This example creates a new worker role template in a folder named WebRoleTemplate in the current directory.</span></span>

### <span data-ttu-id="47d05-116">Exempel 3: skapa en rollprovider i en anpassad katalog</span><span class="sxs-lookup"><span data-stu-id="47d05-116">Example 3: Create a role template in a custom directory</span></span>
```
PS C:\> New-AzureRoleTemplate -Web -Output C:\MyWebRoleTemplate
```

<span data-ttu-id="47d05-117">I det här exemplet skapas en ny webb Rolls mal len i katalogen MyWebRoleTemplate i stället för i den aktuella katalogen.</span><span class="sxs-lookup"><span data-stu-id="47d05-117">This example creates a new web role template in directory named MyWebRoleTemplate, instead of in the current directory.</span></span>

## <span data-ttu-id="47d05-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="47d05-118">PARAMETERS</span></span>

### <span data-ttu-id="47d05-119">-Utdata</span><span class="sxs-lookup"><span data-stu-id="47d05-119">-Output</span></span>
<span data-ttu-id="47d05-120">Anger utgångs Sök vägen för den genererade mallen.</span><span class="sxs-lookup"><span data-stu-id="47d05-120">Specifies the output path of generated template.</span></span>

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

### <span data-ttu-id="47d05-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="47d05-121">-Profile</span></span>
<span data-ttu-id="47d05-122">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="47d05-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="47d05-123">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="47d05-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="47d05-124">-Webb</span><span class="sxs-lookup"><span data-stu-id="47d05-124">-Web</span></span>
<span data-ttu-id="47d05-125">Anger att du vill skapa en mall för webb roller.</span><span class="sxs-lookup"><span data-stu-id="47d05-125">Specifies that you want to create a web role template.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47d05-126">-Arbeta</span><span class="sxs-lookup"><span data-stu-id="47d05-126">-Worker</span></span>
<span data-ttu-id="47d05-127">Anger att du vill skapa en mall för en arbets roll.</span><span class="sxs-lookup"><span data-stu-id="47d05-127">Specifies that you want to create a worker role template.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WorkerRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47d05-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47d05-128">CommonParameters</span></span>
<span data-ttu-id="47d05-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47d05-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47d05-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47d05-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47d05-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="47d05-131">INPUTS</span></span>

## <span data-ttu-id="47d05-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="47d05-132">OUTPUTS</span></span>

## <span data-ttu-id="47d05-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="47d05-133">NOTES</span></span>

## <span data-ttu-id="47d05-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="47d05-134">RELATED LINKS</span></span>

[<span data-ttu-id="47d05-135">Add-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="47d05-135">Add-AzureWebRole</span></span>](./Add-AzureWebRole.md)

[<span data-ttu-id="47d05-136">Add-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="47d05-136">Add-AzureWorkerRole</span></span>](./Add-AzureWorkerRole.md)


