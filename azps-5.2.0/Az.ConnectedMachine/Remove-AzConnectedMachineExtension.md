---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
ms.openlocfilehash: ee746fd2f9a35415e4efd3c2f8aaba803d182beb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389154"
---
# <span data-ttu-id="752ec-101">Remove-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="752ec-101">Remove-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="752ec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="752ec-102">SYNOPSIS</span></span>
<span data-ttu-id="752ec-103">Åtgärden för att ta bort tillägget.</span><span class="sxs-lookup"><span data-stu-id="752ec-103">The operation to delete the extension.</span></span>

## <span data-ttu-id="752ec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="752ec-104">SYNTAX</span></span>

### <span data-ttu-id="752ec-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="752ec-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="752ec-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="752ec-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="752ec-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="752ec-107">DESCRIPTION</span></span>
<span data-ttu-id="752ec-108">Åtgärden för att ta bort tillägget.</span><span class="sxs-lookup"><span data-stu-id="752ec-108">The operation to delete the extension.</span></span>

## <span data-ttu-id="752ec-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="752ec-109">EXAMPLES</span></span>

### <span data-ttu-id="752ec-110">Exempel 1: ta bort ett dator tillägg.</span><span class="sxs-lookup"><span data-stu-id="752ec-110">Example 1: Remove a machine extension.</span></span>
```powershell
PS C:\> Remove-AzConnectedMachineExtension -MachineName myMachine -ResourceGroupName myRG -Name custom

```

<span data-ttu-id="752ec-111">Tar bort tillägget på datorn.</span><span class="sxs-lookup"><span data-stu-id="752ec-111">Deletes the extension on the machine.</span></span>

### <span data-ttu-id="752ec-112">Exempel 2: ta bort förlängning via pipeline</span><span class="sxs-lookup"><span data-stu-id="752ec-112">Example 2: Remove extension via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName myMachine | Remove-AzConnectedMachineExtension

```

<span data-ttu-id="752ec-113">Tar bort alla tillägg på datorn.</span><span class="sxs-lookup"><span data-stu-id="752ec-113">Removes all extensions in the specified machine.</span></span>

## <span data-ttu-id="752ec-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="752ec-114">PARAMETERS</span></span>

### <span data-ttu-id="752ec-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="752ec-115">-AsJob</span></span>
<span data-ttu-id="752ec-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="752ec-116">Run the command as a job</span></span>

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

### <span data-ttu-id="752ec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="752ec-117">-DefaultProfile</span></span>
<span data-ttu-id="752ec-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="752ec-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="752ec-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="752ec-119">-InputObject</span></span>
<span data-ttu-id="752ec-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="752ec-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="752ec-121">-MachineName</span><span class="sxs-lookup"><span data-stu-id="752ec-121">-MachineName</span></span>
<span data-ttu-id="752ec-122">Namnet på den dator där tillägget ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="752ec-122">The name of the machine where the extension should be deleted.</span></span>

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

### <span data-ttu-id="752ec-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="752ec-123">-Name</span></span>
<span data-ttu-id="752ec-124">Namnet på dator tillägget.</span><span class="sxs-lookup"><span data-stu-id="752ec-124">The name of the machine extension.</span></span>

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

### <span data-ttu-id="752ec-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="752ec-125">-NoWait</span></span>
<span data-ttu-id="752ec-126">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="752ec-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="752ec-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="752ec-127">-PassThru</span></span>
<span data-ttu-id="752ec-128">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="752ec-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="752ec-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="752ec-129">-ResourceGroupName</span></span>
<span data-ttu-id="752ec-130">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="752ec-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="752ec-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="752ec-131">-SubscriptionId</span></span>
<span data-ttu-id="752ec-132">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="752ec-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="752ec-133">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="752ec-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="752ec-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="752ec-134">-Confirm</span></span>
<span data-ttu-id="752ec-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="752ec-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="752ec-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="752ec-136">-WhatIf</span></span>
<span data-ttu-id="752ec-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="752ec-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="752ec-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="752ec-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="752ec-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="752ec-139">CommonParameters</span></span>
<span data-ttu-id="752ec-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="752ec-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="752ec-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="752ec-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="752ec-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="752ec-142">INPUTS</span></span>

### <span data-ttu-id="752ec-143">Microsoft. Azure. PowerShell. cmdletar. ConnectedMachine. Models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="752ec-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="752ec-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="752ec-144">OUTPUTS</span></span>

### <span data-ttu-id="752ec-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="752ec-145">System.Boolean</span></span>

## <span data-ttu-id="752ec-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="752ec-146">NOTES</span></span>

<span data-ttu-id="752ec-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="752ec-147">ALIASES</span></span>

<span data-ttu-id="752ec-148">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="752ec-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="752ec-149">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="752ec-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="752ec-150">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="752ec-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="752ec-151">INPUTOBJECT <IConnectedMachineIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="752ec-151">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="752ec-152">`[ExtensionName <String>]`: Namnet på dator tillägget.</span><span class="sxs-lookup"><span data-stu-id="752ec-152">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="752ec-153">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="752ec-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="752ec-154">`[Name <String>]`: Hybrid datorns namn.</span><span class="sxs-lookup"><span data-stu-id="752ec-154">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="752ec-155">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="752ec-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="752ec-156">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="752ec-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="752ec-157">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="752ec-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="752ec-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="752ec-158">RELATED LINKS</span></span>

