---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 59a5cbde2bde2c2cbe5834f73199c7b86791d247
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755654"
---
# <span data-ttu-id="12fe6-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="12fe6-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="12fe6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12fe6-102">SYNOPSIS</span></span>
<span data-ttu-id="12fe6-103">Skapar ett abonnemang för ASR-återställning.</span><span class="sxs-lookup"><span data-stu-id="12fe6-103">Creates an ASR recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12fe6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12fe6-104">SYNTAX</span></span>

### <span data-ttu-id="12fe6-105">EnterpriseToEnterprise (standard)</span><span class="sxs-lookup"><span data-stu-id="12fe6-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric>
 -RecoveryFabric <ASRFabric> -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12fe6-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="12fe6-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12fe6-107">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="12fe6-107">ByRPFile</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12fe6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12fe6-108">DESCRIPTION</span></span>
<span data-ttu-id="12fe6-109">Cmdleten **New-AzureRmRecoveryServicesAsrRecoveryPlan** skapar ett Azure Site Recovery-abonnemang i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="12fe6-109">The **New-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="12fe6-110">En återställnings plan samlar virtuella datorer som tillhör en tillämpning i en enhet så att de kan återvinnas tillsammans.</span><span class="sxs-lookup"><span data-stu-id="12fe6-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="12fe6-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12fe6-111">EXAMPLES</span></span>

### <span data-ttu-id="12fe6-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="12fe6-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="12fe6-113">Startar åtgärden Skapa återställnings plan med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="12fe6-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="12fe6-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12fe6-114">PARAMETERS</span></span>

### <span data-ttu-id="12fe6-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="12fe6-115">-Azure</span></span>
<span data-ttu-id="12fe6-116">Byt parameter för att ange att återställnings platsen för återställnings plan är Azure.</span><span class="sxs-lookup"><span data-stu-id="12fe6-116">Switch parameter to specify that the recovery location for recovery plan is Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12fe6-117">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="12fe6-117">-FailoverDeploymentModel</span></span>
<span data-ttu-id="12fe6-118">Anger distributions modellen för redundansväxling (klassisk eller Resource Manager) för de replikerade objekt som kommer att ingå i återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="12fe6-118">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12fe6-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="12fe6-119">-Name</span></span>
<span data-ttu-id="12fe6-120">Namn på återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="12fe6-120">Name of the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12fe6-121">-Path</span><span class="sxs-lookup"><span data-stu-id="12fe6-121">-Path</span></span>
<span data-ttu-id="12fe6-122">Anger sökvägen till den definitions fil för redatafilen för återställnings plan.</span><span class="sxs-lookup"><span data-stu-id="12fe6-122">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="12fe6-123">En definition JSON för återhämtnings plan kan användas för att skapa återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="12fe6-123">A recovery plan definition json can be used to create the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12fe6-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="12fe6-124">-PrimaryFabric</span></span>
<span data-ttu-id="12fe6-125">Anger ASR-Fabric-objektet för den primära ASR-Fabric för de replikerade objekt som kommer att ingå i återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="12fe6-125">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12fe6-126">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="12fe6-126">-RecoveryFabric</span></span>
<span data-ttu-id="12fe6-127">Anger ASR-Fabric-objektet för återställning av ASR-Fabric för replikerade objekt som kommer att ingå i denna återställnings plan.</span><span class="sxs-lookup"><span data-stu-id="12fe6-127">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12fe6-128">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="12fe6-128">-ReplicationProtectedItem</span></span>
<span data-ttu-id="12fe6-129">Listan över replikerade objekt som ska läggas till i den första gruppen i återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="12fe6-129">The list of replication protected items to add to the first group of the recovery plan.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12fe6-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="12fe6-130">-Confirm</span></span>
<span data-ttu-id="12fe6-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="12fe6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12fe6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12fe6-132">-WhatIf</span></span>
<span data-ttu-id="12fe6-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="12fe6-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12fe6-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="12fe6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12fe6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12fe6-135">CommonParameters</span></span>
<span data-ttu-id="12fe6-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12fe6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12fe6-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12fe6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12fe6-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12fe6-138">INPUTS</span></span>

### <span data-ttu-id="12fe6-139">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="12fe6-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="12fe6-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12fe6-140">OUTPUTS</span></span>

### <span data-ttu-id="12fe6-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="12fe6-141">System.Object</span></span>

## <span data-ttu-id="12fe6-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12fe6-142">NOTES</span></span>

## <span data-ttu-id="12fe6-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12fe6-143">RELATED LINKS</span></span>

[<span data-ttu-id="12fe6-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="12fe6-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="12fe6-145">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="12fe6-145">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="12fe6-146">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="12fe6-146">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


