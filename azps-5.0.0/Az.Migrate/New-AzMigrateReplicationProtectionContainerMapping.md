---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: b92d483689c94e6dd9f9af69e47f5b17ea1ab795
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271865"
---
# <span data-ttu-id="bb4eb-101">New-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="bb4eb-101">New-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="bb4eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bb4eb-102">SYNOPSIS</span></span>
<span data-ttu-id="bb4eb-103">Åtgärden för att skapa en mappning för skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="bb4eb-103">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="bb4eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bb4eb-104">SYNTAX</span></span>

```
New-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-PolicyId <String>]
 [-ProviderSpecificInput <IReplicationProviderSpecificContainerMappingInput>]
 [-TargetProtectionContainerId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="bb4eb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bb4eb-105">DESCRIPTION</span></span>
<span data-ttu-id="bb4eb-106">Åtgärden för att skapa en mappning för skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="bb4eb-106">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="bb4eb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bb4eb-107">EXAMPLES</span></span>

### <span data-ttu-id="bb4eb-108">Exempel 1: skapa en mappning</span><span class="sxs-lookup"><span data-stu-id="bb4eb-108">Example 1: Create a mapping</span></span>
```powershell
PS C:\> $providerSpecificInput = [Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtContainerMappingInput]::new()
PS C:\> $providerSpecificInput.InstanceType = "VMwareCbt"
PS C:\> $providerSpecificInput.KeyVaultId = "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.KeyVault/vaults/migratekv846827101"
PS C:\> $providerSpecificInput.KeyVaultUri = "https://migratekv846827101.vault.azure.net"
PS C:\> $providerSpecificInput.ServiceBusConnectionStringSecretName = "ServiceBusConnectionString"
PS C:\> $providerSpecificInput.StorageAccountId = "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Storage/storageAccounts/migrategwsa846827101"
PS C:\> $providerSpecificInput.StorageAccountSasSecretName = "migrategwsa846827101-gwySas"
PS C:\> $providerSpecificInput.TargetLocation = "centraluseuap"

PS C:\> New-AzMigrateReplicationProtectionContainerMapping -FabricName "AzMigratePWSHTc8d1replicationfabric" -MappingName "containermapping" -ProtectionContainerName "AzMigratePWSHTc8d1replicationcontainer" -ResourceGroupName "azmigratepwshtestasr13072020" -ResourceName "AzMigrateTestProjectPWSH02aarsvault"  -PolicyId "/subscriptionsxxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy"  -ProviderSpecificInput $providerSpecificInput -TargetProtectionContainerId  "Microsoft Azure"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="bb4eb-109">Skapa en mappning</span><span class="sxs-lookup"><span data-stu-id="bb4eb-109">Create a mapping</span></span>

## <span data-ttu-id="bb4eb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bb4eb-110">PARAMETERS</span></span>

### <span data-ttu-id="bb4eb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb4eb-111">-AsJob</span></span>
<span data-ttu-id="bb4eb-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="bb4eb-112">Run the command as a job</span></span>

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

### <span data-ttu-id="bb4eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb4eb-113">-DefaultProfile</span></span>
<span data-ttu-id="bb4eb-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bb4eb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb4eb-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="bb4eb-115">-FabricName</span></span>
<span data-ttu-id="bb4eb-116">Fabric-namn.</span><span class="sxs-lookup"><span data-stu-id="bb4eb-116">Fabric name.</span></span>

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

### <span data-ttu-id="bb4eb-117">-MappingName</span><span class="sxs-lookup"><span data-stu-id="bb4eb-117">-MappingName</span></span>
<span data-ttu-id="bb4eb-118">Mappnings namn för skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="bb4eb-118">Protection container mapping name.</span></span>

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

### <span data-ttu-id="bb4eb-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="bb4eb-119">-NoWait</span></span>
<span data-ttu-id="bb4eb-120">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="bb4eb-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bb4eb-121">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="bb4eb-121">-PolicyId</span></span>
<span data-ttu-id="bb4eb-122">Tillämplig policy.</span><span class="sxs-lookup"><span data-stu-id="bb4eb-122">Applicable policy.</span></span>

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

### <span data-ttu-id="bb4eb-123">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="bb4eb-123">-ProtectionContainerName</span></span>
<span data-ttu-id="bb4eb-124">Namn på skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="bb4eb-124">Protection container name.</span></span>

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

### <span data-ttu-id="bb4eb-125">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="bb4eb-125">-ProviderSpecificInput</span></span>
<span data-ttu-id="bb4eb-126">Leverantör specifik inmatning för ihopparning.</span><span class="sxs-lookup"><span data-stu-id="bb4eb-126">Provider specific input for pairing.</span></span>
<span data-ttu-id="bb4eb-127">För att konstruera kan du läsa avsnittet anteckningar för PROVIDERSPECIFICINPUT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="bb4eb-127">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IReplicationProviderSpecificContainerMappingInput
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb4eb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb4eb-128">-ResourceGroupName</span></span>
<span data-ttu-id="bb4eb-129">Namnet på resurs gruppen där Recovery Services-valvet finns.</span><span class="sxs-lookup"><span data-stu-id="bb4eb-129">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="bb4eb-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="bb4eb-130">-ResourceName</span></span>
<span data-ttu-id="bb4eb-131">Namnet på Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="bb4eb-131">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="bb4eb-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bb4eb-132">-SubscriptionId</span></span>
<span data-ttu-id="bb4eb-133">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="bb4eb-133">The subscription Id.</span></span>

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

### <span data-ttu-id="bb4eb-134">-TargetProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="bb4eb-134">-TargetProtectionContainerId</span></span>
<span data-ttu-id="bb4eb-135">Namnet på unikt mål för skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="bb4eb-135">The target unique protection container name.</span></span>

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

### <span data-ttu-id="bb4eb-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bb4eb-136">-Confirm</span></span>
<span data-ttu-id="bb4eb-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bb4eb-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb4eb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb4eb-138">-WhatIf</span></span>
<span data-ttu-id="bb4eb-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bb4eb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb4eb-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bb4eb-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb4eb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb4eb-141">CommonParameters</span></span>
<span data-ttu-id="bb4eb-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb4eb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb4eb-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb4eb-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb4eb-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bb4eb-144">INPUTS</span></span>

## <span data-ttu-id="bb4eb-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bb4eb-145">OUTPUTS</span></span>

### <span data-ttu-id="bb4eb-146">Microsoft. Azure. PowerShell. cmdletar. Migrate. Models. Api20180110. IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="bb4eb-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="bb4eb-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bb4eb-147">NOTES</span></span>

<span data-ttu-id="bb4eb-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="bb4eb-148">ALIASES</span></span>

<span data-ttu-id="bb4eb-149">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="bb4eb-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bb4eb-150">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="bb4eb-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bb4eb-151">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bb4eb-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bb4eb-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput> : leverantörsspecifik specifik inmatning för ihopparning.</span><span class="sxs-lookup"><span data-stu-id="bb4eb-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput>: Provider specific input for pairing.</span></span>
  - <span data-ttu-id="bb4eb-153">`[InstanceType <String>]`: Klass typen.</span><span class="sxs-lookup"><span data-stu-id="bb4eb-153">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="bb4eb-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bb4eb-154">RELATED LINKS</span></span>

