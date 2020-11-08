---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4696BB05-F507-4FFB-8D96-6BAA2EBB0F0A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 03acdfb16c7f1e7e8ee5e6b95902ef1ed056412a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093184"
---
# <span data-ttu-id="99fe3-101">Save-AzureWebsiteLog</span><span class="sxs-lookup"><span data-stu-id="99fe3-101">Save-AzureWebsiteLog</span></span>

## <span data-ttu-id="99fe3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="99fe3-102">SYNOPSIS</span></span>
<span data-ttu-id="99fe3-103">Laddar ned och sparar loggarna för en viss webbplats.</span><span class="sxs-lookup"><span data-stu-id="99fe3-103">Downloads and saves the logs for a specified website.</span></span>

## <span data-ttu-id="99fe3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="99fe3-104">SYNTAX</span></span>

```
Save-AzureWebsiteLog [-Output <String>] [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="99fe3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="99fe3-105">DESCRIPTION</span></span>
<span data-ttu-id="99fe3-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="99fe3-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="99fe3-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="99fe3-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="99fe3-108">Cmdleten **Save-AzureWebsiteLog** laddar ned loggarna för en viss webbplats.</span><span class="sxs-lookup"><span data-stu-id="99fe3-108">The **Save-AzureWebsiteLog** cmdlet downloads the logs for a specified website.</span></span>

## <span data-ttu-id="99fe3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="99fe3-109">EXAMPLES</span></span>

### <span data-ttu-id="99fe3-110">Exempel 1: Ladda ned och Spara loggar för en webbplats</span><span class="sxs-lookup"><span data-stu-id="99fe3-110">Example 1: Download and save logs for a website</span></span>
```
PS C:\> Save-AzureWebsiteLogs -Name mySite -Output .\logs.zip
```

<span data-ttu-id="99fe3-111">I det här exemplet hämtas körnings-och distributions loggar för webbplatsen min webbplats till filen logs.zip i den aktuella katalogen.</span><span class="sxs-lookup"><span data-stu-id="99fe3-111">This example downloads the runtime and deployment logs for website mySite to the file logs.zip in the current directory.</span></span>

## <span data-ttu-id="99fe3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="99fe3-112">PARAMETERS</span></span>

### <span data-ttu-id="99fe3-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="99fe3-113">-Name</span></span>
<span data-ttu-id="99fe3-114">Anger namnet på webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="99fe3-114">Specifies the name of the website.</span></span>

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

### <span data-ttu-id="99fe3-115">-Utdata</span><span class="sxs-lookup"><span data-stu-id="99fe3-115">-Output</span></span>
<span data-ttu-id="99fe3-116">Anger sökvägen för att lagra den hämtade filen.</span><span class="sxs-lookup"><span data-stu-id="99fe3-116">Specifies the path to store the downloaded file.</span></span>

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

### <span data-ttu-id="99fe3-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99fe3-117">-PassThru</span></span>
<span data-ttu-id="99fe3-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="99fe3-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="99fe3-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="99fe3-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="99fe3-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="99fe3-120">-Profile</span></span>
<span data-ttu-id="99fe3-121">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="99fe3-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="99fe3-122">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="99fe3-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="99fe3-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="99fe3-123">-Slot</span></span>
<span data-ttu-id="99fe3-124">Anger plats namnet.</span><span class="sxs-lookup"><span data-stu-id="99fe3-124">Specifies the slot name.</span></span>

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

### <span data-ttu-id="99fe3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99fe3-125">CommonParameters</span></span>
<span data-ttu-id="99fe3-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99fe3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99fe3-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99fe3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99fe3-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="99fe3-128">INPUTS</span></span>

## <span data-ttu-id="99fe3-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="99fe3-129">OUTPUTS</span></span>

## <span data-ttu-id="99fe3-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="99fe3-130">NOTES</span></span>

## <span data-ttu-id="99fe3-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="99fe3-131">RELATED LINKS</span></span>

[<span data-ttu-id="99fe3-132">Återställ-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="99fe3-132">Restore-AzureWebsiteDeployment</span></span>](./Restore-AzureWebsiteDeployment.md)


