---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A2CBF963-1FAE-41B0-964E-EFF52076AB32
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c4bb84111b8ec22b1b529622e61ca476cf6081b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099737"
---
# <span data-ttu-id="65980-101">Get-AzureWebsiteJobHistory</span><span class="sxs-lookup"><span data-stu-id="65980-101">Get-AzureWebsiteJobHistory</span></span>

## <span data-ttu-id="65980-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65980-102">SYNOPSIS</span></span>
<span data-ttu-id="65980-103">Hämtar en historik för ett webb jobb.</span><span class="sxs-lookup"><span data-stu-id="65980-103">Gets a web job history.</span></span>

## <span data-ttu-id="65980-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65980-104">SYNTAX</span></span>

### <span data-ttu-id="65980-105">HistoryParameterSetName</span><span class="sxs-lookup"><span data-stu-id="65980-105">HistoryParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="65980-106">RunIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="65980-106">RunIdParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> -RunId <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="65980-107">LatestParameterSetName</span><span class="sxs-lookup"><span data-stu-id="65980-107">LatestParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> [-Latest] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="65980-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65980-108">DESCRIPTION</span></span>
<span data-ttu-id="65980-109">Hämtar en historik för ett webb jobb.</span><span class="sxs-lookup"><span data-stu-id="65980-109">Gets a web job history.</span></span>

## <span data-ttu-id="65980-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65980-110">EXAMPLES</span></span>

### <span data-ttu-id="65980-111">Exempel 1: få fullständig historik för ett webb jobb</span><span class="sxs-lookup"><span data-stu-id="65980-111">Example 1: Get complete history for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="65980-112">Hämtar fullständig historik för MyWebJob.</span><span class="sxs-lookup"><span data-stu-id="65980-112">Gets complete history for MyWebJob.</span></span>

### <span data-ttu-id="65980-113">Exempel 2: Hämta senaste körningen för ett webb jobb</span><span class="sxs-lookup"><span data-stu-id="65980-113">Example 2: Get latest run for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob -Latest
```

<span data-ttu-id="65980-114">Hämtar den senaste kör-informationen för MyWebJob.</span><span class="sxs-lookup"><span data-stu-id="65980-114">Gets latest run info for MyWebJob.</span></span>

### <span data-ttu-id="65980-115">Exempel 3: få specifik kör för ett webb jobb</span><span class="sxs-lookup"><span data-stu-id="65980-115">Example 3: Get specific run for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob -RunId 10
```

<span data-ttu-id="65980-116">Hämtar all information om hur man kör med ID 10 för MyWebJob.</span><span class="sxs-lookup"><span data-stu-id="65980-116">Gets all info about run with id 10 for MyWebJob.</span></span>

## <span data-ttu-id="65980-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65980-117">PARAMETERS</span></span>

### <span data-ttu-id="65980-118">-JobName</span><span class="sxs-lookup"><span data-stu-id="65980-118">-JobName</span></span>
<span data-ttu-id="65980-119">Namnet på webb jobbet.</span><span class="sxs-lookup"><span data-stu-id="65980-119">The web job name.</span></span>

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

### <span data-ttu-id="65980-120">-Senaste</span><span class="sxs-lookup"><span data-stu-id="65980-120">-Latest</span></span>
<span data-ttu-id="65980-121">Returnera den senaste kör-historiken om den anges.</span><span class="sxs-lookup"><span data-stu-id="65980-121">If specified, return the latest run history.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LatestParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65980-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="65980-122">-Name</span></span>
<span data-ttu-id="65980-123">Namnet på Azure-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="65980-123">The name of the Azure website.</span></span>

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

### <span data-ttu-id="65980-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="65980-124">-Profile</span></span>
<span data-ttu-id="65980-125">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="65980-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="65980-126">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="65980-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="65980-127">-RunId</span><span class="sxs-lookup"><span data-stu-id="65980-127">-RunId</span></span>
<span data-ttu-id="65980-128">Anger ID för den kör historik som du vill visa.</span><span class="sxs-lookup"><span data-stu-id="65980-128">Specifies the ID of the run history you want to see.</span></span>

```yaml
Type: String
Parameter Sets: RunIdParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65980-129">-Plats</span><span class="sxs-lookup"><span data-stu-id="65980-129">-Slot</span></span>
<span data-ttu-id="65980-130">Plats namnet för Azure-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="65980-130">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="65980-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65980-131">CommonParameters</span></span>
<span data-ttu-id="65980-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65980-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65980-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65980-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65980-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65980-134">INPUTS</span></span>

## <span data-ttu-id="65980-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65980-135">OUTPUTS</span></span>

## <span data-ttu-id="65980-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65980-136">NOTES</span></span>

## <span data-ttu-id="65980-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65980-137">RELATED LINKS</span></span>

[<span data-ttu-id="65980-138">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="65980-138">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="65980-139">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="65980-139">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="65980-140">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="65980-140">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="65980-141">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="65980-141">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="65980-142">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="65980-142">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)


