---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/remove-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
ms.openlocfilehash: c165f9d69b18631f53bdc9444a623f43599532fa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527060"
---
# <span data-ttu-id="0341d-101">Remove-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="0341d-101">Remove-AzCommunicationService</span></span>

## <span data-ttu-id="0341d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0341d-102">SYNOPSIS</span></span>
<span data-ttu-id="0341d-103">Åtgärd för att ta bort en CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="0341d-103">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="0341d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0341d-104">SYNTAX</span></span>

### <span data-ttu-id="0341d-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="0341d-105">Delete (Default)</span></span>
```
Remove-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0341d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0341d-106">DeleteViaIdentity</span></span>
```
Remove-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0341d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0341d-107">DESCRIPTION</span></span>
<span data-ttu-id="0341d-108">Åtgärd för att ta bort en CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="0341d-108">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="0341d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0341d-109">EXAMPLES</span></span>

### <span data-ttu-id="0341d-110">Exempel 1: ta bort den angivna Azure Communication-resursen</span><span class="sxs-lookup"><span data-stu-id="0341d-110">Example 1: Remove the specified Azure Communication resource</span></span>
```powershell
PS C:\> Remove-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1
```

<span data-ttu-id="0341d-111">Ta bort/ta bort Azure Communication-resursen.</span><span class="sxs-lookup"><span data-stu-id="0341d-111">Remove / Delete the Azure Communication resource.</span></span>

## <span data-ttu-id="0341d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0341d-112">PARAMETERS</span></span>

### <span data-ttu-id="0341d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0341d-113">-AsJob</span></span>
<span data-ttu-id="0341d-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="0341d-114">Run the command as a job</span></span>

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

### <span data-ttu-id="0341d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0341d-115">-DefaultProfile</span></span>
<span data-ttu-id="0341d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0341d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0341d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0341d-117">-InputObject</span></span>
<span data-ttu-id="0341d-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="0341d-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0341d-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="0341d-119">-Name</span></span>
<span data-ttu-id="0341d-120">Namnet på CommunicationService-resursen.</span><span class="sxs-lookup"><span data-stu-id="0341d-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0341d-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="0341d-121">-NoWait</span></span>
<span data-ttu-id="0341d-122">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="0341d-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0341d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0341d-123">-PassThru</span></span>
<span data-ttu-id="0341d-124">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="0341d-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0341d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0341d-125">-ResourceGroupName</span></span>
<span data-ttu-id="0341d-126">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="0341d-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="0341d-127">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="0341d-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="0341d-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0341d-128">-SubscriptionId</span></span>
<span data-ttu-id="0341d-129">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0341d-129">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="0341d-130">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="0341d-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0341d-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0341d-131">-Confirm</span></span>
<span data-ttu-id="0341d-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0341d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0341d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0341d-133">-WhatIf</span></span>
<span data-ttu-id="0341d-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0341d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0341d-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0341d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0341d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0341d-136">CommonParameters</span></span>
<span data-ttu-id="0341d-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0341d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0341d-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0341d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0341d-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0341d-139">INPUTS</span></span>

### <span data-ttu-id="0341d-140">Microsoft. Azure. PowerShell. cmdletar. Communication. Models. ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="0341d-140">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="0341d-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0341d-141">OUTPUTS</span></span>

### <span data-ttu-id="0341d-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0341d-142">System.Boolean</span></span>

## <span data-ttu-id="0341d-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0341d-143">NOTES</span></span>

<span data-ttu-id="0341d-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0341d-144">ALIASES</span></span>

<span data-ttu-id="0341d-145">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="0341d-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0341d-146">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="0341d-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0341d-147">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0341d-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0341d-148">INPUTOBJECT <ICommunicationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="0341d-148">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0341d-149">`[CommunicationServiceName <String>]`: Namnet på CommunicationService-resursen.</span><span class="sxs-lookup"><span data-stu-id="0341d-149">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="0341d-150">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="0341d-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0341d-151">`[Location <String>]`: Azure-regionen</span><span class="sxs-lookup"><span data-stu-id="0341d-151">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="0341d-152">`[OperationId <String>]`: ID för pågående asynkron åtgärd</span><span class="sxs-lookup"><span data-stu-id="0341d-152">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="0341d-153">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="0341d-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="0341d-154">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="0341d-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="0341d-155">`[SubscriptionId <String>]`: Hämtar prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0341d-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="0341d-156">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="0341d-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0341d-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0341d-157">RELATED LINKS</span></span>

