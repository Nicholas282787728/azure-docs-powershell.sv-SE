---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C2DAFB2C-A58B-406C-8349-8728771B279E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59aef29c27d7eb96834d270c2fce48ff3acb9554
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099622"
---
# <span data-ttu-id="bab4c-101">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="bab4c-101">Add-AzureNodeWebRole</span></span>

## <span data-ttu-id="bab4c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bab4c-102">SYNOPSIS</span></span>
<span data-ttu-id="bab4c-103">Skapar nödvändiga filer och mappar för ett Node.js-program.</span><span class="sxs-lookup"><span data-stu-id="bab4c-103">Creates required files and folders for a Node.js application.</span></span>

## <span data-ttu-id="bab4c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bab4c-104">SYNTAX</span></span>

```
Add-AzureNodeWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bab4c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bab4c-105">DESCRIPTION</span></span>
<span data-ttu-id="bab4c-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="bab4c-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="bab4c-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="bab4c-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="bab4c-108">**AzureNodeWebRole** skapar nödvändiga filer och mappar, som ibland kallas för scaffolding, för ett Node.js-program som ska finnas i molnet via IIS.</span><span class="sxs-lookup"><span data-stu-id="bab4c-108">The **Add-AzureNodeWebRole** creates required files and folders, sometimes referred to as scaffolding, for a Node.js application to be hosted in the cloud via IIS.</span></span>

## <span data-ttu-id="bab4c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bab4c-109">EXAMPLES</span></span>

### <span data-ttu-id="bab4c-110">Exempel 1: webb rollen enkel instans</span><span class="sxs-lookup"><span data-stu-id="bab4c-110">Example 1: Single instance web role</span></span>
```
PS C:\> Add-AzureNodeWebRole -Name MyWebRole
```

<span data-ttu-id="bab4c-111">I det här exemplet läggs scaffolding för en webb roll med namnet **MyWebRole** till det aktuella programmet.</span><span class="sxs-lookup"><span data-stu-id="bab4c-111">This example adds scaffolding for a single web role named **MyWebRole** to the current application.</span></span>

### <span data-ttu-id="bab4c-112">Exempel 2: webb rollen flera instanser</span><span class="sxs-lookup"><span data-stu-id="bab4c-112">Example 2: Multiple instance web role</span></span>
```
PS C:\> Add-AzureNodeWebRole MyWebRole -I 2
```

<span data-ttu-id="bab4c-113">I det här exemplet läggs scaffolding till för en ny webb roll med namnet **MyWebRole** till det aktuella programmet, med antal roller på en roll instans.</span><span class="sxs-lookup"><span data-stu-id="bab4c-113">This example adds scaffolding for a new web role named **MyWebRole** to the current application, with a role instance count of 2.</span></span>

## <span data-ttu-id="bab4c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bab4c-114">PARAMETERS</span></span>

### <span data-ttu-id="bab4c-115">-Instanser</span><span class="sxs-lookup"><span data-stu-id="bab4c-115">-Instances</span></span>
<span data-ttu-id="bab4c-116">Anger antalet roll instanser för webb rollen.</span><span class="sxs-lookup"><span data-stu-id="bab4c-116">Specifies the number of role instances for this web role.</span></span>
<span data-ttu-id="bab4c-117">Standardvärdet är 1.</span><span class="sxs-lookup"><span data-stu-id="bab4c-117">The default is 1.</span></span>

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

### <span data-ttu-id="bab4c-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="bab4c-118">-Name</span></span>
<span data-ttu-id="bab4c-119">Anger namnet på webb rollen.</span><span class="sxs-lookup"><span data-stu-id="bab4c-119">Specifies the name of the web role.</span></span>
<span data-ttu-id="bab4c-120">Det bestämmer också namnet på den katalog som innehåller scaffolding för det node.js-program som finns i webb rollen.</span><span class="sxs-lookup"><span data-stu-id="bab4c-120">It also determines the name of the directory that contains the scaffolding for the node.js application that will be hosted in the web role.</span></span>
<span data-ttu-id="bab4c-121">Standardvärdet för webrole #, där # anger antalet webb roller i tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bab4c-121">The default is WebRole#, where # indicates the number of web roles in the service.</span></span>

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

### <span data-ttu-id="bab4c-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="bab4c-122">-Profile</span></span>
<span data-ttu-id="bab4c-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="bab4c-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bab4c-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="bab4c-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bab4c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bab4c-125">CommonParameters</span></span>
<span data-ttu-id="bab4c-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bab4c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bab4c-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bab4c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bab4c-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bab4c-128">INPUTS</span></span>

## <span data-ttu-id="bab4c-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bab4c-129">OUTPUTS</span></span>

## <span data-ttu-id="bab4c-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bab4c-130">NOTES</span></span>

## <span data-ttu-id="bab4c-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bab4c-131">RELATED LINKS</span></span>

[<span data-ttu-id="bab4c-132">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="bab4c-132">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="bab4c-133">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="bab4c-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


