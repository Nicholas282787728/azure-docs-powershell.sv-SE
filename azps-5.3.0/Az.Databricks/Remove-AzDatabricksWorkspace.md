---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
ms.openlocfilehash: 629b12a7db506b0a96633396b97e0df3d66e1760
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525260"
---
# <span data-ttu-id="38ebf-101">Remove-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="38ebf-101">Remove-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="38ebf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="38ebf-102">SYNOPSIS</span></span>
<span data-ttu-id="38ebf-103">Tar bort arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="38ebf-103">Deletes the workspace.</span></span>

## <span data-ttu-id="38ebf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="38ebf-104">SYNTAX</span></span>

### <span data-ttu-id="38ebf-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="38ebf-105">Delete (Default)</span></span>
```
Remove-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="38ebf-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="38ebf-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="38ebf-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="38ebf-107">DESCRIPTION</span></span>
<span data-ttu-id="38ebf-108">Tar bort arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="38ebf-108">Deletes the workspace.</span></span>

## <span data-ttu-id="38ebf-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="38ebf-109">EXAMPLES</span></span>

### <span data-ttu-id="38ebf-110">Exempel 1: ta bort en Databricks-arbetsyta</span><span class="sxs-lookup"><span data-stu-id="38ebf-110">Example 1: Remove a Databricks workspace</span></span>
```powershell
PS C:\> Remove-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test
```

<span data-ttu-id="38ebf-111">Det här kommandot tar bort en Databricks-arbetsyta från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="38ebf-111">This command removes a Databricks workspace from a resource group.</span></span>

### <span data-ttu-id="38ebf-112">Exempel 2: ta bort en Databricks-arbetsyta efter objekt</span><span class="sxs-lookup"><span data-stu-id="38ebf-112">Example 2: Remove a Databricks workspace by object</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test02
PS C:\> Remove-AzDatabricksWorkspace -InputObject $dbr
```

<span data-ttu-id="38ebf-113">Det här kommandot tar bort en Databricks-arbetsyta från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="38ebf-113">This command removes a Databricks workspace from a resource group.</span></span>

## <span data-ttu-id="38ebf-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="38ebf-114">PARAMETERS</span></span>

### <span data-ttu-id="38ebf-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38ebf-115">-AsJob</span></span>
<span data-ttu-id="38ebf-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="38ebf-116">Run the command as a job</span></span>

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

### <span data-ttu-id="38ebf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38ebf-117">-DefaultProfile</span></span>
<span data-ttu-id="38ebf-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="38ebf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38ebf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38ebf-119">-InputObject</span></span>
<span data-ttu-id="38ebf-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="38ebf-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38ebf-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="38ebf-121">-Name</span></span>
<span data-ttu-id="38ebf-122">Namnet på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="38ebf-122">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ebf-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="38ebf-123">-NoWait</span></span>
<span data-ttu-id="38ebf-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="38ebf-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="38ebf-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38ebf-125">-PassThru</span></span>
<span data-ttu-id="38ebf-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="38ebf-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="38ebf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38ebf-127">-ResourceGroupName</span></span>
<span data-ttu-id="38ebf-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="38ebf-128">The name of the resource group.</span></span>
<span data-ttu-id="38ebf-129">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="38ebf-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="38ebf-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="38ebf-130">-SubscriptionId</span></span>
<span data-ttu-id="38ebf-131">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="38ebf-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="38ebf-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="38ebf-132">-Confirm</span></span>
<span data-ttu-id="38ebf-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="38ebf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38ebf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38ebf-134">-WhatIf</span></span>
<span data-ttu-id="38ebf-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="38ebf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38ebf-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="38ebf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38ebf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38ebf-137">CommonParameters</span></span>
<span data-ttu-id="38ebf-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38ebf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38ebf-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38ebf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38ebf-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="38ebf-140">INPUTS</span></span>

### <span data-ttu-id="38ebf-141">Microsoft. Azure. PowerShell. cmdletar. Databricks. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="38ebf-141">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="38ebf-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="38ebf-142">OUTPUTS</span></span>

### <span data-ttu-id="38ebf-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="38ebf-143">System.Boolean</span></span>

## <span data-ttu-id="38ebf-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="38ebf-144">NOTES</span></span>

<span data-ttu-id="38ebf-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="38ebf-145">ALIASES</span></span>

<span data-ttu-id="38ebf-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="38ebf-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="38ebf-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="38ebf-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="38ebf-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="38ebf-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="38ebf-149">INPUTOBJECT <IDatabricksIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="38ebf-149">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="38ebf-150">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="38ebf-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="38ebf-151">`[PeeringName <String>]`: Namnet på arbets ytans vNet-peering.</span><span class="sxs-lookup"><span data-stu-id="38ebf-151">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="38ebf-152">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="38ebf-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="38ebf-153">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="38ebf-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="38ebf-154">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="38ebf-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="38ebf-155">`[WorkspaceName <String>]`: Arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="38ebf-155">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="38ebf-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="38ebf-156">RELATED LINKS</span></span>

