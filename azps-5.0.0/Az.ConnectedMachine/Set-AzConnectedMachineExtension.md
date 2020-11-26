---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/set-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
ms.openlocfilehash: b136f5194bdc7e0f4b4dfc969564d7ef8476d9bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271962"
---
# <span data-ttu-id="8b6a8-101">Set-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="8b6a8-101">Set-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="8b6a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8b6a8-102">SYNOPSIS</span></span>
<span data-ttu-id="8b6a8-103">Åtgärden för att skapa eller uppdatera tillägget.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="8b6a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8b6a8-104">SYNTAX</span></span>

### <span data-ttu-id="8b6a8-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="8b6a8-105">UpdateExpanded (Default)</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8b6a8-106">Uppdatera</span><span class="sxs-lookup"><span data-stu-id="8b6a8-106">Update</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8b6a8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8b6a8-107">DESCRIPTION</span></span>
<span data-ttu-id="8b6a8-108">Åtgärden för att skapa eller uppdatera tillägget.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-108">The operation to create or update the extension.</span></span>

## <span data-ttu-id="8b6a8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8b6a8-109">EXAMPLES</span></span>

### <span data-ttu-id="8b6a8-110">Exempel 1: Ange ett tillägg på en dator</span><span class="sxs-lookup"><span data-stu-id="8b6a8-110">Example 1: Set an extension on a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="8b6a8-111">Anger ett tillägg på en dator.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-111">Sets an extension on a machine.</span></span>

### <span data-ttu-id="8b6a8-112">Exempel 2: Ange ett tillägg med parametrar för tillägg som anges via pipeline</span><span class="sxs-lookup"><span data-stu-id="8b6a8-112">Example 2: Set an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="8b6a8-113">Detta anger ett tillägg med de tilläggs parametrar som tillhandahålls av objektet som skickas via pipeline.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-113">This sets an extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="8b6a8-114">Det är bra om du vill ta fram parametrarna på en dator och använda den på en annan dator.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-114">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

## <span data-ttu-id="8b6a8-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8b6a8-115">PARAMETERS</span></span>

### <span data-ttu-id="8b6a8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b6a8-116">-AsJob</span></span>
<span data-ttu-id="8b6a8-117">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="8b6a8-117">Run the command as a job</span></span>

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

### <span data-ttu-id="8b6a8-118">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="8b6a8-118">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="8b6a8-119">Anger om tillägget ska använda en nyare del version om en sådan finns tillgänglig vid distribution.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-119">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="8b6a8-120">När tillägget har distribuerats uppgraderas inte del versioner såvida inte den här egenskapen är angiven till true.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-120">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6a8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b6a8-121">-DefaultProfile</span></span>
<span data-ttu-id="8b6a8-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b6a8-123">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="8b6a8-123">-ExtensionParameter</span></span>
<span data-ttu-id="8b6a8-124">Beskriver ett dator tillägg.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-124">Describes a Machine Extension.</span></span>
<span data-ttu-id="8b6a8-125">För att konstruera kan du läsa avsnittet anteckningar för EXTENSIONPARAMETER-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-125">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b6a8-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="8b6a8-126">-ExtensionType</span></span>
<span data-ttu-id="8b6a8-127">Anger typen av förlängning; ett exempel är "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="8b6a8-127">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6a8-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="8b6a8-128">-ForceRerun</span></span>
<span data-ttu-id="8b6a8-129">Så här tvingas förlängnings hanteraren att uppdateras även om tilläggs konfigurationen inte har ändrats.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-129">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6a8-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="8b6a8-130">-Location</span></span>
<span data-ttu-id="8b6a8-131">Den Geo-plats där resursen bor</span><span class="sxs-lookup"><span data-stu-id="8b6a8-131">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6a8-132">-MachineName</span><span class="sxs-lookup"><span data-stu-id="8b6a8-132">-MachineName</span></span>
<span data-ttu-id="8b6a8-133">Namnet på den dator där fil namns tillägget ska skapas eller uppdateras.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-133">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="8b6a8-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="8b6a8-134">-Name</span></span>
<span data-ttu-id="8b6a8-135">Namnet på dator tillägget.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-135">The name of the machine extension.</span></span>

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

