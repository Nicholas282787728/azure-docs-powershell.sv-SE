---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restart-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: c53cc7b410f0898af7a643babef1781433cbd120
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747349"
---
# <span data-ttu-id="e89c2-101">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="e89c2-101">Restart-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="e89c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e89c2-102">SYNOPSIS</span></span>
<span data-ttu-id="e89c2-103">Startar om ett Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="e89c2-103">Restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="e89c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e89c2-104">SYNTAX</span></span>

### <span data-ttu-id="e89c2-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="e89c2-105">ByObject (Default)</span></span>
```
Restart-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e89c2-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e89c2-106">ByName</span></span>
```
Restart-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e89c2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e89c2-107">DESCRIPTION</span></span>
<span data-ttu-id="e89c2-108">Cmdleten **restart-AzRecoveryServicesAsrJob** startar om ett Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="e89c2-108">The **Restart-AzRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="e89c2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e89c2-109">EXAMPLES</span></span>

### <span data-ttu-id="e89c2-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e89c2-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="e89c2-111">Startar om det angivna ASR-jobbet och returnerar det uppdaterade ASR-jobbet för ASR-jobbet.</span><span class="sxs-lookup"><span data-stu-id="e89c2-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="e89c2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e89c2-112">PARAMETERS</span></span>

### <span data-ttu-id="e89c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e89c2-113">-DefaultProfile</span></span>
<span data-ttu-id="e89c2-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e89c2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e89c2-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e89c2-115">-InputObject</span></span>
<span data-ttu-id="e89c2-116">Indatavärdet till cmdleten: det ASR-objekt som motsvarar det ASR-jobb som ska startas om</span><span class="sxs-lookup"><span data-stu-id="e89c2-116">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>


```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e89c2-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="e89c2-117">-Name</span></span>
<span data-ttu-id="e89c2-118">Ange jobbet efter namn.</span><span class="sxs-lookup"><span data-stu-id="e89c2-118">Specify the job by name.</span></span>

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

### <span data-ttu-id="e89c2-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e89c2-119">-Confirm</span></span>
<span data-ttu-id="e89c2-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e89c2-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e89c2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e89c2-121">-WhatIf</span></span>
<span data-ttu-id="e89c2-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e89c2-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e89c2-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e89c2-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e89c2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e89c2-124">CommonParameters</span></span>
<span data-ttu-id="e89c2-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e89c2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e89c2-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e89c2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e89c2-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e89c2-127">INPUTS</span></span>

### <span data-ttu-id="e89c2-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e89c2-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e89c2-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e89c2-129">OUTPUTS</span></span>

### <span data-ttu-id="e89c2-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e89c2-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e89c2-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e89c2-131">NOTES</span></span>

## <span data-ttu-id="e89c2-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e89c2-132">RELATED LINKS</span></span>

[<span data-ttu-id="e89c2-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="e89c2-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="e89c2-134">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="e89c2-134">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="e89c2-135">Stopp-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="e89c2-135">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
