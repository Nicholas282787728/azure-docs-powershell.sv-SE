---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 2f219882199010b2765ebd4386691451d74a182d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756884"
---
# <span data-ttu-id="1a1b0-101">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="1a1b0-101">Restart-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="1a1b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1a1b0-102">SYNOPSIS</span></span>
<span data-ttu-id="1a1b0-103">Startar om ett Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="1a1b0-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a1b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1a1b0-104">SYNTAX</span></span>

### <span data-ttu-id="1a1b0-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="1a1b0-105">ByObject (Default)</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a1b0-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1a1b0-106">ByName</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a1b0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1a1b0-107">DESCRIPTION</span></span>
<span data-ttu-id="1a1b0-108">Cmdleten **restart-AzureRmRecoveryServicesAsrJob** startar om ett Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="1a1b0-108">The **Restart-AzureRmRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="1a1b0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1a1b0-109">EXAMPLES</span></span>

### <span data-ttu-id="1a1b0-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1a1b0-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="1a1b0-111">Startar om det angivna ASR-jobbet och returnerar det uppdaterade ASR-jobbet för ASR-jobbet.</span><span class="sxs-lookup"><span data-stu-id="1a1b0-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="1a1b0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1a1b0-112">PARAMETERS</span></span>

### <span data-ttu-id="1a1b0-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a1b0-113">-InputObject</span></span>
<span data-ttu-id="1a1b0-114">Indatavärdet till cmdleten: det ASR-objekt som motsvarar det ASR-jobb som ska startas om</span><span class="sxs-lookup"><span data-stu-id="1a1b0-114">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>
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

### <span data-ttu-id="1a1b0-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="1a1b0-115">-Name</span></span>
<span data-ttu-id="1a1b0-116">Ange jobbet efter namn.</span><span class="sxs-lookup"><span data-stu-id="1a1b0-116">Specify the job by name.</span></span>

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

### <span data-ttu-id="1a1b0-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1a1b0-117">-Confirm</span></span>
<span data-ttu-id="1a1b0-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1a1b0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a1b0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a1b0-119">-WhatIf</span></span>
<span data-ttu-id="1a1b0-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1a1b0-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a1b0-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1a1b0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a1b0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a1b0-122">CommonParameters</span></span>
<span data-ttu-id="1a1b0-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a1b0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a1b0-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a1b0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a1b0-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1a1b0-125">INPUTS</span></span>

### <span data-ttu-id="1a1b0-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1a1b0-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1a1b0-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1a1b0-127">OUTPUTS</span></span>

### <span data-ttu-id="1a1b0-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1a1b0-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1a1b0-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1a1b0-129">NOTES</span></span>

## <span data-ttu-id="1a1b0-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1a1b0-130">RELATED LINKS</span></span>

[<span data-ttu-id="1a1b0-131">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="1a1b0-131">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="1a1b0-132">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="1a1b0-132">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="1a1b0-133">Stopp-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="1a1b0-133">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
