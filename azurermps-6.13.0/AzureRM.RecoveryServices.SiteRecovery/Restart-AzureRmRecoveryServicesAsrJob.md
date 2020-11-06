---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/restart-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 94f4f44da8da4b2ad16db6dff86ad22908847a62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583492"
---
# <span data-ttu-id="c87b4-101">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c87b4-101">Restart-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="c87b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c87b4-102">SYNOPSIS</span></span>
<span data-ttu-id="c87b4-103">Startar om ett Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="c87b4-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c87b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c87b4-104">SYNTAX</span></span>

### <span data-ttu-id="c87b4-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="c87b4-105">ByObject (Default)</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c87b4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c87b4-106">ByName</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c87b4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c87b4-107">DESCRIPTION</span></span>
<span data-ttu-id="c87b4-108">Cmdleten **restart-AzureRmRecoveryServicesAsrJob** startar om ett Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="c87b4-108">The **Restart-AzureRmRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="c87b4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c87b4-109">EXAMPLES</span></span>

### <span data-ttu-id="c87b4-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c87b4-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="c87b4-111">Startar om det angivna ASR-jobbet och returnerar det uppdaterade ASR-jobbet för ASR-jobbet.</span><span class="sxs-lookup"><span data-stu-id="c87b4-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="c87b4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c87b4-112">PARAMETERS</span></span>

### <span data-ttu-id="c87b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c87b4-113">-DefaultProfile</span></span>
<span data-ttu-id="c87b4-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c87b4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c87b4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c87b4-115">-InputObject</span></span>
<span data-ttu-id="c87b4-116">Indatavärdet till cmdleten: det ASR-objekt som motsvarar det ASR-jobb som ska startas om</span><span class="sxs-lookup"><span data-stu-id="c87b4-116">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>


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

### <span data-ttu-id="c87b4-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="c87b4-117">-Name</span></span>
<span data-ttu-id="c87b4-118">Ange jobbet efter namn.</span><span class="sxs-lookup"><span data-stu-id="c87b4-118">Specify the job by name.</span></span>

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

### <span data-ttu-id="c87b4-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c87b4-119">-Confirm</span></span>
<span data-ttu-id="c87b4-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c87b4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c87b4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c87b4-121">-WhatIf</span></span>
<span data-ttu-id="c87b4-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c87b4-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c87b4-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c87b4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c87b4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c87b4-124">CommonParameters</span></span>
<span data-ttu-id="c87b4-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c87b4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c87b4-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c87b4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c87b4-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c87b4-127">INPUTS</span></span>

### <span data-ttu-id="c87b4-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c87b4-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c87b4-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c87b4-129">OUTPUTS</span></span>

### <span data-ttu-id="c87b4-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c87b4-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c87b4-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c87b4-131">NOTES</span></span>

## <span data-ttu-id="c87b4-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c87b4-132">RELATED LINKS</span></span>

[<span data-ttu-id="c87b4-133">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c87b4-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="c87b4-134">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c87b4-134">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="c87b4-135">Stopp-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c87b4-135">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
