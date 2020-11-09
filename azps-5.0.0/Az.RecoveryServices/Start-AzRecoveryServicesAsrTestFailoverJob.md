---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: 11d254fbf43a05e4e58f0d51f5226a6a7065dd50
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324510"
---
# <span data-ttu-id="af9c6-101">Start-AzRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="af9c6-101">Start-AzRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="af9c6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af9c6-102">SYNOPSIS</span></span>
<span data-ttu-id="af9c6-103">Startar en redundanstest.</span><span class="sxs-lookup"><span data-stu-id="af9c6-103">Starts a test failover operation.</span></span>

## <span data-ttu-id="af9c6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af9c6-104">SYNTAX</span></span>

### <span data-ttu-id="af9c6-105">ByRPIObject (standard)</span><span class="sxs-lookup"><span data-stu-id="af9c6-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af9c6-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="af9c6-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af9c6-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="af9c6-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af9c6-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="af9c6-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af9c6-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="af9c6-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af9c6-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="af9c6-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af9c6-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af9c6-111">DESCRIPTION</span></span>
<span data-ttu-id="af9c6-112">Cmdleten **Start-AzRecoveryServicesAsrTestFailoverJob** startar testredundans av ett skyddat objekt eller en återställnings plan för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="af9c6-112">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="af9c6-113">Du kan kontrol lera om jobbet lyckades med Get-AzRecoveryServicesAsrJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af9c6-113">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="af9c6-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af9c6-114">EXAMPLES</span></span>

### <span data-ttu-id="af9c6-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="af9c6-115">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="af9c6-116">Startar redundanstestning-åtgärden för återställnings planen med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="af9c6-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="af9c6-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="af9c6-117">Example 2</span></span>

<span data-ttu-id="af9c6-118">Startar en redundanstest.</span><span class="sxs-lookup"><span data-stu-id="af9c6-118">Starts a test failover operation.</span></span> <span data-ttu-id="af9c6-119">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="af9c6-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrTestFailoverJob -AzureVMNetworkId <String> -Direction PrimaryToRecovery -RecoveryPlan $RP
```

## <span data-ttu-id="af9c6-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af9c6-120">PARAMETERS</span></span>

### <span data-ttu-id="af9c6-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="af9c6-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="af9c6-122">Anger Azure VM-nätverks-ID för återställning av VM efter redundans.</span><span class="sxs-lookup"><span data-stu-id="af9c6-122">Specifies the Azure vm network id for recovery VM after failover.</span></span>

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

### <span data-ttu-id="af9c6-123">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="af9c6-123">-CloudServiceCreationOption</span></span>
<span data-ttu-id="af9c6-124">Anger om en ny moln tjänst ska skapas eller om återställnings moln tjänsten som är konfigurerad för den virtuella datorn ska användas för redundanstestning.</span><span class="sxs-lookup"><span data-stu-id="af9c6-124">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

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

### <span data-ttu-id="af9c6-125">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="af9c6-125">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="af9c6-126">Anger den primära certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="af9c6-126">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="af9c6-127">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="af9c6-127">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="af9c6-128">Anger den sekundära certifikats filen.</span><span class="sxs-lookup"><span data-stu-id="af9c6-128">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="af9c6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af9c6-129">-DefaultProfile</span></span>
<span data-ttu-id="af9c6-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="af9c6-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="af9c6-131">-Riktning</span><span class="sxs-lookup"><span data-stu-id="af9c6-131">-Direction</span></span>
<span data-ttu-id="af9c6-132">Anger växlings riktning.</span><span class="sxs-lookup"><span data-stu-id="af9c6-132">Specifies the failover direction.</span></span>
<span data-ttu-id="af9c6-133">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="af9c6-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="af9c6-134">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="af9c6-134">PrimaryToRecovery</span></span>
- <span data-ttu-id="af9c6-135">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="af9c6-135">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="af9c6-136">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="af9c6-136">-RecoveryPlan</span></span>
<span data-ttu-id="af9c6-137">Anger ett plan objekt för ASR-återställning.</span><span class="sxs-lookup"><span data-stu-id="af9c6-137">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="af9c6-138">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="af9c6-138">-RecoveryPoint</span></span>
<span data-ttu-id="af9c6-139">Anger en anpassad återställnings punkt för att testa redundans på den skyddade datorn.</span><span class="sxs-lookup"><span data-stu-id="af9c6-139">Specifies a custom recovery point to test failover the protected machine to.</span></span>

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

### <span data-ttu-id="af9c6-140">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="af9c6-140">-RecoveryTag</span></span>
<span data-ttu-id="af9c6-141">Anger återställnings tag gen för redundanstest till</span><span class="sxs-lookup"><span data-stu-id="af9c6-141">Specifies the recovery tag to test failover to</span></span>

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

### <span data-ttu-id="af9c6-142">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="af9c6-142">-ReplicationProtectedItem</span></span>
<span data-ttu-id="af9c6-143">Anger ett skyddat objekt i ASR-replikering.</span><span class="sxs-lookup"><span data-stu-id="af9c6-143">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="af9c6-144">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="af9c6-144">-VMNetwork</span></span>
<span data-ttu-id="af9c6-145">Anger det virtuella dator nätverket för webbplats återställning för att ansluta den virtuella datorn för redundanstest till.</span><span class="sxs-lookup"><span data-stu-id="af9c6-145">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

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

### <span data-ttu-id="af9c6-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="af9c6-146">-Confirm</span></span>
<span data-ttu-id="af9c6-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="af9c6-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af9c6-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af9c6-148">-WhatIf</span></span>
<span data-ttu-id="af9c6-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="af9c6-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af9c6-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="af9c6-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af9c6-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af9c6-151">CommonParameters</span></span>
<span data-ttu-id="af9c6-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af9c6-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af9c6-153">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af9c6-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af9c6-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af9c6-154">INPUTS</span></span>

### <span data-ttu-id="af9c6-155">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="af9c6-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="af9c6-156">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="af9c6-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="af9c6-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af9c6-157">OUTPUTS</span></span>

### <span data-ttu-id="af9c6-158">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="af9c6-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="af9c6-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af9c6-159">NOTES</span></span>

## <span data-ttu-id="af9c6-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af9c6-160">RELATED LINKS</span></span>

[<span data-ttu-id="af9c6-161">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="af9c6-161">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
