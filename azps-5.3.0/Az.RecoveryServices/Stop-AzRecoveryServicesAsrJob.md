---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: a86e58fe3c933ffaa9a382dc1e5140d3b42a34cb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525230"
---
# <span data-ttu-id="e5a6e-101">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="e5a6e-101">Stop-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="e5a6e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e5a6e-102">SYNOPSIS</span></span>
<span data-ttu-id="e5a6e-103">Stoppar ett Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="e5a6e-103">Stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="e5a6e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e5a6e-104">SYNTAX</span></span>

### <span data-ttu-id="e5a6e-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="e5a6e-105">ByObject (Default)</span></span>
```
Stop-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5a6e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e5a6e-106">ByName</span></span>
```
Stop-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5a6e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e5a6e-107">DESCRIPTION</span></span>
<span data-ttu-id="e5a6e-108">Cmdleten **Stop-AzRecoveryServicesAsrJob** stoppar det angivna Azure Site Recovery-jobbet.</span><span class="sxs-lookup"><span data-stu-id="e5a6e-108">The **Stop-AzRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="e5a6e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e5a6e-109">EXAMPLES</span></span>

### <span data-ttu-id="e5a6e-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e5a6e-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="e5a6e-111">Försöker stoppa det angivna jobbet och returnerar ett uppdaterat objekt i ASR-jobbet.</span><span class="sxs-lookup"><span data-stu-id="e5a6e-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="e5a6e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e5a6e-112">PARAMETERS</span></span>

### <span data-ttu-id="e5a6e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5a6e-113">-DefaultProfile</span></span>
<span data-ttu-id="e5a6e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e5a6e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e5a6e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5a6e-115">-InputObject</span></span>
<span data-ttu-id="e5a6e-116">Indatavärdet: Ange det ASR-objekt som motsvarar det ASR-jobb som ska stoppas</span><span class="sxs-lookup"><span data-stu-id="e5a6e-116">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

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

### <span data-ttu-id="e5a6e-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="e5a6e-117">-Name</span></span>
<span data-ttu-id="e5a6e-118">Ange det ASR-jobb som ska stoppas av det automatiska jobb namnet.</span><span class="sxs-lookup"><span data-stu-id="e5a6e-118">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="e5a6e-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e5a6e-119">-Confirm</span></span>
<span data-ttu-id="e5a6e-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e5a6e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5a6e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5a6e-121">-WhatIf</span></span>
<span data-ttu-id="e5a6e-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e5a6e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5a6e-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e5a6e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5a6e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5a6e-124">CommonParameters</span></span>
<span data-ttu-id="e5a6e-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5a6e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5a6e-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5a6e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5a6e-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e5a6e-127">INPUTS</span></span>

### <span data-ttu-id="e5a6e-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e5a6e-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e5a6e-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e5a6e-129">OUTPUTS</span></span>

### <span data-ttu-id="e5a6e-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e5a6e-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e5a6e-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e5a6e-131">NOTES</span></span>

## <span data-ttu-id="e5a6e-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e5a6e-132">RELATED LINKS</span></span>

[<span data-ttu-id="e5a6e-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="e5a6e-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="e5a6e-134">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="e5a6e-134">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="e5a6e-135">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="e5a6e-135">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)
