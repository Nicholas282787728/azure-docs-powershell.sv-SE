---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 851f9d52b3247fed0755b4567e3c463b1202c34b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092414"
---
# <span data-ttu-id="45200-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="45200-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="45200-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45200-102">SYNOPSIS</span></span>
<span data-ttu-id="45200-103">Skapar ett abonnemang för ASR-återställning.</span><span class="sxs-lookup"><span data-stu-id="45200-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="45200-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45200-104">SYNTAX</span></span>

### <span data-ttu-id="45200-105">EnterpriseToEnterprise (standard)</span><span class="sxs-lookup"><span data-stu-id="45200-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45200-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="45200-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45200-107">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="45200-107">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45200-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45200-108">DESCRIPTION</span></span>
<span data-ttu-id="45200-109">Cmdleten **New-AzRecoveryServicesAsrRecoveryPlan** skapar en Azure Site Recovery, återställnings plan i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="45200-109">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="45200-110">En återställnings plan samlar virtuella datorer som tillhör en tillämpning i en enhet så att de kan återvinnas tillsammans.</span><span class="sxs-lookup"><span data-stu-id="45200-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="45200-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45200-111">EXAMPLES</span></span>

### <span data-ttu-id="45200-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="45200-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="45200-113">Startar åtgärden Skapa återställnings plan med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="45200-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="45200-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45200-114">PARAMETERS</span></span>

### <span data-ttu-id="45200-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="45200-115">-Azure</span></span>
<span data-ttu-id="45200-116">Switch parameter anger scenariot för återställning av en Azure-till-Azure-krasch, återställnings plan.</span><span class="sxs-lookup"><span data-stu-id="45200-116">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

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

### <span data-ttu-id="45200-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45200-117">-DefaultProfile</span></span>
<span data-ttu-id="45200-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="45200-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="45200-119">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="45200-119">-FailoverDeploymentModel</span></span>
<span data-ttu-id="45200-120">Anger distributions modellen för redundansväxling (klassisk eller Resource Manager) för de replikerade objekt som kommer att ingå i återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="45200-120">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="45200-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="45200-121">-Name</span></span>
<span data-ttu-id="45200-122">Namn på återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="45200-122">Name of the recovery plan.</span></span>

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

### <span data-ttu-id="45200-123">-Path</span><span class="sxs-lookup"><span data-stu-id="45200-123">-Path</span></span>
<span data-ttu-id="45200-124">Anger sökvägen till den definitions fil för redatafilen för återställnings plan.</span><span class="sxs-lookup"><span data-stu-id="45200-124">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="45200-125">En definition JSON för återhämtnings plan kan användas för att skapa återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="45200-125">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="45200-126">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="45200-126">-PrimaryFabric</span></span>
<span data-ttu-id="45200-127">Anger ASR-Fabric-objektet för den primära ASR-Fabric för de replikerade objekt som kommer att ingå i återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="45200-127">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="45200-128">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="45200-128">-RecoveryFabric</span></span>
<span data-ttu-id="45200-129">Anger ASR-Fabric-objektet för återställning av ASR-Fabric för replikerade objekt som kommer att ingå i denna återställnings plan.</span><span class="sxs-lookup"><span data-stu-id="45200-129">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="45200-130">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="45200-130">-ReplicationProtectedItem</span></span>
<span data-ttu-id="45200-131">Listan över replikerade objekt som ska läggas till i den första gruppen i återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="45200-131">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

### <span data-ttu-id="45200-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="45200-132">-Confirm</span></span>
<span data-ttu-id="45200-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="45200-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45200-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45200-134">-WhatIf</span></span>
<span data-ttu-id="45200-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="45200-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45200-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="45200-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45200-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45200-137">CommonParameters</span></span>
<span data-ttu-id="45200-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45200-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45200-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45200-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45200-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45200-140">INPUTS</span></span>

### <span data-ttu-id="45200-141">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="45200-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="45200-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45200-142">OUTPUTS</span></span>

### <span data-ttu-id="45200-143">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="45200-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="45200-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45200-144">NOTES</span></span>

## <span data-ttu-id="45200-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45200-145">RELATED LINKS</span></span>

[<span data-ttu-id="45200-146">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="45200-146">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="45200-147">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="45200-147">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="45200-148">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="45200-148">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


