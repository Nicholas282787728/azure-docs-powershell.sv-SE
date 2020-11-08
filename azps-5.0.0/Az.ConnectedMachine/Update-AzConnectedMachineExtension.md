---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/update-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
ms.openlocfilehash: 95334b4f67685183e499518b068f1003f5bb6547
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271958"
---
# <span data-ttu-id="c6273-101">Update-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="c6273-101">Update-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="c6273-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c6273-102">SYNOPSIS</span></span>
<span data-ttu-id="c6273-103">Åtgärden för att skapa eller uppdatera tillägget.</span><span class="sxs-lookup"><span data-stu-id="c6273-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="c6273-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c6273-104">SYNTAX</span></span>

### <span data-ttu-id="c6273-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="c6273-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>] [-Type <String>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c6273-106">Uppdatera</span><span class="sxs-lookup"><span data-stu-id="c6273-106">Update</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtensionUpdate> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c6273-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c6273-107">UpdateViaIdentity</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtensionUpdate> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c6273-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c6273-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-AutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>]
 [-Type <String>] [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c6273-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c6273-109">DESCRIPTION</span></span>
<span data-ttu-id="c6273-110">Åtgärden för att skapa eller uppdatera tillägget.</span><span class="sxs-lookup"><span data-stu-id="c6273-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="c6273-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c6273-111">EXAMPLES</span></span>

### <span data-ttu-id="c6273-112">Exempel 1: uppdatera ett tillägg</span><span class="sxs-lookup"><span data-stu-id="c6273-112">Example 1: Update an extension</span></span>
```powershell
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
            Settings = @{
                commandToExecute = "ls -l"
            }
        }
PS C:\> Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="c6273-113">Uppdaterar en anknytning på en specifik dator.</span><span class="sxs-lookup"><span data-stu-id="c6273-113">Updates an extension on a specific machine.</span></span>

### <span data-ttu-id="c6273-114">Exempel 2: uppdatera en anknytning med platsen som anges via pipeline</span><span class="sxs-lookup"><span data-stu-id="c6273-114">Example 2: Update an extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -Settings @{
                commandToExecute = "ls -l"
            }

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="c6273-115">Uppdaterar ett specifikt tillägg som skickas in via pipeline.</span><span class="sxs-lookup"><span data-stu-id="c6273-115">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="c6273-116">Här ska vi använda tillägget som skickas via pipeline för att hjälpa oss att identifiera vilket tillägg vi vill använda och vilka som vi vill ändra via normala parametrar (som `-Settings` )</span><span class="sxs-lookup"><span data-stu-id="c6273-116">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on and are specifying what we want to change via the normal parameters (like `-Settings`)</span></span>

### <span data-ttu-id="c6273-117">Exempel 3: uppdatera ett tillägg med tilläggs parametrar som anges via pipeline</span><span class="sxs-lookup"><span data-stu-id="c6273-117">Example 3: Update an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
        }
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="c6273-118">Uppdaterar ett specifikt tillägg som skickas in via pipeline.</span><span class="sxs-lookup"><span data-stu-id="c6273-118">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="c6273-119">Här ska vi använda tillägget som skickas via pipeline för att tillhandahålla de ändringar vi vill göra i tillägget.</span><span class="sxs-lookup"><span data-stu-id="c6273-119">Here we are using the extension passed in via the pipeline to provide the changes we want to make on the extension.</span></span>
<span data-ttu-id="c6273-120">Placeringen av tillägget hämtas inte via pipeline, utan i stället via parametrarna som anges normalt (med parametern splat).</span><span class="sxs-lookup"><span data-stu-id="c6273-120">The location of the extension is not retrieved via the pipeline but rather via the parameters specified normally (by the splat parameter).</span></span>

### <span data-ttu-id="c6273-121">Exempel 4: använda ett objekt som både plats och parametrar för uppdatering</span><span class="sxs-lookup"><span data-stu-id="c6273-121">Example 4: Using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -ExtensionParameter $extToUpdate

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="c6273-122">Uppdaterar ett specifikt tillägg som skickas in via pipeline.</span><span class="sxs-lookup"><span data-stu-id="c6273-122">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="c6273-123">Här ska vi använda tillägget som skickades via pipeline för att hjälpa oss att identifiera vilket tillägg vi vill använda.</span><span class="sxs-lookup"><span data-stu-id="c6273-123">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on.</span></span>
<span data-ttu-id="c6273-124">Dessutom används parametrarna för tillägget för att ange vad som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="c6273-124">In addition to that, we are using the parameters of the extension object to specify what to update.</span></span>

## <span data-ttu-id="c6273-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c6273-125">PARAMETERS</span></span>

### <span data-ttu-id="c6273-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6273-126">-AsJob</span></span>
<span data-ttu-id="c6273-127">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="c6273-127">Run the command as a job</span></span>

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

### <span data-ttu-id="c6273-128">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="c6273-128">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="c6273-129">Anger om tillägget ska använda en nyare del version om en sådan finns tillgänglig vid distribution.</span><span class="sxs-lookup"><span data-stu-id="c6273-129">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="c6273-130">När tillägget har distribuerats uppgraderas inte del versioner såvida inte den här egenskapen är angiven till true.</span><span class="sxs-lookup"><span data-stu-id="c6273-130">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6273-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6273-131">-DefaultProfile</span></span>
<span data-ttu-id="c6273-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c6273-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6273-133">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="c6273-133">-ExtensionParameter</span></span>
<span data-ttu-id="c6273-134">Beskriver en dator tilläggs uppdatering.</span><span class="sxs-lookup"><span data-stu-id="c6273-134">Describes a Machine Extension Update.</span></span>
<span data-ttu-id="c6273-135">För att konstruera kan du läsa avsnittet anteckningar för EXTENSIONPARAMETER-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="c6273-135">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate
Parameter Sets: Update, UpdateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6273-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="c6273-136">-ForceRerun</span></span>
<span data-ttu-id="c6273-137">Så här tvingas förlängnings hanteraren att uppdateras även om tilläggs konfigurationen inte har ändrats.</span><span class="sxs-lookup"><span data-stu-id="c6273-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6273-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6273-138">-InputObject</span></span>
<span data-ttu-id="c6273-139">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="c6273-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: UpdateViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6273-140">-MachineName</span><span class="sxs-lookup"><span data-stu-id="c6273-140">-MachineName</span></span>
<span data-ttu-id="c6273-141">Namnet på den dator där fil namns tillägget ska skapas eller uppdateras.</span><span class="sxs-lookup"><span data-stu-id="c6273-141">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6273-142">-Namn</span><span class="sxs-lookup"><span data-stu-id="c6273-142">-Name</span></span>
<span data-ttu-id="c6273-143">Namnet på dator tillägget.</span><span class="sxs-lookup"><span data-stu-id="c6273-143">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6273-144">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c6273-144">-NoWait</span></span>
<span data-ttu-id="c6273-145">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="c6273-145">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c6273-146">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="c6273-146">-ProtectedSetting</span></span>
<span data-ttu-id="c6273-147">Tillägget kan innehålla antingen protectedSettings eller protectedSettingsFromKeyVault eller inga skyddade inställningar alls.</span><span class="sxs-lookup"><span data-stu-id="c6273-147">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesProtectedSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6273-148">-Publisher</span><span class="sxs-lookup"><span data-stu-id="c6273-148">-Publisher</span></span>
<span data-ttu-id="c6273-149">Namnet på tilläggs hanterarens utgivare.</span><span class="sxs-lookup"><span data-stu-id="c6273-149">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6273-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6273-150">-ResourceGroupName</span></span>
<span data-ttu-id="c6273-151">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c6273-151">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6273-152">-Ställ in</span><span class="sxs-lookup"><span data-stu-id="c6273-152">-Setting</span></span>
<span data-ttu-id="c6273-153">JSON-formaterade offentliga inställningar för tillägget.</span><span class="sxs-lookup"><span data-stu-id="c6273-153">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6273-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c6273-154">-SubscriptionId</span></span>
<span data-ttu-id="c6273-155">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c6273-155">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c6273-156">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="c6273-156">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6273-157">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c6273-157">-Tag</span></span>
<span data-ttu-id="c6273-158">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="c6273-158">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6273-159">– Skriv</span><span class="sxs-lookup"><span data-stu-id="c6273-159">-Type</span></span>
<span data-ttu-id="c6273-160">Anger typen av förlängning; ett exempel är "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="c6273-160">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6273-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="c6273-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="c6273-162">Anger versionen för skript hanteraren.</span><span class="sxs-lookup"><span data-stu-id="c6273-162">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6273-163">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c6273-163">-Confirm</span></span>
<span data-ttu-id="c6273-164">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c6273-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6273-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6273-165">-WhatIf</span></span>
<span data-ttu-id="c6273-166">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c6273-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6273-167">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c6273-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6273-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6273-168">CommonParameters</span></span>
<span data-ttu-id="c6273-169">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6273-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6273-170">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6273-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6273-171">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c6273-171">INPUTS</span></span>

### <span data-ttu-id="c6273-172">Microsoft. Azure. PowerShell. cmdletar. ConnectedMachine. Models. Api20200802. IMachineExtensionUpdate</span><span class="sxs-lookup"><span data-stu-id="c6273-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span></span>

### <span data-ttu-id="c6273-173">Microsoft. Azure. PowerShell. cmdletar. ConnectedMachine. Models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="c6273-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="c6273-174">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c6273-174">OUTPUTS</span></span>

### <span data-ttu-id="c6273-175">Microsoft. Azure. PowerShell. cmdletar. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="c6273-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="c6273-176">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c6273-176">NOTES</span></span>

<span data-ttu-id="c6273-177">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c6273-177">ALIASES</span></span>

<span data-ttu-id="c6273-178">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="c6273-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c6273-179">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="c6273-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c6273-180">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c6273-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c6273-181">EXTENSIONPARAMETER <IMachineExtensionUpdate> : beskriver en dator tilläggs uppdatering.</span><span class="sxs-lookup"><span data-stu-id="c6273-181">EXTENSIONPARAMETER <IMachineExtensionUpdate>: Describes a Machine Extension Update.</span></span>
  - <span data-ttu-id="c6273-182">`[Tag <IUpdateResourceTags>]`: Resursfiler</span><span class="sxs-lookup"><span data-stu-id="c6273-182">`[Tag <IUpdateResourceTags>]`: Resource tags</span></span>
    - <span data-ttu-id="c6273-183">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="c6273-183">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="c6273-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Anger om tillägget ska använda en nyare del version om en sådan finns tillgänglig vid distributions tillfället.</span><span class="sxs-lookup"><span data-stu-id="c6273-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="c6273-185">När tillägget har distribuerats uppgraderas inte del versioner såvida inte den här egenskapen är angiven till true.</span><span class="sxs-lookup"><span data-stu-id="c6273-185">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="c6273-186">`[ForceUpdateTag <String>]`: Hur tilläggs hanteraren ska tvingas uppdatera även om tilläggs konfigurationen inte har ändrats.</span><span class="sxs-lookup"><span data-stu-id="c6273-186">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="c6273-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: Tillägget kan innehålla antingen protectedSettings eller protectedSettingsFromKeyVault eller inga skyddade inställningar alls.</span><span class="sxs-lookup"><span data-stu-id="c6273-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="c6273-188">`[Publisher <String>]`: Namnet på tilläggs hanterarens utgivare.</span><span class="sxs-lookup"><span data-stu-id="c6273-188">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="c6273-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: JSON-formaterade offentliga inställningar för tillägget.</span><span class="sxs-lookup"><span data-stu-id="c6273-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="c6273-190">`[Type <String>]`: Anger typen av tillägget. ett exempel är "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="c6273-190">`[Type <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="c6273-191">`[TypeHandlerVersion <String>]`: Anger versionen för skript hanteraren.</span><span class="sxs-lookup"><span data-stu-id="c6273-191">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="c6273-192">INPUTOBJECT <IConnectedMachineIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="c6273-192">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c6273-193">`[ExtensionName <String>]`: Namnet på dator tillägget.</span><span class="sxs-lookup"><span data-stu-id="c6273-193">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="c6273-194">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="c6273-194">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c6273-195">`[Name <String>]`: Hybrid datorns namn.</span><span class="sxs-lookup"><span data-stu-id="c6273-195">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="c6273-196">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c6273-196">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="c6273-197">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c6273-197">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c6273-198">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="c6273-198">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c6273-199">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c6273-199">RELATED LINKS</span></span>

