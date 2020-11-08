---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7785F288-1CDF-444E-B72F-597E75B76074
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1e6e6d9921710bbed81eab727d2fe60927d2ed7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099015"
---
# <span data-ttu-id="7e968-101">Show-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7e968-101">Show-AzureWebsite</span></span>

## <span data-ttu-id="7e968-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e968-102">SYNOPSIS</span></span>
<span data-ttu-id="7e968-103">Öppnar en webbläsare på en angiven webbplats.</span><span class="sxs-lookup"><span data-stu-id="7e968-103">Opens a browser on a specified website.</span></span>

## <span data-ttu-id="7e968-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e968-104">SYNTAX</span></span>

```
Show-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7e968-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e968-105">DESCRIPTION</span></span>
<span data-ttu-id="7e968-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="7e968-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7e968-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7e968-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7e968-108">Cmdleten **show-AzureWebsite** öppnar en webbläsare på en angiven webbplats.</span><span class="sxs-lookup"><span data-stu-id="7e968-108">The **Show-AzureWebsite** cmdlet opens a browser on a specified website.</span></span>

## <span data-ttu-id="7e968-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e968-109">EXAMPLES</span></span>

## <span data-ttu-id="7e968-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e968-110">PARAMETERS</span></span>

### <span data-ttu-id="7e968-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="7e968-111">-Name</span></span>
<span data-ttu-id="7e968-112">Anger namnet på den webbplats som ska öppnas i webbläsaren.</span><span class="sxs-lookup"><span data-stu-id="7e968-112">Specifies the name of the site to open in the browser.</span></span>

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

### <span data-ttu-id="7e968-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="7e968-113">-Profile</span></span>
<span data-ttu-id="7e968-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="7e968-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7e968-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="7e968-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7e968-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="7e968-116">-Slot</span></span>
<span data-ttu-id="7e968-117">Anger webbplatsens namn.</span><span class="sxs-lookup"><span data-stu-id="7e968-117">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="7e968-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e968-118">CommonParameters</span></span>
<span data-ttu-id="7e968-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e968-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e968-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e968-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e968-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e968-121">INPUTS</span></span>

## <span data-ttu-id="7e968-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e968-122">OUTPUTS</span></span>

## <span data-ttu-id="7e968-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e968-123">NOTES</span></span>

## <span data-ttu-id="7e968-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e968-124">RELATED LINKS</span></span>

[<span data-ttu-id="7e968-125">Show-AzurePortal</span><span class="sxs-lookup"><span data-stu-id="7e968-125">Show-AzurePortal</span></span>](./Show-AzurePortal.md)

[<span data-ttu-id="7e968-126">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7e968-126">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="7e968-127">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7e968-127">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="7e968-128">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7e968-128">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="7e968-129">Restart-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7e968-129">Restart-AzureWebsite</span></span>](./Restart-AzureWebsite.md)

[<span data-ttu-id="7e968-130">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7e968-130">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


