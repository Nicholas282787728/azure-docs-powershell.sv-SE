---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: ba31be7094da4c4c17fa8c674728b8c32bfa2b8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573348"
---
# <span data-ttu-id="56900-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="56900-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="56900-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="56900-102">SYNOPSIS</span></span>
<span data-ttu-id="56900-103">Startar en oplanerad redundansväxling.</span><span class="sxs-lookup"><span data-stu-id="56900-103">Starts a unplanned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56900-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="56900-104">SYNTAX</span></span>

### <span data-ttu-id="56900-105">ByRPIObject (standard)</span><span class="sxs-lookup"><span data-stu-id="56900-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56900-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="56900-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56900-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="56900-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56900-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="56900-108">DESCRIPTION</span></span>
<span data-ttu-id="56900-109">Cmdleten **Start-AzureRmRecoveryServicesAsrTestFailoverJob** startar testredundans av ett skyddat objekt eller en återställnings plan för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="56900-109">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="56900-110">Du kan kontrol lera om jobbet lyckades med Get-AzureRmRecoveryServicesAsrJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56900-110">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="56900-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="56900-111">EXAMPLES</span></span>

### <span data-ttu-id="56900-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="56900-112">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="56900-113">Startar redundanstestning-åtgärden för återställnings planen med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="56900-113">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="56900-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="56900-114">PARAMETERS</span></span>

### <span data-ttu-id="56900-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="56900-115">-Confirm</span></span>
<span data-ttu-id="56900-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="56900-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56900-117">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="56900-117">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="56900-118">Anger sökvägen till primär certifikat för data kryptering för redundansväxling av skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="56900-118">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56900-119">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="56900-119">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="56900-120">Anger sökvägen till den sekundära certifikat filen för data kryptering för redundansväxling av skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="56900-120">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56900-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56900-121">-DefaultProfile</span></span>
<span data-ttu-id="56900-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="56900-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="56900-123">-Riktning</span><span class="sxs-lookup"><span data-stu-id="56900-123">-Direction</span></span>
<span data-ttu-id="56900-124">Anger växlings riktning.</span><span class="sxs-lookup"><span data-stu-id="56900-124">Specifies the failover direction.</span></span>
<span data-ttu-id="56900-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="56900-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="56900-126">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="56900-126">PrimaryToRecovery</span></span>
- <span data-ttu-id="56900-127">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="56900-127">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56900-128">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="56900-128">-PerformSourceSideAction</span></span>
<span data-ttu-id="56900-129">Utför åtgärden på käll sidan innan oplanerad redundans startas.</span><span class="sxs-lookup"><span data-stu-id="56900-129">Perform operation in source side before starting unplanned failover.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56900-130">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="56900-130">-RecoveryPlan</span></span>
<span data-ttu-id="56900-131">Anger ett plan objekt för ASR-återställning.</span><span class="sxs-lookup"><span data-stu-id="56900-131">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56900-132">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="56900-132">-RecoveryPoint</span></span>
<span data-ttu-id="56900-133">Anger en anpassad återställnings punkt för att redundansväxla den skyddade datorn till.</span><span class="sxs-lookup"><span data-stu-id="56900-133">Specifies a custom recovery point to failover the protected machine to.</span></span>

```yaml
Type: ASRRecoveryPoint
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56900-134">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="56900-134">-RecoveryTag</span></span>
<span data-ttu-id="56900-135">Anger återställnings tag gen till redundans.</span><span class="sxs-lookup"><span data-stu-id="56900-135">Specifies the recovery tag to failover to.</span></span>

```yaml
Type: String
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
Type: String
Parameter Sets: ByRPIObjectWithRecoveryTag
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56900-136">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="56900-136">-ReplicationProtectedItem</span></span>
<span data-ttu-id="56900-137">Anger ett skyddat objekt i Azure Site Recovery-objektet.</span><span class="sxs-lookup"><span data-stu-id="56900-137">Specifies an azure site recovery replication protected item.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithRecoveryTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56900-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56900-138">-WhatIf</span></span>
<span data-ttu-id="56900-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="56900-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56900-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="56900-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56900-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56900-141">CommonParameters</span></span>
<span data-ttu-id="56900-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56900-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56900-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56900-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56900-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="56900-144">INPUTS</span></span>

### <span data-ttu-id="56900-145">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="56900-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="56900-146">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="56900-146">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="56900-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="56900-147">OUTPUTS</span></span>

### <span data-ttu-id="56900-148">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="56900-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="56900-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="56900-149">NOTES</span></span>

## <span data-ttu-id="56900-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="56900-150">RELATED LINKS</span></span>

[<span data-ttu-id="56900-151">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="56900-151">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
