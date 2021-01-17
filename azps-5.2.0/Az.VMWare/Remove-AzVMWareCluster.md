---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareCluster.md
ms.openlocfilehash: 936ed70f7040f9558db891b4e75299759c647bf9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418011"
---
# <span data-ttu-id="acf64-101">Remove-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="acf64-101">Remove-AzVMWareCluster</span></span>

## <span data-ttu-id="acf64-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="acf64-102">SYNOPSIS</span></span>
<span data-ttu-id="acf64-103">Ta bort ett kluster i ett privat moln</span><span class="sxs-lookup"><span data-stu-id="acf64-103">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="acf64-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="acf64-104">SYNTAX</span></span>

### <span data-ttu-id="acf64-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="acf64-105">Delete (Default)</span></span>
```
Remove-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="acf64-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="acf64-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="acf64-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="acf64-107">DESCRIPTION</span></span>
<span data-ttu-id="acf64-108">Ta bort ett kluster i ett privat moln</span><span class="sxs-lookup"><span data-stu-id="acf64-108">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="acf64-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="acf64-109">EXAMPLES</span></span>

### <span data-ttu-id="acf64-110">Exempel 1: ta bort kluster i privat moln</span><span class="sxs-lookup"><span data-stu-id="acf64-110">Example 1: Delete cluster in private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="acf64-111">Ta bort kluster i privata moln</span><span class="sxs-lookup"><span data-stu-id="acf64-111">Delete cluster in private cloud</span></span>

## <span data-ttu-id="acf64-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="acf64-112">PARAMETERS</span></span>

### <span data-ttu-id="acf64-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="acf64-113">-AsJob</span></span>
<span data-ttu-id="acf64-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="acf64-114">Run the command as a job</span></span>

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

### <span data-ttu-id="acf64-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acf64-115">-DefaultProfile</span></span>
<span data-ttu-id="acf64-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="acf64-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acf64-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acf64-117">-InputObject</span></span>
<span data-ttu-id="acf64-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="acf64-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="acf64-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="acf64-119">-Name</span></span>
<span data-ttu-id="acf64-120">Namnet på klustret i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="acf64-120">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="acf64-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="acf64-121">-NoWait</span></span>
<span data-ttu-id="acf64-122">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="acf64-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="acf64-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="acf64-123">-PassThru</span></span>
<span data-ttu-id="acf64-124">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="acf64-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="acf64-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="acf64-125">-PrivateCloudName</span></span>
<span data-ttu-id="acf64-126">Namn på det privata molnet</span><span class="sxs-lookup"><span data-stu-id="acf64-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="acf64-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acf64-127">-ResourceGroupName</span></span>
<span data-ttu-id="acf64-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="acf64-128">The name of the resource group.</span></span>
<span data-ttu-id="acf64-129">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="acf64-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="acf64-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="acf64-130">-SubscriptionId</span></span>
<span data-ttu-id="acf64-131">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="acf64-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="acf64-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="acf64-132">-Confirm</span></span>
<span data-ttu-id="acf64-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="acf64-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acf64-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acf64-134">-WhatIf</span></span>
<span data-ttu-id="acf64-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="acf64-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acf64-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="acf64-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acf64-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acf64-137">CommonParameters</span></span>
<span data-ttu-id="acf64-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acf64-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acf64-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="acf64-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acf64-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="acf64-140">INPUTS</span></span>

### <span data-ttu-id="acf64-141">Microsoft. Azure. PowerShell. cmdletar. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="acf64-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="acf64-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="acf64-142">OUTPUTS</span></span>

### <span data-ttu-id="acf64-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="acf64-143">System.Boolean</span></span>

## <span data-ttu-id="acf64-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="acf64-144">NOTES</span></span>

<span data-ttu-id="acf64-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="acf64-145">ALIASES</span></span>

<span data-ttu-id="acf64-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="acf64-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="acf64-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="acf64-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="acf64-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="acf64-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="acf64-149">INPUTOBJECT <IVMWareIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="acf64-149">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="acf64-150">`[AuthorizationName <String>]`: Namnet på ExpressRoute-kretsen i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="acf64-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="acf64-151">`[ClusterName <String>]`: Namnet på klustret i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="acf64-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="acf64-152">`[HcxEnterpriseSiteName <String>]`: Namnet på den HCX företags webbplatsen i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="acf64-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="acf64-153">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="acf64-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="acf64-154">`[Location <String>]`: Azure-region</span><span class="sxs-lookup"><span data-stu-id="acf64-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="acf64-155">`[PrivateCloudName <String>]`: Namnet på det privata molnet</span><span class="sxs-lookup"><span data-stu-id="acf64-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="acf64-156">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="acf64-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="acf64-157">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="acf64-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="acf64-158">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="acf64-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="acf64-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="acf64-159">RELATED LINKS</span></span>

