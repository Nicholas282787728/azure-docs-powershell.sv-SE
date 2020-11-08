---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 545CAB1C-F08C-4472-A41A-1FE900D2EDA5
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc8ae51b2f239fd9ec7f09fe27e08ccdaa41c4bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093208"
---
# <span data-ttu-id="7c0a5-101">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="7c0a5-101">Remove-AzureWebsiteJob</span></span>

## <span data-ttu-id="7c0a5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7c0a5-102">SYNOPSIS</span></span>
<span data-ttu-id="7c0a5-103">Tar bort ett befintligt webb jobb för en webbplats.</span><span class="sxs-lookup"><span data-stu-id="7c0a5-103">Removes an existing web job for a website.</span></span>

## <span data-ttu-id="7c0a5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7c0a5-104">SYNTAX</span></span>

```
Remove-AzureWebsiteJob -JobName <String> -JobType <WebJobType> [-Force] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7c0a5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7c0a5-105">DESCRIPTION</span></span>
<span data-ttu-id="7c0a5-106">Tar bort ett befintligt webb jobb för en webbplats.</span><span class="sxs-lookup"><span data-stu-id="7c0a5-106">Removes an existing web job for a website.</span></span>

## <span data-ttu-id="7c0a5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7c0a5-107">EXAMPLES</span></span>

### <span data-ttu-id="7c0a5-108">Exempel 1: ta bort ett befintligt webb jobb för en webbplats</span><span class="sxs-lookup"><span data-stu-id="7c0a5-108">Example 1: Remove an existing web job for a website</span></span>
```
PS C:\> Remove-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous
```

<span data-ttu-id="7c0a5-109">Tar bort ett webb jobb som heter MyWebJob för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="7c0a5-109">Removes a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="7c0a5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7c0a5-110">PARAMETERS</span></span>

### <span data-ttu-id="7c0a5-111">-Force</span><span class="sxs-lookup"><span data-stu-id="7c0a5-111">-Force</span></span>
<span data-ttu-id="7c0a5-112">Anger att denna cmdlet tar bort webb jobbet utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="7c0a5-112">Indicates that this cmdlet removes the web job without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="7c0a5-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="7c0a5-113">-JobName</span></span>
<span data-ttu-id="7c0a5-114">Namnet på webb jobbet.</span><span class="sxs-lookup"><span data-stu-id="7c0a5-114">The web job name.</span></span>

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

### <span data-ttu-id="7c0a5-115">-JobType</span><span class="sxs-lookup"><span data-stu-id="7c0a5-115">-JobType</span></span>
<span data-ttu-id="7c0a5-116">Webb jobb typen.</span><span class="sxs-lookup"><span data-stu-id="7c0a5-116">The web job type.</span></span>
<span data-ttu-id="7c0a5-117">Kan utlösas eller fort löp ande.</span><span class="sxs-lookup"><span data-stu-id="7c0a5-117">Can be triggered or continuous.</span></span>

```yaml
Type: WebJobType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c0a5-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="7c0a5-118">-Name</span></span>
<span data-ttu-id="7c0a5-119">Namnet på Azure-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="7c0a5-119">The name of the Azure website.</span></span>

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

### <span data-ttu-id="7c0a5-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="7c0a5-120">-Profile</span></span>
<span data-ttu-id="7c0a5-121">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="7c0a5-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7c0a5-122">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="7c0a5-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7c0a5-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="7c0a5-123">-Slot</span></span>
<span data-ttu-id="7c0a5-124">Plats namnet för Azure-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="7c0a5-124">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="7c0a5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c0a5-125">CommonParameters</span></span>
<span data-ttu-id="7c0a5-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c0a5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c0a5-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c0a5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c0a5-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7c0a5-128">INPUTS</span></span>

## <span data-ttu-id="7c0a5-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7c0a5-129">OUTPUTS</span></span>

## <span data-ttu-id="7c0a5-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7c0a5-130">NOTES</span></span>

## <span data-ttu-id="7c0a5-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7c0a5-131">RELATED LINKS</span></span>

[<span data-ttu-id="7c0a5-132">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7c0a5-132">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="7c0a5-133">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="7c0a5-133">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="7c0a5-134">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="7c0a5-134">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="7c0a5-135">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="7c0a5-135">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="7c0a5-136">Stopp-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="7c0a5-136">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)


