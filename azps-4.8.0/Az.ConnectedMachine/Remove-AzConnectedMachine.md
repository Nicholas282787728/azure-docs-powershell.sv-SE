---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
ms.openlocfilehash: e8988f5dd6e2e37cc98c31ceab244693eae1941e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262823"
---
# <span data-ttu-id="41c84-101">Remove-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="41c84-101">Remove-AzConnectedMachine</span></span>

## <span data-ttu-id="41c84-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="41c84-102">SYNOPSIS</span></span>
<span data-ttu-id="41c84-103">Åtgärden för att ta bort en hybrid dator identitet i Azure.</span><span class="sxs-lookup"><span data-stu-id="41c84-103">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="41c84-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="41c84-104">SYNTAX</span></span>

### <span data-ttu-id="41c84-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="41c84-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="41c84-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="41c84-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachine -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="41c84-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="41c84-107">DESCRIPTION</span></span>
<span data-ttu-id="41c84-108">Åtgärden för att ta bort en hybrid dator identitet i Azure.</span><span class="sxs-lookup"><span data-stu-id="41c84-108">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="41c84-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="41c84-109">EXAMPLES</span></span>

### <span data-ttu-id="41c84-110">Exempel 1: ta bort en ansluten dator</span><span class="sxs-lookup"><span data-stu-id="41c84-110">Example 1: Remove a connected machine</span></span>
```powershell
PS C:\> Remove-AzConnectedMachine -Name myMachine -ResourceGroupName myRG

```

<span data-ttu-id="41c84-111">Tar bort den anslutna datorn.</span><span class="sxs-lookup"><span data-stu-id="41c84-111">Deletes the connected machine.</span></span>

### <span data-ttu-id="41c84-112">Exempel 2: ta bort anslutna maskiner via pipeline</span><span class="sxs-lookup"><span data-stu-id="41c84-112">Example 2: Remove connected machines via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines | Remove-AzConnectedMachine

```

<span data-ttu-id="41c84-113">Tar bort alla datorer i `contoso-connected-machines` resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="41c84-113">Removes all machines in the `contoso-connected-machines` resource group.</span></span>

## <span data-ttu-id="41c84-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="41c84-114">PARAMETERS</span></span>

### <span data-ttu-id="41c84-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41c84-115">-DefaultProfile</span></span>
<span data-ttu-id="41c84-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="41c84-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41c84-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41c84-117">-InputObject</span></span>
<span data-ttu-id="41c84-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="41c84-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41c84-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="41c84-119">-Name</span></span>
<span data-ttu-id="41c84-120">Namnet på Hybrid datorn.</span><span class="sxs-lookup"><span data-stu-id="41c84-120">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="41c84-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41c84-121">-PassThru</span></span>
<span data-ttu-id="41c84-122">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="41c84-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="41c84-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41c84-123">-ResourceGroupName</span></span>
<span data-ttu-id="41c84-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="41c84-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="41c84-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="41c84-125">-SubscriptionId</span></span>
<span data-ttu-id="41c84-126">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="41c84-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="41c84-127">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="41c84-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="41c84-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="41c84-128">-Confirm</span></span>
<span data-ttu-id="41c84-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="41c84-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41c84-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41c84-130">-WhatIf</span></span>
<span data-ttu-id="41c84-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="41c84-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41c84-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="41c84-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41c84-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41c84-133">CommonParameters</span></span>
<span data-ttu-id="41c84-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41c84-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41c84-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41c84-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41c84-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="41c84-136">INPUTS</span></span>

### <span data-ttu-id="41c84-137">Microsoft. Azure. PowerShell. cmdletar. ConnectedMachine. Models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="41c84-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="41c84-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="41c84-138">OUTPUTS</span></span>

### <span data-ttu-id="41c84-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="41c84-139">System.Boolean</span></span>

## <span data-ttu-id="41c84-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="41c84-140">NOTES</span></span>

<span data-ttu-id="41c84-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="41c84-141">ALIASES</span></span>

<span data-ttu-id="41c84-142">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="41c84-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="41c84-143">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="41c84-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="41c84-144">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="41c84-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="41c84-145">INPUTOBJECT <IConnectedMachineIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="41c84-145">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="41c84-146">`[ExtensionName <String>]`: Namnet på dator tillägget.</span><span class="sxs-lookup"><span data-stu-id="41c84-146">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="41c84-147">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="41c84-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="41c84-148">`[Name <String>]`: Hybrid datorns namn.</span><span class="sxs-lookup"><span data-stu-id="41c84-148">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="41c84-149">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="41c84-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="41c84-150">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="41c84-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="41c84-151">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="41c84-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="41c84-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="41c84-152">RELATED LINKS</span></span>

