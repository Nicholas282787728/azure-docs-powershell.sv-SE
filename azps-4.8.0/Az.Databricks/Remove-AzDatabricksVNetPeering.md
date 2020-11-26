---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
ms.openlocfilehash: 1c75bb4e8f94fadfb3b56c2fbb44889c5eaff458
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262285"
---
# <span data-ttu-id="2c8f2-101">Remove-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="2c8f2-101">Remove-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="2c8f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c8f2-102">SYNOPSIS</span></span>
<span data-ttu-id="2c8f2-103">Tar bort arbets ytans vNetPeering.</span><span class="sxs-lookup"><span data-stu-id="2c8f2-103">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="2c8f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c8f2-104">SYNTAX</span></span>

### <span data-ttu-id="2c8f2-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="2c8f2-105">Delete (Default)</span></span>
```
Remove-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2c8f2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2c8f2-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2c8f2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c8f2-107">DESCRIPTION</span></span>
<span data-ttu-id="2c8f2-108">Tar bort arbets ytans vNetPeering.</span><span class="sxs-lookup"><span data-stu-id="2c8f2-108">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="2c8f2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c8f2-109">EXAMPLES</span></span>

### <span data-ttu-id="2c8f2-110">Exempel 1: ta bort en VNet-peering of databricks efter namn</span><span class="sxs-lookup"><span data-stu-id="2c8f2-110">Example 1: Remove a vnet peering of databricks by name</span></span>
```powershell
PS C:\> Remove-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01

```

<span data-ttu-id="2c8f2-111">Det här kommandot tar bort en VNet-peering of databricks efter namn</span><span class="sxs-lookup"><span data-stu-id="2c8f2-111">This command removes a vnet peering of databricks by name</span></span>

### <span data-ttu-id="2c8f2-112">Exempel 2: ta bort en VNet-peering of databricks efter objekt</span><span class="sxs-lookup"><span data-stu-id="2c8f2-112">Example 2: Remove a vnet peering of databricks by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01 | Remove-AzDatabricksVNetPeering

```

<span data-ttu-id="2c8f2-113">Det här kommandot tar bort en VNet-peering av databricks efter objekt</span><span class="sxs-lookup"><span data-stu-id="2c8f2-113">This command removes a vnet peering of databricks by object</span></span>

## <span data-ttu-id="2c8f2-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c8f2-114">PARAMETERS</span></span>

### <span data-ttu-id="2c8f2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c8f2-115">-AsJob</span></span>
<span data-ttu-id="2c8f2-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="2c8f2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="2c8f2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c8f2-117">-DefaultProfile</span></span>
<span data-ttu-id="2c8f2-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2c8f2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c8f2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c8f2-119">-InputObject</span></span>
<span data-ttu-id="2c8f2-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="2c8f2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2c8f2-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="2c8f2-121">-Name</span></span>
<span data-ttu-id="2c8f2-122">Namnet på arbets ytans vNet-peering.</span><span class="sxs-lookup"><span data-stu-id="2c8f2-122">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="2c8f2-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2c8f2-123">-NoWait</span></span>
<span data-ttu-id="2c8f2-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="2c8f2-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2c8f2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c8f2-125">-PassThru</span></span>
<span data-ttu-id="2c8f2-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="2c8f2-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2c8f2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c8f2-127">-ResourceGroupName</span></span>
<span data-ttu-id="2c8f2-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2c8f2-128">The name of the resource group.</span></span>
<span data-ttu-id="2c8f2-129">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="2c8f2-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2c8f2-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2c8f2-130">-SubscriptionId</span></span>
<span data-ttu-id="2c8f2-131">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="2c8f2-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2c8f2-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2c8f2-132">-WorkspaceName</span></span>
<span data-ttu-id="2c8f2-133">Namnet på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="2c8f2-133">The name of the workspace.</span></span>

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

### <span data-ttu-id="2c8f2-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2c8f2-134">-Confirm</span></span>
<span data-ttu-id="2c8f2-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2c8f2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c8f2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c8f2-136">-WhatIf</span></span>
<span data-ttu-id="2c8f2-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2c8f2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c8f2-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2c8f2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c8f2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c8f2-139">CommonParameters</span></span>
<span data-ttu-id="2c8f2-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c8f2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c8f2-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c8f2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c8f2-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c8f2-142">INPUTS</span></span>

### <span data-ttu-id="2c8f2-143">Microsoft. Azure. PowerShell. cmdletar. Databricks. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="2c8f2-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="2c8f2-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c8f2-144">OUTPUTS</span></span>

### <span data-ttu-id="2c8f2-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2c8f2-145">System.Boolean</span></span>

## <span data-ttu-id="2c8f2-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c8f2-146">NOTES</span></span>

<span data-ttu-id="2c8f2-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2c8f2-147">ALIASES</span></span>

<span data-ttu-id="2c8f2-148">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="2c8f2-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2c8f2-149">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="2c8f2-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2c8f2-150">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2c8f2-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2c8f2-151">INPUTOBJECT <IDatabricksIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="2c8f2-151">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2c8f2-152">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="2c8f2-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2c8f2-153">`[PeeringName <String>]`: Namnet på arbets ytans vNet-peering.</span><span class="sxs-lookup"><span data-stu-id="2c8f2-153">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="2c8f2-154">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2c8f2-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2c8f2-155">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="2c8f2-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="2c8f2-156">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="2c8f2-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2c8f2-157">`[WorkspaceName <String>]`: Arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="2c8f2-157">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="2c8f2-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c8f2-158">RELATED LINKS</span></span>
