---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/resume-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 6af467e5fd90a7d3028d67297b62f517f512b1b1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091260"
---
# <span data-ttu-id="f3f00-101">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f3f00-101">Resume-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="f3f00-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f3f00-102">SYNOPSIS</span></span>
<span data-ttu-id="f3f00-103">Återupptar en pausad Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="f3f00-103">Resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="f3f00-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f3f00-104">SYNTAX</span></span>

### <span data-ttu-id="f3f00-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="f3f00-105">ByObject (Default)</span></span>
```
Resume-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3f00-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f3f00-106">ByName</span></span>
```
Resume-AzRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3f00-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f3f00-107">DESCRIPTION</span></span>
<span data-ttu-id="f3f00-108">Cmdleten **Resume-AzRecoveryServicesAsrJob** återupptar en pausad Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="f3f00-108">The **Resume-AzRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="f3f00-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f3f00-109">EXAMPLES</span></span>

### <span data-ttu-id="f3f00-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f3f00-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="f3f00-111">Fortsätt det angivna jobbet om det är i vänte läge eller väntetillstånd och returnera det uppdaterade ASR-jobbet som motsvarar ASR-jobbet.</span><span class="sxs-lookup"><span data-stu-id="f3f00-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="f3f00-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f3f00-112">PARAMETERS</span></span>

### <span data-ttu-id="f3f00-113">-Kommentera</span><span class="sxs-lookup"><span data-stu-id="f3f00-113">-Comment</span></span>
<span data-ttu-id="f3f00-114">Kommentarer för jobb loggen.</span><span class="sxs-lookup"><span data-stu-id="f3f00-114">Comments for the job log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3f00-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3f00-115">-DefaultProfile</span></span>
<span data-ttu-id="f3f00-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f3f00-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f3f00-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3f00-117">-InputObject</span></span>
<span data-ttu-id="f3f00-118">Indatavärdet till cmdleten: det ASR Job-objekt som motsvarar jobbet som ska återupptas.</span><span class="sxs-lookup"><span data-stu-id="f3f00-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="f3f00-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="f3f00-119">-Name</span></span>
<span data-ttu-id="f3f00-120">Ange ASR-jobbet efter namn.</span><span class="sxs-lookup"><span data-stu-id="f3f00-120">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="f3f00-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f3f00-121">-Confirm</span></span>
<span data-ttu-id="f3f00-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f3f00-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3f00-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3f00-123">-WhatIf</span></span>
<span data-ttu-id="f3f00-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f3f00-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3f00-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f3f00-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3f00-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3f00-126">CommonParameters</span></span>
<span data-ttu-id="f3f00-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3f00-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3f00-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3f00-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3f00-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f3f00-129">INPUTS</span></span>

### <span data-ttu-id="f3f00-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f3f00-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f3f00-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f3f00-131">OUTPUTS</span></span>

### <span data-ttu-id="f3f00-132">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f3f00-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f3f00-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f3f00-133">NOTES</span></span>

## <span data-ttu-id="f3f00-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f3f00-134">RELATED LINKS</span></span>

[<span data-ttu-id="f3f00-135">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f3f00-135">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="f3f00-136">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f3f00-136">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="f3f00-137">Stopp-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f3f00-137">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
