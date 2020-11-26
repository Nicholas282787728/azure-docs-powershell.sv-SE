---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
ms.openlocfilehash: 913011a9230b70c59b772eae306913c1e1e87432
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261655"
---
# <span data-ttu-id="8f3eb-101">Remove-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="8f3eb-101">Remove-AzSpringCloud</span></span>

## <span data-ttu-id="8f3eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8f3eb-102">SYNOPSIS</span></span>
<span data-ttu-id="8f3eb-103">Åtgärd för att ta bort en tjänst.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-103">Operation to delete a Service.</span></span>

## <span data-ttu-id="8f3eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8f3eb-104">SYNTAX</span></span>

### <span data-ttu-id="8f3eb-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="8f3eb-105">Delete (Default)</span></span>
```
Remove-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8f3eb-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8f3eb-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8f3eb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8f3eb-107">DESCRIPTION</span></span>
<span data-ttu-id="8f3eb-108">Åtgärd för att ta bort en tjänst.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-108">Operation to delete a Service.</span></span>

## <span data-ttu-id="8f3eb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8f3eb-109">EXAMPLES</span></span>

### <span data-ttu-id="8f3eb-110">Exempel 1: ta bort våren Cloud service med namn.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-110">Example 1: Remove Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
```

<span data-ttu-id="8f3eb-111">Ta bort vår moln tjänst efter namn.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-111">Remove Spring Cloud Service by name.</span></span>

### <span data-ttu-id="8f3eb-112">Exempel 2: ta bort vår moln tjänst från en pipe.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-112">Example 2: Remove Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Remove-AzSpringCloud
```

<span data-ttu-id="8f3eb-113">Ta bort vår moln tjänst från en pipe.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-113">Remove Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="8f3eb-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8f3eb-114">PARAMETERS</span></span>

### <span data-ttu-id="8f3eb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f3eb-115">-AsJob</span></span>
<span data-ttu-id="8f3eb-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="8f3eb-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8f3eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f3eb-117">-DefaultProfile</span></span>
<span data-ttu-id="8f3eb-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f3eb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f3eb-119">-InputObject</span></span>
<span data-ttu-id="8f3eb-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f3eb-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="8f3eb-121">-Name</span></span>
<span data-ttu-id="8f3eb-122">Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-122">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3eb-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="8f3eb-123">-NoWait</span></span>
<span data-ttu-id="8f3eb-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="8f3eb-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8f3eb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f3eb-125">-PassThru</span></span>
<span data-ttu-id="8f3eb-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="8f3eb-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8f3eb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f3eb-127">-ResourceGroupName</span></span>
<span data-ttu-id="8f3eb-128">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8f3eb-129">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8f3eb-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8f3eb-130">-SubscriptionId</span></span>
<span data-ttu-id="8f3eb-131">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="8f3eb-132">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8f3eb-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8f3eb-133">-Confirm</span></span>
<span data-ttu-id="8f3eb-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f3eb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f3eb-135">-WhatIf</span></span>
<span data-ttu-id="8f3eb-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f3eb-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f3eb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f3eb-138">CommonParameters</span></span>
<span data-ttu-id="8f3eb-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f3eb-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f3eb-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f3eb-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8f3eb-141">INPUTS</span></span>

### <span data-ttu-id="8f3eb-142">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="8f3eb-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="8f3eb-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8f3eb-143">OUTPUTS</span></span>

### <span data-ttu-id="8f3eb-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8f3eb-144">System.Boolean</span></span>

## <span data-ttu-id="8f3eb-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8f3eb-145">NOTES</span></span>

<span data-ttu-id="8f3eb-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8f3eb-146">ALIASES</span></span>

<span data-ttu-id="8f3eb-147">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="8f3eb-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8f3eb-148">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8f3eb-149">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8f3eb-150">INPUTOBJECT <ISpringCloudIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="8f3eb-150">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8f3eb-151">`[AppName <String>]`: Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-151">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="8f3eb-152">`[BindingName <String>]`: Namnet på bindnings resursen.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-152">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="8f3eb-153">`[CertificateName <String>]`: Namnet på certifikat resursen.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-153">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="8f3eb-154">`[DeploymentName <String>]`: Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-154">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="8f3eb-155">`[DomainName <String>]`: Namnet på den anpassade domän resursen.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-155">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="8f3eb-156">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="8f3eb-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8f3eb-157">`[Location <String>]`: regionen</span><span class="sxs-lookup"><span data-stu-id="8f3eb-157">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="8f3eb-158">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-158">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="8f3eb-159">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-159">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="8f3eb-160">`[ServiceName <String>]`: Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-160">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="8f3eb-161">`[SubscriptionId <String>]`: Hämtar prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="8f3eb-162">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-162">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8f3eb-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8f3eb-163">RELATED LINKS</span></span>
