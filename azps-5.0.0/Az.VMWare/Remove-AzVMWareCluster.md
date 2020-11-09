---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareCluster.md
ms.openlocfilehash: 936ed70f7040f9558db891b4e75299759c647bf9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323496"
---
# <span data-ttu-id="16e4d-101">Remove-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="16e4d-101">Remove-AzVMWareCluster</span></span>

## <span data-ttu-id="16e4d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="16e4d-102">SYNOPSIS</span></span>
<span data-ttu-id="16e4d-103">Ta bort ett kluster i ett privat moln</span><span class="sxs-lookup"><span data-stu-id="16e4d-103">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="16e4d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="16e4d-104">SYNTAX</span></span>

### <span data-ttu-id="16e4d-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="16e4d-105">Delete (Default)</span></span>
```
Remove-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="16e4d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="16e4d-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="16e4d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="16e4d-107">DESCRIPTION</span></span>
<span data-ttu-id="16e4d-108">Ta bort ett kluster i ett privat moln</span><span class="sxs-lookup"><span data-stu-id="16e4d-108">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="16e4d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="16e4d-109">EXAMPLES</span></span>

### <span data-ttu-id="16e4d-110">Exempel 1: ta bort kluster i privat moln</span><span class="sxs-lookup"><span data-stu-id="16e4d-110">Example 1: Delete cluster in private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="16e4d-111">Ta bort kluster i privata moln</span><span class="sxs-lookup"><span data-stu-id="16e4d-111">Delete cluster in private cloud</span></span>

## <span data-ttu-id="16e4d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="16e4d-112">PARAMETERS</span></span>

### <span data-ttu-id="16e4d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16e4d-113">-AsJob</span></span>
<span data-ttu-id="16e4d-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="16e4d-114">Run the command as a job</span></span>

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

### <span data-ttu-id="16e4d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e4d-115">-DefaultProfile</span></span>
<span data-ttu-id="16e4d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="16e4d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16e4d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16e4d-117">-InputObject</span></span>
<span data-ttu-id="16e4d-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="16e4d-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16e4d-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="16e4d-119">-Name</span></span>
<span data-ttu-id="16e4d-120">Namnet på klustret i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="16e4d-120">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16e4d-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="16e4d-121">-NoWait</span></span>
<span data-ttu-id="16e4d-122">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="16e4d-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="16e4d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16e4d-123">-PassThru</span></span>
<span data-ttu-id="16e4d-124">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="16e4d-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="16e4d-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="16e4d-125">-PrivateCloudName</span></span>
<span data-ttu-id="16e4d-126">Namn på det privata molnet</span><span class="sxs-lookup"><span data-stu-id="16e4d-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="16e4d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16e4d-127">-ResourceGroupName</span></span>
<span data-ttu-id="16e4d-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="16e4d-128">The name of the resource group.</span></span>
<span data-ttu-id="16e4d-129">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="16e4d-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="16e4d-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16e4d-130">-SubscriptionId</span></span>
<span data-ttu-id="16e4d-131">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="16e4d-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="16e4d-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="16e4d-132">-Confirm</span></span>
<span data-ttu-id="16e4d-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="16e4d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16e4d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16e4d-134">-WhatIf</span></span>
<span data-ttu-id="16e4d-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="16e4d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16e4d-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="16e4d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16e4d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e4d-137">CommonParameters</span></span>
<span data-ttu-id="16e4d-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16e4d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e4d-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16e4d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e4d-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="16e4d-140">INPUTS</span></span>

### <span data-ttu-id="16e4d-141">Microsoft. Azure. PowerShell. cmdletar. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="16e4d-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="16e4d-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="16e4d-142">OUTPUTS</span></span>

### <span data-ttu-id="16e4d-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="16e4d-143">System.Boolean</span></span>

## <span data-ttu-id="16e4d-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="16e4d-144">NOTES</span></span>

<span data-ttu-id="16e4d-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="16e4d-145">ALIASES</span></span>

<span data-ttu-id="16e4d-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="16e4d-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="16e4d-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="16e4d-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="16e4d-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="16e4d-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="16e4d-149">INPUTOBJECT <IVMWareIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="16e4d-149">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="16e4d-150">`[AuthorizationName <String>]`: Namnet på ExpressRoute-kretsen i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="16e4d-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="16e4d-151">`[ClusterName <String>]`: Namnet på klustret i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="16e4d-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="16e4d-152">`[HcxEnterpriseSiteName <String>]`: Namnet på den HCX företags webbplatsen i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="16e4d-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="16e4d-153">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="16e4d-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="16e4d-154">`[Location <String>]`: Azure-region</span><span class="sxs-lookup"><span data-stu-id="16e4d-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="16e4d-155">`[PrivateCloudName <String>]`: Namnet på det privata molnet</span><span class="sxs-lookup"><span data-stu-id="16e4d-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="16e4d-156">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="16e4d-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="16e4d-157">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="16e4d-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="16e4d-158">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="16e4d-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="16e4d-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="16e4d-159">RELATED LINKS</span></span>

