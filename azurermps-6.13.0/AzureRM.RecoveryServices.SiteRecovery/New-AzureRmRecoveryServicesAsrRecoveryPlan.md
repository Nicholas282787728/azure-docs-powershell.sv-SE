---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: ceedd758a660828ed3ee93390384c1e212c55097
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572656"
---
# <span data-ttu-id="28de5-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="28de5-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="28de5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="28de5-102">SYNOPSIS</span></span>
<span data-ttu-id="28de5-103">Skapar ett abonnemang för ASR-återställning.</span><span class="sxs-lookup"><span data-stu-id="28de5-103">Creates an ASR recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28de5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="28de5-104">SYNTAX</span></span>

### <span data-ttu-id="28de5-105">EnterpriseToEnterprise (standard)</span><span class="sxs-lookup"><span data-stu-id="28de5-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric>
 -RecoveryFabric <ASRFabric> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28de5-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="28de5-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28de5-107">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="28de5-107">ByRPFile</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28de5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="28de5-108">DESCRIPTION</span></span>
<span data-ttu-id="28de5-109">Cmdleten **New-AzureRmRecoveryServicesAsrRecoveryPlan** skapar ett Azure Site Recovery-abonnemang i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="28de5-109">The **New-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="28de5-110">En återställnings plan samlar virtuella datorer som tillhör en tillämpning i en enhet så att de kan återvinnas tillsammans.</span><span class="sxs-lookup"><span data-stu-id="28de5-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="28de5-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="28de5-111">EXAMPLES</span></span>

### <span data-ttu-id="28de5-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="28de5-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="28de5-113">Startar åtgärden Skapa återställnings plan med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="28de5-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="28de5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="28de5-114">PARAMETERS</span></span>

### <span data-ttu-id="28de5-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="28de5-115">-Azure</span></span>
<span data-ttu-id="28de5-116">Byt parameter för att ange att återställnings platsen för återställnings plan är Azure.</span><span class="sxs-lookup"><span data-stu-id="28de5-116">Switch parameter to specify that the recovery location for recovery plan is Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28de5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28de5-117">-DefaultProfile</span></span>
<span data-ttu-id="28de5-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="28de5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="28de5-119">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="28de5-119">-FailoverDeploymentModel</span></span>
<span data-ttu-id="28de5-120">Anger distributions modellen för redundansväxling (klassisk eller Resource Manager) för de replikerade objekt som kommer att ingå i återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="28de5-120">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases:
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28de5-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="28de5-121">-Name</span></span>
<span data-ttu-id="28de5-122">Namn på återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="28de5-122">Name of the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28de5-123">-Path</span><span class="sxs-lookup"><span data-stu-id="28de5-123">-Path</span></span>
<span data-ttu-id="28de5-124">Anger sökvägen till den definitions fil för redatafilen för återställnings plan.</span><span class="sxs-lookup"><span data-stu-id="28de5-124">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="28de5-125">En definition JSON för återhämtnings plan kan användas för att skapa återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="28de5-125">A recovery plan definition json can be used to create the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28de5-126">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="28de5-126">-PrimaryFabric</span></span>
<span data-ttu-id="28de5-127">Anger ASR-Fabric-objektet för den primära ASR-Fabric för de replikerade objekt som kommer att ingå i återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="28de5-127">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28de5-128">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="28de5-128">-RecoveryFabric</span></span>
<span data-ttu-id="28de5-129">Anger ASR-Fabric-objektet för återställning av ASR-Fabric för replikerade objekt som kommer att ingå i denna återställnings plan.</span><span class="sxs-lookup"><span data-stu-id="28de5-129">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28de5-130">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="28de5-130">-ReplicationProtectedItem</span></span>
<span data-ttu-id="28de5-131">Listan över replikerade objekt som ska läggas till i den första gruppen i återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="28de5-131">The list of replication protected items to add to the first group of the recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28de5-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="28de5-132">-Confirm</span></span>
<span data-ttu-id="28de5-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="28de5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28de5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28de5-134">-WhatIf</span></span>
<span data-ttu-id="28de5-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="28de5-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28de5-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="28de5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28de5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28de5-137">CommonParameters</span></span>
<span data-ttu-id="28de5-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28de5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28de5-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28de5-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28de5-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="28de5-140">INPUTS</span></span>

### <span data-ttu-id="28de5-141">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="28de5-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="28de5-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="28de5-142">OUTPUTS</span></span>

### <span data-ttu-id="28de5-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="28de5-143">System.Object</span></span>

## <span data-ttu-id="28de5-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="28de5-144">NOTES</span></span>

## <span data-ttu-id="28de5-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="28de5-145">RELATED LINKS</span></span>

[<span data-ttu-id="28de5-146">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="28de5-146">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="28de5-147">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="28de5-147">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="28de5-148">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="28de5-148">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


