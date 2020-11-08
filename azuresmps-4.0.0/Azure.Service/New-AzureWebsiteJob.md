---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1254A28B-F670-44B2-BB0E-BD41B9483E3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1910a0da546bdc4d5b167d82685608669b7565c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099413"
---
# <span data-ttu-id="dc2df-101">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="dc2df-101">New-AzureWebsiteJob</span></span>

## <span data-ttu-id="dc2df-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dc2df-102">SYNOPSIS</span></span>
<span data-ttu-id="dc2df-103">Skapar ett webb jobb för en webbplats.</span><span class="sxs-lookup"><span data-stu-id="dc2df-103">Creates a web job for a website.</span></span>

## <span data-ttu-id="dc2df-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dc2df-104">SYNTAX</span></span>

```
New-AzureWebsiteJob -JobName <String> -JobType <WebJobType> -JobFile <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dc2df-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dc2df-105">DESCRIPTION</span></span>
<span data-ttu-id="dc2df-106">Cmdleten **New-AzureWebsiteJob** skapar ett webb jobb för en webbplats.</span><span class="sxs-lookup"><span data-stu-id="dc2df-106">The **New-AzureWebsiteJob** cmdlet creates a web job for a website.</span></span>

## <span data-ttu-id="dc2df-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dc2df-107">EXAMPLES</span></span>

### <span data-ttu-id="dc2df-108">Exempel 1: skapa ett nytt webb jobb för en webbplats</span><span class="sxs-lookup"><span data-stu-id="dc2df-108">Example 1: Create new web job for a website</span></span>
```
PS C:\> New-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous -JobFile job.bat
```

<span data-ttu-id="dc2df-109">Skapar ett fort löp ande jobb för att ringa job.bat webbplatsen webbplats.</span><span class="sxs-lookup"><span data-stu-id="dc2df-109">Creates a continuous job to call job.bat on website MyWebsite.</span></span>

## <span data-ttu-id="dc2df-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dc2df-110">PARAMETERS</span></span>

### <span data-ttu-id="dc2df-111">-JobFile</span><span class="sxs-lookup"><span data-stu-id="dc2df-111">-JobFile</span></span>
<span data-ttu-id="dc2df-112">Webb filen.</span><span class="sxs-lookup"><span data-stu-id="dc2df-112">The web job file.</span></span>

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

### <span data-ttu-id="dc2df-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="dc2df-113">-JobName</span></span>
<span data-ttu-id="dc2df-114">Namnet på webb jobbet.</span><span class="sxs-lookup"><span data-stu-id="dc2df-114">The web job name.</span></span>

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

### <span data-ttu-id="dc2df-115">-JobType</span><span class="sxs-lookup"><span data-stu-id="dc2df-115">-JobType</span></span>
<span data-ttu-id="dc2df-116">Webb jobb typen.</span><span class="sxs-lookup"><span data-stu-id="dc2df-116">The web job type.</span></span>
<span data-ttu-id="dc2df-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="dc2df-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dc2df-118">Utlöses</span><span class="sxs-lookup"><span data-stu-id="dc2df-118">Triggered</span></span> 
- <span data-ttu-id="dc2df-119">Ständig</span><span class="sxs-lookup"><span data-stu-id="dc2df-119">Continuous</span></span>

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

### <span data-ttu-id="dc2df-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="dc2df-120">-Name</span></span>
<span data-ttu-id="dc2df-121">Namnet på Azure-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="dc2df-121">The name of the Azure website.</span></span>

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

### <span data-ttu-id="dc2df-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="dc2df-122">-Profile</span></span>
<span data-ttu-id="dc2df-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="dc2df-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dc2df-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="dc2df-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dc2df-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="dc2df-125">-Slot</span></span>
<span data-ttu-id="dc2df-126">Plats namnet för Azure-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="dc2df-126">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="dc2df-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc2df-127">CommonParameters</span></span>
<span data-ttu-id="dc2df-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc2df-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc2df-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc2df-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc2df-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dc2df-130">INPUTS</span></span>

## <span data-ttu-id="dc2df-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dc2df-131">OUTPUTS</span></span>

## <span data-ttu-id="dc2df-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dc2df-132">NOTES</span></span>

## <span data-ttu-id="dc2df-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dc2df-133">RELATED LINKS</span></span>

[<span data-ttu-id="dc2df-134">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="dc2df-134">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="dc2df-135">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="dc2df-135">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="dc2df-136">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="dc2df-136">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="dc2df-137">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="dc2df-137">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="dc2df-138">Stopp-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="dc2df-138">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)


