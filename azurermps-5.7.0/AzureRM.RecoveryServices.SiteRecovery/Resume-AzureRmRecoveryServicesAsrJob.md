---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/resume-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: e6c384f56e7af9bacad40dfbc1fbf87d26dd8320
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576461"
---
# <span data-ttu-id="46bbe-101">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="46bbe-101">Resume-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="46bbe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="46bbe-102">SYNOPSIS</span></span>
<span data-ttu-id="46bbe-103">Återupptar en pausad Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="46bbe-103">Resumes a suspended Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46bbe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="46bbe-104">SYNTAX</span></span>

### <span data-ttu-id="46bbe-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="46bbe-105">ByObject (Default)</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46bbe-106">ByName</span><span class="sxs-lookup"><span data-stu-id="46bbe-106">ByName</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -Name <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46bbe-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="46bbe-107">DESCRIPTION</span></span>
<span data-ttu-id="46bbe-108">Cmdleten **Resume-AzureRmRecoveryServicesAsrJob** återupptar en pausad Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="46bbe-108">The **Resume-AzureRmRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="46bbe-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="46bbe-109">EXAMPLES</span></span>

### <span data-ttu-id="46bbe-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="46bbe-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="46bbe-111">Fortsätt det angivna jobbet om det är i vänte läge eller väntetillstånd och returnera det uppdaterade ASR-jobbet som motsvarar ASR-jobbet.</span><span class="sxs-lookup"><span data-stu-id="46bbe-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="46bbe-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="46bbe-112">PARAMETERS</span></span>

### <span data-ttu-id="46bbe-113">-Kommentera</span><span class="sxs-lookup"><span data-stu-id="46bbe-113">-Comment</span></span>
<span data-ttu-id="46bbe-114">Kommentarer för jobb loggen.</span><span class="sxs-lookup"><span data-stu-id="46bbe-114">Comments for the job log.</span></span>

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

### <span data-ttu-id="46bbe-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="46bbe-115">-Confirm</span></span>
<span data-ttu-id="46bbe-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="46bbe-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46bbe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46bbe-117">-DefaultProfile</span></span>
<span data-ttu-id="46bbe-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="46bbe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="46bbe-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46bbe-119">-InputObject</span></span>
<span data-ttu-id="46bbe-120">Indatavärdet till cmdleten: det ASR Job-objekt som motsvarar jobbet som ska återupptas.</span><span class="sxs-lookup"><span data-stu-id="46bbe-120">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="46bbe-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="46bbe-121">-Name</span></span>
<span data-ttu-id="46bbe-122">Ange ASR-jobbet efter namn.</span><span class="sxs-lookup"><span data-stu-id="46bbe-122">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="46bbe-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46bbe-123">-WhatIf</span></span>
<span data-ttu-id="46bbe-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="46bbe-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46bbe-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="46bbe-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46bbe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46bbe-126">CommonParameters</span></span>
<span data-ttu-id="46bbe-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46bbe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46bbe-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46bbe-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46bbe-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="46bbe-129">INPUTS</span></span>

### <span data-ttu-id="46bbe-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="46bbe-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="46bbe-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="46bbe-131">OUTPUTS</span></span>

### <span data-ttu-id="46bbe-132">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="46bbe-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="46bbe-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="46bbe-133">NOTES</span></span>

## <span data-ttu-id="46bbe-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="46bbe-134">RELATED LINKS</span></span>

[<span data-ttu-id="46bbe-135">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="46bbe-135">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="46bbe-136">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="46bbe-136">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="46bbe-137">Stopp-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="46bbe-137">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
