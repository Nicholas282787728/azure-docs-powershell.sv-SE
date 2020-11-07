---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: e639e6fc42e440b5088a34ee29e21d324ed7d235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756880"
---
# <span data-ttu-id="54278-101">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="54278-101">Stop-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="54278-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54278-102">SYNOPSIS</span></span>
<span data-ttu-id="54278-103">Stoppar ett Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="54278-103">Stops an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54278-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54278-104">SYNTAX</span></span>

### <span data-ttu-id="54278-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="54278-105">ByObject (Default)</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54278-106">ByName</span><span class="sxs-lookup"><span data-stu-id="54278-106">ByName</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54278-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54278-107">DESCRIPTION</span></span>
<span data-ttu-id="54278-108">Cmdleten **Stop-AzureRmRecoveryServicesAsrJob** stoppar det angivna Azure Site Recovery-jobbet.</span><span class="sxs-lookup"><span data-stu-id="54278-108">The **Stop-AzureRmRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="54278-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54278-109">EXAMPLES</span></span>

### <span data-ttu-id="54278-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="54278-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="54278-111">Försöker stoppa det angivna jobbet och returnerar ett uppdaterat objekt i ASR-jobbet.</span><span class="sxs-lookup"><span data-stu-id="54278-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="54278-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54278-112">PARAMETERS</span></span>

### <span data-ttu-id="54278-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54278-113">-InputObject</span></span>
<span data-ttu-id="54278-114">Indatavärdet: Ange det ASR-objekt som motsvarar det ASR-jobb som ska stoppas</span><span class="sxs-lookup"><span data-stu-id="54278-114">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

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

### <span data-ttu-id="54278-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="54278-115">-Name</span></span>
<span data-ttu-id="54278-116">Ange det ASR-jobb som ska stoppas av det automatiska jobb namnet.</span><span class="sxs-lookup"><span data-stu-id="54278-116">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="54278-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="54278-117">-Confirm</span></span>
<span data-ttu-id="54278-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="54278-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54278-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54278-119">-WhatIf</span></span>
<span data-ttu-id="54278-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="54278-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54278-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="54278-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54278-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54278-122">CommonParameters</span></span>
<span data-ttu-id="54278-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54278-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54278-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54278-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54278-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54278-125">INPUTS</span></span>

### <span data-ttu-id="54278-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="54278-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="54278-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54278-127">OUTPUTS</span></span>

### <span data-ttu-id="54278-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="54278-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="54278-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54278-129">NOTES</span></span>

## <span data-ttu-id="54278-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54278-130">RELATED LINKS</span></span>

[<span data-ttu-id="54278-131">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="54278-131">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="54278-132">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="54278-132">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="54278-133">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="54278-133">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)
