---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: E33F9131-9240-4D50-972D-810775AF1506
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverytestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
ms.openlocfilehash: 236ba6a3cbf65786af7d17e587ef5de0af86a296
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574159"
---
# <span data-ttu-id="f738e-101">Start-AzureRmSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="f738e-101">Start-AzureRmSiteRecoveryTestFailoverJob</span></span>

## <span data-ttu-id="f738e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f738e-102">SYNOPSIS</span></span>
<span data-ttu-id="f738e-103">Startar en redundanstest för en entitet för webbplats återställnings skydd.</span><span class="sxs-lookup"><span data-stu-id="f738e-103">Starts a test failover for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f738e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f738e-104">SYNTAX</span></span>

### <span data-ttu-id="f738e-105">ByPEObject (standard)</span><span class="sxs-lookup"><span data-stu-id="f738e-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f738e-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="f738e-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f738e-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="f738e-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f738e-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="f738e-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f738e-109">ByPEObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="f738e-109">ByPEObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f738e-110">ByPEObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="f738e-110">ByPEObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f738e-111">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="f738e-111">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f738e-112">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="f738e-112">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f738e-113">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="f738e-113">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f738e-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f738e-114">DESCRIPTION</span></span>
<span data-ttu-id="f738e-115">Cmdleten **Start-AzureRmSiteRecoveryTestFailoverJob** startar redundanstestning för en Azure Site Recovery-enhet eller återställnings plan.</span><span class="sxs-lookup"><span data-stu-id="f738e-115">The **Start-AzureRmSiteRecoveryTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="f738e-116">Du kan kontrol lera om jobbet lyckades med Get-AzureRmSiteRecoveryJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f738e-116">You can check whether the job succeeded by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="f738e-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f738e-117">EXAMPLES</span></span>

## <span data-ttu-id="f738e-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f738e-118">PARAMETERS</span></span>

### <span data-ttu-id="f738e-119">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="f738e-119">-AzureVMNetworkId</span></span>
<span data-ttu-id="f738e-120">Anger ID för Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="f738e-120">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByPEObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f738e-121">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="f738e-121">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="f738e-122">Anger den primära certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="f738e-122">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="f738e-123">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="f738e-123">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="f738e-124">Anger den sekundära certifikats filen.</span><span class="sxs-lookup"><span data-stu-id="f738e-124">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="f738e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f738e-125">-DefaultProfile</span></span>
<span data-ttu-id="f738e-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f738e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f738e-127">-Riktning</span><span class="sxs-lookup"><span data-stu-id="f738e-127">-Direction</span></span>
<span data-ttu-id="f738e-128">Anger växlings riktning.</span><span class="sxs-lookup"><span data-stu-id="f738e-128">Specifies the failover direction.</span></span>
<span data-ttu-id="f738e-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f738e-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f738e-130">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="f738e-130">PrimaryToRecovery</span></span>
- <span data-ttu-id="f738e-131">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="f738e-131">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="f738e-132">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f738e-132">-ProtectionEntity</span></span>
<span data-ttu-id="f738e-133">Anger objektet för webbplats återställnings skydd.</span><span class="sxs-lookup"><span data-stu-id="f738e-133">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject, ByPEObjectWithVMNetwork, ByPEObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f738e-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f738e-134">-RecoveryPlan</span></span>
<span data-ttu-id="f738e-135">Anger ett återställnings plan objekt.</span><span class="sxs-lookup"><span data-stu-id="f738e-135">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="f738e-136">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f738e-136">-ReplicationProtectedItem</span></span>
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

### <span data-ttu-id="f738e-137">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="f738e-137">-VMNetwork</span></span>
<span data-ttu-id="f738e-138">Anger det virtuella dator nätverket för webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="f738e-138">Specifies the Site Recovery virtual machine network.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByPEObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f738e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f738e-139">CommonParameters</span></span>
<span data-ttu-id="f738e-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f738e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f738e-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f738e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f738e-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f738e-142">INPUTS</span></span>

### <span data-ttu-id="f738e-143">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f738e-143">ASRProtectionEntity</span></span>
<span data-ttu-id="f738e-144">Parametern ' ProtectionEntity ' godkänner värdet av typen ' ASRProtectionEntity ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f738e-144">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="f738e-145">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f738e-145">ASRRecoveryPlan</span></span>
<span data-ttu-id="f738e-146">Parametern ' RecoveryPlan ' godkänner värdet av typen ' ASRRecoveryPlan ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f738e-146">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="f738e-147">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f738e-147">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="f738e-148">Parametern ' ReplicationProtectedItem ' godkänner värdet av typen ' ASRReplicationProtectedItem ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f738e-148">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="f738e-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f738e-149">OUTPUTS</span></span>

### <span data-ttu-id="f738e-150">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f738e-150">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f738e-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f738e-151">NOTES</span></span>

## <span data-ttu-id="f738e-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f738e-152">RELATED LINKS</span></span>

[<span data-ttu-id="f738e-153">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="f738e-153">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)
