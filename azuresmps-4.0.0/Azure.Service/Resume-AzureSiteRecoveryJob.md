---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: E214AFEB-90A6-4553-94D4-FBEA6ADE572E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ee340c2302670628bb8a3893567d7f8a2da754f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099670"
---
# <span data-ttu-id="4706b-101">Resume-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="4706b-101">Resume-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="4706b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4706b-102">SYNOPSIS</span></span>
<span data-ttu-id="4706b-103">Återupptar en pausad webbplats återställnings jobb.</span><span class="sxs-lookup"><span data-stu-id="4706b-103">Resumes a suspended Site Recovery job.</span></span>

## <span data-ttu-id="4706b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4706b-104">SYNTAX</span></span>

### <span data-ttu-id="4706b-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="4706b-105">ByObject (Default)</span></span>
```
Resume-AzureSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4706b-106">ById</span><span class="sxs-lookup"><span data-stu-id="4706b-106">ById</span></span>
```
Resume-AzureSiteRecoveryJob -Id <String> [-Comments <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4706b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4706b-107">DESCRIPTION</span></span>
<span data-ttu-id="4706b-108">Cmdleten **Resume-AzureSiteRecoveryJob** återupptar en pausad Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="4706b-108">The **Resume-AzureSiteRecoveryJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="4706b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4706b-109">EXAMPLES</span></span>

### <span data-ttu-id="4706b-110">Exempel 1: återuppta alla jobb</span><span class="sxs-lookup"><span data-stu-id="4706b-110">Example 1: Resume all jobs</span></span>
```
PS C:\> $Jobs = Get-AzureSiteRecoveryJob  
PS C:\> Resume-AzureSiteRecoveryJob -Job $Jobs
ID               : d16397fb-cdf1-4972-b677-c333f3c557b4
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : Suspended
StateDescription : WaitingForManualAction
StartTime        : 10/6/2014 10:19:28 AM
EndTime          : 10/6/2014 10:19:31 AM
AllowedActions   : {Cancel, RestartTestFailoverCleanup}
Name             : Test failover
Tasks            : {Recovery plan preflight checks, Create test environment, All groups failover: Pre steps (1), 
                   Recovery plan failover...} 
Errors           : {}
```

<span data-ttu-id="4706b-111">Det första kommandot får alla Azure Site Recovery-jobb för det aktuella Site Recovery-valvet med cmdleten **Get-AzureSiteRecoveryJob** och lagrar sedan resultatet i variabeln $Jobs.</span><span class="sxs-lookup"><span data-stu-id="4706b-111">The first command gets all the Azure Site Recovery jobs for the current Site Recovery vault by using the **Get-AzureSiteRecoveryJob** cmdlet, and then stores the results in the $Jobs variable.</span></span>

<span data-ttu-id="4706b-112">Det andra kommandot återupptar det jobb som anges av $Jobs.</span><span class="sxs-lookup"><span data-stu-id="4706b-112">The second command resumes the job specified by $Jobs.</span></span>

## <span data-ttu-id="4706b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4706b-113">PARAMETERS</span></span>

### <span data-ttu-id="4706b-114">-Kommentarer</span><span class="sxs-lookup"><span data-stu-id="4706b-114">-Comments</span></span>
<span data-ttu-id="4706b-115">Anger kommentarer för jobb loggen.</span><span class="sxs-lookup"><span data-stu-id="4706b-115">Specifies the comments for the job log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4706b-116">-ID</span><span class="sxs-lookup"><span data-stu-id="4706b-116">-Id</span></span>
<span data-ttu-id="4706b-117">Anger ID för ett jobb att fortsätta.</span><span class="sxs-lookup"><span data-stu-id="4706b-117">Specifies the ID of a job to resume.</span></span>

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

### <span data-ttu-id="4706b-118">-Jobb</span><span class="sxs-lookup"><span data-stu-id="4706b-118">-Job</span></span>
<span data-ttu-id="4706b-119">Anger vilket jobb som ska återupptas.</span><span class="sxs-lookup"><span data-stu-id="4706b-119">Specifies the job to resume.</span></span>

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

### <span data-ttu-id="4706b-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="4706b-120">-Profile</span></span>
<span data-ttu-id="4706b-121">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="4706b-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4706b-122">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="4706b-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4706b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4706b-123">CommonParameters</span></span>
<span data-ttu-id="4706b-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4706b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4706b-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4706b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4706b-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4706b-126">INPUTS</span></span>

## <span data-ttu-id="4706b-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4706b-127">OUTPUTS</span></span>

## <span data-ttu-id="4706b-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4706b-128">NOTES</span></span>

## <span data-ttu-id="4706b-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4706b-129">RELATED LINKS</span></span>

[<span data-ttu-id="4706b-130">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="4706b-130">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="4706b-131">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="4706b-131">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="4706b-132">Stopp-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="4706b-132">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


