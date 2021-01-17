---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/update-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
ms.openlocfilehash: 5aa286eeedb08e6f582210d98a1d29bcd0074031
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388581"
---
# <span data-ttu-id="8a191-101">Update-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="8a191-101">Update-AzDedicatedHsm</span></span>

## <span data-ttu-id="8a191-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a191-102">SYNOPSIS</span></span>
<span data-ttu-id="8a191-103">Uppdatera en dedikerad HSM i det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8a191-103">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="8a191-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a191-104">SYNTAX</span></span>

### <span data-ttu-id="8a191-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="8a191-105">UpdateExpanded (Default)</span></span>
```
Update-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8a191-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8a191-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8a191-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a191-107">DESCRIPTION</span></span>
<span data-ttu-id="8a191-108">Uppdatera en dedikerad HSM i det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8a191-108">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="8a191-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a191-109">EXAMPLES</span></span>

### <span data-ttu-id="8a191-110">Exempel 1: uppdatera parameter tag gen för dedikerad HSM efter namn</span><span class="sxs-lookup"><span data-stu-id="8a191-110">Example 1: Update the parameter tag of the Dedicated HSM by name</span></span>
```powershell
PS C:\> Update-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="8a191-111">Det här kommandot uppdaterar parameter tag gen för dedicerad HSM efter namn</span><span class="sxs-lookup"><span data-stu-id="8a191-111">This command updates the parameter tag of the Dedicated HSM by name</span></span>

### <span data-ttu-id="8a191-112">Exempel 2: uppdatera parameter tag gen för dedicerad HSM efter objekt</span><span class="sxs-lookup"><span data-stu-id="8a191-112">Example 2: Update the parameter tag of the Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz 
PS C:\> Update-AzDedicatedHsm -InputObject -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="8a191-113">Det här kommandot uppdaterar parameter tag gen för dedicerad HSM efter objekt</span><span class="sxs-lookup"><span data-stu-id="8a191-113">This command updates the parameter tag of the Dedicated HSM by object</span></span>

## <span data-ttu-id="8a191-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a191-114">PARAMETERS</span></span>

### <span data-ttu-id="8a191-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a191-115">-AsJob</span></span>
<span data-ttu-id="8a191-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="8a191-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8a191-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a191-117">-DefaultProfile</span></span>
<span data-ttu-id="8a191-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8a191-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a191-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a191-119">-InputObject</span></span>
<span data-ttu-id="8a191-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="8a191-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a191-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="8a191-121">-Name</span></span>
<span data-ttu-id="8a191-122">Namn på dedikerad HSM</span><span class="sxs-lookup"><span data-stu-id="8a191-122">Name of the dedicated HSM</span></span>

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

### <span data-ttu-id="8a191-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="8a191-123">-NoWait</span></span>
<span data-ttu-id="8a191-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="8a191-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8a191-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a191-125">-ResourceGroupName</span></span>
<span data-ttu-id="8a191-126">Namnet på den resurs grupp som servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="8a191-126">The name of the Resource Group to which the server belongs.</span></span>

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

### <span data-ttu-id="8a191-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a191-127">-SubscriptionId</span></span>
<span data-ttu-id="8a191-128">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8a191-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8a191-129">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="8a191-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8a191-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="8a191-130">-Tag</span></span>
<span data-ttu-id="8a191-131">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="8a191-131">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a191-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8a191-132">-Confirm</span></span>
<span data-ttu-id="8a191-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8a191-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a191-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a191-134">-WhatIf</span></span>
<span data-ttu-id="8a191-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8a191-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a191-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8a191-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a191-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a191-137">CommonParameters</span></span>
<span data-ttu-id="8a191-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a191-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a191-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a191-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a191-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a191-140">INPUTS</span></span>

### <span data-ttu-id="8a191-141">Microsoft. Azure. PowerShell. cmdletar. DedicatedHsm. Models. IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="8a191-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="8a191-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a191-142">OUTPUTS</span></span>

### <span data-ttu-id="8a191-143">Microsoft. Azure. PowerShell. cmdletar. DedicatedHsm. Models. Api20181031. IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="8a191-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="8a191-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a191-144">NOTES</span></span>

<span data-ttu-id="8a191-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8a191-145">ALIASES</span></span>

<span data-ttu-id="8a191-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="8a191-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8a191-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="8a191-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8a191-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8a191-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8a191-149">INPUTOBJECT <IDedicatedHsmIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="8a191-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8a191-150">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="8a191-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8a191-151">`[Name <String>]`: Namnet på den dedikerade HSM</span><span class="sxs-lookup"><span data-stu-id="8a191-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="8a191-152">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som resursen tillhör.</span><span class="sxs-lookup"><span data-stu-id="8a191-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="8a191-153">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8a191-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8a191-154">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="8a191-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8a191-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a191-155">RELATED LINKS</span></span>

