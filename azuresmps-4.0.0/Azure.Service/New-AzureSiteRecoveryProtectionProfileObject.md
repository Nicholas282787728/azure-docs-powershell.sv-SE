---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 853D5585-2A92-4B65-BA8C-EC06BEE8C237
online version: ''
schema: 2.0.0
ms.openlocfilehash: 63274c772c6085fc8c491557851673a38056aa77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099121"
---
# <span data-ttu-id="a0cee-101">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="a0cee-101">New-AzureSiteRecoveryProtectionProfileObject</span></span>

## <span data-ttu-id="a0cee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a0cee-102">SYNOPSIS</span></span>
<span data-ttu-id="a0cee-103">Skapar ett profil objekt för webbplats återställnings skydd.</span><span class="sxs-lookup"><span data-stu-id="a0cee-103">Creates a Site Recovery protection profile object.</span></span>

## <span data-ttu-id="a0cee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a0cee-104">SYNTAX</span></span>

### <span data-ttu-id="a0cee-105">EnterpriseToAzure (standard)</span><span class="sxs-lookup"><span data-stu-id="a0cee-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 -RecoveryAzureSubscription <String> -RecoveryAzureStorageAccount <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a0cee-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="a0cee-106">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-CompressionEnabled] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-AllowReplicaDeletion] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a0cee-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a0cee-107">DESCRIPTION</span></span>
<span data-ttu-id="a0cee-108">Cmdleten **New-AzureSiteRecoveryProtectionProfileObject** skapar ett Azure Site Recovery Protection-profil objekt.</span><span class="sxs-lookup"><span data-stu-id="a0cee-108">The **New-AzureSiteRecoveryProtectionProfileObject** cmdlet creates an Azure Site Recovery protection profile object.</span></span>
<span data-ttu-id="a0cee-109">Denna cmdlet skapar ett **ASRProtectionProfile** -objekt som ska användas med andra cmdletar.</span><span class="sxs-lookup"><span data-stu-id="a0cee-109">This cmdlet creates an **ASRProtectionProfile** object to use with other cmdlets.</span></span>

## <span data-ttu-id="a0cee-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a0cee-110">EXAMPLES</span></span>

### <span data-ttu-id="a0cee-111">Exempel 1: skapa en skydds profil</span><span class="sxs-lookup"><span data-stu-id="a0cee-111">Example 1: Create a protection profile</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
Name                                     : 
ID                                       : 
ReplicationProvider                      : HyperVReplica
HyperVReplicaProviderSettingsObject      : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaProviderSettings
HyperVReplicaAzureProviderSettingsObject :
```

<span data-ttu-id="a0cee-112">Det här kommandot skapar ett skydds profil objekt.</span><span class="sxs-lookup"><span data-stu-id="a0cee-112">This command creates a protection profile object.</span></span>

### <span data-ttu-id="a0cee-113">Exempel 2: skapa en skydds profil för HyperVReplicaAzure-leverantören</span><span class="sxs-lookup"><span data-stu-id="a0cee-113">Example 2: Create a protection profile for HyperVReplicaAzure provider</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -Name "ProtectionProfile" -ReplicationProvider "HyperVReplicaAzure" -RecoveryAzureSubscription "cb53d0c3-bd59-4721-89bc-06916a9147ef" -RecoveryAzureStorageAccount "Contoso01" -ReplicationFrequencyInSeconds 30 -RecoveryPoints 1 -Force
Name                                     : ProtectionProfile
ID                                       : 
ReplicationProvider                      : HyperVReplicaAzure
HyperVReplicaProviderSettingsObject      : 
HyperVReplicaAzureProviderSettingsObject : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaAzureProviderSettings
```

<span data-ttu-id="a0cee-114">Det här kommandot skapar en skydds profil för en HyperVReplicaAzure-leverantör.</span><span class="sxs-lookup"><span data-stu-id="a0cee-114">This command creates a protection profile for a HyperVReplicaAzure provider.</span></span>

## <span data-ttu-id="a0cee-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a0cee-115">PARAMETERS</span></span>

### <span data-ttu-id="a0cee-116">-AllowReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="a0cee-116">-AllowReplicaDeletion</span></span>
<span data-ttu-id="a0cee-117">Anger att skydds profilen tillåter borttagning av replik enheter.</span><span class="sxs-lookup"><span data-stu-id="a0cee-117">Indicates that the protection profile enables deletion of replica entities.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0cee-118">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="a0cee-118">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="a0cee-119">Anger frekvensen i timmar för programspecifika stillbilder.</span><span class="sxs-lookup"><span data-stu-id="a0cee-119">Specifies the frequency, in hours, for application consistent snapshots.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0cee-120">-Inloggningsautentisering</span><span class="sxs-lookup"><span data-stu-id="a0cee-120">-Authentication</span></span>
<span data-ttu-id="a0cee-121">Anger vilken typ av verifikation som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a0cee-121">Specifies the type of authentication to use.</span></span>
<span data-ttu-id="a0cee-122">De acceptabla värdena för den här parametern är: certifikat och Kerberos.</span><span class="sxs-lookup"><span data-stu-id="a0cee-122">The acceptable values for this parameter are: Certificate and Kerberos.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0cee-123">-CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="a0cee-123">-CompressionEnabled</span></span>
<span data-ttu-id="a0cee-124">Anger att skydds profilen aktiverar komprimering.</span><span class="sxs-lookup"><span data-stu-id="a0cee-124">Indicates that the protection profile enables compression.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0cee-125">-Force</span><span class="sxs-lookup"><span data-stu-id="a0cee-125">-Force</span></span>
<span data-ttu-id="a0cee-126">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a0cee-126">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0cee-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="a0cee-127">-Name</span></span>
<span data-ttu-id="a0cee-128">Anger ett namn på skydds profilen.</span><span class="sxs-lookup"><span data-stu-id="a0cee-128">Specifies a name for the protection profile.</span></span>

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

