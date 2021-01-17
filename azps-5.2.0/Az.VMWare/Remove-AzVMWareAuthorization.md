---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareAuthorization.md
ms.openlocfilehash: 13f5e76a7fbb101e9fa6b1247f233c0f85aba8bf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393008"
---
# <span data-ttu-id="00859-101">Remove-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="00859-101">Remove-AzVMWareAuthorization</span></span>

## <span data-ttu-id="00859-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="00859-102">SYNOPSIS</span></span>
<span data-ttu-id="00859-103">Ta bort en ExpressRoute i ett privat moln</span><span class="sxs-lookup"><span data-stu-id="00859-103">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="00859-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="00859-104">SYNTAX</span></span>

### <span data-ttu-id="00859-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="00859-105">Delete (Default)</span></span>
```
Remove-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="00859-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="00859-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="00859-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="00859-107">DESCRIPTION</span></span>
<span data-ttu-id="00859-108">Ta bort en ExpressRoute i ett privat moln</span><span class="sxs-lookup"><span data-stu-id="00859-108">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="00859-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="00859-109">EXAMPLES</span></span>

### <span data-ttu-id="00859-110">Exempel 1: ta bort auktorisering för privat moln</span><span class="sxs-lookup"><span data-stu-id="00859-110">Example 1: Delete authorization for private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="00859-111">Ta bort auktorisering för privat moln</span><span class="sxs-lookup"><span data-stu-id="00859-111">Delete authorization for private cloud</span></span>

## <span data-ttu-id="00859-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="00859-112">PARAMETERS</span></span>

### <span data-ttu-id="00859-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00859-113">-AsJob</span></span>
<span data-ttu-id="00859-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="00859-114">Run the command as a job</span></span>

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

### <span data-ttu-id="00859-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00859-115">-DefaultProfile</span></span>
<span data-ttu-id="00859-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="00859-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00859-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00859-117">-InputObject</span></span>
<span data-ttu-id="00859-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="00859-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="00859-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="00859-119">-Name</span></span>
<span data-ttu-id="00859-120">Namn på ExpressRoute-kretsen i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="00859-120">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00859-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="00859-121">-NoWait</span></span>
<span data-ttu-id="00859-122">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="00859-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="00859-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00859-123">-PassThru</span></span>
<span data-ttu-id="00859-124">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="00859-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="00859-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="00859-125">-PrivateCloudName</span></span>
<span data-ttu-id="00859-126">Namn på det privata molnet</span><span class="sxs-lookup"><span data-stu-id="00859-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="00859-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00859-127">-ResourceGroupName</span></span>
<span data-ttu-id="00859-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="00859-128">The name of the resource group.</span></span>
<span data-ttu-id="00859-129">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="00859-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="00859-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="00859-130">-SubscriptionId</span></span>
<span data-ttu-id="00859-131">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="00859-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="00859-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="00859-132">-Confirm</span></span>
<span data-ttu-id="00859-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="00859-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00859-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00859-134">-WhatIf</span></span>
<span data-ttu-id="00859-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="00859-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00859-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="00859-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00859-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00859-137">CommonParameters</span></span>
<span data-ttu-id="00859-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00859-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00859-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00859-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00859-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="00859-140">INPUTS</span></span>

### <span data-ttu-id="00859-141">Microsoft. Azure. PowerShell. cmdletar. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="00859-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="00859-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="00859-142">OUTPUTS</span></span>

### <span data-ttu-id="00859-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="00859-143">System.Boolean</span></span>

## <span data-ttu-id="00859-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="00859-144">NOTES</span></span>

<span data-ttu-id="00859-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="00859-145">ALIASES</span></span>

<span data-ttu-id="00859-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="00859-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="00859-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="00859-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="00859-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="00859-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="00859-149">INPUTOBJECT <IVMWareIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="00859-149">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="00859-150">`[AuthorizationName <String>]`: Namnet på ExpressRoute-kretsen i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="00859-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="00859-151">`[ClusterName <String>]`: Namnet på klustret i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="00859-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="00859-152">`[HcxEnterpriseSiteName <String>]`: Namnet på den HCX företags webbplatsen i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="00859-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="00859-153">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="00859-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="00859-154">`[Location <String>]`: Azure-region</span><span class="sxs-lookup"><span data-stu-id="00859-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="00859-155">`[PrivateCloudName <String>]`: Namnet på det privata molnet</span><span class="sxs-lookup"><span data-stu-id="00859-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="00859-156">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="00859-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="00859-157">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="00859-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="00859-158">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="00859-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="00859-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="00859-159">RELATED LINKS</span></span>

