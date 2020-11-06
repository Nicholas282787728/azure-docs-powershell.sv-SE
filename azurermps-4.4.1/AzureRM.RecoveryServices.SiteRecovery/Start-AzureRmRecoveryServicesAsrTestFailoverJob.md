---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: d547de0af8d4f7b4f98a572d95dcc023d975fc2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582252"
---
# <span data-ttu-id="1f1ff-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="1f1ff-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="1f1ff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1f1ff-102">SYNOPSIS</span></span>
<span data-ttu-id="1f1ff-103">Startar en redundanstest.</span><span class="sxs-lookup"><span data-stu-id="1f1ff-103">Starts a test failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f1ff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1f1ff-104">SYNTAX</span></span>

### <span data-ttu-id="1f1ff-105">ByRPIObject (standard)</span><span class="sxs-lookup"><span data-stu-id="1f1ff-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f1ff-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="1f1ff-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f1ff-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="1f1ff-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f1ff-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="1f1ff-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f1ff-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="1f1ff-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f1ff-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="1f1ff-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f1ff-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1f1ff-111">DESCRIPTION</span></span>
<span data-ttu-id="1f1ff-112">Cmdleten **Start-AzureRmRecoveryServicesAsrTestFailoverJob** startar testredundans av ett skyddat objekt eller en återställnings plan för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1f1ff-112">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="1f1ff-113">Du kan kontrol lera om jobbet lyckades med Get-AzureRmRecoveryServicesAsrJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f1ff-113">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="1f1ff-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1f1ff-114">EXAMPLES</span></span>

### <span data-ttu-id="1f1ff-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1f1ff-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="1f1ff-116">Startar redundanstestning-åtgärden för återställnings planen med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="1f1ff-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="1f1ff-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1f1ff-117">PARAMETERS</span></span>

### <span data-ttu-id="1f1ff-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="1f1ff-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="1f1ff-119">Anger ID för Azure Virtual Network för att ansluta testet Miss lyckas via virtuella datorer till.</span><span class="sxs-lookup"><span data-stu-id="1f1ff-119">Specifies the Azure virtual network ID to connect the test fail over virtual machine(s) to.</span></span>

```yaml
Type: String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f1ff-120">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="1f1ff-120">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="1f1ff-121">Anger den primära certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="1f1ff-121">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="1f1ff-122">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="1f1ff-122">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="1f1ff-123">Anger den sekundära certifikats filen.</span><span class="sxs-lookup"><span data-stu-id="1f1ff-123">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="1f1ff-124">-Riktning</span><span class="sxs-lookup"><span data-stu-id="1f1ff-124">-Direction</span></span>
<span data-ttu-id="1f1ff-125">Anger växlings riktning.</span><span class="sxs-lookup"><span data-stu-id="1f1ff-125">Specifies the failover direction.</span></span>
<span data-ttu-id="1f1ff-126">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="1f1ff-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1f1ff-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="1f1ff-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="1f1ff-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="1f1ff-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="1f1ff-129">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1f1ff-129">-RecoveryPlan</span></span>
<span data-ttu-id="1f1ff-130">Anger ett plan objekt för ASR-återställning.</span><span class="sxs-lookup"><span data-stu-id="1f1ff-130">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f1ff-131">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1f1ff-131">-ReplicationProtectedItem</span></span>
<span data-ttu-id="1f1ff-132">Anger ett skyddat objekt i ASR-replikering.</span><span class="sxs-lookup"><span data-stu-id="1f1ff-132">Specifies an ASR replication protected item.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f1ff-133">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="1f1ff-133">-VMNetwork</span></span>
<span data-ttu-id="1f1ff-134">Anger det virtuella dator nätverket för webbplats återställning för att ansluta den virtuella datorn för redundanstest till.</span><span class="sxs-lookup"><span data-stu-id="1f1ff-134">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f1ff-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1f1ff-135">-Confirm</span></span>
<span data-ttu-id="1f1ff-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1f1ff-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f1ff-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f1ff-137">-WhatIf</span></span>
<span data-ttu-id="1f1ff-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1f1ff-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f1ff-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1f1ff-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f1ff-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f1ff-140">CommonParameters</span></span>
<span data-ttu-id="1f1ff-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f1ff-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f1ff-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f1ff-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f1ff-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1f1ff-143">INPUTS</span></span>

### <span data-ttu-id="1f1ff-144">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1f1ff-144">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="1f1ff-145">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1f1ff-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="1f1ff-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1f1ff-146">OUTPUTS</span></span>

### <span data-ttu-id="1f1ff-147">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1f1ff-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1f1ff-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1f1ff-148">NOTES</span></span>

## <span data-ttu-id="1f1ff-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1f1ff-149">RELATED LINKS</span></span>

[<span data-ttu-id="1f1ff-150">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="1f1ff-150">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
