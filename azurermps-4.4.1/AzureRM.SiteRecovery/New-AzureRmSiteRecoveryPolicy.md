---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 85C543FE-BBC1-4A1B-9974-1D3BF520085C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: e876e1a7beeee19cd68ac629eb08d48356f98da8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757735"
---
# <span data-ttu-id="15365-101">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="15365-101">New-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="15365-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="15365-102">SYNOPSIS</span></span>
<span data-ttu-id="15365-103">Skapar en replikeringsprincip för en webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="15365-103">Creates a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15365-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="15365-104">SYNTAX</span></span>

### <span data-ttu-id="15365-105">EnterpriseToAzure (standard)</span><span class="sxs-lookup"><span data-stu-id="15365-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="15365-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="15365-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15365-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="15365-107">DESCRIPTION</span></span>
<span data-ttu-id="15365-108">Cmdleten **New-AzureRmSiteRecoveryPolicy** skapar en Azure Site Recovery Replication-replikeringsprincip.</span><span class="sxs-lookup"><span data-stu-id="15365-108">The **New-AzureRmSiteRecoveryPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="15365-109">Replikeringsprincipen används för att ange replikeringsinställningar som replikeringsfrekvens och antal återställnings punkter.</span><span class="sxs-lookup"><span data-stu-id="15365-109">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="15365-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="15365-110">EXAMPLES</span></span>

## <span data-ttu-id="15365-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="15365-111">PARAMETERS</span></span>

### <span data-ttu-id="15365-112">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="15365-112">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="15365-113">Anger frekvensen för programkonsekvent ögonblicks bild i timmar.</span><span class="sxs-lookup"><span data-stu-id="15365-113">Specifies the frequency of the application consistent snapshot in hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15365-114">-Inloggningsautentisering</span><span class="sxs-lookup"><span data-stu-id="15365-114">-Authentication</span></span>
<span data-ttu-id="15365-115">Anger vilken typ av verifikation som används.</span><span class="sxs-lookup"><span data-stu-id="15365-115">Specifies the type of authentication used.</span></span>
<span data-ttu-id="15365-116">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="15365-116">Valid values are:</span></span>

- <span data-ttu-id="15365-117">Upplåsningscertifikat</span><span class="sxs-lookup"><span data-stu-id="15365-117">Certificate</span></span>
-  <span data-ttu-id="15365-118">Kerberos</span><span class="sxs-lookup"><span data-stu-id="15365-118">Kerberos</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15365-119">-Komprimering</span><span class="sxs-lookup"><span data-stu-id="15365-119">-Compression</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15365-120">-Kryptering</span><span class="sxs-lookup"><span data-stu-id="15365-120">-Encryption</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15365-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="15365-121">-Name</span></span>
<span data-ttu-id="15365-122">Anger ett vänligt namn som identifierar replikeringsprincipen för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="15365-122">Specifies a friendly name which identifies the Site Recovery replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15365-123">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="15365-123">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="15365-124">Anger ID för Azure Storage-kontot för målobjektet.</span><span class="sxs-lookup"><span data-stu-id="15365-124">Specifies the Azure storage account ID of the replication target.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15365-125">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="15365-125">-RecoveryPoints</span></span>
<span data-ttu-id="15365-126">Anger antalet timmar som återställnings punkter ska sparas i.</span><span class="sxs-lookup"><span data-stu-id="15365-126">Specifies the number of hours to retain recovery points.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15365-127">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="15365-127">-ReplicaDeletion</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15365-128">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="15365-128">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="15365-129">Anger frekvens intervallet för replikering i sekunder.</span><span class="sxs-lookup"><span data-stu-id="15365-129">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="15365-130">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="15365-130">Valid values are:</span></span>

- <span data-ttu-id="15365-131">halvtimme</span><span class="sxs-lookup"><span data-stu-id="15365-131">30</span></span>
- <span data-ttu-id="15365-132">300</span><span class="sxs-lookup"><span data-stu-id="15365-132">300</span></span>
- <span data-ttu-id="15365-133">900</span><span class="sxs-lookup"><span data-stu-id="15365-133">900</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15365-134">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="15365-134">-ReplicationMethod</span></span>
<span data-ttu-id="15365-135">Anger replikeringsfrekvensen.</span><span class="sxs-lookup"><span data-stu-id="15365-135">Specifies the replication method.</span></span>
<span data-ttu-id="15365-136">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="15365-136">Valid values are:</span></span>

- <span data-ttu-id="15365-137">Support</span><span class="sxs-lookup"><span data-stu-id="15365-137">Online</span></span>
- <span data-ttu-id="15365-138">Arbetade</span><span class="sxs-lookup"><span data-stu-id="15365-138">Offline</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15365-139">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="15365-139">-ReplicationPort</span></span>
<span data-ttu-id="15365-140">Anger vilken port som används för replikering.</span><span class="sxs-lookup"><span data-stu-id="15365-140">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15365-141">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="15365-141">-ReplicationProvider</span></span>
<span data-ttu-id="15365-142">Anger replikeringsprovidern.</span><span class="sxs-lookup"><span data-stu-id="15365-142">Specifies the replication provider.</span></span>
<span data-ttu-id="15365-143">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="15365-143">Valid values are:</span></span>

- <span data-ttu-id="15365-144">HyperVReplica2012R2</span><span class="sxs-lookup"><span data-stu-id="15365-144">HyperVReplica2012R2</span></span>
- <span data-ttu-id="15365-145">HyperVReplica2012</span><span class="sxs-lookup"><span data-stu-id="15365-145">HyperVReplica2012</span></span>
- <span data-ttu-id="15365-146">HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="15365-146">HyperVReplicaAzure</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15365-147">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="15365-147">-ReplicationStartTime</span></span>
<span data-ttu-id="15365-148">Anger start tiden för replikering.</span><span class="sxs-lookup"><span data-stu-id="15365-148">Specifies the replication start time.</span></span>
<span data-ttu-id="15365-149">Det får inte vara senare än 24 timmar från början av jobbet.</span><span class="sxs-lookup"><span data-stu-id="15365-149">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15365-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15365-150">-DefaultProfile</span></span>
<span data-ttu-id="15365-151">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="15365-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15365-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15365-152">CommonParameters</span></span>
<span data-ttu-id="15365-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15365-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15365-154">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15365-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15365-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="15365-155">INPUTS</span></span>

## <span data-ttu-id="15365-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="15365-156">OUTPUTS</span></span>

## <span data-ttu-id="15365-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="15365-157">NOTES</span></span>

## <span data-ttu-id="15365-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="15365-158">RELATED LINKS</span></span>

[<span data-ttu-id="15365-159">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="15365-159">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="15365-160">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="15365-160">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
