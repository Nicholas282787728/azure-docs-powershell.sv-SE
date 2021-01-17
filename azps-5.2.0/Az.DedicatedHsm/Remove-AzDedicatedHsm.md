---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/remove-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
ms.openlocfilehash: aeb8eddcc094e951c78cfe778182cece70448111
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388587"
---
# <span data-ttu-id="12f97-101">Remove-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="12f97-101">Remove-AzDedicatedHsm</span></span>

## <span data-ttu-id="12f97-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12f97-102">SYNOPSIS</span></span>
<span data-ttu-id="12f97-103">Tar bort den angivna Azure-dedikerade HSM.</span><span class="sxs-lookup"><span data-stu-id="12f97-103">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="12f97-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12f97-104">SYNTAX</span></span>

### <span data-ttu-id="12f97-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="12f97-105">Delete (Default)</span></span>
```
Remove-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="12f97-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="12f97-106">DeleteViaIdentity</span></span>
```
Remove-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="12f97-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12f97-107">DESCRIPTION</span></span>
<span data-ttu-id="12f97-108">Tar bort den angivna Azure-dedikerade HSM.</span><span class="sxs-lookup"><span data-stu-id="12f97-108">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="12f97-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12f97-109">EXAMPLES</span></span>

### <span data-ttu-id="12f97-110">Exempel 1: ta bort en dedikerad HSM efter namn</span><span class="sxs-lookup"><span data-stu-id="12f97-110">Example 1: Remove a Dedicated HSM by name</span></span>
```powershell
PS C:\> Remove-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="12f97-111">Med den här commnad tas en HSM bort med namn.</span><span class="sxs-lookup"><span data-stu-id="12f97-111">This commnad removes a hardware security module(HSM) by name.</span></span>

### <span data-ttu-id="12f97-112">Exempel 2: ta bort en dedicerad HSM efter objekt</span><span class="sxs-lookup"><span data-stu-id="12f97-112">Example 2: Remove a Dedicated HSM  by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz
PS C:\> Remove-AzDedicatedHsm -InputObject  $hsm

```

<span data-ttu-id="12f97-113">Denna commnad tar bort en dedicerad HSM efter objekt.</span><span class="sxs-lookup"><span data-stu-id="12f97-113">This commnad removes a Dedicated HSM by object.</span></span>

## <span data-ttu-id="12f97-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12f97-114">PARAMETERS</span></span>

### <span data-ttu-id="12f97-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12f97-115">-AsJob</span></span>
<span data-ttu-id="12f97-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="12f97-116">Run the command as a job</span></span>

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

### <span data-ttu-id="12f97-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12f97-117">-DefaultProfile</span></span>
<span data-ttu-id="12f97-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="12f97-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12f97-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12f97-119">-InputObject</span></span>
<span data-ttu-id="12f97-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="12f97-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12f97-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="12f97-121">-Name</span></span>
<span data-ttu-id="12f97-122">Namnet på den dedikerade HSM som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="12f97-122">The name of the dedicated HSM to delete</span></span>

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

### <span data-ttu-id="12f97-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="12f97-123">-NoWait</span></span>
<span data-ttu-id="12f97-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="12f97-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="12f97-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12f97-125">-PassThru</span></span>
<span data-ttu-id="12f97-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="12f97-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="12f97-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12f97-127">-ResourceGroupName</span></span>
<span data-ttu-id="12f97-128">Namnet på resurs gruppen som den dedikerade HSM tillhör.</span><span class="sxs-lookup"><span data-stu-id="12f97-128">The name of the Resource Group to which the dedicated HSM belongs.</span></span>

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

### <span data-ttu-id="12f97-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="12f97-129">-SubscriptionId</span></span>
<span data-ttu-id="12f97-130">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="12f97-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="12f97-131">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="12f97-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="12f97-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="12f97-132">-Confirm</span></span>
<span data-ttu-id="12f97-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="12f97-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12f97-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12f97-134">-WhatIf</span></span>
<span data-ttu-id="12f97-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="12f97-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12f97-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="12f97-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12f97-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12f97-137">CommonParameters</span></span>
<span data-ttu-id="12f97-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12f97-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12f97-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12f97-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12f97-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12f97-140">INPUTS</span></span>

### <span data-ttu-id="12f97-141">Microsoft. Azure. PowerShell. cmdletar. DedicatedHsm. Models. IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="12f97-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="12f97-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12f97-142">OUTPUTS</span></span>

### <span data-ttu-id="12f97-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="12f97-143">System.Boolean</span></span>

## <span data-ttu-id="12f97-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12f97-144">NOTES</span></span>

<span data-ttu-id="12f97-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="12f97-145">ALIASES</span></span>

<span data-ttu-id="12f97-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="12f97-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="12f97-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="12f97-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="12f97-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="12f97-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="12f97-149">INPUTOBJECT <IDedicatedHsmIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="12f97-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="12f97-150">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="12f97-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="12f97-151">`[Name <String>]`: Namnet på den dedikerade HSM</span><span class="sxs-lookup"><span data-stu-id="12f97-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="12f97-152">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som resursen tillhör.</span><span class="sxs-lookup"><span data-stu-id="12f97-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="12f97-153">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="12f97-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="12f97-154">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="12f97-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="12f97-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12f97-155">RELATED LINKS</span></span>

