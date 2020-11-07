---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 4931b32cf2c74180ad06b071d19ef57f4be2285e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747363"
---
# <span data-ttu-id="f0106-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f0106-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="f0106-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f0106-102">SYNOPSIS</span></span>
<span data-ttu-id="f0106-103">Tar bort den angivna planen för ASR-återställning från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="f0106-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

## <span data-ttu-id="f0106-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f0106-104">SYNTAX</span></span>

### <span data-ttu-id="f0106-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="f0106-105">ByObject (Default)</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0106-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f0106-106">ByName</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0106-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f0106-107">DESCRIPTION</span></span>
<span data-ttu-id="f0106-108">Cmdleten **Remove-AzRecoveryServicesAsrRecoveryPlan** tar bort den angivna återställnings planen från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="f0106-108">The **Remove-AzRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="f0106-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f0106-109">EXAMPLES</span></span>

### <span data-ttu-id="f0106-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f0106-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="f0106-111">Tar bort den angivna återställnings planen och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="f0106-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f0106-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f0106-112">PARAMETERS</span></span>

### <span data-ttu-id="f0106-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0106-113">-DefaultProfile</span></span>
<span data-ttu-id="f0106-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f0106-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f0106-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0106-115">-InputObject</span></span>
<span data-ttu-id="f0106-116">Indatavärdet till cmdleten: det objekt för ASR-återställning som motsvarar återställnings planen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f0106-116">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0106-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="f0106-117">-Name</span></span>
<span data-ttu-id="f0106-118">Anger namnet på den återställnings plan som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f0106-118">Specifies the name of the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="f0106-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f0106-119">-Confirm</span></span>
<span data-ttu-id="f0106-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f0106-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0106-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0106-121">-WhatIf</span></span>
<span data-ttu-id="f0106-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f0106-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0106-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f0106-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0106-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0106-124">CommonParameters</span></span>
<span data-ttu-id="f0106-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0106-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0106-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0106-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0106-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f0106-127">INPUTS</span></span>

### <span data-ttu-id="f0106-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f0106-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="f0106-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f0106-129">OUTPUTS</span></span>

### <span data-ttu-id="f0106-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f0106-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f0106-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f0106-131">NOTES</span></span>

## <span data-ttu-id="f0106-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f0106-132">RELATED LINKS</span></span>

[<span data-ttu-id="f0106-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f0106-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="f0106-134">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f0106-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="f0106-135">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f0106-135">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)

