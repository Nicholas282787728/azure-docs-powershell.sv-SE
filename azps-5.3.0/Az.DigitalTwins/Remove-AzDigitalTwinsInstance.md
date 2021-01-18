---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/remove-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
ms.openlocfilehash: 495fecf922bc27eb43849b7ba6e44793c572b8cd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522641"
---
# <span data-ttu-id="267b7-101">Remove-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="267b7-101">Remove-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="267b7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="267b7-102">SYNOPSIS</span></span>
<span data-ttu-id="267b7-103">Ta bort en DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="267b7-103">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="267b7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="267b7-104">SYNTAX</span></span>

### <span data-ttu-id="267b7-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="267b7-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="267b7-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="267b7-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="267b7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="267b7-107">DESCRIPTION</span></span>
<span data-ttu-id="267b7-108">Ta bort en DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="267b7-108">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="267b7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="267b7-109">EXAMPLES</span></span>

### <span data-ttu-id="267b7-110">Exempel 1: ta bort ett AzDigitalTwinsInstance efter namn</span><span class="sxs-lookup"><span data-stu-id="267b7-110">Example 1: Remove an AzDigitalTwinsInstance by name</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin


```

<span data-ttu-id="267b7-111">Det här kommandot tar bort ett AzDigitalTwinsInstance efter namn</span><span class="sxs-lookup"><span data-stu-id="267b7-111">This command removes an AzDigitalTwinsInstance by name</span></span>

### <span data-ttu-id="267b7-112">Exempel 2: ta bort en AzDigitalTwinsInstance från InputObject</span><span class="sxs-lookup"><span data-stu-id="267b7-112">Example 2: Remove an AzDigitalTwinsInstance by InputObject</span></span>
```powershell
PS C:\> $GetAzDigitalTwins =  Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsInstance -InputObject $GetAzDigitalTwins


```

<span data-ttu-id="267b7-113">Det här kommandot tar bort ett AzDigitalTwinsInstance efter namn</span><span class="sxs-lookup"><span data-stu-id="267b7-113">This command removes an AzDigitalTwinsInstance by name</span></span>

## <span data-ttu-id="267b7-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="267b7-114">PARAMETERS</span></span>

### <span data-ttu-id="267b7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="267b7-115">-AsJob</span></span>
<span data-ttu-id="267b7-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="267b7-116">Run the command as a job</span></span>

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

### <span data-ttu-id="267b7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="267b7-117">-DefaultProfile</span></span>
<span data-ttu-id="267b7-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="267b7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="267b7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="267b7-119">-InputObject</span></span>
<span data-ttu-id="267b7-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="267b7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="267b7-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="267b7-121">-NoWait</span></span>
<span data-ttu-id="267b7-122">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="267b7-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="267b7-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="267b7-123">-PassThru</span></span>
<span data-ttu-id="267b7-124">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="267b7-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="267b7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="267b7-125">-ResourceGroupName</span></span>
<span data-ttu-id="267b7-126">Namnet på resurs gruppen som innehåller DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="267b7-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="267b7-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="267b7-127">-ResourceName</span></span>
<span data-ttu-id="267b7-128">Namnet på DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="267b7-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="267b7-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="267b7-129">-SubscriptionId</span></span>
<span data-ttu-id="267b7-130">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="267b7-130">The subscription identifier.</span></span>

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

### <span data-ttu-id="267b7-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="267b7-131">-Confirm</span></span>
<span data-ttu-id="267b7-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="267b7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="267b7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="267b7-133">-WhatIf</span></span>
<span data-ttu-id="267b7-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="267b7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="267b7-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="267b7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="267b7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="267b7-136">CommonParameters</span></span>
<span data-ttu-id="267b7-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="267b7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="267b7-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="267b7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="267b7-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="267b7-139">INPUTS</span></span>

### <span data-ttu-id="267b7-140">Microsoft. Azure. PowerShell. cmdletar. DigitalTwins. Models. IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="267b7-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="267b7-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="267b7-141">OUTPUTS</span></span>

### <span data-ttu-id="267b7-142">Microsoft. Azure. PowerShell. cmdletar. DigitalTwins. Models. Api20201031. IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="267b7-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="267b7-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="267b7-143">NOTES</span></span>

<span data-ttu-id="267b7-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="267b7-144">ALIASES</span></span>

<span data-ttu-id="267b7-145">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="267b7-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="267b7-146">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="267b7-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="267b7-147">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="267b7-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="267b7-148">INPUTOBJECT <IDigitalTwinsIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="267b7-148">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="267b7-149">`[EndpointName <String>]`: Slut punkts resursens namn.</span><span class="sxs-lookup"><span data-stu-id="267b7-149">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="267b7-150">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="267b7-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="267b7-151">`[Location <String>]`: Plats för DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="267b7-151">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="267b7-152">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="267b7-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="267b7-153">`[ResourceName <String>]`: Namnet på DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="267b7-153">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="267b7-154">`[SubscriptionId <String>]`: Prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="267b7-154">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="267b7-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="267b7-155">RELATED LINKS</span></span>

