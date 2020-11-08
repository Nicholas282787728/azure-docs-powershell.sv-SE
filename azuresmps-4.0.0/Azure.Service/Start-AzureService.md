---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 821CB3E4-102E-440A-8C92-D1890899A6EE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 64924d579eebb826bc9c36468da1617370f48cf7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099260"
---
# <span data-ttu-id="27587-101">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="27587-101">Start-AzureService</span></span>

## <span data-ttu-id="27587-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="27587-102">SYNOPSIS</span></span>
<span data-ttu-id="27587-103">Startar den angivna värdbaserade tjänsten i Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="27587-103">Starts the specified hosted service in Windows Azure.</span></span>

## <span data-ttu-id="27587-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="27587-104">SYNTAX</span></span>

```
Start-AzureService [-ServiceName <String>] [-Slot <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="27587-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="27587-105">DESCRIPTION</span></span>
<span data-ttu-id="27587-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="27587-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="27587-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="27587-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="27587-108">Cmdleten **Start-AzureService** startar den angivna värdbaserade tjänsten i Windows Azure, om tjänsten är i stoppat tillstånd.</span><span class="sxs-lookup"><span data-stu-id="27587-108">The **Start-AzureService** cmdlet starts the specified hosted service in Windows Azure, if the service is in the stopped state.</span></span>
<span data-ttu-id="27587-109">Observera att cmdleten **AzureServiceProject** automatiskt försöker starta tjänsten.</span><span class="sxs-lookup"><span data-stu-id="27587-109">Note that the **Publish-AzureServiceProject** cmdlet automatically attempts to start the service.</span></span>

## <span data-ttu-id="27587-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="27587-110">EXAMPLES</span></span>

## <span data-ttu-id="27587-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="27587-111">PARAMETERS</span></span>

### <span data-ttu-id="27587-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27587-112">-PassThru</span></span>
<span data-ttu-id="27587-113">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="27587-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="27587-114">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="27587-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="27587-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="27587-115">-Profile</span></span>
<span data-ttu-id="27587-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="27587-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="27587-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="27587-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="27587-118">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="27587-118">-ServiceName</span></span>
<span data-ttu-id="27587-119">Anger namnet på den värdbaserade tjänst som ska startas.</span><span class="sxs-lookup"><span data-stu-id="27587-119">Specifies the name of the hosted service to start.</span></span>
<span data-ttu-id="27587-120">Om du inte anger något namn startas den aktuella värdbaserade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="27587-120">If no name is specified, the cmdlet starts the current hosted service.</span></span>

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

### <span data-ttu-id="27587-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="27587-121">-Slot</span></span>
<span data-ttu-id="27587-122">Anger distributions platsen där tjänsten ska startas, antingen för produktion eller produktion.</span><span class="sxs-lookup"><span data-stu-id="27587-122">Specifies the deployment slot in which to start the service, either Staging or Production.</span></span>

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

### <span data-ttu-id="27587-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27587-123">CommonParameters</span></span>
<span data-ttu-id="27587-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27587-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27587-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27587-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27587-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="27587-126">INPUTS</span></span>

## <span data-ttu-id="27587-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="27587-127">OUTPUTS</span></span>

## <span data-ttu-id="27587-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="27587-128">NOTES</span></span>

## <span data-ttu-id="27587-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="27587-129">RELATED LINKS</span></span>

[<span data-ttu-id="27587-130">Remove-AzureService</span><span class="sxs-lookup"><span data-stu-id="27587-130">Remove-AzureService</span></span>](./Remove-AzureService.md)

[<span data-ttu-id="27587-131">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="27587-131">Start-AzureService</span></span>](./Start-AzureService.md)

[<span data-ttu-id="27587-132">Stopp-AzureService</span><span class="sxs-lookup"><span data-stu-id="27587-132">Stop-AzureService</span></span>](./Stop-AzureService.md)


