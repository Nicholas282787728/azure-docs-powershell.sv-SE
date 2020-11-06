---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/resume-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: c5efb6b9aa7d78ef5f8d50ef80c5155c7e731f11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583495"
---
# <span data-ttu-id="9de72-101">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9de72-101">Resume-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="9de72-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9de72-102">SYNOPSIS</span></span>
<span data-ttu-id="9de72-103">Återupptar en pausad Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="9de72-103">Resumes a suspended Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9de72-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9de72-104">SYNTAX</span></span>

### <span data-ttu-id="9de72-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="9de72-105">ByObject (Default)</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9de72-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9de72-106">ByName</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -Name <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9de72-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9de72-107">DESCRIPTION</span></span>
<span data-ttu-id="9de72-108">Cmdleten **Resume-AzureRmRecoveryServicesAsrJob** återupptar en pausad Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="9de72-108">The **Resume-AzureRmRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="9de72-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9de72-109">EXAMPLES</span></span>

### <span data-ttu-id="9de72-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9de72-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="9de72-111">Fortsätt det angivna jobbet om det är i vänte läge eller väntetillstånd och returnera det uppdaterade ASR-jobbet som motsvarar ASR-jobbet.</span><span class="sxs-lookup"><span data-stu-id="9de72-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="9de72-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9de72-112">PARAMETERS</span></span>

### <span data-ttu-id="9de72-113">-Kommentera</span><span class="sxs-lookup"><span data-stu-id="9de72-113">-Comment</span></span>
<span data-ttu-id="9de72-114">Kommentarer för jobb loggen.</span><span class="sxs-lookup"><span data-stu-id="9de72-114">Comments for the job log.</span></span>

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

### <span data-ttu-id="9de72-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9de72-115">-DefaultProfile</span></span>
<span data-ttu-id="9de72-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9de72-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9de72-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9de72-117">-InputObject</span></span>
<span data-ttu-id="9de72-118">Indatavärdet till cmdleten: det ASR Job-objekt som motsvarar jobbet som ska återupptas.</span><span class="sxs-lookup"><span data-stu-id="9de72-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="9de72-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="9de72-119">-Name</span></span>
<span data-ttu-id="9de72-120">Ange ASR-jobbet efter namn.</span><span class="sxs-lookup"><span data-stu-id="9de72-120">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="9de72-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9de72-121">-Confirm</span></span>
<span data-ttu-id="9de72-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9de72-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9de72-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9de72-123">-WhatIf</span></span>
<span data-ttu-id="9de72-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9de72-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9de72-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9de72-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9de72-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9de72-126">CommonParameters</span></span>
<span data-ttu-id="9de72-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9de72-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9de72-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9de72-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9de72-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9de72-129">INPUTS</span></span>

### <span data-ttu-id="9de72-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9de72-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9de72-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9de72-131">OUTPUTS</span></span>

### <span data-ttu-id="9de72-132">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9de72-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9de72-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9de72-133">NOTES</span></span>

## <span data-ttu-id="9de72-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9de72-134">RELATED LINKS</span></span>

[<span data-ttu-id="9de72-135">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9de72-135">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="9de72-136">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9de72-136">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="9de72-137">Stopp-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9de72-137">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
