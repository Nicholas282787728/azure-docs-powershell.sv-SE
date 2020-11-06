---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: bab9cb87f347b198b430c1dadc65a002dfa94141
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573351"
---
# <span data-ttu-id="7c525-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="7c525-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="7c525-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7c525-102">SYNOPSIS</span></span>
<span data-ttu-id="7c525-103">Startar en redundanstest.</span><span class="sxs-lookup"><span data-stu-id="7c525-103">Starts a test failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c525-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7c525-104">SYNTAX</span></span>

### <span data-ttu-id="7c525-105">ByRPIObject (standard)</span><span class="sxs-lookup"><span data-stu-id="7c525-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c525-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="7c525-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c525-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="7c525-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c525-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="7c525-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c525-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="7c525-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c525-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="7c525-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7c525-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7c525-111">DESCRIPTION</span></span>
<span data-ttu-id="7c525-112">Cmdleten **Start-AzureRmRecoveryServicesAsrTestFailoverJob** startar testredundans av ett skyddat objekt eller en återställnings plan för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7c525-112">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="7c525-113">Du kan kontrol lera om jobbet lyckades med Get-AzureRmRecoveryServicesAsrJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c525-113">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="7c525-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7c525-114">EXAMPLES</span></span>

### <span data-ttu-id="7c525-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7c525-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="7c525-116">Startar redundanstestning-åtgärden för återställnings planen med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="7c525-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7c525-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7c525-117">PARAMETERS</span></span>

### <span data-ttu-id="7c525-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="7c525-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="7c525-119">Anger ID för Azure Virtual Network för att ansluta testet Miss lyckas via virtuella datorer till.</span><span class="sxs-lookup"><span data-stu-id="7c525-119">Specifies the Azure virtual network ID to connect the test fail over virtual machine(s) to.</span></span>

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

### <span data-ttu-id="7c525-120">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="7c525-120">-CloudServiceCreationOption</span></span>
<span data-ttu-id="7c525-121">Anger om en ny moln tjänst ska skapas eller om återställnings moln tjänsten som är konfigurerad för den virtuella datorn ska användas för redundanstestning.</span><span class="sxs-lookup"><span data-stu-id="7c525-121">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

```yaml
Type: String
Parameter Sets: ByRPIObject, ByRPObject, ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:
Accepted values: UseRecoveryCloudService, AutoCreateCloudService

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c525-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7c525-122">-Confirm</span></span>
<span data-ttu-id="7c525-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7c525-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c525-124">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="7c525-124">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="7c525-125">Anger den primära certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="7c525-125">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="7c525-126">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="7c525-126">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="7c525-127">Anger den sekundära certifikats filen.</span><span class="sxs-lookup"><span data-stu-id="7c525-127">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="7c525-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c525-128">-DefaultProfile</span></span>
<span data-ttu-id="7c525-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7c525-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="7c525-130">-Riktning</span><span class="sxs-lookup"><span data-stu-id="7c525-130">-Direction</span></span>
<span data-ttu-id="7c525-131">Anger växlings riktning.</span><span class="sxs-lookup"><span data-stu-id="7c525-131">Specifies the failover direction.</span></span>
<span data-ttu-id="7c525-132">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="7c525-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7c525-133">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="7c525-133">PrimaryToRecovery</span></span>
- <span data-ttu-id="7c525-134">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="7c525-134">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="7c525-135">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7c525-135">-RecoveryPlan</span></span>
<span data-ttu-id="7c525-136">Anger ett plan objekt för ASR-återställning.</span><span class="sxs-lookup"><span data-stu-id="7c525-136">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="7c525-137">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="7c525-137">-RecoveryPoint</span></span>
<span data-ttu-id="7c525-138">Anger en anpassad återställnings punkt för att testa redundans på den skyddade datorn.</span><span class="sxs-lookup"><span data-stu-id="7c525-138">Specifies a custom recovery point to test failover the protected machine to.</span></span>

```yaml
Type: ASRRecoveryPoint
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c525-139">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="7c525-139">-RecoveryTag</span></span>
<span data-ttu-id="7c525-140">Anger återställnings tag gen för redundanstest till</span><span class="sxs-lookup"><span data-stu-id="7c525-140">Specifies the recovery tag to test failover to</span></span>

```yaml
Type: String
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c525-141">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7c525-141">-ReplicationProtectedItem</span></span>
<span data-ttu-id="7c525-142">Anger ett skyddat objekt i ASR-replikering.</span><span class="sxs-lookup"><span data-stu-id="7c525-142">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="7c525-143">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="7c525-143">-VMNetwork</span></span>
<span data-ttu-id="7c525-144">Anger det virtuella dator nätverket för webbplats återställning för att ansluta den virtuella datorn för redundanstest till.</span><span class="sxs-lookup"><span data-stu-id="7c525-144">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

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

### <span data-ttu-id="7c525-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c525-145">-WhatIf</span></span>
<span data-ttu-id="7c525-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7c525-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c525-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7c525-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c525-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c525-148">CommonParameters</span></span>
<span data-ttu-id="7c525-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c525-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c525-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c525-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c525-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7c525-151">INPUTS</span></span>

### <span data-ttu-id="7c525-152">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7c525-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="7c525-153">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7c525-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="7c525-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7c525-154">OUTPUTS</span></span>

### <span data-ttu-id="7c525-155">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7c525-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7c525-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7c525-156">NOTES</span></span>

## <span data-ttu-id="7c525-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7c525-157">RELATED LINKS</span></span>

[<span data-ttu-id="7c525-158">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="7c525-158">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
