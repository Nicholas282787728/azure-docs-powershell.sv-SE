---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: ac3f3c843f13fd500156cf148b5c80436e2e2649
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582255"
---
# <span data-ttu-id="dd374-101">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="dd374-101">Resume-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="dd374-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dd374-102">SYNOPSIS</span></span>
<span data-ttu-id="dd374-103">Återupptar en pausad Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="dd374-103">Resumes a suspended Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd374-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dd374-104">SYNTAX</span></span>

### <span data-ttu-id="dd374-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="dd374-105">ByObject (Default)</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd374-106">ByName</span><span class="sxs-lookup"><span data-stu-id="dd374-106">ByName</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd374-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dd374-107">DESCRIPTION</span></span>
<span data-ttu-id="dd374-108">Cmdleten **Resume-AzureRmRecoveryServicesAsrJob** återupptar en pausad Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="dd374-108">The **Resume-AzureRmRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="dd374-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dd374-109">EXAMPLES</span></span>

### <span data-ttu-id="dd374-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dd374-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="dd374-111">Fortsätt det angivna jobbet om det är i vänte läge eller väntetillstånd och returnera det uppdaterade ASR-jobbet som motsvarar ASR-jobbet.</span><span class="sxs-lookup"><span data-stu-id="dd374-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="dd374-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dd374-112">PARAMETERS</span></span>

### <span data-ttu-id="dd374-113">-Kommentera</span><span class="sxs-lookup"><span data-stu-id="dd374-113">-Comment</span></span>
<span data-ttu-id="dd374-114">Kommentarer för jobb loggen.</span><span class="sxs-lookup"><span data-stu-id="dd374-114">Comments for the job log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd374-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd374-115">-InputObject</span></span>
<span data-ttu-id="dd374-116">Indatavärdet till cmdleten: det ASR Job-objekt som motsvarar jobbet som ska återupptas.</span><span class="sxs-lookup"><span data-stu-id="dd374-116">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd374-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="dd374-117">-Name</span></span>
<span data-ttu-id="dd374-118">Ange ASR-jobbet efter namn.</span><span class="sxs-lookup"><span data-stu-id="dd374-118">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="dd374-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dd374-119">-Confirm</span></span>
<span data-ttu-id="dd374-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dd374-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd374-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd374-121">-WhatIf</span></span>
<span data-ttu-id="dd374-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dd374-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd374-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dd374-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd374-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd374-124">CommonParameters</span></span>
<span data-ttu-id="dd374-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd374-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd374-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd374-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd374-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dd374-127">INPUTS</span></span>

### <span data-ttu-id="dd374-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="dd374-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="dd374-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dd374-129">OUTPUTS</span></span>

### <span data-ttu-id="dd374-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="dd374-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="dd374-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dd374-131">NOTES</span></span>

## <span data-ttu-id="dd374-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dd374-132">RELATED LINKS</span></span>

[<span data-ttu-id="dd374-133">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="dd374-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="dd374-134">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="dd374-134">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="dd374-135">Stopp-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="dd374-135">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
