---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailovercleanupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverCleanupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverCleanupJob.md
ms.openlocfilehash: 4143bc481091889b293d206192e0c5eba386d68a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920175"
---
# <span data-ttu-id="4def7-101">Start-AzRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="4def7-101">Start-AzRecoveryServicesAsrTestFailoverCleanupJob</span></span>

## <span data-ttu-id="4def7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4def7-102">SYNOPSIS</span></span>
<span data-ttu-id="4def7-103">Startar rensning av redundanstestning.</span><span class="sxs-lookup"><span data-stu-id="4def7-103">Starts the test failover cleanup operation.</span></span>

## <span data-ttu-id="4def7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4def7-104">SYNTAX</span></span>

### <span data-ttu-id="4def7-105">ByRPIObject (standard)</span><span class="sxs-lookup"><span data-stu-id="4def7-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Comment <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4def7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4def7-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ResourceId <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4def7-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="4def7-107">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan <ASRRecoveryPlan> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4def7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4def7-108">DESCRIPTION</span></span>
<span data-ttu-id="4def7-109">Cmdleten **Start-AzRecoveryServicesAsrTestFailoverCleanupJob** startar rensning av redundanstest för ett replikerat objekt eller en återställnings plan där en redundanstestning har utförts.</span><span class="sxs-lookup"><span data-stu-id="4def7-109">The **Start-AzRecoveryServicesAsrTestFailoverCleanupJob** cmdlet starts the test failover cleanup operation on a replication protected item or recovery plan on which a test failover has been performed.</span></span>

## <span data-ttu-id="4def7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4def7-110">EXAMPLES</span></span>

### <span data-ttu-id="4def7-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4def7-111">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $rpi -Comments "testing done"
```

<span data-ttu-id="4def7-112">Jobb för att spåra rensning av redundanstestning av ett skyddat objekt i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4def7-112">Job to track test failover Cleanup of an Azure Site Recovery replication protected item.</span></span>

### <span data-ttu-id="4def7-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4def7-113">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan $recoveryPlan -Comment "testing done"
```

<span data-ttu-id="4def7-114">Jobb för att spåra rensning av redundanstestning av en Azure Site Recovery-recoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="4def7-114">Job to track test failover Cleanup of an Azure Site Recovery recoveryPlan.</span></span>

## <span data-ttu-id="4def7-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4def7-115">PARAMETERS</span></span>

### <span data-ttu-id="4def7-116">-Kommentera</span><span class="sxs-lookup"><span data-stu-id="4def7-116">-Comment</span></span>
<span data-ttu-id="4def7-117">Användar kommentar för testning av redundans.</span><span class="sxs-lookup"><span data-stu-id="4def7-117">User Comment for Test Failover.</span></span>

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

### <span data-ttu-id="4def7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4def7-118">-DefaultProfile</span></span>
<span data-ttu-id="4def7-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4def7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4def7-120">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4def7-120">-RecoveryPlan</span></span>
<span data-ttu-id="4def7-121">Återställnings plan för rensning av redundanstestning på.</span><span class="sxs-lookup"><span data-stu-id="4def7-121">Recovery Plan to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="4def7-122">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4def7-122">-ReplicationProtectedItem</span></span>
<span data-ttu-id="4def7-123">Replikerat objekt som ska användas för testning av redundans.</span><span class="sxs-lookup"><span data-stu-id="4def7-123">Replication Protected Item to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="4def7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4def7-124">-ResourceId</span></span>
<span data-ttu-id="4def7-125">Resurs-ID för ett replikerat objekt/återställnings plan för cleaningup.</span><span class="sxs-lookup"><span data-stu-id="4def7-125">Resource Id of replication protected item / recovery plan for cleaningup test failover.</span></span>

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

### <span data-ttu-id="4def7-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4def7-126">-Confirm</span></span>
<span data-ttu-id="4def7-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4def7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4def7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4def7-128">-WhatIf</span></span>
<span data-ttu-id="4def7-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4def7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4def7-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4def7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4def7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4def7-131">CommonParameters</span></span>
<span data-ttu-id="4def7-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4def7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4def7-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4def7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4def7-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4def7-134">INPUTS</span></span>

### <span data-ttu-id="4def7-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4def7-135">System.String</span></span>

### <span data-ttu-id="4def7-136">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4def7-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="4def7-137">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4def7-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="4def7-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4def7-138">OUTPUTS</span></span>

### <span data-ttu-id="4def7-139">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4def7-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4def7-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4def7-140">NOTES</span></span>

## <span data-ttu-id="4def7-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4def7-141">RELATED LINKS</span></span>
