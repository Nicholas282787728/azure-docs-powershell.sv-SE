---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/stop-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 3f98161e56019394dc67ab8909aac3fb70a611a2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419739"
---
# <span data-ttu-id="97dc5-101">Stop-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="97dc5-101">Stop-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="97dc5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="97dc5-102">SYNOPSIS</span></span>
<span data-ttu-id="97dc5-103">Stoppa distributionen.</span><span class="sxs-lookup"><span data-stu-id="97dc5-103">Stop the deployment.</span></span>

## <span data-ttu-id="97dc5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="97dc5-104">SYNTAX</span></span>

### <span data-ttu-id="97dc5-105">Stopp (standard)</span><span class="sxs-lookup"><span data-stu-id="97dc5-105">Stop (Default)</span></span>
```
Stop-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="97dc5-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="97dc5-106">StopViaIdentity</span></span>
```
Stop-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="97dc5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="97dc5-107">DESCRIPTION</span></span>
<span data-ttu-id="97dc5-108">Stoppa distributionen.</span><span class="sxs-lookup"><span data-stu-id="97dc5-108">Stop the deployment.</span></span>

## <span data-ttu-id="97dc5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="97dc5-109">EXAMPLES</span></span>

### <span data-ttu-id="97dc5-110">Exempel 1: stoppa vår moln tjänst efter namn.</span><span class="sxs-lookup"><span data-stu-id="97dc5-110">Example 1: Stop Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Stop-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="97dc5-111">Stoppa vår moln tjänst efter namn.</span><span class="sxs-lookup"><span data-stu-id="97dc5-111">Stop Spring Cloud Service by name.</span></span>

### <span data-ttu-id="97dc5-112">Exempel 2: stoppa vår moln tjänst från en pipe.</span><span class="sxs-lookup"><span data-stu-id="97dc5-112">Example 2: Stop Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Stop-AzSpringCloud
```

<span data-ttu-id="97dc5-113">Stoppa vår moln tjänst från en pipe.</span><span class="sxs-lookup"><span data-stu-id="97dc5-113">Stop Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="97dc5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="97dc5-114">PARAMETERS</span></span>

### <span data-ttu-id="97dc5-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="97dc5-115">-AppName</span></span>
<span data-ttu-id="97dc5-116">Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="97dc5-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97dc5-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97dc5-117">-AsJob</span></span>
<span data-ttu-id="97dc5-118">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="97dc5-118">Run the command as a job</span></span>

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

### <span data-ttu-id="97dc5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97dc5-119">-DefaultProfile</span></span>
<span data-ttu-id="97dc5-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="97dc5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97dc5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97dc5-121">-InputObject</span></span>
<span data-ttu-id="97dc5-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="97dc5-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97dc5-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="97dc5-123">-Name</span></span>
<span data-ttu-id="97dc5-124">Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="97dc5-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97dc5-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="97dc5-125">-NoWait</span></span>
<span data-ttu-id="97dc5-126">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="97dc5-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="97dc5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97dc5-127">-PassThru</span></span>
<span data-ttu-id="97dc5-128">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="97dc5-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="97dc5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97dc5-129">-ResourceGroupName</span></span>
<span data-ttu-id="97dc5-130">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="97dc5-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="97dc5-131">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="97dc5-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97dc5-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="97dc5-132">-ServiceName</span></span>
<span data-ttu-id="97dc5-133">Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="97dc5-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97dc5-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="97dc5-134">-SubscriptionId</span></span>
<span data-ttu-id="97dc5-135">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="97dc5-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="97dc5-136">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="97dc5-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97dc5-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="97dc5-137">-Confirm</span></span>
<span data-ttu-id="97dc5-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="97dc5-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97dc5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97dc5-139">-WhatIf</span></span>
<span data-ttu-id="97dc5-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="97dc5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97dc5-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="97dc5-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97dc5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97dc5-142">CommonParameters</span></span>
<span data-ttu-id="97dc5-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97dc5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97dc5-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97dc5-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97dc5-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="97dc5-145">INPUTS</span></span>

### <span data-ttu-id="97dc5-146">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="97dc5-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="97dc5-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="97dc5-147">OUTPUTS</span></span>

### <span data-ttu-id="97dc5-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="97dc5-148">System.Boolean</span></span>

## <span data-ttu-id="97dc5-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="97dc5-149">NOTES</span></span>

<span data-ttu-id="97dc5-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="97dc5-150">ALIASES</span></span>

<span data-ttu-id="97dc5-151">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="97dc5-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="97dc5-152">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="97dc5-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="97dc5-153">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="97dc5-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="97dc5-154">INPUTOBJECT <ISpringCloudIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="97dc5-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="97dc5-155">`[AppName <String>]`: Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="97dc5-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="97dc5-156">`[BindingName <String>]`: Namnet på bindnings resursen.</span><span class="sxs-lookup"><span data-stu-id="97dc5-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="97dc5-157">`[CertificateName <String>]`: Namnet på certifikat resursen.</span><span class="sxs-lookup"><span data-stu-id="97dc5-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="97dc5-158">`[DeploymentName <String>]`: Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="97dc5-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="97dc5-159">`[DomainName <String>]`: Namnet på den anpassade domän resursen.</span><span class="sxs-lookup"><span data-stu-id="97dc5-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="97dc5-160">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="97dc5-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="97dc5-161">`[Location <String>]`: regionen</span><span class="sxs-lookup"><span data-stu-id="97dc5-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="97dc5-162">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="97dc5-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="97dc5-163">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="97dc5-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="97dc5-164">`[ServiceName <String>]`: Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="97dc5-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="97dc5-165">`[SubscriptionId <String>]`: Hämtar prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="97dc5-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="97dc5-166">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="97dc5-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="97dc5-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="97dc5-167">RELATED LINKS</span></span>

