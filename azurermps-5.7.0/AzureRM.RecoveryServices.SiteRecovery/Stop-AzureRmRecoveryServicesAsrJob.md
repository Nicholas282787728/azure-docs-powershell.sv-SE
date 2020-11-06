---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/stop-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: c573cd8162961660dac57be3d3f5fe18cd055a89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573347"
---
# <span data-ttu-id="42ad1-101">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="42ad1-101">Stop-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="42ad1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="42ad1-102">SYNOPSIS</span></span>
<span data-ttu-id="42ad1-103">Stoppar ett Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="42ad1-103">Stops an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42ad1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="42ad1-104">SYNTAX</span></span>

### <span data-ttu-id="42ad1-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="42ad1-105">ByObject (Default)</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42ad1-106">ByName</span><span class="sxs-lookup"><span data-stu-id="42ad1-106">ByName</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42ad1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="42ad1-107">DESCRIPTION</span></span>
<span data-ttu-id="42ad1-108">Cmdleten **Stop-AzureRmRecoveryServicesAsrJob** stoppar det angivna Azure Site Recovery-jobbet.</span><span class="sxs-lookup"><span data-stu-id="42ad1-108">The **Stop-AzureRmRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="42ad1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="42ad1-109">EXAMPLES</span></span>

### <span data-ttu-id="42ad1-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="42ad1-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="42ad1-111">Försöker stoppa det angivna jobbet och returnerar ett uppdaterat objekt i ASR-jobbet.</span><span class="sxs-lookup"><span data-stu-id="42ad1-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="42ad1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="42ad1-112">PARAMETERS</span></span>

### <span data-ttu-id="42ad1-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="42ad1-113">-Confirm</span></span>
<span data-ttu-id="42ad1-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="42ad1-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42ad1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42ad1-115">-DefaultProfile</span></span>
<span data-ttu-id="42ad1-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="42ad1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ad1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42ad1-117">-InputObject</span></span>
<span data-ttu-id="42ad1-118">Indatavärdet: Ange det ASR-objekt som motsvarar det ASR-jobb som ska stoppas</span><span class="sxs-lookup"><span data-stu-id="42ad1-118">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

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

### <span data-ttu-id="42ad1-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="42ad1-119">-Name</span></span>
<span data-ttu-id="42ad1-120">Ange det ASR-jobb som ska stoppas av det automatiska jobb namnet.</span><span class="sxs-lookup"><span data-stu-id="42ad1-120">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="42ad1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42ad1-121">-WhatIf</span></span>
<span data-ttu-id="42ad1-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="42ad1-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42ad1-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="42ad1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42ad1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42ad1-124">CommonParameters</span></span>
<span data-ttu-id="42ad1-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42ad1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42ad1-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42ad1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42ad1-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="42ad1-127">INPUTS</span></span>

### <span data-ttu-id="42ad1-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="42ad1-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="42ad1-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="42ad1-129">OUTPUTS</span></span>

### <span data-ttu-id="42ad1-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="42ad1-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="42ad1-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="42ad1-131">NOTES</span></span>

## <span data-ttu-id="42ad1-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="42ad1-132">RELATED LINKS</span></span>

[<span data-ttu-id="42ad1-133">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="42ad1-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="42ad1-134">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="42ad1-134">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="42ad1-135">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="42ad1-135">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)
