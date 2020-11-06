---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: E33F9131-9240-4D50-972D-810775AF1506
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
ms.openlocfilehash: 330af3701741cbc83573afbbe7e283fdee294cdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583748"
---
# <span data-ttu-id="91208-101">Start-AzureRmSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="91208-101">Start-AzureRmSiteRecoveryTestFailoverJob</span></span>

## <span data-ttu-id="91208-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="91208-102">SYNOPSIS</span></span>
<span data-ttu-id="91208-103">Startar en redundanstest för en entitet för webbplats återställnings skydd.</span><span class="sxs-lookup"><span data-stu-id="91208-103">Starts a test failover for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91208-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="91208-104">SYNTAX</span></span>

### <span data-ttu-id="91208-105">ByPEObject (standard)</span><span class="sxs-lookup"><span data-stu-id="91208-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91208-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="91208-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91208-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="91208-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91208-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="91208-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91208-109">ByPEObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="91208-109">ByPEObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91208-110">ByPEObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="91208-110">ByPEObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91208-111">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="91208-111">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91208-112">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="91208-112">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91208-113">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="91208-113">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91208-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="91208-114">DESCRIPTION</span></span>
<span data-ttu-id="91208-115">Cmdleten **Start-AzureRmSiteRecoveryTestFailoverJob** startar redundanstestning för en Azure Site Recovery-enhet eller återställnings plan.</span><span class="sxs-lookup"><span data-stu-id="91208-115">The **Start-AzureRmSiteRecoveryTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="91208-116">Du kan kontrol lera om jobbet lyckades med Get-AzureRmSiteRecoveryJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91208-116">You can check whether the job succeeded by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="91208-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="91208-117">EXAMPLES</span></span>

## <span data-ttu-id="91208-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="91208-118">PARAMETERS</span></span>

### <span data-ttu-id="91208-119">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="91208-119">-AzureVMNetworkId</span></span>
<span data-ttu-id="91208-120">Anger ID för Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="91208-120">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByPEObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91208-121">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="91208-121">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="91208-122">Anger den primära certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="91208-122">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="91208-123">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="91208-123">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="91208-124">Anger den sekundära certifikats filen.</span><span class="sxs-lookup"><span data-stu-id="91208-124">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="91208-125">-Riktning</span><span class="sxs-lookup"><span data-stu-id="91208-125">-Direction</span></span>
<span data-ttu-id="91208-126">Anger växlings riktning.</span><span class="sxs-lookup"><span data-stu-id="91208-126">Specifies the failover direction.</span></span>
<span data-ttu-id="91208-127">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="91208-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91208-128">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="91208-128">PrimaryToRecovery</span></span>
- <span data-ttu-id="91208-129">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="91208-129">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="91208-130">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="91208-130">-ProtectionEntity</span></span>
<span data-ttu-id="91208-131">Anger objektet för webbplats återställnings skydd.</span><span class="sxs-lookup"><span data-stu-id="91208-131">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject, ByPEObjectWithVMNetwork, ByPEObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91208-132">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="91208-132">-RecoveryPlan</span></span>
<span data-ttu-id="91208-133">Anger ett återställnings plan objekt.</span><span class="sxs-lookup"><span data-stu-id="91208-133">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91208-134">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="91208-134">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91208-135">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="91208-135">-VMNetwork</span></span>
<span data-ttu-id="91208-136">Anger det virtuella dator nätverket för webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="91208-136">Specifies the Site Recovery virtual machine network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByPEObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91208-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91208-137">-DefaultProfile</span></span>
<span data-ttu-id="91208-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="91208-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91208-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91208-139">CommonParameters</span></span>
<span data-ttu-id="91208-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91208-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91208-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91208-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91208-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="91208-142">INPUTS</span></span>

### <span data-ttu-id="91208-143">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="91208-143">ASRProtectionEntity</span></span>
<span data-ttu-id="91208-144">Parametern ' ProtectionEntity ' godkänner värdet av typen ' ASRProtectionEntity ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="91208-144">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="91208-145">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="91208-145">ASRRecoveryPlan</span></span>
<span data-ttu-id="91208-146">Parametern ' RecoveryPlan ' godkänner värdet av typen ' ASRRecoveryPlan ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="91208-146">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="91208-147">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="91208-147">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="91208-148">Parametern ' ReplicationProtectedItem ' godkänner värdet av typen ' ASRReplicationProtectedItem ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="91208-148">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="91208-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="91208-149">OUTPUTS</span></span>

### <span data-ttu-id="91208-150">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="91208-150">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="91208-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="91208-151">NOTES</span></span>

## <span data-ttu-id="91208-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="91208-152">RELATED LINKS</span></span>

[<span data-ttu-id="91208-153">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="91208-153">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)
