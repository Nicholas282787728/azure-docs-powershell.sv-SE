---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AE26EA0F-9D92-4FDF-92EF-CA33BF06C0DB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68a97359e5181bbc27183c0c1dbb6f526fa2e529
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099306"
---
# <span data-ttu-id="9299c-101">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9299c-101">Restart-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="9299c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9299c-102">SYNOPSIS</span></span>
<span data-ttu-id="9299c-103">Startar om återställnings jobbet för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="9299c-103">Restarts a Site Recovery job.</span></span>

## <span data-ttu-id="9299c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9299c-104">SYNTAX</span></span>

### <span data-ttu-id="9299c-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="9299c-105">ByObject (Default)</span></span>
```
Restart-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9299c-106">ById</span><span class="sxs-lookup"><span data-stu-id="9299c-106">ById</span></span>
```
Restart-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9299c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9299c-107">DESCRIPTION</span></span>
<span data-ttu-id="9299c-108">Cmdleten **restart-AzureSiteRecoveryJob** startar om ett Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="9299c-108">The **Restart-AzureSiteRecoveryJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="9299c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9299c-109">EXAMPLES</span></span>

### <span data-ttu-id="9299c-110">Exempel 1: starta om ett jobb</span><span class="sxs-lookup"><span data-stu-id="9299c-110">Example 1: Restart a job</span></span>
```
PS C:\> Restart-AzureSiteRecoveryJob -Id "bbf0b839-9aaa-49e1-8354-601c9145966d"
ID               : bbf0b839-9aaa-49e1-8354-601c9145966d
ClientRequestId  : ef42c8b0-640c-4442-960b-349f83d161a5-2014-24-06 14:24:04Z-P
State            : Failed
StateDescription : Failed
StartTime        : 10/6/2014 9:41:08 AM
EndTime          : 10/6/2014 9:41:21 AM
AllowedActions   : {Cancel, Restart}
Name             : Enable protection
Tasks            : {Prerequisites check for enabling protection , Identifying replication target, Enable replication, 
                   Starting initial replication...} 
Errors           : {CreateProtectionTargetTask}
```

<span data-ttu-id="9299c-111">Det här kommandot startar om jobbet med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="9299c-111">This command restarts the job that has the specified ID.</span></span>

## <span data-ttu-id="9299c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9299c-112">PARAMETERS</span></span>

### <span data-ttu-id="9299c-113">-ID</span><span class="sxs-lookup"><span data-stu-id="9299c-113">-Id</span></span>
<span data-ttu-id="9299c-114">Anger ID för det jobb som ska startas om.</span><span class="sxs-lookup"><span data-stu-id="9299c-114">Specifies the ID of the job to restart.</span></span>

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

### <span data-ttu-id="9299c-115">-Jobb</span><span class="sxs-lookup"><span data-stu-id="9299c-115">-Job</span></span>
<span data-ttu-id="9299c-116">Anger vilket jobb som ska startas om.</span><span class="sxs-lookup"><span data-stu-id="9299c-116">Specifies the job to restart.</span></span>

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

### <span data-ttu-id="9299c-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="9299c-117">-Profile</span></span>
<span data-ttu-id="9299c-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="9299c-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9299c-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="9299c-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9299c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9299c-120">CommonParameters</span></span>
<span data-ttu-id="9299c-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9299c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9299c-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9299c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9299c-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9299c-123">INPUTS</span></span>

## <span data-ttu-id="9299c-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9299c-124">OUTPUTS</span></span>

## <span data-ttu-id="9299c-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9299c-125">NOTES</span></span>

## <span data-ttu-id="9299c-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9299c-126">RELATED LINKS</span></span>

[<span data-ttu-id="9299c-127">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9299c-127">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="9299c-128">Resume-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9299c-128">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="9299c-129">Stopp-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9299c-129">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


