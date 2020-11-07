---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 85479392a34e81395d3f00e3ef3891772a2dcbec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747469"
---
# <span data-ttu-id="2a3c1-101">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2a3c1-101">Get-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="2a3c1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a3c1-102">SYNOPSIS</span></span>
<span data-ttu-id="2a3c1-103">Hämtar information om det angivna ASR-jobbet eller listan över senaste ASR-jobb i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="2a3c1-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="2a3c1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a3c1-104">SYNTAX</span></span>

### <span data-ttu-id="2a3c1-105">ByParam (standard)</span><span class="sxs-lookup"><span data-stu-id="2a3c1-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a3c1-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2a3c1-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a3c1-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="2a3c1-107">ByObject</span></span>
```
Get-AzRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a3c1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a3c1-108">DESCRIPTION</span></span>
<span data-ttu-id="2a3c1-109">Cmdleten **Get-AzRecoveryServicesAsrJob** får Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="2a3c1-109">The **Get-AzRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="2a3c1-110">Du kan använda denna cmdlet för att Visa ASR-jobben i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="2a3c1-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="2a3c1-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a3c1-111">EXAMPLES</span></span>

### <span data-ttu-id="2a3c1-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2a3c1-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="2a3c1-113">Returnerar alla jobb i ett visst ASR-objekt (refererar till det ASR-objekt, till exempel ett replikerat objekt eller en återställnings plan efter ID).</span><span class="sxs-lookup"><span data-stu-id="2a3c1-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="2a3c1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a3c1-114">PARAMETERS</span></span>

### <span data-ttu-id="2a3c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a3c1-115">-DefaultProfile</span></span>
<span data-ttu-id="2a3c1-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2a3c1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2a3c1-117">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="2a3c1-117">-EndTime</span></span>
<span data-ttu-id="2a3c1-118">Anger slut tiden för jobben.</span><span class="sxs-lookup"><span data-stu-id="2a3c1-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="2a3c1-119">Denna cmdlet hämtar alla jobb som startade före angiven tid.</span><span class="sxs-lookup"><span data-stu-id="2a3c1-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="2a3c1-120">Om du vill hämta ett **datetime** -objekt för den här parametern använder du Get-Date cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a3c1-120">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="2a3c1-121">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="2a3c1-121">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="2a3c1-122">-Jobb</span><span class="sxs-lookup"><span data-stu-id="2a3c1-122">-Job</span></span>
<span data-ttu-id="2a3c1-123">Anger ASR-jobbet för att få uppdaterad information om.</span><span class="sxs-lookup"><span data-stu-id="2a3c1-123">Specifies the ASR job object to get updated details for.</span></span>

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

### <span data-ttu-id="2a3c1-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="2a3c1-124">-Name</span></span>
<span data-ttu-id="2a3c1-125">Ange ASR-jobbet efter namn.</span><span class="sxs-lookup"><span data-stu-id="2a3c1-125">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="2a3c1-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2a3c1-126">-StartTime</span></span>
<span data-ttu-id="2a3c1-127">Anger start tiden för jobben.</span><span class="sxs-lookup"><span data-stu-id="2a3c1-127">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="2a3c1-128">Denna cmdlet hämtar alla jobb som startas efter den angivna tiden.</span><span class="sxs-lookup"><span data-stu-id="2a3c1-128">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="2a3c1-129">-State</span><span class="sxs-lookup"><span data-stu-id="2a3c1-129">-State</span></span>
<span data-ttu-id="2a3c1-130">Anger tillståndet för ett ASR-jobb.</span><span class="sxs-lookup"><span data-stu-id="2a3c1-130">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="2a3c1-131">Denna cmdlet hämtar alla jobb som matchar det angivna tillståndet.</span><span class="sxs-lookup"><span data-stu-id="2a3c1-131">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="2a3c1-132">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="2a3c1-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2a3c1-133">NotStarted</span><span class="sxs-lookup"><span data-stu-id="2a3c1-133">NotStarted</span></span>
- <span data-ttu-id="2a3c1-134">Inaktive</span><span class="sxs-lookup"><span data-stu-id="2a3c1-134">InProgress</span></span>
- <span data-ttu-id="2a3c1-135">Utför</span><span class="sxs-lookup"><span data-stu-id="2a3c1-135">Succeeded</span></span>
- <span data-ttu-id="2a3c1-136">Övrigt</span><span class="sxs-lookup"><span data-stu-id="2a3c1-136">Other</span></span>
- <span data-ttu-id="2a3c1-137">Startade</span><span class="sxs-lookup"><span data-stu-id="2a3c1-137">Failed</span></span>
- <span data-ttu-id="2a3c1-138">Annullerats</span><span class="sxs-lookup"><span data-stu-id="2a3c1-138">Cancelled</span></span>
- <span data-ttu-id="2a3c1-139">Hängande</span><span class="sxs-lookup"><span data-stu-id="2a3c1-139">Suspended</span></span>

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

### <span data-ttu-id="2a3c1-140">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="2a3c1-140">-TargetObjectId</span></span>
<span data-ttu-id="2a3c1-141">Anger ID för objektet.</span><span class="sxs-lookup"><span data-stu-id="2a3c1-141">Specifies the ID of the object.</span></span> <span data-ttu-id="2a3c1-142">Används för att söka efter jobb på angivet objekt.</span><span class="sxs-lookup"><span data-stu-id="2a3c1-142">Used to search for jobs on the specified object.</span></span>

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

### <span data-ttu-id="2a3c1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a3c1-143">CommonParameters</span></span>
<span data-ttu-id="2a3c1-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a3c1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a3c1-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a3c1-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a3c1-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a3c1-146">INPUTS</span></span>

### <span data-ttu-id="2a3c1-147">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2a3c1-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2a3c1-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a3c1-148">OUTPUTS</span></span>

### <span data-ttu-id="2a3c1-149">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2a3c1-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2a3c1-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a3c1-150">NOTES</span></span>

## <span data-ttu-id="2a3c1-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a3c1-151">RELATED LINKS</span></span>

[<span data-ttu-id="2a3c1-152">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2a3c1-152">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="2a3c1-153">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2a3c1-153">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="2a3c1-154">Stopp-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2a3c1-154">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
