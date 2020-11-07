---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: b71c9a5da3c89916b18bdb5446f311e3d71615bf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925786"
---
# <span data-ttu-id="62bd3-101">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="62bd3-101">Get-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="62bd3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62bd3-102">SYNOPSIS</span></span>
<span data-ttu-id="62bd3-103">Hämtar information om det angivna ASR-jobbet eller listan över senaste ASR-jobb i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="62bd3-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="62bd3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62bd3-104">SYNTAX</span></span>

### <span data-ttu-id="62bd3-105">ByParam (standard)</span><span class="sxs-lookup"><span data-stu-id="62bd3-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62bd3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="62bd3-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62bd3-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="62bd3-107">ByObject</span></span>
```
Get-AzRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62bd3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62bd3-108">DESCRIPTION</span></span>
<span data-ttu-id="62bd3-109">Cmdleten **Get-AzRecoveryServicesAsrJob** får Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="62bd3-109">The **Get-AzRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="62bd3-110">Du kan använda denna cmdlet för att Visa ASR-jobben i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="62bd3-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="62bd3-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62bd3-111">EXAMPLES</span></span>

### <span data-ttu-id="62bd3-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="62bd3-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="62bd3-113">Returnerar alla jobb i ett visst ASR-objekt (refererar till det ASR-objekt, till exempel ett replikerat objekt eller en återställnings plan efter ID).</span><span class="sxs-lookup"><span data-stu-id="62bd3-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="62bd3-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62bd3-114">PARAMETERS</span></span>

### <span data-ttu-id="62bd3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62bd3-115">-DefaultProfile</span></span>
<span data-ttu-id="62bd3-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="62bd3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bd3-117">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="62bd3-117">-EndTime</span></span>
<span data-ttu-id="62bd3-118">Anger slut tiden för jobben.</span><span class="sxs-lookup"><span data-stu-id="62bd3-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="62bd3-119">Denna cmdlet hämtar alla jobb som startade före angiven tid.</span><span class="sxs-lookup"><span data-stu-id="62bd3-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="62bd3-120">Om du vill hämta ett **datetime** -objekt för den här parametern använder du Get-Date cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62bd3-120">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="62bd3-121">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="62bd3-121">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bd3-122">-Jobb</span><span class="sxs-lookup"><span data-stu-id="62bd3-122">-Job</span></span>
<span data-ttu-id="62bd3-123">Anger ASR-jobbet för att få uppdaterad information om.</span><span class="sxs-lookup"><span data-stu-id="62bd3-123">Specifies the ASR job object to get updated details for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62bd3-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="62bd3-124">-Name</span></span>
<span data-ttu-id="62bd3-125">Ange ASR-jobbet efter namn.</span><span class="sxs-lookup"><span data-stu-id="62bd3-125">Specify the ASR job by name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bd3-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="62bd3-126">-StartTime</span></span>
<span data-ttu-id="62bd3-127">Anger start tiden för jobben.</span><span class="sxs-lookup"><span data-stu-id="62bd3-127">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="62bd3-128">Denna cmdlet hämtar alla jobb som startas efter den angivna tiden.</span><span class="sxs-lookup"><span data-stu-id="62bd3-128">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bd3-129">-State</span><span class="sxs-lookup"><span data-stu-id="62bd3-129">-State</span></span>
<span data-ttu-id="62bd3-130">Anger tillståndet för ett ASR-jobb.</span><span class="sxs-lookup"><span data-stu-id="62bd3-130">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="62bd3-131">Denna cmdlet hämtar alla jobb som matchar det angivna tillståndet.</span><span class="sxs-lookup"><span data-stu-id="62bd3-131">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="62bd3-132">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="62bd3-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="62bd3-133">NotStarted</span><span class="sxs-lookup"><span data-stu-id="62bd3-133">NotStarted</span></span>
- <span data-ttu-id="62bd3-134">Inaktive</span><span class="sxs-lookup"><span data-stu-id="62bd3-134">InProgress</span></span>
- <span data-ttu-id="62bd3-135">Utför</span><span class="sxs-lookup"><span data-stu-id="62bd3-135">Succeeded</span></span>
- <span data-ttu-id="62bd3-136">Övrigt</span><span class="sxs-lookup"><span data-stu-id="62bd3-136">Other</span></span>
- <span data-ttu-id="62bd3-137">Startade</span><span class="sxs-lookup"><span data-stu-id="62bd3-137">Failed</span></span>
- <span data-ttu-id="62bd3-138">Annullerats</span><span class="sxs-lookup"><span data-stu-id="62bd3-138">Cancelled</span></span>
- <span data-ttu-id="62bd3-139">Hängande</span><span class="sxs-lookup"><span data-stu-id="62bd3-139">Suspended</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bd3-140">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="62bd3-140">-TargetObjectId</span></span>
<span data-ttu-id="62bd3-141">Anger ID för objektet.</span><span class="sxs-lookup"><span data-stu-id="62bd3-141">Specifies the ID of the object.</span></span> <span data-ttu-id="62bd3-142">Används för att söka efter jobb på angivet objekt.</span><span class="sxs-lookup"><span data-stu-id="62bd3-142">Used to search for jobs on the specified object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bd3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62bd3-143">CommonParameters</span></span>
<span data-ttu-id="62bd3-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62bd3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62bd3-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62bd3-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62bd3-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62bd3-146">INPUTS</span></span>

### <span data-ttu-id="62bd3-147">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="62bd3-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="62bd3-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62bd3-148">OUTPUTS</span></span>

### <span data-ttu-id="62bd3-149">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="62bd3-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="62bd3-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62bd3-150">NOTES</span></span>

## <span data-ttu-id="62bd3-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62bd3-151">RELATED LINKS</span></span>

[<span data-ttu-id="62bd3-152">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="62bd3-152">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="62bd3-153">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="62bd3-153">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="62bd3-154">Stopp-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="62bd3-154">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
