---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A66ADA39-56D9-421B-BC69-996253352236
online version: ''
schema: 2.0.0
ms.openlocfilehash: b5b2cfaea544b5a8575715ec89735b5b9a1ad28f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093493"
---
# <span data-ttu-id="429e2-101">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="429e2-101">Start-AzureWebsiteJob</span></span>

## <span data-ttu-id="429e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="429e2-102">SYNOPSIS</span></span>
<span data-ttu-id="429e2-103">Startar ett webb jobb för en webbplats.</span><span class="sxs-lookup"><span data-stu-id="429e2-103">Starts a web job for a website.</span></span>

## <span data-ttu-id="429e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="429e2-104">SYNTAX</span></span>

```
Start-AzureWebsiteJob -JobName <String> -JobType <WebJobType> [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="429e2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="429e2-105">DESCRIPTION</span></span>
<span data-ttu-id="429e2-106">Cmdleten **Start-AzureWebsiteJob** startar ett webb jobb för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="429e2-106">The **Start-AzureWebsiteJob** cmdlet starts a web job for a website.</span></span>

## <span data-ttu-id="429e2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="429e2-107">EXAMPLES</span></span>

### <span data-ttu-id="429e2-108">Exempel 1: starta ett webb jobb för en webbplats</span><span class="sxs-lookup"><span data-stu-id="429e2-108">Example 1: Start a web job for a website</span></span>
```
PS C:\> Start-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous
```

<span data-ttu-id="429e2-109">Startar ett webb jobb med namnet MyWebJob för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="429e2-109">Starts a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="429e2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="429e2-110">PARAMETERS</span></span>

### <span data-ttu-id="429e2-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="429e2-111">-JobName</span></span>
<span data-ttu-id="429e2-112">Namnet på webb jobbet.</span><span class="sxs-lookup"><span data-stu-id="429e2-112">The web job name.</span></span>

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

### <span data-ttu-id="429e2-113">-JobType</span><span class="sxs-lookup"><span data-stu-id="429e2-113">-JobType</span></span>
<span data-ttu-id="429e2-114">Webb jobb typen.</span><span class="sxs-lookup"><span data-stu-id="429e2-114">The web job type.</span></span>
<span data-ttu-id="429e2-115">Kan utlösas eller fort löp ande.</span><span class="sxs-lookup"><span data-stu-id="429e2-115">Can be triggered or continuous.</span></span>

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

### <span data-ttu-id="429e2-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="429e2-116">-Name</span></span>
<span data-ttu-id="429e2-117">Namnet på Azure-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="429e2-117">The name of the Azure website.</span></span>

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

### <span data-ttu-id="429e2-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="429e2-118">-PassThru</span></span>
<span data-ttu-id="429e2-119">Returnerar ett booleskt värde som anger att jobbet startade.</span><span class="sxs-lookup"><span data-stu-id="429e2-119">Returns a boolean value indicating that the job started successfully.</span></span>
<span data-ttu-id="429e2-120">Denna cmdlet returnerar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="429e2-120">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="429e2-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="429e2-121">-Profile</span></span>
<span data-ttu-id="429e2-122">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="429e2-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="429e2-123">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="429e2-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="429e2-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="429e2-124">-Slot</span></span>
<span data-ttu-id="429e2-125">Plats namnet för Azure-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="429e2-125">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="429e2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="429e2-126">CommonParameters</span></span>
<span data-ttu-id="429e2-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="429e2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="429e2-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="429e2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="429e2-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="429e2-129">INPUTS</span></span>

## <span data-ttu-id="429e2-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="429e2-130">OUTPUTS</span></span>

## <span data-ttu-id="429e2-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="429e2-131">NOTES</span></span>

## <span data-ttu-id="429e2-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="429e2-132">RELATED LINKS</span></span>

[<span data-ttu-id="429e2-133">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="429e2-133">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="429e2-134">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="429e2-134">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="429e2-135">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="429e2-135">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="429e2-136">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="429e2-136">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="429e2-137">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="429e2-137">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)


