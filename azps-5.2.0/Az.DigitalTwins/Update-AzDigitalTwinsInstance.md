---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/update-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
ms.openlocfilehash: 4de7ab82f60c651e23565569ccf2cda7f4d949b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402403"
---
# <span data-ttu-id="e2ca4-101">Update-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="e2ca4-101">Update-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="e2ca4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e2ca4-102">SYNOPSIS</span></span>
<span data-ttu-id="e2ca4-103">Uppdatera metadata för DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e2ca4-103">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="e2ca4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e2ca4-104">SYNTAX</span></span>

### <span data-ttu-id="e2ca4-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="e2ca4-105">UpdateExpanded (Default)</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e2ca4-106">Uppdatera</span><span class="sxs-lookup"><span data-stu-id="e2ca4-106">Update</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e2ca4-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e2ca4-107">UpdateViaIdentity</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e2ca4-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e2ca4-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e2ca4-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e2ca4-109">DESCRIPTION</span></span>
<span data-ttu-id="e2ca4-110">Uppdatera metadata för DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e2ca4-110">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="e2ca4-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e2ca4-111">EXAMPLES</span></span>

### <span data-ttu-id="e2ca4-112">Exempel 1: UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="e2ca4-112">Example 1: UpdateExpanded (Default)</span></span>
```powershell
PS C:\> Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwinsTest -Tag @{“dtt”="001"}

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="e2ca4-113">Uppdatera angiven DigitalTwinsInstance med ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2ca4-113">Update the specified DigitalTwinsInstance by ResourceGroupName</span></span>

### <span data-ttu-id="e2ca4-114">Exempel 2: uppdatera AzDigitalTwinsInstance med en annan AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="e2ca4-114">Example 2: Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>
```powershell
PS C:\> $updateDigitalTwinInstance1 = Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwin1 -Tag @{"dtt"="002"}
Update-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest -DigitalTwinsPatchDescription $updateDigitalTwinInstance1

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="e2ca4-115">Uppdatera AzDigitalTwinsInstance av en annan AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="e2ca4-115">Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="e2ca4-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e2ca4-116">PARAMETERS</span></span>

### <span data-ttu-id="e2ca4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2ca4-117">-DefaultProfile</span></span>
<span data-ttu-id="e2ca4-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e2ca4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2ca4-119">-DigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="e2ca4-119">-DigitalTwinsPatchDescription</span></span>
<span data-ttu-id="e2ca4-120">Beskrivning av DigitalTwins-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e2ca4-120">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="e2ca4-121">För att konstruera kan du läsa avsnittet anteckningar för DIGITALTWINSPATCHDESCRIPTION-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e2ca4-121">To construct, see NOTES section for DIGITALTWINSPATCHDESCRIPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription
Parameter Sets: Update, UpdateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2ca4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2ca4-122">-InputObject</span></span>
<span data-ttu-id="e2ca4-123">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e2ca4-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: UpdateViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2ca4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2ca4-124">-ResourceGroupName</span></span>
<span data-ttu-id="e2ca4-125">Namnet på resurs gruppen som innehåller DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e2ca4-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2ca4-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e2ca4-126">-ResourceName</span></span>
<span data-ttu-id="e2ca4-127">Namnet på DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e2ca4-127">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2ca4-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e2ca4-128">-SubscriptionId</span></span>
<span data-ttu-id="e2ca4-129">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="e2ca4-129">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2ca4-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="e2ca4-130">-Tag</span></span>
<span data-ttu-id="e2ca4-131">Instanstaggar</span><span class="sxs-lookup"><span data-stu-id="e2ca4-131">Instance tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2ca4-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e2ca4-132">-Confirm</span></span>
<span data-ttu-id="e2ca4-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e2ca4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2ca4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2ca4-134">-WhatIf</span></span>
<span data-ttu-id="e2ca4-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e2ca4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2ca4-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e2ca4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2ca4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2ca4-137">CommonParameters</span></span>
<span data-ttu-id="e2ca4-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2ca4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2ca4-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2ca4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2ca4-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e2ca4-140">INPUTS</span></span>

### <span data-ttu-id="e2ca4-141">Microsoft. Azure. PowerShell. cmdletar. DigitalTwins. Models. Api20201031. IDigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="e2ca4-141">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription</span></span>

### <span data-ttu-id="e2ca4-142">Microsoft. Azure. PowerShell. cmdletar. DigitalTwins. Models. IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="e2ca4-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="e2ca4-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e2ca4-143">OUTPUTS</span></span>

### <span data-ttu-id="e2ca4-144">Microsoft. Azure. PowerShell. cmdletar. DigitalTwins. Models. Api20201031. IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="e2ca4-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="e2ca4-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e2ca4-145">NOTES</span></span>

<span data-ttu-id="e2ca4-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e2ca4-146">ALIASES</span></span>

<span data-ttu-id="e2ca4-147">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="e2ca4-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e2ca4-148">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="e2ca4-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e2ca4-149">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e2ca4-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e2ca4-150">DIGITALTWINSPATCHDESCRIPTION <IDigitalTwinsPatchDescription> : beskrivningen av DigitalTwins-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e2ca4-150">DIGITALTWINSPATCHDESCRIPTION <IDigitalTwinsPatchDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="e2ca4-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: Instanstaggar</span><span class="sxs-lookup"><span data-stu-id="e2ca4-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: Instance tags</span></span>
    - <span data-ttu-id="e2ca4-152">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="e2ca4-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="e2ca4-153">INPUTOBJECT <IDigitalTwinsIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="e2ca4-153">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e2ca4-154">`[EndpointName <String>]`: Slut punkts resursens namn.</span><span class="sxs-lookup"><span data-stu-id="e2ca4-154">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="e2ca4-155">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="e2ca4-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e2ca4-156">`[Location <String>]`: Plats för DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e2ca4-156">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="e2ca4-157">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e2ca4-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="e2ca4-158">`[ResourceName <String>]`: Namnet på DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e2ca4-158">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="e2ca4-159">`[SubscriptionId <String>]`: Prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="e2ca4-159">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="e2ca4-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e2ca4-160">RELATED LINKS</span></span>

