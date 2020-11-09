---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
ms.openlocfilehash: accf225acfb05fdcaf49eb5dde4d1bae0332d300
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322554"
---
# <span data-ttu-id="4caef-101">Remove-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="4caef-101">Remove-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="4caef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4caef-102">SYNOPSIS</span></span>
<span data-ttu-id="4caef-103">Ta bort ett privat moln</span><span class="sxs-lookup"><span data-stu-id="4caef-103">Delete a private cloud</span></span>

## <span data-ttu-id="4caef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4caef-104">SYNTAX</span></span>

### <span data-ttu-id="4caef-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="4caef-105">Delete (Default)</span></span>
```
Remove-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4caef-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4caef-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4caef-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4caef-107">DESCRIPTION</span></span>
<span data-ttu-id="4caef-108">Ta bort ett privat moln</span><span class="sxs-lookup"><span data-stu-id="4caef-108">Delete a private cloud</span></span>

## <span data-ttu-id="4caef-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4caef-109">EXAMPLES</span></span>

### <span data-ttu-id="4caef-110">Exempel 1: ta bort ett privat moln</span><span class="sxs-lookup"><span data-stu-id="4caef-110">Example 1: Delete private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

<span data-ttu-id="4caef-111">Ta bort privat moln</span><span class="sxs-lookup"><span data-stu-id="4caef-111">Delete private cloud</span></span>

## <span data-ttu-id="4caef-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4caef-112">PARAMETERS</span></span>

### <span data-ttu-id="4caef-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4caef-113">-AsJob</span></span>
<span data-ttu-id="4caef-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="4caef-114">Run the command as a job</span></span>

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

### <span data-ttu-id="4caef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4caef-115">-DefaultProfile</span></span>
<span data-ttu-id="4caef-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4caef-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4caef-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4caef-117">-InputObject</span></span>
<span data-ttu-id="4caef-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="4caef-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4caef-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="4caef-119">-Name</span></span>
<span data-ttu-id="4caef-120">Namn på det privata molnet</span><span class="sxs-lookup"><span data-stu-id="4caef-120">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4caef-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="4caef-121">-NoWait</span></span>
<span data-ttu-id="4caef-122">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="4caef-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4caef-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4caef-123">-PassThru</span></span>
<span data-ttu-id="4caef-124">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="4caef-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4caef-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4caef-125">-ResourceGroupName</span></span>
<span data-ttu-id="4caef-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4caef-126">The name of the resource group.</span></span>
<span data-ttu-id="4caef-127">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="4caef-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4caef-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4caef-128">-SubscriptionId</span></span>
<span data-ttu-id="4caef-129">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4caef-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4caef-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4caef-130">-Confirm</span></span>
<span data-ttu-id="4caef-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4caef-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4caef-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4caef-132">-WhatIf</span></span>
<span data-ttu-id="4caef-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4caef-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4caef-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4caef-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4caef-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4caef-135">CommonParameters</span></span>
<span data-ttu-id="4caef-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4caef-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4caef-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4caef-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4caef-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4caef-138">INPUTS</span></span>

### <span data-ttu-id="4caef-139">Microsoft. Azure. PowerShell. cmdletar. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="4caef-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="4caef-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4caef-140">OUTPUTS</span></span>

### <span data-ttu-id="4caef-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4caef-141">System.Boolean</span></span>

## <span data-ttu-id="4caef-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4caef-142">NOTES</span></span>

<span data-ttu-id="4caef-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4caef-143">ALIASES</span></span>

<span data-ttu-id="4caef-144">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="4caef-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4caef-145">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="4caef-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4caef-146">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4caef-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4caef-147">INPUTOBJECT <IVMWareIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="4caef-147">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4caef-148">`[AuthorizationName <String>]`: Namnet på ExpressRoute-kretsen i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="4caef-148">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="4caef-149">`[ClusterName <String>]`: Namnet på klustret i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="4caef-149">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="4caef-150">`[HcxEnterpriseSiteName <String>]`: Namnet på den HCX företags webbplatsen i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="4caef-150">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="4caef-151">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="4caef-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4caef-152">`[Location <String>]`: Azure-region</span><span class="sxs-lookup"><span data-stu-id="4caef-152">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="4caef-153">`[PrivateCloudName <String>]`: Namnet på det privata molnet</span><span class="sxs-lookup"><span data-stu-id="4caef-153">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="4caef-154">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4caef-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4caef-155">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="4caef-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="4caef-156">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="4caef-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="4caef-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4caef-157">RELATED LINKS</span></span>

