---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8FF1362B-C7AB-4769-A88B-D1B6E214A006
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf8275b8dfec4263c5ab7a8022dcb65edccb1171
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099637"
---
# <span data-ttu-id="9d9c7-101">Stop-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9d9c7-101">Stop-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="9d9c7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9d9c7-102">SYNOPSIS</span></span>
<span data-ttu-id="9d9c7-103">Stoppar ett återställnings jobb för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="9d9c7-103">Stops a Site Recovery job.</span></span>

## <span data-ttu-id="9d9c7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9d9c7-104">SYNTAX</span></span>

### <span data-ttu-id="9d9c7-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="9d9c7-105">ByObject (Default)</span></span>
```
Stop-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9d9c7-106">ById</span><span class="sxs-lookup"><span data-stu-id="9d9c7-106">ById</span></span>
```
Stop-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9d9c7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9d9c7-107">DESCRIPTION</span></span>
<span data-ttu-id="9d9c7-108">Cmdleten **Stop-AzureSiteRecoveryJob** stoppar ett Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="9d9c7-108">The **Stop-AzureSiteRecoveryJob** cmdlet stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="9d9c7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9d9c7-109">EXAMPLES</span></span>

### <span data-ttu-id="9d9c7-110">Exempel 1: stoppa alla jobb</span><span class="sxs-lookup"><span data-stu-id="9d9c7-110">Example 1: Stop all jobs</span></span>
```
PS C:\>$Jobs = Get-AzureSiteRecoveryJob 
PS C:\> Stop-AzureSiteRecoveryJob -Job $Jobs
```

<span data-ttu-id="9d9c7-111">Det första kommandot får Azure Site Recovery-jobb för det aktuella Azure Site Recovery-valvet med cmdleten **Get-AzureSiteRecoveryJob** och lagrar sedan resultatet i variabeln $Jobs.</span><span class="sxs-lookup"><span data-stu-id="9d9c7-111">The first command gets the Azure Site Recovery jobs for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryJob** cmdlet, and then stores the results in the $Jobs variable.</span></span>

<span data-ttu-id="9d9c7-112">Det andra kommandot stoppar de jobb som anges av $Jobs.</span><span class="sxs-lookup"><span data-stu-id="9d9c7-112">The second command stops the jobs specified by $Jobs.</span></span>

## <span data-ttu-id="9d9c7-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9d9c7-113">PARAMETERS</span></span>

### <span data-ttu-id="9d9c7-114">-ID</span><span class="sxs-lookup"><span data-stu-id="9d9c7-114">-Id</span></span>
<span data-ttu-id="9d9c7-115">Anger ID för jobbet som ska stoppas.</span><span class="sxs-lookup"><span data-stu-id="9d9c7-115">Specifies the ID of the job to stop.</span></span>

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

### <span data-ttu-id="9d9c7-116">-Jobb</span><span class="sxs-lookup"><span data-stu-id="9d9c7-116">-Job</span></span>
<span data-ttu-id="9d9c7-117">Anger vilket jobb som ska stoppas.</span><span class="sxs-lookup"><span data-stu-id="9d9c7-117">Specifies the job to stop.</span></span>

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

### <span data-ttu-id="9d9c7-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="9d9c7-118">-Profile</span></span>
<span data-ttu-id="9d9c7-119">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="9d9c7-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9d9c7-120">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="9d9c7-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9d9c7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d9c7-121">CommonParameters</span></span>
<span data-ttu-id="9d9c7-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d9c7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d9c7-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d9c7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d9c7-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9d9c7-124">INPUTS</span></span>

## <span data-ttu-id="9d9c7-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9d9c7-125">OUTPUTS</span></span>

## <span data-ttu-id="9d9c7-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9d9c7-126">NOTES</span></span>

## <span data-ttu-id="9d9c7-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9d9c7-127">RELATED LINKS</span></span>

[<span data-ttu-id="9d9c7-128">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9d9c7-128">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="9d9c7-129">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9d9c7-129">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="9d9c7-130">Resume-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9d9c7-130">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)


