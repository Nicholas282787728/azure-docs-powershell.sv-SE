---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6313BAB9-32D1-4B4B-A0C7-345F20629505
online version: ''
schema: 2.0.0
ms.openlocfilehash: 73b461bb5dfd70576079d333366c50f5e6f56900
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099502"
---
# <span data-ttu-id="90757-101">Get-AzureWebsiteLocation</span><span class="sxs-lookup"><span data-stu-id="90757-101">Get-AzureWebsiteLocation</span></span>

## <span data-ttu-id="90757-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90757-102">SYNOPSIS</span></span>
<span data-ttu-id="90757-103">Hämtar alla tillgängliga webbplats platser.</span><span class="sxs-lookup"><span data-stu-id="90757-103">Gets all available website locations.</span></span>

## <span data-ttu-id="90757-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90757-104">SYNTAX</span></span>

```
Get-AzureWebsiteLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="90757-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90757-105">DESCRIPTION</span></span>
<span data-ttu-id="90757-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="90757-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="90757-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="90757-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="90757-108">Hämtar alla tillgängliga webbplats platser för det aktuella abonnemanget</span><span class="sxs-lookup"><span data-stu-id="90757-108">Gets all of the available website locations for the current subscription</span></span>

## <span data-ttu-id="90757-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90757-109">EXAMPLES</span></span>

### <span data-ttu-id="90757-110">Exempel 1: Hämta alla tillgängliga platser</span><span class="sxs-lookup"><span data-stu-id="90757-110">Example 1: Get all available locations</span></span>
```
PS C:\> Get-AzureWebsiteLocations
```

<span data-ttu-id="90757-111">Det här exemplet får alla tillgängliga webbplats platser för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="90757-111">This example gets all of the available website locations for the current subscription.</span></span>

## <span data-ttu-id="90757-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90757-112">PARAMETERS</span></span>

### <span data-ttu-id="90757-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="90757-113">-Profile</span></span>
<span data-ttu-id="90757-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="90757-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="90757-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="90757-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="90757-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90757-116">CommonParameters</span></span>
<span data-ttu-id="90757-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90757-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90757-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90757-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90757-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90757-119">INPUTS</span></span>

## <span data-ttu-id="90757-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90757-120">OUTPUTS</span></span>

## <span data-ttu-id="90757-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90757-121">NOTES</span></span>

## <span data-ttu-id="90757-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90757-122">RELATED LINKS</span></span>

[<span data-ttu-id="90757-123">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="90757-123">New-AzureWebsite</span></span>](./New-AzureWebsite.md)


