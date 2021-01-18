---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/update-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
ms.openlocfilehash: 717c0981397ecbf419edbaa9f62bcc66443946fc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527051"
---
# <span data-ttu-id="50628-101">Update-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="50628-101">Update-AzCommunicationService</span></span>

## <span data-ttu-id="50628-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50628-102">SYNOPSIS</span></span>
<span data-ttu-id="50628-103">Åtgärd för att uppdatera en befintlig CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="50628-103">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="50628-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50628-104">SYNTAX</span></span>

### <span data-ttu-id="50628-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="50628-105">UpdateExpanded (Default)</span></span>
```
Update-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="50628-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="50628-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzCommunicationService -InputObject <ICommunicationIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="50628-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50628-107">DESCRIPTION</span></span>
<span data-ttu-id="50628-108">Åtgärd för att uppdatera en befintlig CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="50628-108">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="50628-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50628-109">EXAMPLES</span></span>

### <span data-ttu-id="50628-110">Exempel 1: uppdatera en befintlig ACS-resurs som innehåller Taggar</span><span class="sxs-lookup"><span data-stu-id="50628-110">Example 1: Update an existing ACS resource to have tags</span></span>
```powershell
PS C:\> Update-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Tag @{ExampleKey1="ExampleValue1"}

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="50628-111">Bifogar angivna taggar till den angivna ACS-resursen.</span><span class="sxs-lookup"><span data-stu-id="50628-111">Attaches the given tags to the specified ACS resource.</span></span>

## <span data-ttu-id="50628-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50628-112">PARAMETERS</span></span>

### <span data-ttu-id="50628-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50628-113">-DefaultProfile</span></span>
<span data-ttu-id="50628-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="50628-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50628-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50628-115">-InputObject</span></span>
<span data-ttu-id="50628-116">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="50628-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50628-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="50628-117">-Name</span></span>
<span data-ttu-id="50628-118">Namnet på CommunicationService-resursen.</span><span class="sxs-lookup"><span data-stu-id="50628-118">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50628-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50628-119">-ResourceGroupName</span></span>
<span data-ttu-id="50628-120">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="50628-120">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="50628-121">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="50628-121">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="50628-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="50628-122">-SubscriptionId</span></span>
<span data-ttu-id="50628-123">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="50628-123">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="50628-124">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="50628-124">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="50628-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="50628-125">-Tag</span></span>
<span data-ttu-id="50628-126">Taggar för tjänsten som är en lista över de värde par som beskriver resursen.</span><span class="sxs-lookup"><span data-stu-id="50628-126">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="50628-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="50628-127">-Confirm</span></span>
<span data-ttu-id="50628-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="50628-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50628-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50628-129">-WhatIf</span></span>
<span data-ttu-id="50628-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="50628-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50628-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="50628-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50628-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50628-132">CommonParameters</span></span>
<span data-ttu-id="50628-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50628-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50628-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50628-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50628-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50628-135">INPUTS</span></span>

### <span data-ttu-id="50628-136">Microsoft. Azure. PowerShell. cmdletar. Communication. Models. ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="50628-136">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="50628-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50628-137">OUTPUTS</span></span>

### <span data-ttu-id="50628-138">Microsoft. Azure. PowerShell. cmdletar. Communication. Models. Api20200820Preview. ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="50628-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="50628-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50628-139">NOTES</span></span>

<span data-ttu-id="50628-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="50628-140">ALIASES</span></span>

<span data-ttu-id="50628-141">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="50628-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="50628-142">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="50628-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="50628-143">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="50628-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="50628-144">INPUTOBJECT <ICommunicationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="50628-144">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="50628-145">`[CommunicationServiceName <String>]`: Namnet på CommunicationService-resursen.</span><span class="sxs-lookup"><span data-stu-id="50628-145">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="50628-146">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="50628-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="50628-147">`[Location <String>]`: Azure-regionen</span><span class="sxs-lookup"><span data-stu-id="50628-147">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="50628-148">`[OperationId <String>]`: ID för pågående asynkron åtgärd</span><span class="sxs-lookup"><span data-stu-id="50628-148">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="50628-149">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="50628-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="50628-150">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="50628-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="50628-151">`[SubscriptionId <String>]`: Hämtar prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="50628-151">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="50628-152">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="50628-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="50628-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50628-153">RELATED LINKS</span></span>

