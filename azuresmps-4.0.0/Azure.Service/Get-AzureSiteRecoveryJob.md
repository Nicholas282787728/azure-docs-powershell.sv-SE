---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2957C0DE-3A2F-4337-A778-2B95654972E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d0b272732cf6c1e1b2025c8e7f48b58e4807cdb3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093321"
---
# <span data-ttu-id="0761e-101">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="0761e-101">Get-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="0761e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0761e-102">SYNOPSIS</span></span>
<span data-ttu-id="0761e-103">Hämtar åtgärds informationen för ett webbplats återställnings valv.</span><span class="sxs-lookup"><span data-stu-id="0761e-103">Gets the operation information for a Site Recovery vault.</span></span>

## <span data-ttu-id="0761e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0761e-104">SYNTAX</span></span>

### <span data-ttu-id="0761e-105">ByParam (standard)</span><span class="sxs-lookup"><span data-stu-id="0761e-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0761e-106">ById</span><span class="sxs-lookup"><span data-stu-id="0761e-106">ById</span></span>
```
Get-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0761e-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="0761e-107">ByObject</span></span>
```
Get-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0761e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0761e-108">DESCRIPTION</span></span>
<span data-ttu-id="0761e-109">Cmdleten **Get-AzureSiteRecoveryJob** får Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="0761e-109">The **Get-AzureSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="0761e-110">Du kan använda denna cmdlet för att Visa åtgärds informationen för det aktuella Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="0761e-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="0761e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0761e-111">EXAMPLES</span></span>

### <span data-ttu-id="0761e-112">Exempel 1: Hämta ett jobb genom att ange ett ID</span><span class="sxs-lookup"><span data-stu-id="0761e-112">Example 1: Get a job by specifying an ID</span></span>
```
PS C:\> Get-AzureSiteRecoveryJob -Id "033785cc-9f72-4f07-8e78-e4d1e942a7ae" 
Name             : SaveRecoveryPlan
ID               : 033785cc-9f72-4f07-8e78-e4d1e942a7ae
ClientRequestId  : d604206b-32e1-4d5b-9a23-32b118d14a1e-2015-02-20 07:20:42Z-P
State            : Succeeded
StateDescription : Completed
StartTime        : 20-02-2015 07:20:45 +05:30
EndTime          : 20-02-2015 07:20:46 +05:30
TargetObjectId   : cfb445bf-fd14-4b5d-b9ac-5154e1415ef2
TargetObjectType : RecoveryPlan
TargetObjectName : RP
AllowedActions   : {Cancel}
Tasks            : {Save a recovery plan task}
Errors           : {}
```

<span data-ttu-id="0761e-113">Det här kommandot får Azure Site Recovery-jobbet med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="0761e-113">This command gets the  Azure Site Recovery job that has the specified ID.</span></span>

### <span data-ttu-id="0761e-114">Exempel 2: hämtar ett jobb baserat på tid</span><span class="sxs-lookup"><span data-stu-id="0761e-114">Example 2: Gets a job based on time</span></span>
```
PS C:\> Get-AzureSiteRecoveryJob -StartTime "20-02-2015 01:00:00" -EndTime "21-02-2015 01:00:00"
Name             : SaveRecoveryPlan
ID               : 033785cc-9f72-4f07-8e78-e4d1e942a7ae
ClientRequestId  : d604206b-32e1-4d5b-9a23-32b118d14a1e-2015-02-20 07:20:42Z-P
State            : Succeeded
StateDescription : Completed
StartTime        : 20-02-2015 07:20:45 +05:30
EndTime          : 20-02-2015 07:20:46 +05:30
TargetObjectId   : cfb445bf-fd14-4b5d-b9ac-5154e1415ef2
TargetObjectType : RecoveryPlan
TargetObjectName : RP
AllowedActions   : {Cancel}
Tasks            : {Save a recovery plan task}
Errors           : {}
```

<span data-ttu-id="0761e-115">Det här kommandot får plats återställnings jobb som faller mellan angiven start tid och slut tid.</span><span class="sxs-lookup"><span data-stu-id="0761e-115">This command gets Site Recovery jobs that fall between the specified start time and end time.</span></span>

## <span data-ttu-id="0761e-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0761e-116">PARAMETERS</span></span>

