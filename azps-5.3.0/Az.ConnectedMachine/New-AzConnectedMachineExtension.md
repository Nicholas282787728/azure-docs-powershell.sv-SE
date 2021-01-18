---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/new-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
ms.openlocfilehash: 13095d24bd095e27bac788d0d578bdcdf3e1a0f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526544"
---
# <span data-ttu-id="f7552-101">New-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="f7552-101">New-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="f7552-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f7552-102">SYNOPSIS</span></span>
<span data-ttu-id="f7552-103">Åtgärden för att skapa eller uppdatera tillägget.</span><span class="sxs-lookup"><span data-stu-id="f7552-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="f7552-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f7552-104">SYNTAX</span></span>

### <span data-ttu-id="f7552-105">CreateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="f7552-105">CreateExpanded (Default)</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f7552-106">Göra</span><span class="sxs-lookup"><span data-stu-id="f7552-106">Create</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f7552-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f7552-107">CreateViaIdentity</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtension> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f7552-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f7552-108">CreateViaIdentityExpanded</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> -Location <String>
 [-AutoUpgradeMinorVersion] [-ExtensionType <String>] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>] [-TypeHandlerVersion <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f7552-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f7552-109">DESCRIPTION</span></span>
<span data-ttu-id="f7552-110">Åtgärden för att skapa eller uppdatera tillägget.</span><span class="sxs-lookup"><span data-stu-id="f7552-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="f7552-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f7552-111">EXAMPLES</span></span>

### <span data-ttu-id="f7552-112">Exempel 1: lägga till en ny anknytning till en dator</span><span class="sxs-lookup"><span data-stu-id="f7552-112">Example 1: Add a new extension to a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="f7552-113">Anger ett tillägg på en dator.</span><span class="sxs-lookup"><span data-stu-id="f7552-113">Sets an extension on a machine.</span></span>

### <span data-ttu-id="f7552-114">Exempel 2: lägga till ett nytt tillägg med parametrar för tillägg som anges via pipeline</span><span class="sxs-lookup"><span data-stu-id="f7552-114">Example 2: Add a new extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="f7552-115">Detta skapar ett nytt tillägg med de tilläggs parametrar som tillhandahålls av objektet som skickas via pipeline.</span><span class="sxs-lookup"><span data-stu-id="f7552-115">This creates a new extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="f7552-116">Det är bra om du vill ta fram parametrarna på en dator och använda den på en annan dator.</span><span class="sxs-lookup"><span data-stu-id="f7552-116">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

### <span data-ttu-id="f7552-117">Exempel 3: Lägg till ett nytt tillägg med platsen som anges via pipeline</span><span class="sxs-lookup"><span data-stu-id="f7552-117">Example 3: Add a new extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $identity = [Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.ConnectedMachineIdentity]@{
    Id = "/subscriptions/$($SubscriptionId)/resourceGroups/$($ResourceGroupName)/providers/Microsoft.HybridCompute/machines/$MachineName/extensions/$ExtensionName"
}
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> $identity | New-AzConnectedMachineExtension -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="f7552-118">Detta skapar ett nytt dator tillägg med den identitet som tillhandahålls via pipeline.</span><span class="sxs-lookup"><span data-stu-id="f7552-118">This creates a new machine extension using the identity provided via the pipeline.</span></span>
<span data-ttu-id="f7552-119">Du kommer troligen inte att göra det, men det är möjligt.</span><span class="sxs-lookup"><span data-stu-id="f7552-119">You likely won't do this, but it's possible.</span></span>

