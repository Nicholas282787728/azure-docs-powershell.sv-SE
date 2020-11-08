---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7190C668-6A0C-4E1D-9B5A-0CEEF53E3F85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93573caf43a6c711e1aa1308c851c82faaef5bcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099619"
---
# <span data-ttu-id="4f1e2-101">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="4f1e2-101">Add-AzureNodeWorkerRole</span></span>

## <span data-ttu-id="4f1e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f1e2-102">SYNOPSIS</span></span>
<span data-ttu-id="4f1e2-103">Skapar de filer och mappar som behövs för att ett Node.js program ska finnas med i molnet via node.exe</span><span class="sxs-lookup"><span data-stu-id="4f1e2-103">Creates the required files and folders for a Node.js application to be hosted in the cloud via node.exe</span></span>

## <span data-ttu-id="4f1e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f1e2-104">SYNTAX</span></span>

```
Add-AzureNodeWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4f1e2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f1e2-105">DESCRIPTION</span></span>
<span data-ttu-id="4f1e2-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="4f1e2-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="4f1e2-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="4f1e2-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="4f1e2-108">Cmdleten **Add-AzureNodeWorkerRole** skapar nödvändiga filer och mappar, som ibland kallas för scaffolding, för ett Node.js-program som ska finnas i molnet via node.exe.</span><span class="sxs-lookup"><span data-stu-id="4f1e2-108">The **Add-AzureNodeWorkerRole** cmdlet creates the required files and folders, sometimes referred to as scaffolding, for a Node.js application to be hosted in the cloud via node.exe.</span></span>

## <span data-ttu-id="4f1e2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f1e2-109">EXAMPLES</span></span>

### <span data-ttu-id="4f1e2-110">Exempel 1: roll för en instans arbetare</span><span class="sxs-lookup"><span data-stu-id="4f1e2-110">Example 1: Single instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole
```

<span data-ttu-id="4f1e2-111">I det här exemplet läggs scaffolding för en arbets roll som heter **MyWorkerRole** till det aktuella programmet.</span><span class="sxs-lookup"><span data-stu-id="4f1e2-111">This example adds scaffolding for a single worker role named **MyWorkerRole** to the current application.</span></span>

### <span data-ttu-id="4f1e2-112">Exempel 2: roll för flera instanser</span><span class="sxs-lookup"><span data-stu-id="4f1e2-112">Example 2: Multiple instance worker role</span></span>
```
PS C:\> Add-AzureNodeWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="4f1e2-113">I det här exemplet läggs scaffolding för en arbets roll som heter **MyWorkerRole** till det aktuella programmet med en roll instans räkning på 2.</span><span class="sxs-lookup"><span data-stu-id="4f1e2-113">This example adds scaffolding for a single worker role named **MyWorkerRole** to the current application, with a role instance count of 2.</span></span>

## <span data-ttu-id="4f1e2-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f1e2-114">PARAMETERS</span></span>

### <span data-ttu-id="4f1e2-115">-Instanser</span><span class="sxs-lookup"><span data-stu-id="4f1e2-115">-Instances</span></span>
<span data-ttu-id="4f1e2-116">Anger antalet roll instanser för denna arbets roll.</span><span class="sxs-lookup"><span data-stu-id="4f1e2-116">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="4f1e2-117">Standardvärdet är 1.</span><span class="sxs-lookup"><span data-stu-id="4f1e2-117">Default is 1.</span></span>

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

### <span data-ttu-id="4f1e2-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="4f1e2-118">-Name</span></span>
<span data-ttu-id="4f1e2-119">Anger namnet på arbets rollen.</span><span class="sxs-lookup"><span data-stu-id="4f1e2-119">Specifies the name of the worker role.</span></span>
<span data-ttu-id="4f1e2-120">Värdet bestämmer mappnamnet som innehåller scaffolding för den node.js tjänst som är värd för arbets rollen.</span><span class="sxs-lookup"><span data-stu-id="4f1e2-120">The value determines the folder name that contains the scaffolding for the node.js service hosted in the worker role.</span></span>
<span data-ttu-id="4f1e2-121">Standard är WorkerRole1.</span><span class="sxs-lookup"><span data-stu-id="4f1e2-121">Default is WorkerRole1.</span></span>

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

### <span data-ttu-id="4f1e2-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="4f1e2-122">-Profile</span></span>
<span data-ttu-id="4f1e2-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="4f1e2-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4f1e2-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="4f1e2-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4f1e2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f1e2-125">CommonParameters</span></span>
<span data-ttu-id="4f1e2-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f1e2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f1e2-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f1e2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f1e2-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f1e2-128">INPUTS</span></span>

## <span data-ttu-id="4f1e2-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f1e2-129">OUTPUTS</span></span>

## <span data-ttu-id="4f1e2-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f1e2-130">NOTES</span></span>

## <span data-ttu-id="4f1e2-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f1e2-131">RELATED LINKS</span></span>

[<span data-ttu-id="4f1e2-132">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="4f1e2-132">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="4f1e2-133">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="4f1e2-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


