---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 25b7b5c93f769982364a0df8f14f5fbe2f804fa2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419755"
---
# <span data-ttu-id="80525-101">Remove-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="80525-101">Remove-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="80525-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="80525-102">SYNOPSIS</span></span>
<span data-ttu-id="80525-103">Åtgärd för att ta bort en distribution.</span><span class="sxs-lookup"><span data-stu-id="80525-103">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="80525-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="80525-104">SYNTAX</span></span>

### <span data-ttu-id="80525-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="80525-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="80525-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="80525-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="80525-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="80525-107">DESCRIPTION</span></span>
<span data-ttu-id="80525-108">Åtgärd för att ta bort en distribution.</span><span class="sxs-lookup"><span data-stu-id="80525-108">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="80525-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="80525-109">EXAMPLES</span></span>

### <span data-ttu-id="80525-110">Exempel 1: ta bort vår moln distribution efter namn.</span><span class="sxs-lookup"><span data-stu-id="80525-110">Example 1: Remove Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="80525-111">Ta bort vår moln distribution efter namn.</span><span class="sxs-lookup"><span data-stu-id="80525-111">Remove Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="80525-112">Exempel 2: ta bort vår moln distribution från pipe.</span><span class="sxs-lookup"><span data-stu-id="80525-112">Example 2: Remove Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Remove-AzSpringCloudAppDeployment
```

<span data-ttu-id="80525-113">Ta bort vår moln distribution från pipe.</span><span class="sxs-lookup"><span data-stu-id="80525-113">Remove Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="80525-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="80525-114">PARAMETERS</span></span>

### <span data-ttu-id="80525-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="80525-115">-AppName</span></span>
<span data-ttu-id="80525-116">Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="80525-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="80525-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80525-117">-AsJob</span></span>
<span data-ttu-id="80525-118">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="80525-118">Run the command as a job</span></span>

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

### <span data-ttu-id="80525-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80525-119">-DefaultProfile</span></span>
<span data-ttu-id="80525-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="80525-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80525-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80525-121">-InputObject</span></span>
<span data-ttu-id="80525-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="80525-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="80525-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="80525-123">-Name</span></span>
<span data-ttu-id="80525-124">Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="80525-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80525-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="80525-125">-NoWait</span></span>
<span data-ttu-id="80525-126">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="80525-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="80525-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80525-127">-PassThru</span></span>
<span data-ttu-id="80525-128">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="80525-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="80525-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80525-129">-ResourceGroupName</span></span>
<span data-ttu-id="80525-130">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="80525-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="80525-131">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="80525-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="80525-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="80525-132">-ServiceName</span></span>
<span data-ttu-id="80525-133">Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="80525-133">The name of the Service resource.</span></span>

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

### <span data-ttu-id="80525-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80525-134">-SubscriptionId</span></span>
<span data-ttu-id="80525-135">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="80525-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="80525-136">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="80525-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="80525-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="80525-137">-Confirm</span></span>
<span data-ttu-id="80525-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="80525-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80525-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80525-139">-WhatIf</span></span>
<span data-ttu-id="80525-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="80525-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80525-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="80525-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80525-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80525-142">CommonParameters</span></span>
<span data-ttu-id="80525-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80525-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80525-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80525-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80525-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="80525-145">INPUTS</span></span>

### <span data-ttu-id="80525-146">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="80525-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="80525-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="80525-147">OUTPUTS</span></span>

### <span data-ttu-id="80525-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="80525-148">System.Boolean</span></span>

## <span data-ttu-id="80525-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="80525-149">NOTES</span></span>

<span data-ttu-id="80525-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="80525-150">ALIASES</span></span>

<span data-ttu-id="80525-151">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="80525-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="80525-152">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="80525-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="80525-153">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="80525-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="80525-154">INPUTOBJECT <ISpringCloudIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="80525-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="80525-155">`[AppName <String>]`: Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="80525-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="80525-156">`[BindingName <String>]`: Namnet på bindnings resursen.</span><span class="sxs-lookup"><span data-stu-id="80525-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="80525-157">`[CertificateName <String>]`: Namnet på certifikat resursen.</span><span class="sxs-lookup"><span data-stu-id="80525-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="80525-158">`[DeploymentName <String>]`: Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="80525-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="80525-159">`[DomainName <String>]`: Namnet på den anpassade domän resursen.</span><span class="sxs-lookup"><span data-stu-id="80525-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="80525-160">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="80525-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="80525-161">`[Location <String>]`: regionen</span><span class="sxs-lookup"><span data-stu-id="80525-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="80525-162">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="80525-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="80525-163">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="80525-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="80525-164">`[ServiceName <String>]`: Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="80525-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="80525-165">`[SubscriptionId <String>]`: Hämtar prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="80525-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="80525-166">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="80525-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="80525-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="80525-167">RELATED LINKS</span></span>

