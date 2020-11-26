---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
ms.openlocfilehash: 5978c247f14507934662f5a5d1846a02180cd812
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270545"
---
# <span data-ttu-id="10000-101">New-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="10000-101">New-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="10000-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10000-102">SYNOPSIS</span></span>
<span data-ttu-id="10000-103">Åtgärden för att skapa en replikeringsprincip</span><span class="sxs-lookup"><span data-stu-id="10000-103">The operation to create a replication policy</span></span>

## <span data-ttu-id="10000-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10000-104">SYNTAX</span></span>

```
New-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-ProviderSpecificInput <IPolicyProviderSpecificInput>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="10000-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10000-105">DESCRIPTION</span></span>
<span data-ttu-id="10000-106">Åtgärden för att skapa en replikeringsprincip</span><span class="sxs-lookup"><span data-stu-id="10000-106">The operation to create a replication policy</span></span>

## <span data-ttu-id="10000-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10000-107">EXAMPLES</span></span>

### <span data-ttu-id="10000-108">Exempel 1: skapa en replikeringsprincip</span><span class="sxs-lookup"><span data-stu-id="10000-108">Example 1: Create a replication policy</span></span>
```powershell
PS C:\> $providerSpecificPolicy = [Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtPolicyCreationInput]::new()
PS C:\> $providerSpecificPolicy.AppConsistentFrequencyInMinute = 240
PS C:\> $providerSpecificPolicy.InstanceType = "VMwareCbt"
PS C:\> $providerSpecificPolicy.RecoveryPointHistoryInMinute = 4320
PS C:\> $providerSpecificPolicy.CrashConsistentFrequencyInMinute = 60
PS C:\> New-AzMigrateReplicationPolicy -PolicyName TestPolicy -ResourceGroupName ResourceGroup -ResourceName VaultName -SubscriptionId SubscriptionId -ProviderSpecificInput $providerSpecificPolicy

Location Name       Type
-------- ----       ----
         TestPolicy Microsoft.RecoveryServices/vaults/replicationPolicies
         
```

<span data-ttu-id="10000-109">Skapar en princip för VmWare CBT</span><span class="sxs-lookup"><span data-stu-id="10000-109">Creates a policy for VmWare Cbt</span></span>

## <span data-ttu-id="10000-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10000-110">PARAMETERS</span></span>

### <span data-ttu-id="10000-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10000-111">-AsJob</span></span>
<span data-ttu-id="10000-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="10000-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10000-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10000-113">-DefaultProfile</span></span>
<span data-ttu-id="10000-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="10000-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10000-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="10000-115">-NoWait</span></span>
<span data-ttu-id="10000-116">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="10000-116">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10000-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="10000-117">-PolicyName</span></span>
<span data-ttu-id="10000-118">Namn på replikeringsprincip</span><span class="sxs-lookup"><span data-stu-id="10000-118">Replication policy name</span></span>

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

### <span data-ttu-id="10000-119">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="10000-119">-ProviderSpecificInput</span></span>
<span data-ttu-id="10000-120">ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="10000-120">The ReplicationProviderSettings.</span></span>
<span data-ttu-id="10000-121">För att konstruera kan du läsa avsnittet anteckningar för PROVIDERSPECIFICINPUT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="10000-121">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicyProviderSpecificInput
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10000-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10000-122">-ResourceGroupName</span></span>
<span data-ttu-id="10000-123">Namnet på resurs gruppen där Recovery Services-valvet finns.</span><span class="sxs-lookup"><span data-stu-id="10000-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="10000-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="10000-124">-ResourceName</span></span>
<span data-ttu-id="10000-125">Namnet på Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="10000-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="10000-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="10000-126">-SubscriptionId</span></span>
<span data-ttu-id="10000-127">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="10000-127">The subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10000-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="10000-128">-Confirm</span></span>
<span data-ttu-id="10000-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="10000-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10000-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10000-130">-WhatIf</span></span>
<span data-ttu-id="10000-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="10000-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10000-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="10000-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10000-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10000-133">CommonParameters</span></span>
<span data-ttu-id="10000-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10000-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10000-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10000-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10000-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10000-136">INPUTS</span></span>

## <span data-ttu-id="10000-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10000-137">OUTPUTS</span></span>

### <span data-ttu-id="10000-138">Microsoft. Azure. PowerShell. cmdletar. Migrate. Models. Api20180110. IPolicy</span><span class="sxs-lookup"><span data-stu-id="10000-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="10000-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10000-139">NOTES</span></span>

<span data-ttu-id="10000-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="10000-140">ALIASES</span></span>

<span data-ttu-id="10000-141">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="10000-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="10000-142">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="10000-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="10000-143">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="10000-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="10000-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput> : ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="10000-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput>: The ReplicationProviderSettings.</span></span>
  - <span data-ttu-id="10000-145">`[InstanceType <String>]`: Klass typen.</span><span class="sxs-lookup"><span data-stu-id="10000-145">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="10000-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10000-146">RELATED LINKS</span></span>