### <span data-ttu-id="0761e-117">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="0761e-117">-EndTime</span></span>
<span data-ttu-id="0761e-118">Anger slut tiden för jobben.</span><span class="sxs-lookup"><span data-stu-id="0761e-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="0761e-119">Denna cmdlet hämtar alla jobb som startade före angiven tid.</span><span class="sxs-lookup"><span data-stu-id="0761e-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="0761e-120">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="0761e-120">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="0761e-121">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="0761e-121">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="0761e-122">-ID</span><span class="sxs-lookup"><span data-stu-id="0761e-122">-Id</span></span>
<span data-ttu-id="0761e-123">Anger ID för det jobb som ska visas.</span><span class="sxs-lookup"><span data-stu-id="0761e-123">Specifies the ID of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0761e-124">-Jobb</span><span class="sxs-lookup"><span data-stu-id="0761e-124">-Job</span></span>
<span data-ttu-id="0761e-125">Anger ett jobb som ska visas.</span><span class="sxs-lookup"><span data-stu-id="0761e-125">Specifies a job to get.</span></span>

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

### <span data-ttu-id="0761e-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="0761e-126">-Profile</span></span>
<span data-ttu-id="0761e-127">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="0761e-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0761e-128">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="0761e-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0761e-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0761e-129">-StartTime</span></span>
<span data-ttu-id="0761e-130">Anger start tiden för jobben.</span><span class="sxs-lookup"><span data-stu-id="0761e-130">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="0761e-131">Denna cmdlet hämtar alla jobb som startas efter den angivna tiden.</span><span class="sxs-lookup"><span data-stu-id="0761e-131">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="0761e-132">-State</span><span class="sxs-lookup"><span data-stu-id="0761e-132">-State</span></span>
<span data-ttu-id="0761e-133">Anger inmatnings läget för ett webbplats återställnings jobb.</span><span class="sxs-lookup"><span data-stu-id="0761e-133">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="0761e-134">Denna cmdlet hämtar alla jobb som matchar det angivna tillståndet.</span><span class="sxs-lookup"><span data-stu-id="0761e-134">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="0761e-135">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0761e-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0761e-136">NotStarted</span><span class="sxs-lookup"><span data-stu-id="0761e-136">NotStarted</span></span>
- <span data-ttu-id="0761e-137">Inaktive</span><span class="sxs-lookup"><span data-stu-id="0761e-137">InProgress</span></span>
- <span data-ttu-id="0761e-138">Utför</span><span class="sxs-lookup"><span data-stu-id="0761e-138">Succeeded</span></span>
- <span data-ttu-id="0761e-139">Övrigt</span><span class="sxs-lookup"><span data-stu-id="0761e-139">Other</span></span>
- <span data-ttu-id="0761e-140">Startade</span><span class="sxs-lookup"><span data-stu-id="0761e-140">Failed</span></span>
- <span data-ttu-id="0761e-141">Annullerats</span><span class="sxs-lookup"><span data-stu-id="0761e-141">Cancelled</span></span>
- <span data-ttu-id="0761e-142">Hängande</span><span class="sxs-lookup"><span data-stu-id="0761e-142">Suspended</span></span>

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

### <span data-ttu-id="0761e-143">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="0761e-143">-TargetObjectId</span></span>
<span data-ttu-id="0761e-144">Anger ID för det objekt som är inriktat för jobbet.</span><span class="sxs-lookup"><span data-stu-id="0761e-144">Specifies the ID of the object targeted by the job.</span></span>

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

### <span data-ttu-id="0761e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0761e-145">CommonParameters</span></span>
<span data-ttu-id="0761e-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0761e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0761e-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0761e-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0761e-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0761e-148">INPUTS</span></span>

## <span data-ttu-id="0761e-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0761e-149">OUTPUTS</span></span>

## <span data-ttu-id="0761e-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0761e-150">NOTES</span></span>

## <span data-ttu-id="0761e-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0761e-151">RELATED LINKS</span></span>

[<span data-ttu-id="0761e-152">Azure Site Recovery Services-cmdletar</span><span class="sxs-lookup"><span data-stu-id="0761e-152">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)

[<span data-ttu-id="0761e-153">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="0761e-153">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="0761e-154">Resume-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="0761e-154">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="0761e-155">Stopp-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="0761e-155">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


