---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailovercleanupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverCleanupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverCleanupJob.md
ms.openlocfilehash: 24fbbd3d0d9d2e165a2edfbf289b434c886b0b0c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927538"
---
# <span data-ttu-id="abf7d-101">Start-AzRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="abf7d-101">Start-AzRecoveryServicesAsrTestFailoverCleanupJob</span></span>

## <span data-ttu-id="abf7d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="abf7d-102">SYNOPSIS</span></span>
<span data-ttu-id="abf7d-103">Startar rensning av redundanstestning.</span><span class="sxs-lookup"><span data-stu-id="abf7d-103">Starts the test failover cleanup operation.</span></span>

## <span data-ttu-id="abf7d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="abf7d-104">SYNTAX</span></span>

### <span data-ttu-id="abf7d-105">ByRPIObject (standard)</span><span class="sxs-lookup"><span data-stu-id="abf7d-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Comment <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abf7d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="abf7d-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ResourceId <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abf7d-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="abf7d-107">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan <ASRRecoveryPlan> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abf7d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="abf7d-108">DESCRIPTION</span></span>
<span data-ttu-id="abf7d-109">Cmdleten **Start-AzRecoveryServicesAsrTestFailoverCleanupJob** startar rensning av redundanstest för ett replikerat objekt eller en återställnings plan där en redundanstestning har utförts.</span><span class="sxs-lookup"><span data-stu-id="abf7d-109">The **Start-AzRecoveryServicesAsrTestFailoverCleanupJob** cmdlet starts the test failover cleanup operation on a replication protected item or recovery plan on which a test failover has been performed.</span></span>

## <span data-ttu-id="abf7d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="abf7d-110">EXAMPLES</span></span>

### <span data-ttu-id="abf7d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="abf7d-111">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $rpi -Comments "testing done"
```

<span data-ttu-id="abf7d-112">Jobb för att spåra rensning av redundanstestning av ett skyddat objekt i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="abf7d-112">Job to track test failover Cleanup of an Azure Site Recovery replication protected item.</span></span>

### <span data-ttu-id="abf7d-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="abf7d-113">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan $recoveryPlan -Comment "testing done"
```

<span data-ttu-id="abf7d-114">Jobb för att spåra rensning av redundanstestning av en Azure Site Recovery-recoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="abf7d-114">Job to track test failover Cleanup of an Azure Site Recovery recoveryPlan.</span></span>

## <span data-ttu-id="abf7d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="abf7d-115">PARAMETERS</span></span>

### <span data-ttu-id="abf7d-116">-Kommentera</span><span class="sxs-lookup"><span data-stu-id="abf7d-116">-Comment</span></span>
<span data-ttu-id="abf7d-117">Användar kommentar för testning av redundans.</span><span class="sxs-lookup"><span data-stu-id="abf7d-117">User Comment for Test Failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf7d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abf7d-118">-DefaultProfile</span></span>
<span data-ttu-id="abf7d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="abf7d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abf7d-120">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="abf7d-120">-RecoveryPlan</span></span>
<span data-ttu-id="abf7d-121">Återställnings plan för rensning av redundanstestning på.</span><span class="sxs-lookup"><span data-stu-id="abf7d-121">Recovery Plan to perform the test failover cleanup on.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abf7d-122">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="abf7d-122">-ReplicationProtectedItem</span></span>
<span data-ttu-id="abf7d-123">Replikerat objekt som ska användas för testning av redundans.</span><span class="sxs-lookup"><span data-stu-id="abf7d-123">Replication Protected Item to perform the test failover cleanup on.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abf7d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abf7d-124">-ResourceId</span></span>
<span data-ttu-id="abf7d-125">Resurs-ID för ett replikerat objekt/återställnings plan för cleaningup.</span><span class="sxs-lookup"><span data-stu-id="abf7d-125">Resource Id of replication protected item / recovery plan for cleaningup test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abf7d-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="abf7d-126">-Confirm</span></span>
<span data-ttu-id="abf7d-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="abf7d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abf7d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abf7d-128">-WhatIf</span></span>
<span data-ttu-id="abf7d-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="abf7d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abf7d-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="abf7d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abf7d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abf7d-131">CommonParameters</span></span>
<span data-ttu-id="abf7d-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abf7d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abf7d-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="abf7d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abf7d-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="abf7d-134">INPUTS</span></span>

### <span data-ttu-id="abf7d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="abf7d-135">System.String</span></span>

### <span data-ttu-id="abf7d-136">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="abf7d-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="abf7d-137">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="abf7d-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="abf7d-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="abf7d-138">OUTPUTS</span></span>

### <span data-ttu-id="abf7d-139">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="abf7d-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="abf7d-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="abf7d-140">NOTES</span></span>

## <span data-ttu-id="abf7d-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="abf7d-141">RELATED LINKS</span></span>
