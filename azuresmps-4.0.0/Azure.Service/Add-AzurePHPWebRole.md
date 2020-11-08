---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F9A06B8B-55DB-48A5-B246-53347E759E64
online version: ''
schema: 2.0.0
ms.openlocfilehash: 050c05f2cdad546388744bcebca4f28a12a03038
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099620"
---
# <span data-ttu-id="7aeb4-101">Add-AzurePHPWebRole</span><span class="sxs-lookup"><span data-stu-id="7aeb4-101">Add-AzurePHPWebRole</span></span>

## <span data-ttu-id="7aeb4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7aeb4-102">SYNOPSIS</span></span>
<span data-ttu-id="7aeb4-103">Skapar nödvändiga filer och konfiguration för ett PHP-program.</span><span class="sxs-lookup"><span data-stu-id="7aeb4-103">Creates the required files and configuration for a PHP application.</span></span>

## <span data-ttu-id="7aeb4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7aeb4-104">SYNTAX</span></span>

```
Add-AzurePHPWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7aeb4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7aeb4-105">DESCRIPTION</span></span>
<span data-ttu-id="7aeb4-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="7aeb4-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7aeb4-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7aeb4-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7aeb4-108">Cmdleten **Add-AzurePHPWebRole** skapar filer och konfigurationer, som ibland kallas för scaffolding, för ett PHP-program som hanteras i Azure via IIS.</span><span class="sxs-lookup"><span data-stu-id="7aeb4-108">The **Add-AzurePHPWebRole** cmdlet creates the files and configuration, sometimes referred to as scaffolding, for a PHP application that will be hosted in Azure through IIS.</span></span>

## <span data-ttu-id="7aeb4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7aeb4-109">EXAMPLES</span></span>

### <span data-ttu-id="7aeb4-110">Exempel 1: lägga till en webb roll med standardvärden</span><span class="sxs-lookup"><span data-stu-id="7aeb4-110">Example 1: Add a web role using default values</span></span>
```
PS C:\> Add-AzurePHPWebRole
```

<span data-ttu-id="7aeb4-111">I det här exemplet läggs nödvändiga filer och konfiguration för ny webb roll till med standardvärdena för en tjänst med namnet "WebRole1" med 1 instans.</span><span class="sxs-lookup"><span data-stu-id="7aeb4-111">This example adds the required files and configuration for new web role using the default values of a service named "WebRole1" with 1 instance.</span></span>

### <span data-ttu-id="7aeb4-112">Exempel 2: lägga till en webb roll med flera instanser</span><span class="sxs-lookup"><span data-stu-id="7aeb4-112">Example 2: Add a web role with multiple instances</span></span>
```
PS C:\> Add-AzurePHPWebRole MyWebRole -I 2
```

<span data-ttu-id="7aeb4-113">I det här exemplet läggs nödvändiga filer och inställningar till för den nya webb rollen till det aktuella programmet, med namnet "MyWebRole" och en roll instans räkning på 2.</span><span class="sxs-lookup"><span data-stu-id="7aeb4-113">This example adds the required files and configuration for a new web role to the current application, using the name "MyWebRole" and a role instance count of 2.</span></span>

## <span data-ttu-id="7aeb4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7aeb4-114">PARAMETERS</span></span>

### <span data-ttu-id="7aeb4-115">-Instanser</span><span class="sxs-lookup"><span data-stu-id="7aeb4-115">-Instances</span></span>
<span data-ttu-id="7aeb4-116">Anger antalet roll instanser för webb rollen.</span><span class="sxs-lookup"><span data-stu-id="7aeb4-116">Specifies the number of role instances for this web role.</span></span>
<span data-ttu-id="7aeb4-117">Standardvärdet är 1.</span><span class="sxs-lookup"><span data-stu-id="7aeb4-117">The default is 1.</span></span>

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

### <span data-ttu-id="7aeb4-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="7aeb4-118">-Name</span></span>
<span data-ttu-id="7aeb4-119">Anger namnet på webb rollen.</span><span class="sxs-lookup"><span data-stu-id="7aeb4-119">Specifies the name of the web role.</span></span>
<span data-ttu-id="7aeb4-120">Namnet bestämmer namnet på den katalog som innehåller de nödvändiga filerna och konfigurationen för PHP-programmet.</span><span class="sxs-lookup"><span data-stu-id="7aeb4-120">The name determines the name of the directory that contains the required files and configuration for the PHP application.</span></span>
<span data-ttu-id="7aeb4-121">Standardvärdet för webrole #, där # är antalet webb roller i tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7aeb4-121">The default is WebRole#, where # is the number of web roles in the service.</span></span>

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

### <span data-ttu-id="7aeb4-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="7aeb4-122">-Profile</span></span>
<span data-ttu-id="7aeb4-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="7aeb4-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7aeb4-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="7aeb4-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7aeb4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aeb4-125">CommonParameters</span></span>
<span data-ttu-id="7aeb4-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7aeb4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aeb4-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7aeb4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aeb4-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7aeb4-128">INPUTS</span></span>

## <span data-ttu-id="7aeb4-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7aeb4-129">OUTPUTS</span></span>

## <span data-ttu-id="7aeb4-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7aeb4-130">NOTES</span></span>

## <span data-ttu-id="7aeb4-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7aeb4-131">RELATED LINKS</span></span>

[<span data-ttu-id="7aeb4-132">Add-AzurePHPWorkerRole</span><span class="sxs-lookup"><span data-stu-id="7aeb4-132">Add-AzurePHPWorkerRole</span></span>](./Add-AzurePHPWorkerRole.md)

[<span data-ttu-id="7aeb4-133">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="7aeb4-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


