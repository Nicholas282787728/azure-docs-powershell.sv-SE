---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7F6EEF0-8896-4639-89A8-810F19161211
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4b32c031a91adc3ab56e06898a1aa8ad70ac4e8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093196"
---
# <span data-ttu-id="d8999-101">Restart-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d8999-101">Restart-AzureWebsite</span></span>

## <span data-ttu-id="d8999-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8999-102">SYNOPSIS</span></span>
<span data-ttu-id="d8999-103">Stoppar och startar sedan om den angivna webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="d8999-103">Stops and then restarts the specified website.</span></span>

## <span data-ttu-id="d8999-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8999-104">SYNTAX</span></span>

```
Restart-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8999-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8999-105">DESCRIPTION</span></span>
<span data-ttu-id="d8999-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="d8999-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d8999-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d8999-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d8999-108">Cmdleten **restart-AzureWebsite** stoppar och startar sedan om den angivna webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="d8999-108">The **Restart-AzureWebsite** cmdlet stops and then restarts the specified website.</span></span>

## <span data-ttu-id="d8999-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8999-109">EXAMPLES</span></span>

### <span data-ttu-id="d8999-110">Exempel 1: starta om en webbplats</span><span class="sxs-lookup"><span data-stu-id="d8999-110">Example 1: Restart a website</span></span>
```
PS C:\> Restart-AzureWebsite -Name MyWebsite
```

<span data-ttu-id="d8999-111">I det här exemplet startas en webbplats som heter min webbplats.</span><span class="sxs-lookup"><span data-stu-id="d8999-111">This example restarts a website named MyWebsite.</span></span>

## <span data-ttu-id="d8999-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8999-112">PARAMETERS</span></span>

### <span data-ttu-id="d8999-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="d8999-113">-Name</span></span>
<span data-ttu-id="d8999-114">Anger namnet på den Azure-webbplats som ska startas om.</span><span class="sxs-lookup"><span data-stu-id="d8999-114">Specifies the name of the Azure website to restart.</span></span>

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

### <span data-ttu-id="d8999-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8999-115">-PassThru</span></span>
<span data-ttu-id="d8999-116">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="d8999-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d8999-117">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="d8999-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d8999-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="d8999-118">-Profile</span></span>
<span data-ttu-id="d8999-119">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="d8999-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d8999-120">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="d8999-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d8999-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="d8999-121">-Slot</span></span>
<span data-ttu-id="d8999-122">Anger webbplatsens namn.</span><span class="sxs-lookup"><span data-stu-id="d8999-122">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="d8999-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8999-123">CommonParameters</span></span>
<span data-ttu-id="d8999-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8999-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8999-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8999-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8999-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8999-126">INPUTS</span></span>

## <span data-ttu-id="d8999-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8999-127">OUTPUTS</span></span>

## <span data-ttu-id="d8999-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8999-128">NOTES</span></span>

## <span data-ttu-id="d8999-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8999-129">RELATED LINKS</span></span>

[<span data-ttu-id="d8999-130">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d8999-130">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="d8999-131">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d8999-131">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="d8999-132">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d8999-132">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="d8999-133">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d8999-133">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


