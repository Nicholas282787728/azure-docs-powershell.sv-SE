---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWareCluster.md
ms.openlocfilehash: b8e1f819c01edac24ff23c629de130036442c9e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323495"
---
# <span data-ttu-id="e4714-101">Update-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="e4714-101">Update-AzVMWareCluster</span></span>

## <span data-ttu-id="e4714-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e4714-102">SYNOPSIS</span></span>
<span data-ttu-id="e4714-103">Uppdatera ett kluster i ett privat moln</span><span class="sxs-lookup"><span data-stu-id="e4714-103">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="e4714-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e4714-104">SYNTAX</span></span>

### <span data-ttu-id="e4714-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="e4714-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e4714-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e4714-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWareCluster -InputObject <IVMWareIdentity> [-ClusterSize <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e4714-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e4714-107">DESCRIPTION</span></span>
<span data-ttu-id="e4714-108">Uppdatera ett kluster i ett privat moln</span><span class="sxs-lookup"><span data-stu-id="e4714-108">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="e4714-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e4714-109">EXAMPLES</span></span>

### <span data-ttu-id="e4714-110">Exempel 1: Uppdatera kluster storlek efter namn</span><span class="sxs-lookup"><span data-stu-id="e4714-110">Example 1: Update cluster size by name</span></span>
```powershell
PS C:\> Update-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="e4714-111">Uppdatera kluster storlek efter namn</span><span class="sxs-lookup"><span data-stu-id="e4714-111">Update cluster size by name</span></span>

### <span data-ttu-id="e4714-112">Exempel 2: Uppdatera kluster storlek efter objekt</span><span class="sxs-lookup"><span data-stu-id="e4714-112">Example 2: Update cluster size by input object</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group | Update-AzVMWareCluster -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="e4714-113">Uppdatera kluster storlek efter objekt</span><span class="sxs-lookup"><span data-stu-id="e4714-113">Update cluster size by input object</span></span>

## <span data-ttu-id="e4714-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e4714-114">PARAMETERS</span></span>

### <span data-ttu-id="e4714-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4714-115">-AsJob</span></span>
<span data-ttu-id="e4714-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="e4714-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e4714-117">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="e4714-117">-ClusterSize</span></span>
<span data-ttu-id="e4714-118">Kluster storlek</span><span class="sxs-lookup"><span data-stu-id="e4714-118">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4714-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4714-119">-DefaultProfile</span></span>
<span data-ttu-id="e4714-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e4714-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4714-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4714-121">-InputObject</span></span>
<span data-ttu-id="e4714-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e4714-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4714-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="e4714-123">-Name</span></span>
<span data-ttu-id="e4714-124">Namnet på klustret i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="e4714-124">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4714-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e4714-125">-NoWait</span></span>
<span data-ttu-id="e4714-126">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="e4714-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e4714-127">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="e4714-127">-PrivateCloudName</span></span>
<span data-ttu-id="e4714-128">Namn på det privata molnet</span><span class="sxs-lookup"><span data-stu-id="e4714-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="e4714-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4714-129">-ResourceGroupName</span></span>
<span data-ttu-id="e4714-130">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e4714-130">The name of the resource group.</span></span>
<span data-ttu-id="e4714-131">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="e4714-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e4714-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e4714-132">-SubscriptionId</span></span>
<span data-ttu-id="e4714-133">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e4714-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4714-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e4714-134">-Confirm</span></span>
<span data-ttu-id="e4714-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e4714-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4714-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4714-136">-WhatIf</span></span>
<span data-ttu-id="e4714-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e4714-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4714-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e4714-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4714-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4714-139">CommonParameters</span></span>
<span data-ttu-id="e4714-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4714-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4714-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4714-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4714-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e4714-142">INPUTS</span></span>

### <span data-ttu-id="e4714-143">Microsoft. Azure. PowerShell. cmdletar. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="e4714-143">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="e4714-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e4714-144">OUTPUTS</span></span>

### <span data-ttu-id="e4714-145">Microsoft. Azure. PowerShell. cmdletar. VMWare. Models. Api20200320. ICluster</span><span class="sxs-lookup"><span data-stu-id="e4714-145">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="e4714-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e4714-146">NOTES</span></span>

<span data-ttu-id="e4714-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e4714-147">ALIASES</span></span>

<span data-ttu-id="e4714-148">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="e4714-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e4714-149">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="e4714-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e4714-150">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e4714-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e4714-151">INPUTOBJECT <IVMWareIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="e4714-151">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e4714-152">`[AuthorizationName <String>]`: Namnet på ExpressRoute-kretsen i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="e4714-152">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="e4714-153">`[ClusterName <String>]`: Namnet på klustret i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="e4714-153">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="e4714-154">`[HcxEnterpriseSiteName <String>]`: Namnet på den HCX företags webbplatsen i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="e4714-154">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="e4714-155">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="e4714-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e4714-156">`[Location <String>]`: Azure-region</span><span class="sxs-lookup"><span data-stu-id="e4714-156">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="e4714-157">`[PrivateCloudName <String>]`: Namnet på det privata molnet</span><span class="sxs-lookup"><span data-stu-id="e4714-157">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="e4714-158">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e4714-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e4714-159">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="e4714-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="e4714-160">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="e4714-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="e4714-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e4714-161">RELATED LINKS</span></span>

