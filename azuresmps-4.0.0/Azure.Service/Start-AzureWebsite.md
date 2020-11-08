---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A9542EA9-C709-48D7-8066-496015AB977E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c1e7aab4f7818cbfc7200b521a535d54fb08dc0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093496"
---
# <span data-ttu-id="61e8d-101">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="61e8d-101">Start-AzureWebsite</span></span>

## <span data-ttu-id="61e8d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="61e8d-102">SYNOPSIS</span></span>
<span data-ttu-id="61e8d-103">Startar den angivna webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="61e8d-103">Starts the specified website.</span></span>

## <span data-ttu-id="61e8d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="61e8d-104">SYNTAX</span></span>

```
Start-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="61e8d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="61e8d-105">DESCRIPTION</span></span>
<span data-ttu-id="61e8d-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="61e8d-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="61e8d-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="61e8d-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="61e8d-108">Cmdleten **Start-AzureWebsite** startar en angiven webbplats som körs i Azure.</span><span class="sxs-lookup"><span data-stu-id="61e8d-108">The **Start-AzureWebsite** cmdlet starts a specified website running in Azure.</span></span>

## <span data-ttu-id="61e8d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="61e8d-109">EXAMPLES</span></span>

## <span data-ttu-id="61e8d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="61e8d-110">PARAMETERS</span></span>

### <span data-ttu-id="61e8d-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="61e8d-111">-Name</span></span>
<span data-ttu-id="61e8d-112">Anger namnet på den webbplats som ska startas.</span><span class="sxs-lookup"><span data-stu-id="61e8d-112">Specifies the name of the website to start.</span></span>

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

### <span data-ttu-id="61e8d-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61e8d-113">-PassThru</span></span>
<span data-ttu-id="61e8d-114">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="61e8d-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="61e8d-115">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="61e8d-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="61e8d-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="61e8d-116">-Profile</span></span>
<span data-ttu-id="61e8d-117">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="61e8d-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="61e8d-118">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="61e8d-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="61e8d-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="61e8d-119">-Slot</span></span>
<span data-ttu-id="61e8d-120">Anger webbplatsens namn.</span><span class="sxs-lookup"><span data-stu-id="61e8d-120">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="61e8d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61e8d-121">CommonParameters</span></span>
<span data-ttu-id="61e8d-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61e8d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61e8d-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61e8d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61e8d-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="61e8d-124">INPUTS</span></span>

## <span data-ttu-id="61e8d-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="61e8d-125">OUTPUTS</span></span>

## <span data-ttu-id="61e8d-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="61e8d-126">NOTES</span></span>

## <span data-ttu-id="61e8d-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="61e8d-127">RELATED LINKS</span></span>

[<span data-ttu-id="61e8d-128">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="61e8d-128">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="61e8d-129">Restart-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="61e8d-129">Restart-AzureWebsite</span></span>](./Restart-AzureWebsite.md)

[<span data-ttu-id="61e8d-130">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="61e8d-130">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)

[<span data-ttu-id="61e8d-131">Show-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="61e8d-131">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)

[<span data-ttu-id="61e8d-132">Stopp-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="61e8d-132">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


