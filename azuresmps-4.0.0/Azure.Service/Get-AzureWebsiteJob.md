---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6B406310-287F-4BD3-BA38-A9C97E8EDC45
online version: ''
schema: 2.0.0
ms.openlocfilehash: d9f68ca1667e7b028c7646bf5a569e4e467c1b03
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099503"
---
# <span data-ttu-id="d00c2-101">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="d00c2-101">Get-AzureWebsiteJob</span></span>

## <span data-ttu-id="d00c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d00c2-102">SYNOPSIS</span></span>
<span data-ttu-id="d00c2-103">Hämtar de webb jobb som är kopplade till en webbplats.</span><span class="sxs-lookup"><span data-stu-id="d00c2-103">Gets the web jobs associated with a website.</span></span>

## <span data-ttu-id="d00c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d00c2-104">SYNTAX</span></span>

```
Get-AzureWebsiteJob [-JobName <String>] [-JobType <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d00c2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d00c2-105">DESCRIPTION</span></span>
<span data-ttu-id="d00c2-106">Hämtar de webb jobb som är kopplade till en webbplats.</span><span class="sxs-lookup"><span data-stu-id="d00c2-106">Gets the web jobs associated with a website.</span></span>

## <span data-ttu-id="d00c2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d00c2-107">EXAMPLES</span></span>

### <span data-ttu-id="d00c2-108">Exempel 1: få specifik information om webb jobbet</span><span class="sxs-lookup"><span data-stu-id="d00c2-108">Example 1: Get specific web job info</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="d00c2-109">Hämtar ett webb jobb som heter MyWebJob från en webbplats produktions plats.</span><span class="sxs-lookup"><span data-stu-id="d00c2-109">Gets a web job called MyWebJob from MyWebsite production slot.</span></span>

### <span data-ttu-id="d00c2-110">Exempel 2: Hämta alla webb jobb för en webbplats</span><span class="sxs-lookup"><span data-stu-id="d00c2-110">Example 2: Get all web jobs for a website</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite
```

<span data-ttu-id="d00c2-111">Hämtar alla webb jobb som är kopplade till en webbplats produktions plats.</span><span class="sxs-lookup"><span data-stu-id="d00c2-111">Gets all web jobs associated with MyWebsite production slot.</span></span>

### <span data-ttu-id="d00c2-112">Exempel 3: Hämta alla utlösta webb jobb</span><span class="sxs-lookup"><span data-stu-id="d00c2-112">Example 3: Get all triggered web jobs</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -Slot staging -Type Triggered
```

<span data-ttu-id="d00c2-113">Hämtar alla utlösta webb jobb från mellanlagringsplatsen för min webbplats.</span><span class="sxs-lookup"><span data-stu-id="d00c2-113">Gets all triggered web jobs from staging slot of MyWebsite.</span></span>

## <span data-ttu-id="d00c2-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d00c2-114">PARAMETERS</span></span>

### <span data-ttu-id="d00c2-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="d00c2-115">-JobName</span></span>
<span data-ttu-id="d00c2-116">Namn på webb jobbet</span><span class="sxs-lookup"><span data-stu-id="d00c2-116">The web job name</span></span>

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

### <span data-ttu-id="d00c2-117">-JobType</span><span class="sxs-lookup"><span data-stu-id="d00c2-117">-JobType</span></span>
<span data-ttu-id="d00c2-118">Webb jobb typen.</span><span class="sxs-lookup"><span data-stu-id="d00c2-118">The web job type.</span></span>
<span data-ttu-id="d00c2-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d00c2-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d00c2-120">Utlöses</span><span class="sxs-lookup"><span data-stu-id="d00c2-120">Triggered</span></span>
- <span data-ttu-id="d00c2-121">Ständig</span><span class="sxs-lookup"><span data-stu-id="d00c2-121">Continuous</span></span>

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

### <span data-ttu-id="d00c2-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="d00c2-122">-Name</span></span>
<span data-ttu-id="d00c2-123">Namnet på Azure-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="d00c2-123">The name of the Azure website.</span></span>

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

### <span data-ttu-id="d00c2-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="d00c2-124">-Profile</span></span>
<span data-ttu-id="d00c2-125">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="d00c2-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d00c2-126">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="d00c2-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d00c2-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="d00c2-127">-Slot</span></span>
<span data-ttu-id="d00c2-128">Plats namnet för Azure-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="d00c2-128">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="d00c2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d00c2-129">CommonParameters</span></span>
<span data-ttu-id="d00c2-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d00c2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d00c2-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d00c2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d00c2-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d00c2-132">INPUTS</span></span>

## <span data-ttu-id="d00c2-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d00c2-133">OUTPUTS</span></span>

## <span data-ttu-id="d00c2-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d00c2-134">NOTES</span></span>

## <span data-ttu-id="d00c2-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d00c2-135">RELATED LINKS</span></span>

[<span data-ttu-id="d00c2-136">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d00c2-136">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="d00c2-137">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="d00c2-137">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="d00c2-138">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="d00c2-138">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="d00c2-139">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="d00c2-139">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="d00c2-140">Stopp-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="d00c2-140">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)


