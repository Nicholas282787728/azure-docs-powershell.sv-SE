---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: 61bb846067127b8e7d0a4deca0dd9a726d9dd1f0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100908"
---
# <span data-ttu-id="2feb8-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="2feb8-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="2feb8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2feb8-102">SYNOPSIS</span></span>
<span data-ttu-id="2feb8-103">Startar en oplanerad redundansväxling.</span><span class="sxs-lookup"><span data-stu-id="2feb8-103">Starts an unplanned failover operation.</span></span>

## <span data-ttu-id="2feb8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2feb8-104">SYNTAX</span></span>

### <span data-ttu-id="2feb8-105">ByRPIObject (standard)</span><span class="sxs-lookup"><span data-stu-id="2feb8-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2feb8-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="2feb8-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2feb8-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="2feb8-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2feb8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2feb8-108">DESCRIPTION</span></span>
<span data-ttu-id="2feb8-109">Cmdleten **Start-AzRecoveryServicesAsrUnplannedFailoverJob** startar oplanerad redundans av ett skyddat objekt eller en återställnings plan för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2feb8-109">The **Start-AzRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="2feb8-110">Du kan kontrol lera om jobbet lyckades med Get-AzRecoveryServicesAsrJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2feb8-110">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="2feb8-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2feb8-111">EXAMPLES</span></span>

### <span data-ttu-id="2feb8-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2feb8-112">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $RecoveryNetwork
```

<span data-ttu-id="2feb8-113">Startar den oplanerade redundansväxlingen för återställnings planen med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="2feb8-113">Starts the unplanned failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="2feb8-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="2feb8-114">Example 2</span></span>

<span data-ttu-id="2feb8-115">Startar en oplanerad redundansväxling.</span><span class="sxs-lookup"><span data-stu-id="2feb8-115">Starts an unplanned failover operation.</span></span> <span data-ttu-id="2feb8-116">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="2feb8-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrUnplannedFailoverJob -Direction PrimaryToRecovery -RecoveryPoint $rp[0] -ReplicationProtectedItem $ReplicationProtectedItem
```

## <span data-ttu-id="2feb8-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2feb8-117">PARAMETERS</span></span>

### <span data-ttu-id="2feb8-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="2feb8-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="2feb8-119">Anger sökvägen till primär certifikat för data kryptering för redundansväxling av skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="2feb8-119">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="2feb8-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="2feb8-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="2feb8-121">Anger sökvägen till den sekundära certifikat filen för data kryptering för redundansväxling av skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="2feb8-121">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="2feb8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2feb8-122">-DefaultProfile</span></span>
<span data-ttu-id="2feb8-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2feb8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2feb8-124">-Riktning</span><span class="sxs-lookup"><span data-stu-id="2feb8-124">-Direction</span></span>
<span data-ttu-id="2feb8-125">Anger växlings riktning.</span><span class="sxs-lookup"><span data-stu-id="2feb8-125">Specifies the failover direction.</span></span>
<span data-ttu-id="2feb8-126">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="2feb8-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2feb8-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="2feb8-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="2feb8-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="2feb8-128">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2feb8-129">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="2feb8-129">-PerformSourceSideAction</span></span>
<span data-ttu-id="2feb8-130">Utför åtgärden på käll sidan innan oplanerad redundans startas.</span><span class="sxs-lookup"><span data-stu-id="2feb8-130">Perform operation in source side before starting unplanned failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2feb8-131">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2feb8-131">-RecoveryPlan</span></span>
<span data-ttu-id="2feb8-132">Anger ett plan objekt för ASR-återställning.</span><span class="sxs-lookup"><span data-stu-id="2feb8-132">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="2feb8-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="2feb8-133">-RecoveryPoint</span></span>
<span data-ttu-id="2feb8-134">Anger en anpassad återställnings punkt för att redundansväxla den skyddade datorn till.</span><span class="sxs-lookup"><span data-stu-id="2feb8-134">Specifies a custom recovery point to failover the protected machine to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2feb8-135">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="2feb8-135">-RecoveryTag</span></span>
<span data-ttu-id="2feb8-136">Anger återställnings tag gen till redundans.</span><span class="sxs-lookup"><span data-stu-id="2feb8-136">Specifies the recovery tag to failover to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObject
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByRPIObjectWithRecoveryTag
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2feb8-137">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2feb8-137">-ReplicationProtectedItem</span></span>
<span data-ttu-id="2feb8-138">Anger ett skyddat objekt i Azure Site Recovery-objektet.</span><span class="sxs-lookup"><span data-stu-id="2feb8-138">Specifies an azure site recovery replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithRecoveryTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2feb8-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2feb8-139">-Confirm</span></span>
<span data-ttu-id="2feb8-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2feb8-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2feb8-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2feb8-141">-WhatIf</span></span>
<span data-ttu-id="2feb8-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2feb8-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2feb8-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2feb8-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2feb8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2feb8-144">CommonParameters</span></span>
<span data-ttu-id="2feb8-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2feb8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2feb8-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2feb8-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2feb8-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2feb8-147">INPUTS</span></span>

### <span data-ttu-id="2feb8-148">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2feb8-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="2feb8-149">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2feb8-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="2feb8-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2feb8-150">OUTPUTS</span></span>

### <span data-ttu-id="2feb8-151">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2feb8-151">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2feb8-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2feb8-152">NOTES</span></span>

## <span data-ttu-id="2feb8-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2feb8-153">RELATED LINKS</span></span>

[<span data-ttu-id="2feb8-154">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2feb8-154">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)