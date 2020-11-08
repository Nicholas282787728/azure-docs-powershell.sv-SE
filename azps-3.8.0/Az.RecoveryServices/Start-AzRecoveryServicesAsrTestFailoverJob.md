---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: f86c044099795b8c300e649b541a4baee8e6df46
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091644"
---
# <span data-ttu-id="21a6b-101">Start-AzRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="21a6b-101">Start-AzRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="21a6b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="21a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="21a6b-103">Startar en redundanstest.</span><span class="sxs-lookup"><span data-stu-id="21a6b-103">Starts a test failover operation.</span></span>

## <span data-ttu-id="21a6b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="21a6b-104">SYNTAX</span></span>

### <span data-ttu-id="21a6b-105">ByRPIObject (standard)</span><span class="sxs-lookup"><span data-stu-id="21a6b-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21a6b-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="21a6b-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21a6b-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="21a6b-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21a6b-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="21a6b-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21a6b-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="21a6b-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21a6b-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="21a6b-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="21a6b-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="21a6b-111">DESCRIPTION</span></span>
<span data-ttu-id="21a6b-112">Cmdleten **Start-AzRecoveryServicesAsrTestFailoverJob** startar testredundans av ett skyddat objekt eller en återställnings plan för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="21a6b-112">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="21a6b-113">Du kan kontrol lera om jobbet lyckades med Get-AzRecoveryServicesAsrJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21a6b-113">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="21a6b-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="21a6b-114">EXAMPLES</span></span>

### <span data-ttu-id="21a6b-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="21a6b-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="21a6b-116">Startar redundanstestning-åtgärden för återställnings planen med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="21a6b-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="21a6b-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="21a6b-117">PARAMETERS</span></span>

### <span data-ttu-id="21a6b-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="21a6b-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="21a6b-119">Anger Azure VM-nätverks-ID för återställning av VM efter redundans.</span><span class="sxs-lookup"><span data-stu-id="21a6b-119">Specifies the Azure vm network id for recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21a6b-120">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="21a6b-120">-CloudServiceCreationOption</span></span>
<span data-ttu-id="21a6b-121">Anger om en ny moln tjänst ska skapas eller om återställnings moln tjänsten som är konfigurerad för den virtuella datorn ska användas för redundanstestning.</span><span class="sxs-lookup"><span data-stu-id="21a6b-121">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPIObject, ByRPObject, ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:
Accepted values: UseRecoveryCloudService, AutoCreateCloudService

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21a6b-122">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="21a6b-122">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="21a6b-123">Anger den primära certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="21a6b-123">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="21a6b-124">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="21a6b-124">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="21a6b-125">Anger den sekundära certifikats filen.</span><span class="sxs-lookup"><span data-stu-id="21a6b-125">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="21a6b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21a6b-126">-DefaultProfile</span></span>
<span data-ttu-id="21a6b-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="21a6b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="21a6b-128">-Riktning</span><span class="sxs-lookup"><span data-stu-id="21a6b-128">-Direction</span></span>
<span data-ttu-id="21a6b-129">Anger växlings riktning.</span><span class="sxs-lookup"><span data-stu-id="21a6b-129">Specifies the failover direction.</span></span>
<span data-ttu-id="21a6b-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="21a6b-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="21a6b-131">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="21a6b-131">PrimaryToRecovery</span></span>
- <span data-ttu-id="21a6b-132">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="21a6b-132">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="21a6b-133">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="21a6b-133">-RecoveryPlan</span></span>
<span data-ttu-id="21a6b-134">Anger ett plan objekt för ASR-återställning.</span><span class="sxs-lookup"><span data-stu-id="21a6b-134">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21a6b-135">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="21a6b-135">-RecoveryPoint</span></span>
<span data-ttu-id="21a6b-136">Anger en anpassad återställnings punkt för att testa redundans på den skyddade datorn.</span><span class="sxs-lookup"><span data-stu-id="21a6b-136">Specifies a custom recovery point to test failover the protected machine to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21a6b-137">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="21a6b-137">-RecoveryTag</span></span>
<span data-ttu-id="21a6b-138">Anger återställnings tag gen för redundanstest till</span><span class="sxs-lookup"><span data-stu-id="21a6b-138">Specifies the recovery tag to test failover to</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21a6b-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="21a6b-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="21a6b-140">Anger ett skyddat objekt i ASR-replikering.</span><span class="sxs-lookup"><span data-stu-id="21a6b-140">Specifies an ASR replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21a6b-141">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="21a6b-141">-VMNetwork</span></span>
<span data-ttu-id="21a6b-142">Anger det virtuella dator nätverket för webbplats återställning för att ansluta den virtuella datorn för redundanstest till.</span><span class="sxs-lookup"><span data-stu-id="21a6b-142">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21a6b-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="21a6b-143">-Confirm</span></span>
<span data-ttu-id="21a6b-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="21a6b-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21a6b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21a6b-145">-WhatIf</span></span>
<span data-ttu-id="21a6b-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="21a6b-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21a6b-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="21a6b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21a6b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21a6b-148">CommonParameters</span></span>
<span data-ttu-id="21a6b-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21a6b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21a6b-150">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21a6b-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21a6b-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="21a6b-151">INPUTS</span></span>

### <span data-ttu-id="21a6b-152">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="21a6b-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="21a6b-153">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="21a6b-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="21a6b-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="21a6b-154">OUTPUTS</span></span>

### <span data-ttu-id="21a6b-155">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="21a6b-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="21a6b-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="21a6b-156">NOTES</span></span>

## <span data-ttu-id="21a6b-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="21a6b-157">RELATED LINKS</span></span>

[<span data-ttu-id="21a6b-158">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="21a6b-158">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
