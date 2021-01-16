---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 9992c4232bd93e9653f0723911f539b1204ce538
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393315"
---
# <span data-ttu-id="b6b95-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b6b95-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="b6b95-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6b95-102">SYNOPSIS</span></span>
<span data-ttu-id="b6b95-103">Skapar ett abonnemang för ASR-återställning.</span><span class="sxs-lookup"><span data-stu-id="b6b95-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="b6b95-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6b95-104">SYNTAX</span></span>

### <span data-ttu-id="b6b95-105">EnterpriseToEnterprise (standard)</span><span class="sxs-lookup"><span data-stu-id="b6b95-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6b95-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="b6b95-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6b95-107">AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="b6b95-107">AzureZoneToZone</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -PrimaryZone <String>
 -RecoveryZone <String> [-AzureZoneToZone] -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6b95-108">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="b6b95-108">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6b95-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6b95-109">DESCRIPTION</span></span>
<span data-ttu-id="b6b95-110">Cmdleten **New-AzRecoveryServicesAsrRecoveryPlan** skapar en Azure Site Recovery, återställnings plan i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="b6b95-110">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="b6b95-111">En återställnings plan samlar virtuella datorer som tillhör en tillämpning i en enhet så att de kan återvinnas tillsammans.</span><span class="sxs-lookup"><span data-stu-id="b6b95-111">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="b6b95-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6b95-112">EXAMPLES</span></span>

### <span data-ttu-id="b6b95-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b6b95-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="b6b95-114">Startar åtgärden Skapa återställnings plan med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="b6b95-114">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="b6b95-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b6b95-115">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -PrimaryZone $pZone-RecoveryZone $rZone -ReplicationProtectedItem $RPI
```

<span data-ttu-id="b6b95-116">Startar åtgärden för att skapa återställnings plan för Azure Zone till replikerade objekt och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="b6b95-116">Starts the recovery plan creation operation for Azure zone to zone replicated items and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b6b95-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6b95-117">PARAMETERS</span></span>

### <span data-ttu-id="b6b95-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="b6b95-118">-Azure</span></span>
<span data-ttu-id="b6b95-119">Switch parameter anger scenariot för återställning av en Azure-till-Azure-krasch, återställnings plan.</span><span class="sxs-lookup"><span data-stu-id="b6b95-119">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

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

### <span data-ttu-id="b6b95-120">-AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="b6b95-120">-AzureZoneToZone</span></span>
<span data-ttu-id="b6b95-121">Switch parameter anger att det replikerade objektet ska skapas i scenariot för Azure Zone till Zone.</span><span class="sxs-lookup"><span data-stu-id="b6b95-121">Switch parameter specifies creating the replicated item in azure zone to zone scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6b95-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6b95-122">-DefaultProfile</span></span>
<span data-ttu-id="b6b95-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b95-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b6b95-124">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="b6b95-124">-FailoverDeploymentModel</span></span>
<span data-ttu-id="b6b95-125">Anger distributions modellen för redundansväxling (klassisk eller Resource Manager) för de replikerade objekt som kommer att ingå i återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="b6b95-125">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="b6b95-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="b6b95-126">-Name</span></span>
<span data-ttu-id="b6b95-127">Namn på återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="b6b95-127">Name of the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6b95-128">-Path</span><span class="sxs-lookup"><span data-stu-id="b6b95-128">-Path</span></span>
<span data-ttu-id="b6b95-129">Anger sökvägen till den definitions fil för redatafilen för återställnings plan.</span><span class="sxs-lookup"><span data-stu-id="b6b95-129">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="b6b95-130">En definition JSON för återhämtnings plan kan användas för att skapa återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="b6b95-130">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="b6b95-131">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="b6b95-131">-PrimaryFabric</span></span>
<span data-ttu-id="b6b95-132">Anger ASR-Fabric-objektet för den primära ASR-Fabric för de replikerade objekt som kommer att ingå i återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="b6b95-132">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6b95-133">-PrimaryZone</span><span class="sxs-lookup"><span data-stu-id="b6b95-133">-PrimaryZone</span></span>
<span data-ttu-id="b6b95-134">Anger den primära Availabilty Zone för de replikerade objekt som kommer att ingå i denna återställnings plan.</span><span class="sxs-lookup"><span data-stu-id="b6b95-134">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6b95-135">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="b6b95-135">-RecoveryFabric</span></span>
<span data-ttu-id="b6b95-136">Anger ASR-Fabric-objektet för återställning av ASR-Fabric för replikerade objekt som kommer att ingå i denna återställnings plan.</span><span class="sxs-lookup"><span data-stu-id="b6b95-136">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="b6b95-137">-RecoveryZone</span><span class="sxs-lookup"><span data-stu-id="b6b95-137">-RecoveryZone</span></span>
<span data-ttu-id="b6b95-138">Anger den primära Availabilty Zone för de replikerade objekt som kommer att ingå i denna återställnings plan.</span><span class="sxs-lookup"><span data-stu-id="b6b95-138">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6b95-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b6b95-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="b6b95-140">Listan över replikerade objekt som ska läggas till i den första gruppen i återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="b6b95-140">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6b95-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b6b95-141">-Confirm</span></span>
<span data-ttu-id="b6b95-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b6b95-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6b95-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6b95-143">-WhatIf</span></span>
<span data-ttu-id="b6b95-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b6b95-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6b95-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b6b95-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6b95-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6b95-146">CommonParameters</span></span>
<span data-ttu-id="b6b95-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6b95-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6b95-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6b95-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6b95-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6b95-149">INPUTS</span></span>

### <span data-ttu-id="b6b95-150">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="b6b95-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="b6b95-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6b95-151">OUTPUTS</span></span>

### <span data-ttu-id="b6b95-152">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b6b95-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b6b95-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6b95-153">NOTES</span></span>

## <span data-ttu-id="b6b95-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6b95-154">RELATED LINKS</span></span>

[<span data-ttu-id="b6b95-155">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b6b95-155">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="b6b95-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b6b95-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="b6b95-157">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b6b95-157">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


