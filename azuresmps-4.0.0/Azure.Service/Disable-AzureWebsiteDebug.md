---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2480FA03-09C6-4A4F-8DDD-01F6AFF6117E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3805794cdc6105112175e0524a894f571f8b5bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093417"
---
# <span data-ttu-id="d3f2d-101">Disable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="d3f2d-101">Disable-AzureWebsiteDebug</span></span>

## <span data-ttu-id="d3f2d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d3f2d-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f2d-103">Inaktiverar fel sökning av webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="d3f2d-103">Disables the website's debugging.</span></span>

## <span data-ttu-id="d3f2d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d3f2d-104">SYNTAX</span></span>

```
Disable-AzureWebsiteDebug [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3f2d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d3f2d-105">DESCRIPTION</span></span>
<span data-ttu-id="d3f2d-106">Inaktiverar fel sökning av webbplatsen i Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d3f2d-106">Disables the website's debugging in Visual Studio.</span></span>

## <span data-ttu-id="d3f2d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d3f2d-107">EXAMPLES</span></span>

### <span data-ttu-id="d3f2d-108">--------------Inaktivera fel sökning av webbplatser--------------</span><span class="sxs-lookup"><span data-stu-id="d3f2d-108">--------------  Disable website debugging --------------</span></span>
```
PS C:\> Disable-AzureWebsiteDebug -Name MyWebsite
```

<span data-ttu-id="d3f2d-109">Inaktiverar webbplats fel sökning på webbplatsen min webbplats</span><span class="sxs-lookup"><span data-stu-id="d3f2d-109">Disables website debugging on website MyWebsite</span></span>

## <span data-ttu-id="d3f2d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d3f2d-110">PARAMETERS</span></span>

### <span data-ttu-id="d3f2d-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="d3f2d-111">-Name</span></span>
<span data-ttu-id="d3f2d-112">Namnet på Azure-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="d3f2d-112">The name of the Azure website.</span></span>

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

### <span data-ttu-id="d3f2d-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3f2d-113">-PassThru</span></span>
<span data-ttu-id="d3f2d-114">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="d3f2d-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d3f2d-115">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="d3f2d-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d3f2d-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="d3f2d-116">-Profile</span></span>
<span data-ttu-id="d3f2d-117">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="d3f2d-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d3f2d-118">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="d3f2d-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d3f2d-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="d3f2d-119">-Slot</span></span>
<span data-ttu-id="d3f2d-120">Plats namnet för Azure-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="d3f2d-120">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="d3f2d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f2d-121">CommonParameters</span></span>
<span data-ttu-id="d3f2d-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3f2d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f2d-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3f2d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f2d-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d3f2d-124">INPUTS</span></span>

## <span data-ttu-id="d3f2d-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d3f2d-125">OUTPUTS</span></span>

## <span data-ttu-id="d3f2d-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d3f2d-126">NOTES</span></span>

## <span data-ttu-id="d3f2d-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d3f2d-127">RELATED LINKS</span></span>

[<span data-ttu-id="d3f2d-128">Enable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="d3f2d-128">Enable-AzureWebsiteDebug</span></span>](./Enable-AzureWebsiteDebug.md)

[<span data-ttu-id="d3f2d-129">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d3f2d-129">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="d3f2d-130">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d3f2d-130">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="d3f2d-131">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d3f2d-131">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="d3f2d-132">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d3f2d-132">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