### <span data-ttu-id="8b6a8-136">-Nowait</span><span class="sxs-lookup"><span data-stu-id="8b6a8-136">-NoWait</span></span>
<span data-ttu-id="8b6a8-137">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="8b6a8-137">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8b6a8-138">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="8b6a8-138">-ProtectedSetting</span></span>
<span data-ttu-id="8b6a8-139">Tillägget kan innehålla antingen protectedSettings eller protectedSettingsFromKeyVault eller inga skyddade inställningar alls.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-139">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesProtectedSettings
Parameter Sets: UpdateExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6a8-140">-Publisher</span><span class="sxs-lookup"><span data-stu-id="8b6a8-140">-Publisher</span></span>
<span data-ttu-id="8b6a8-141">Namnet på tilläggs hanterarens utgivare.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-141">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6a8-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b6a8-142">-ResourceGroupName</span></span>
<span data-ttu-id="8b6a8-143">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="8b6a8-144">-Ställ in</span><span class="sxs-lookup"><span data-stu-id="8b6a8-144">-Setting</span></span>
<span data-ttu-id="8b6a8-145">JSON-formaterade offentliga inställningar för tillägget.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-145">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesSettings
Parameter Sets: UpdateExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6a8-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8b6a8-146">-SubscriptionId</span></span>
<span data-ttu-id="8b6a8-147">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-147">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8b6a8-148">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-148">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8b6a8-149">-Tagg</span><span class="sxs-lookup"><span data-stu-id="8b6a8-149">-Tag</span></span>
<span data-ttu-id="8b6a8-150">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-150">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6a8-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="8b6a8-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="8b6a8-152">Anger versionen för skript hanteraren.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-152">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6a8-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8b6a8-153">-Confirm</span></span>
<span data-ttu-id="8b6a8-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b6a8-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b6a8-155">-WhatIf</span></span>
<span data-ttu-id="8b6a8-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b6a8-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b6a8-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b6a8-158">CommonParameters</span></span>
<span data-ttu-id="8b6a8-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b6a8-160">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b6a8-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b6a8-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8b6a8-161">INPUTS</span></span>

### <span data-ttu-id="8b6a8-162">Microsoft. Azure. PowerShell. cmdletar. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="8b6a8-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="8b6a8-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8b6a8-163">OUTPUTS</span></span>

### <span data-ttu-id="8b6a8-164">Microsoft. Azure. PowerShell. cmdletar. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="8b6a8-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="8b6a8-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8b6a8-165">NOTES</span></span>

<span data-ttu-id="8b6a8-166">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8b6a8-166">ALIASES</span></span>

<span data-ttu-id="8b6a8-167">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="8b6a8-167">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8b6a8-168">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-168">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8b6a8-169">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-169">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8b6a8-170">EXTENSIONPARAMETER <IMachineExtension> : beskriver ett dator tillägg.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-170">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="8b6a8-171">`Location <String>`: Den Geo-plats där resursen bor</span><span class="sxs-lookup"><span data-stu-id="8b6a8-171">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="8b6a8-172">`[Tag <ITrackedResourceTags>]`: Resursfiler.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-172">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="8b6a8-173">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-173">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="8b6a8-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Anger om tillägget ska använda en nyare del version om en sådan finns tillgänglig vid distributions tillfället.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="8b6a8-175">När tillägget har distribuerats uppgraderas inte del versioner såvida inte den här egenskapen är angiven till true.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-175">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="8b6a8-176">`[ForceUpdateTag <String>]`: Hur tilläggs hanteraren ska tvingas uppdatera även om tilläggs konfigurationen inte har ändrats.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-176">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="8b6a8-177">`[MachineExtensionType <String>]`: Anger typen av tillägget. ett exempel är "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="8b6a8-177">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="8b6a8-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: Tillägget kan innehålla antingen protectedSettings eller protectedSettingsFromKeyVault eller inga skyddade inställningar alls.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="8b6a8-179">`[Publisher <String>]`: Namnet på tilläggs hanterarens utgivare.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-179">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="8b6a8-180">`[Setting <IMachineExtensionPropertiesSettings>]`: JSON-formaterade offentliga inställningar för tillägget.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="8b6a8-181">`[TypeHandlerVersion <String>]`: Anger versionen för skript hanteraren.</span><span class="sxs-lookup"><span data-stu-id="8b6a8-181">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

## <span data-ttu-id="8b6a8-182">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8b6a8-182">RELATED LINKS</span></span>
