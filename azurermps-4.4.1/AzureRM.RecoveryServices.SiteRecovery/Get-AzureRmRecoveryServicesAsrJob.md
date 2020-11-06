---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: afef81ad904ccd5bf53f0b2a09bb10511e71fca1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584568"
---
# <span data-ttu-id="f7525-101">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f7525-101">Get-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="f7525-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f7525-102">SYNOPSIS</span></span>
<span data-ttu-id="f7525-103">Hämtar information om det angivna ASR-jobbet eller listan över senaste ASR-jobb i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="f7525-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7525-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f7525-104">SYNTAX</span></span>

### <span data-ttu-id="f7525-105">ByParam (standard)</span><span class="sxs-lookup"><span data-stu-id="f7525-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [<CommonParameters>]
```

### <span data-ttu-id="f7525-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f7525-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="f7525-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="f7525-107">ByObject</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Job <ASRJob> [<CommonParameters>]
```

## <span data-ttu-id="f7525-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f7525-108">DESCRIPTION</span></span>
<span data-ttu-id="f7525-109">Cmdleten **Get-AzureRmRecoveryServicesAsrJob** får Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="f7525-109">The **Get-AzureRmRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="f7525-110">Du kan använda denna cmdlet för att Visa ASR-jobben i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="f7525-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="f7525-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f7525-111">EXAMPLES</span></span>

### <span data-ttu-id="f7525-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f7525-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzureRmRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="f7525-113">Returnerar alla jobb i ett visst ASR-objekt (refererar till det ASR-objekt, till exempel ett replikerat objekt eller en återställnings plan efter ID).</span><span class="sxs-lookup"><span data-stu-id="f7525-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="f7525-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f7525-114">PARAMETERS</span></span>

### <span data-ttu-id="f7525-115">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="f7525-115">-EndTime</span></span>
<span data-ttu-id="f7525-116">Anger slut tiden för jobben.</span><span class="sxs-lookup"><span data-stu-id="f7525-116">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="f7525-117">Denna cmdlet hämtar alla jobb som startade före angiven tid.</span><span class="sxs-lookup"><span data-stu-id="f7525-117">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="f7525-118">Om du vill hämta ett **datetime** -objekt för den här parametern använder du Get-Date cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7525-118">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="f7525-119">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="f7525-119">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7525-120">-Jobb</span><span class="sxs-lookup"><span data-stu-id="f7525-120">-Job</span></span>
<span data-ttu-id="f7525-121">Anger ASR-jobbet för att få uppdaterad information om.</span><span class="sxs-lookup"><span data-stu-id="f7525-121">Specifies the ASR job object to get updated details for.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7525-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="f7525-122">-Name</span></span>
<span data-ttu-id="f7525-123">Ange ASR-jobbet efter namn.</span><span class="sxs-lookup"><span data-stu-id="f7525-123">Specify the ASR job by name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7525-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f7525-124">-StartTime</span></span>
<span data-ttu-id="f7525-125">Anger start tiden för jobben.</span><span class="sxs-lookup"><span data-stu-id="f7525-125">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="f7525-126">Denna cmdlet hämtar alla jobb som startas efter den angivna tiden.</span><span class="sxs-lookup"><span data-stu-id="f7525-126">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7525-127">-State</span><span class="sxs-lookup"><span data-stu-id="f7525-127">-State</span></span>
<span data-ttu-id="f7525-128">Anger tillståndet för ett ASR-jobb.</span><span class="sxs-lookup"><span data-stu-id="f7525-128">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="f7525-129">Denna cmdlet hämtar alla jobb som matchar det angivna tillståndet.</span><span class="sxs-lookup"><span data-stu-id="f7525-129">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="f7525-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f7525-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f7525-131">NotStarted</span><span class="sxs-lookup"><span data-stu-id="f7525-131">NotStarted</span></span>
- <span data-ttu-id="f7525-132">Inaktive</span><span class="sxs-lookup"><span data-stu-id="f7525-132">InProgress</span></span>
- <span data-ttu-id="f7525-133">Utför</span><span class="sxs-lookup"><span data-stu-id="f7525-133">Succeeded</span></span>
- <span data-ttu-id="f7525-134">Övrigt</span><span class="sxs-lookup"><span data-stu-id="f7525-134">Other</span></span>
- <span data-ttu-id="f7525-135">Startade</span><span class="sxs-lookup"><span data-stu-id="f7525-135">Failed</span></span>
- <span data-ttu-id="f7525-136">Annullerats</span><span class="sxs-lookup"><span data-stu-id="f7525-136">Cancelled</span></span>
- <span data-ttu-id="f7525-137">Hängande</span><span class="sxs-lookup"><span data-stu-id="f7525-137">Suspended</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7525-138">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="f7525-138">-TargetObjectId</span></span>
<span data-ttu-id="f7525-139">Anger ID för objektet.</span><span class="sxs-lookup"><span data-stu-id="f7525-139">Specifies the ID of the object.</span></span> <span data-ttu-id="f7525-140">Används för att söka efter jobb på angivet objekt.</span><span class="sxs-lookup"><span data-stu-id="f7525-140">Used to search for jobs on the specified object.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7525-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7525-141">CommonParameters</span></span>
<span data-ttu-id="f7525-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7525-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7525-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7525-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7525-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f7525-144">INPUTS</span></span>

### <span data-ttu-id="f7525-145">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f7525-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f7525-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f7525-146">OUTPUTS</span></span>

### <span data-ttu-id="f7525-147">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f7525-147">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f7525-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f7525-148">NOTES</span></span>

## <span data-ttu-id="f7525-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f7525-149">RELATED LINKS</span></span>

[<span data-ttu-id="f7525-150">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f7525-150">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="f7525-151">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f7525-151">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="f7525-152">Stopp-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f7525-152">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
