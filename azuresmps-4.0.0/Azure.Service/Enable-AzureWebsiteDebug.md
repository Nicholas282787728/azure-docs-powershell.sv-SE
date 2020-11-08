---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1FB590D3-E5D2-45F0-A611-01A1B701938A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 89d0c4dd73e5d921eb447e213876d8906c210b34
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099604"
---
# <span data-ttu-id="5ec33-101">Enable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="5ec33-101">Enable-AzureWebsiteDebug</span></span>

## <span data-ttu-id="5ec33-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ec33-102">SYNOPSIS</span></span>
<span data-ttu-id="5ec33-103">Aktiverar fel sökning för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="5ec33-103">Enables the website's debug.</span></span>

## <span data-ttu-id="5ec33-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ec33-104">SYNTAX</span></span>

```
Enable-AzureWebsiteDebug [-PassThru] -Version <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5ec33-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ec33-105">DESCRIPTION</span></span>
<span data-ttu-id="5ec33-106">Aktiverar fel söknings funktionen i Visual Studio för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="5ec33-106">Enables the website's debug feature in Visual Studio.</span></span>

## <span data-ttu-id="5ec33-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ec33-107">EXAMPLES</span></span>

### <span data-ttu-id="5ec33-108">Aktivera fel sökning av Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="5ec33-108">Enable debugging of Visual Studio 2013</span></span>
```
PS C:\> Enable-AzureWebsiteDebug -Name MyWebsite -Version VS2013
```

<span data-ttu-id="5ec33-109">Aktiverar fel sökning i VS 2013.</span><span class="sxs-lookup"><span data-stu-id="5ec33-109">Enables debugging on VS 2013.</span></span>

## <span data-ttu-id="5ec33-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ec33-110">PARAMETERS</span></span>

### <span data-ttu-id="5ec33-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="5ec33-111">-Name</span></span>
<span data-ttu-id="5ec33-112">Namnet på Azure-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="5ec33-112">The name of the Azure website.</span></span>

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

### <span data-ttu-id="5ec33-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ec33-113">-PassThru</span></span>
<span data-ttu-id="5ec33-114">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="5ec33-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5ec33-115">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="5ec33-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5ec33-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="5ec33-116">-Profile</span></span>
<span data-ttu-id="5ec33-117">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="5ec33-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5ec33-118">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="5ec33-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5ec33-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="5ec33-119">-Slot</span></span>
<span data-ttu-id="5ec33-120">Plats namnet för Azure-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="5ec33-120">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="5ec33-121">-Version</span><span class="sxs-lookup"><span data-stu-id="5ec33-121">-Version</span></span>
<span data-ttu-id="5ec33-122">Visual Studio-versionen.</span><span class="sxs-lookup"><span data-stu-id="5ec33-122">The Visual Studio version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ec33-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ec33-123">CommonParameters</span></span>
<span data-ttu-id="5ec33-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ec33-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ec33-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ec33-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ec33-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ec33-126">INPUTS</span></span>

## <span data-ttu-id="5ec33-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ec33-127">OUTPUTS</span></span>

## <span data-ttu-id="5ec33-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ec33-128">NOTES</span></span>

## <span data-ttu-id="5ec33-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ec33-129">RELATED LINKS</span></span>

[<span data-ttu-id="5ec33-130">Disable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="5ec33-130">Disable-AzureWebsiteDebug</span></span>](./Disable-AzureWebsiteDebug.md)

[<span data-ttu-id="5ec33-131">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="5ec33-131">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="5ec33-132">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="5ec33-132">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="5ec33-133">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="5ec33-133">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="5ec33-134">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="5ec33-134">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


