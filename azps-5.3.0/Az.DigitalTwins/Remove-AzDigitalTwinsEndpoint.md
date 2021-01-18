---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/remove-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 1c740134cb2613a8efcd950fec4cd780f4f443cf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520880"
---
# <span data-ttu-id="e048b-101">Remove-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="e048b-101">Remove-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="e048b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e048b-102">SYNOPSIS</span></span>
<span data-ttu-id="e048b-103">Ta bort en DigitalTwinsInstance slut punkt.</span><span class="sxs-lookup"><span data-stu-id="e048b-103">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="e048b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e048b-104">SYNTAX</span></span>

### <span data-ttu-id="e048b-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="e048b-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e048b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e048b-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e048b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e048b-107">DESCRIPTION</span></span>
<span data-ttu-id="e048b-108">Ta bort en DigitalTwinsInstance slut punkt.</span><span class="sxs-lookup"><span data-stu-id="e048b-108">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="e048b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e048b-109">EXAMPLES</span></span>

### <span data-ttu-id="e048b-110">Exempel 1: ta bort azDigitalTwinsEndPoint med EndPointName</span><span class="sxs-lookup"><span data-stu-id="e048b-110">Example 1: Delete the azDigitalTwinsEndPoint by EndPointName</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -EndpointName youriEHEndpoint -ResourceName youriDigitalTwinsTest

```

<span data-ttu-id="e048b-111">Ta bort azDigitalTwinsEndPoint via EndPointName ResourceGroupName och ResourceName</span><span class="sxs-lookup"><span data-stu-id="e048b-111">Delete the azDigitalTwinsEndPoint by EndPointName ResourceGroupName and ResourceName</span></span>

### <span data-ttu-id="e048b-112">Exempel 2: ta bort azDigitalTwinsEndPoint efter objekt</span><span class="sxs-lookup"><span data-stu-id="e048b-112">Example 2: Delete the azDigitalTwinsEndPoint by Object</span></span>
```powershell
PS C:\> $GetAzdigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriEHEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsEndpoint -InputObject $GetAzdigitalTwinsEndpoint

```

<span data-ttu-id="e048b-113">Ta bort azDigitalTwinsEndPoint efter objekt</span><span class="sxs-lookup"><span data-stu-id="e048b-113">Delete the azDigitalTwinsEndPoint by Object</span></span>

## <span data-ttu-id="e048b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e048b-114">PARAMETERS</span></span>

### <span data-ttu-id="e048b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e048b-115">-AsJob</span></span>
<span data-ttu-id="e048b-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="e048b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e048b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e048b-117">-DefaultProfile</span></span>
<span data-ttu-id="e048b-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e048b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e048b-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e048b-119">-EndpointName</span></span>
<span data-ttu-id="e048b-120">Namn på slut punkts resurs.</span><span class="sxs-lookup"><span data-stu-id="e048b-120">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="e048b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e048b-121">-InputObject</span></span>
<span data-ttu-id="e048b-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e048b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e048b-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e048b-123">-NoWait</span></span>
<span data-ttu-id="e048b-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="e048b-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e048b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e048b-125">-PassThru</span></span>
<span data-ttu-id="e048b-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="e048b-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e048b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e048b-127">-ResourceGroupName</span></span>
<span data-ttu-id="e048b-128">Namnet på resurs gruppen som innehåller DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e048b-128">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="e048b-129">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e048b-129">-ResourceName</span></span>
<span data-ttu-id="e048b-130">Namnet på DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e048b-130">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="e048b-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e048b-131">-SubscriptionId</span></span>
<span data-ttu-id="e048b-132">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="e048b-132">The subscription identifier.</span></span>

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

### <span data-ttu-id="e048b-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e048b-133">-Confirm</span></span>
<span data-ttu-id="e048b-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e048b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e048b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e048b-135">-WhatIf</span></span>
<span data-ttu-id="e048b-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e048b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e048b-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e048b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e048b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e048b-138">CommonParameters</span></span>
<span data-ttu-id="e048b-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e048b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e048b-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e048b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e048b-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e048b-141">INPUTS</span></span>

### <span data-ttu-id="e048b-142">Microsoft. Azure. PowerShell. cmdletar. DigitalTwins. Models. IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="e048b-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="e048b-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e048b-143">OUTPUTS</span></span>

### <span data-ttu-id="e048b-144">Microsoft. Azure. PowerShell. cmdletar. DigitalTwins. Models. Api20201031. IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="e048b-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="e048b-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e048b-145">NOTES</span></span>

<span data-ttu-id="e048b-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e048b-146">ALIASES</span></span>

<span data-ttu-id="e048b-147">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="e048b-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e048b-148">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="e048b-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e048b-149">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e048b-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e048b-150">INPUTOBJECT <IDigitalTwinsIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="e048b-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e048b-151">`[EndpointName <String>]`: Slut punkts resursens namn.</span><span class="sxs-lookup"><span data-stu-id="e048b-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="e048b-152">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="e048b-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e048b-153">`[Location <String>]`: Plats för DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e048b-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="e048b-154">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e048b-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="e048b-155">`[ResourceName <String>]`: Namnet på DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e048b-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="e048b-156">`[SubscriptionId <String>]`: Prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="e048b-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="e048b-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e048b-157">RELATED LINKS</span></span>