### <span data-ttu-id="f7552-120">Exempel 4: lägga till ett nytt fil namns tillägg med ett objekt som både plats och parametrar för uppdatering</span><span class="sxs-lookup"><span data-stu-id="f7552-120">Example 4: Add a new extension using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $ext = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $ext | New-AzConnectedMachineExtension -ExtensionParameter $ext
```

<span data-ttu-id="f7552-121">Detta skapar ett nytt dator tillägg med den identitet som tillhandahålls via pipeline och tilläggs informationen som tillhandahålls av det överförda tillägget.</span><span class="sxs-lookup"><span data-stu-id="f7552-121">This creates a new machine extension using the identity provided via the pipeline and the extension details provided by the passed in extension object.</span></span>
<span data-ttu-id="f7552-122">Du kommer troligen inte att göra det, men det är möjligt.</span><span class="sxs-lookup"><span data-stu-id="f7552-122">You likely won't do this, but it's possible.</span></span>

## <span data-ttu-id="f7552-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f7552-123">PARAMETERS</span></span>

### <span data-ttu-id="f7552-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7552-124">-AsJob</span></span>
<span data-ttu-id="f7552-125">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="f7552-125">Run the command as a job</span></span>

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

### <span data-ttu-id="f7552-126">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f7552-126">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="f7552-127">Anger om tillägget ska använda en nyare del version om en sådan finns tillgänglig vid distribution.</span><span class="sxs-lookup"><span data-stu-id="f7552-127">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="f7552-128">När tillägget har distribuerats uppgraderas inte del versioner såvida inte den här egenskapen är angiven till true.</span><span class="sxs-lookup"><span data-stu-id="f7552-128">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7552-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7552-129">-DefaultProfile</span></span>
<span data-ttu-id="f7552-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f7552-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7552-131">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="f7552-131">-ExtensionParameter</span></span>
<span data-ttu-id="f7552-132">Beskriver ett dator tillägg.</span><span class="sxs-lookup"><span data-stu-id="f7552-132">Describes a Machine Extension.</span></span>
<span data-ttu-id="f7552-133">För att konstruera kan du läsa avsnittet anteckningar för EXTENSIONPARAMETER-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f7552-133">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7552-134">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="f7552-134">-ExtensionType</span></span>
<span data-ttu-id="f7552-135">Anger typen av förlängning; ett exempel är "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="f7552-135">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7552-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="f7552-136">-ForceRerun</span></span>
<span data-ttu-id="f7552-137">Så här tvingas förlängnings hanteraren att uppdateras även om tilläggs konfigurationen inte har ändrats.</span><span class="sxs-lookup"><span data-stu-id="f7552-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7552-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7552-138">-InputObject</span></span>
<span data-ttu-id="f7552-139">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f7552-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7552-140">-Plats</span><span class="sxs-lookup"><span data-stu-id="f7552-140">-Location</span></span>
<span data-ttu-id="f7552-141">Den Geo-plats där resursen bor</span><span class="sxs-lookup"><span data-stu-id="f7552-141">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7552-142">-MachineName</span><span class="sxs-lookup"><span data-stu-id="f7552-142">-MachineName</span></span>
<span data-ttu-id="f7552-143">Namnet på den dator där fil namns tillägget ska skapas eller uppdateras.</span><span class="sxs-lookup"><span data-stu-id="f7552-143">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7552-144">-Namn</span><span class="sxs-lookup"><span data-stu-id="f7552-144">-Name</span></span>
<span data-ttu-id="f7552-145">Namnet på dator tillägget.</span><span class="sxs-lookup"><span data-stu-id="f7552-145">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7552-146">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f7552-146">-NoWait</span></span>
<span data-ttu-id="f7552-147">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="f7552-147">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f7552-148">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="f7552-148">-ProtectedSetting</span></span>
<span data-ttu-id="f7552-149">Tillägget kan innehålla antingen protectedSettings eller protectedSettingsFromKeyVault eller inga skyddade inställningar alls.</span><span class="sxs-lookup"><span data-stu-id="f7552-149">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesProtectedSettings
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7552-150">-Publisher</span><span class="sxs-lookup"><span data-stu-id="f7552-150">-Publisher</span></span>
<span data-ttu-id="f7552-151">Namnet på tilläggs hanterarens utgivare.</span><span class="sxs-lookup"><span data-stu-id="f7552-151">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7552-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7552-152">-ResourceGroupName</span></span>
<span data-ttu-id="f7552-153">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f7552-153">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7552-154">-Ställ in</span><span class="sxs-lookup"><span data-stu-id="f7552-154">-Setting</span></span>
<span data-ttu-id="f7552-155">JSON-formaterade offentliga inställningar för tillägget.</span><span class="sxs-lookup"><span data-stu-id="f7552-155">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesSettings
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7552-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f7552-156">-SubscriptionId</span></span>
<span data-ttu-id="f7552-157">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f7552-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f7552-158">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="f7552-158">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7552-159">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f7552-159">-Tag</span></span>
<span data-ttu-id="f7552-160">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="f7552-160">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7552-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f7552-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="f7552-162">Anger versionen för skript hanteraren.</span><span class="sxs-lookup"><span data-stu-id="f7552-162">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7552-163">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f7552-163">-Confirm</span></span>
<span data-ttu-id="f7552-164">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f7552-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7552-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7552-165">-WhatIf</span></span>
<span data-ttu-id="f7552-166">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f7552-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7552-167">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f7552-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7552-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7552-168">CommonParameters</span></span>
<span data-ttu-id="f7552-169">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7552-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7552-170">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7552-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7552-171">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f7552-171">INPUTS</span></span>

### <span data-ttu-id="f7552-172">Microsoft. Azure. PowerShell. cmdletar. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="f7552-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

### <span data-ttu-id="f7552-173">Microsoft. Azure. PowerShell. cmdletar. ConnectedMachine. Models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="f7552-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="f7552-174">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f7552-174">OUTPUTS</span></span>

### <span data-ttu-id="f7552-175">Microsoft. Azure. PowerShell. cmdletar. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="f7552-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="f7552-176">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f7552-176">NOTES</span></span>

<span data-ttu-id="f7552-177">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f7552-177">ALIASES</span></span>

<span data-ttu-id="f7552-178">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="f7552-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f7552-179">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="f7552-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f7552-180">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f7552-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f7552-181">EXTENSIONPARAMETER <IMachineExtension> : beskriver ett dator tillägg.</span><span class="sxs-lookup"><span data-stu-id="f7552-181">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="f7552-182">`Location <String>`: Den Geo-plats där resursen bor</span><span class="sxs-lookup"><span data-stu-id="f7552-182">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="f7552-183">`[Tag <ITrackedResourceTags>]`: Resursfiler.</span><span class="sxs-lookup"><span data-stu-id="f7552-183">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="f7552-184">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="f7552-184">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="f7552-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Anger om tillägget ska använda en nyare del version om en sådan finns tillgänglig vid distributions tillfället.</span><span class="sxs-lookup"><span data-stu-id="f7552-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="f7552-186">När tillägget har distribuerats uppgraderas inte del versioner såvida inte den här egenskapen är angiven till true.</span><span class="sxs-lookup"><span data-stu-id="f7552-186">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="f7552-187">`[ForceUpdateTag <String>]`: Hur tilläggs hanteraren ska tvingas uppdatera även om tilläggs konfigurationen inte har ändrats.</span><span class="sxs-lookup"><span data-stu-id="f7552-187">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="f7552-188">`[MachineExtensionType <String>]`: Anger typen av tillägget. ett exempel är "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="f7552-188">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="f7552-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: Tillägget kan innehålla antingen protectedSettings eller protectedSettingsFromKeyVault eller inga skyddade inställningar alls.</span><span class="sxs-lookup"><span data-stu-id="f7552-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="f7552-190">`[Publisher <String>]`: Namnet på tilläggs hanterarens utgivare.</span><span class="sxs-lookup"><span data-stu-id="f7552-190">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="f7552-191">`[Setting <IMachineExtensionPropertiesSettings>]`: JSON-formaterade offentliga inställningar för tillägget.</span><span class="sxs-lookup"><span data-stu-id="f7552-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="f7552-192">`[TypeHandlerVersion <String>]`: Anger versionen för skript hanteraren.</span><span class="sxs-lookup"><span data-stu-id="f7552-192">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="f7552-193">INPUTOBJECT <IConnectedMachineIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="f7552-193">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f7552-194">`[ExtensionName <String>]`: Namnet på dator tillägget.</span><span class="sxs-lookup"><span data-stu-id="f7552-194">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="f7552-195">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="f7552-195">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f7552-196">`[Name <String>]`: Hybrid datorns namn.</span><span class="sxs-lookup"><span data-stu-id="f7552-196">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="f7552-197">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f7552-197">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="f7552-198">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="f7552-198">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f7552-199">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="f7552-199">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f7552-200">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f7552-200">RELATED LINKS</span></span>

