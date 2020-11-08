---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
ms.openlocfilehash: ee746fd2f9a35415e4efd3c2f8aaba803d182beb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271965"
---
# <span data-ttu-id="06409-101">Remove-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="06409-101">Remove-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="06409-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06409-102">SYNOPSIS</span></span>
<span data-ttu-id="06409-103">Åtgärden för att ta bort tillägget.</span><span class="sxs-lookup"><span data-stu-id="06409-103">The operation to delete the extension.</span></span>

## <span data-ttu-id="06409-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06409-104">SYNTAX</span></span>

### <span data-ttu-id="06409-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="06409-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="06409-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="06409-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="06409-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06409-107">DESCRIPTION</span></span>
<span data-ttu-id="06409-108">Åtgärden för att ta bort tillägget.</span><span class="sxs-lookup"><span data-stu-id="06409-108">The operation to delete the extension.</span></span>

## <span data-ttu-id="06409-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06409-109">EXAMPLES</span></span>

### <span data-ttu-id="06409-110">Exempel 1: ta bort ett dator tillägg.</span><span class="sxs-lookup"><span data-stu-id="06409-110">Example 1: Remove a machine extension.</span></span>
```powershell
PS C:\> Remove-AzConnectedMachineExtension -MachineName myMachine -ResourceGroupName myRG -Name custom

```

<span data-ttu-id="06409-111">Tar bort tillägget på datorn.</span><span class="sxs-lookup"><span data-stu-id="06409-111">Deletes the extension on the machine.</span></span>

### <span data-ttu-id="06409-112">Exempel 2: ta bort förlängning via pipeline</span><span class="sxs-lookup"><span data-stu-id="06409-112">Example 2: Remove extension via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName myMachine | Remove-AzConnectedMachineExtension

```

<span data-ttu-id="06409-113">Tar bort alla tillägg på datorn.</span><span class="sxs-lookup"><span data-stu-id="06409-113">Removes all extensions in the specified machine.</span></span>

## <span data-ttu-id="06409-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06409-114">PARAMETERS</span></span>

### <span data-ttu-id="06409-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06409-115">-AsJob</span></span>
<span data-ttu-id="06409-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="06409-116">Run the command as a job</span></span>

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

### <span data-ttu-id="06409-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06409-117">-DefaultProfile</span></span>
<span data-ttu-id="06409-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="06409-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06409-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06409-119">-InputObject</span></span>
<span data-ttu-id="06409-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="06409-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06409-121">-MachineName</span><span class="sxs-lookup"><span data-stu-id="06409-121">-MachineName</span></span>
<span data-ttu-id="06409-122">Namnet på den dator där tillägget ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="06409-122">The name of the machine where the extension should be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06409-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="06409-123">-Name</span></span>
<span data-ttu-id="06409-124">Namnet på dator tillägget.</span><span class="sxs-lookup"><span data-stu-id="06409-124">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06409-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="06409-125">-NoWait</span></span>
<span data-ttu-id="06409-126">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="06409-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="06409-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06409-127">-PassThru</span></span>
<span data-ttu-id="06409-128">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="06409-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="06409-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06409-129">-ResourceGroupName</span></span>
<span data-ttu-id="06409-130">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="06409-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06409-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="06409-131">-SubscriptionId</span></span>
<span data-ttu-id="06409-132">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="06409-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="06409-133">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="06409-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06409-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="06409-134">-Confirm</span></span>
<span data-ttu-id="06409-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="06409-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06409-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06409-136">-WhatIf</span></span>
<span data-ttu-id="06409-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="06409-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06409-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="06409-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06409-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06409-139">CommonParameters</span></span>
<span data-ttu-id="06409-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06409-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06409-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06409-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06409-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06409-142">INPUTS</span></span>

### <span data-ttu-id="06409-143">Microsoft. Azure. PowerShell. cmdletar. ConnectedMachine. Models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="06409-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="06409-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06409-144">OUTPUTS</span></span>

### <span data-ttu-id="06409-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="06409-145">System.Boolean</span></span>

## <span data-ttu-id="06409-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06409-146">NOTES</span></span>

<span data-ttu-id="06409-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="06409-147">ALIASES</span></span>

<span data-ttu-id="06409-148">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="06409-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="06409-149">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="06409-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="06409-150">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="06409-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="06409-151">INPUTOBJECT <IConnectedMachineIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="06409-151">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="06409-152">`[ExtensionName <String>]`: Namnet på dator tillägget.</span><span class="sxs-lookup"><span data-stu-id="06409-152">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="06409-153">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="06409-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="06409-154">`[Name <String>]`: Hybrid datorns namn.</span><span class="sxs-lookup"><span data-stu-id="06409-154">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="06409-155">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="06409-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="06409-156">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="06409-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="06409-157">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="06409-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="06409-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06409-158">RELATED LINKS</span></span>