### <span data-ttu-id="a0cee-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="a0cee-129">-Profile</span></span>
<span data-ttu-id="a0cee-130">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="a0cee-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a0cee-131">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="a0cee-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0cee-132">-RecoveryAzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a0cee-132">-RecoveryAzureStorageAccount</span></span>
<span data-ttu-id="a0cee-133">Anger namnet på ett Azure Storage-konto där du vill att Azure Replica-enheten ska lagras.</span><span class="sxs-lookup"><span data-stu-id="a0cee-133">Specifies the name of an Azure Storage account on which to store the Azure replica entity.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0cee-134">-RecoveryAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="a0cee-134">-RecoveryAzureSubscription</span></span>
<span data-ttu-id="a0cee-135">Anger ID för ett Azure-abonnemang för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="a0cee-135">Specifies the ID for an Azure Subscription for a storage account.</span></span>
<span data-ttu-id="a0cee-136">Den här parametern refererar till det konto som du vill att Azure Replica-enheten ska lagras på.</span><span class="sxs-lookup"><span data-stu-id="a0cee-136">This parameter refers to the account on which to store the Azure replica entity.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0cee-137">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="a0cee-137">-RecoveryPoints</span></span>
<span data-ttu-id="a0cee-138">Anger antalet timmar som återställnings punkter ska sparas i.</span><span class="sxs-lookup"><span data-stu-id="a0cee-138">Specifies the number of hours to retain recovery points.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0cee-139">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="a0cee-139">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="a0cee-140">Anger frekvens intervallet, i sekunder, för replikering.</span><span class="sxs-lookup"><span data-stu-id="a0cee-140">Specifies the frequency interval, in seconds, for replication.</span></span> <span data-ttu-id="a0cee-141">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a0cee-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a0cee-142">halvtimme</span><span class="sxs-lookup"><span data-stu-id="a0cee-142">30</span></span> 
- <span data-ttu-id="a0cee-143">300</span><span class="sxs-lookup"><span data-stu-id="a0cee-143">300</span></span> 
- <span data-ttu-id="a0cee-144">900</span><span class="sxs-lookup"><span data-stu-id="a0cee-144">900</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0cee-145">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="a0cee-145">-ReplicationMethod</span></span>
<span data-ttu-id="a0cee-146">Anger replikeringsfrekvensen.</span><span class="sxs-lookup"><span data-stu-id="a0cee-146">Specifies the replication method.</span></span> <span data-ttu-id="a0cee-147">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a0cee-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a0cee-148">Support.</span><span class="sxs-lookup"><span data-stu-id="a0cee-148">Online.</span></span>
<span data-ttu-id="a0cee-149">Replikering via nätverket.</span><span class="sxs-lookup"><span data-stu-id="a0cee-149">Replication over the network.</span></span>
- <span data-ttu-id="a0cee-150">Arbetade.</span><span class="sxs-lookup"><span data-stu-id="a0cee-150">Offline.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0cee-151">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="a0cee-151">-ReplicationPort</span></span>
<span data-ttu-id="a0cee-152">Anger numret på den port som replikeringen utförs på.</span><span class="sxs-lookup"><span data-stu-id="a0cee-152">Specifies the number of the port on which the replication occurs.</span></span>

```yaml
Type: UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0cee-153">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="a0cee-153">-ReplicationProvider</span></span>
<span data-ttu-id="a0cee-154">Anger typen av replikeringsprovider.</span><span class="sxs-lookup"><span data-stu-id="a0cee-154">Specifies the type of replication provider.</span></span> <span data-ttu-id="a0cee-155">De acceptabla värdena för den här parametern är: HyperVReplica och HyperVReplicaAzure.</span><span class="sxs-lookup"><span data-stu-id="a0cee-155">The acceptable values for this parameter are: HyperVReplica and HyperVReplicaAzure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0cee-156">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="a0cee-156">-ReplicationStartTime</span></span>
<span data-ttu-id="a0cee-157">Anger start tiden för replikeringen.</span><span class="sxs-lookup"><span data-stu-id="a0cee-157">Specifies the start time of the replication.</span></span>
<span data-ttu-id="a0cee-158">Ange en tid inom 24 timmar efter att du har startat jobbet.</span><span class="sxs-lookup"><span data-stu-id="a0cee-158">Specify a time within 24 hours after you start the job.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0cee-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0cee-159">CommonParameters</span></span>
<span data-ttu-id="a0cee-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0cee-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0cee-161">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0cee-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0cee-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a0cee-162">INPUTS</span></span>

## <span data-ttu-id="a0cee-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a0cee-163">OUTPUTS</span></span>

## <span data-ttu-id="a0cee-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a0cee-164">NOTES</span></span>

## <span data-ttu-id="a0cee-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a0cee-165">RELATED LINKS</span></span>

[<span data-ttu-id="a0cee-166">Azure Site Recovery Services-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a0cee-166">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


