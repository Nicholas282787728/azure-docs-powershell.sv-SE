---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/start-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Start-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Start-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 7cab91bf5c7e95258f17a73da4e2b177e30444c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94262946"
---
# <span data-ttu-id="cb1e9-101">Start-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="cb1e9-101">Start-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="cb1e9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cb1e9-102">SYNOPSIS</span></span>
<span data-ttu-id="cb1e9-103">Starta distributionen.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-103">Start the deployment.</span></span>

## <span data-ttu-id="cb1e9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cb1e9-104">SYNTAX</span></span>

### <span data-ttu-id="cb1e9-105">Start (standard)</span><span class="sxs-lookup"><span data-stu-id="cb1e9-105">Start (Default)</span></span>
```
Start-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cb1e9-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cb1e9-106">StartViaIdentity</span></span>
```
Start-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cb1e9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cb1e9-107">DESCRIPTION</span></span>
<span data-ttu-id="cb1e9-108">Starta distributionen.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-108">Start the deployment.</span></span>

## <span data-ttu-id="cb1e9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cb1e9-109">EXAMPLES</span></span>

### <span data-ttu-id="cb1e9-110">Exempel 1: starta våren Cloud service med namn.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-110">Example 1: Start Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Start-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="cb1e9-111">Starta vår moln tjänst efter namn.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-111">Start Spring Cloud Service by name.</span></span>

### <span data-ttu-id="cb1e9-112">Exempel 2: starta vår moln tjänst från en pipe.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-112">Example 2: Start Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Start-AzSpringCloud
```

<span data-ttu-id="cb1e9-113">Starta vår moln tjänst från en pipe.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-113">Start Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="cb1e9-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cb1e9-114">PARAMETERS</span></span>

### <span data-ttu-id="cb1e9-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="cb1e9-115">-AppName</span></span>
<span data-ttu-id="cb1e9-116">Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb1e9-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb1e9-117">-AsJob</span></span>
<span data-ttu-id="cb1e9-118">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="cb1e9-118">Run the command as a job</span></span>

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

### <span data-ttu-id="cb1e9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb1e9-119">-DefaultProfile</span></span>
<span data-ttu-id="cb1e9-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb1e9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb1e9-121">-InputObject</span></span>
<span data-ttu-id="cb1e9-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb1e9-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="cb1e9-123">-Name</span></span>
<span data-ttu-id="cb1e9-124">Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb1e9-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="cb1e9-125">-NoWait</span></span>
<span data-ttu-id="cb1e9-126">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="cb1e9-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cb1e9-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb1e9-127">-PassThru</span></span>
<span data-ttu-id="cb1e9-128">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="cb1e9-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cb1e9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb1e9-129">-ResourceGroupName</span></span>
<span data-ttu-id="cb1e9-130">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="cb1e9-131">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb1e9-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cb1e9-132">-ServiceName</span></span>
<span data-ttu-id="cb1e9-133">Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb1e9-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb1e9-134">-SubscriptionId</span></span>
<span data-ttu-id="cb1e9-135">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="cb1e9-136">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb1e9-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cb1e9-137">-Confirm</span></span>
<span data-ttu-id="cb1e9-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb1e9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb1e9-139">-WhatIf</span></span>
<span data-ttu-id="cb1e9-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb1e9-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb1e9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb1e9-142">CommonParameters</span></span>
<span data-ttu-id="cb1e9-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb1e9-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb1e9-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb1e9-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cb1e9-145">INPUTS</span></span>

### <span data-ttu-id="cb1e9-146">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="cb1e9-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="cb1e9-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cb1e9-147">OUTPUTS</span></span>

### <span data-ttu-id="cb1e9-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cb1e9-148">System.Boolean</span></span>

## <span data-ttu-id="cb1e9-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cb1e9-149">NOTES</span></span>

<span data-ttu-id="cb1e9-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cb1e9-150">ALIASES</span></span>

<span data-ttu-id="cb1e9-151">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="cb1e9-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cb1e9-152">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cb1e9-153">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cb1e9-154">INPUTOBJECT <ISpringCloudIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="cb1e9-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cb1e9-155">`[AppName <String>]`: Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="cb1e9-156">`[BindingName <String>]`: Namnet på bindnings resursen.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="cb1e9-157">`[CertificateName <String>]`: Namnet på certifikat resursen.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="cb1e9-158">`[DeploymentName <String>]`: Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="cb1e9-159">`[DomainName <String>]`: Namnet på den anpassade domän resursen.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="cb1e9-160">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="cb1e9-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cb1e9-161">`[Location <String>]`: regionen</span><span class="sxs-lookup"><span data-stu-id="cb1e9-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="cb1e9-162">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="cb1e9-163">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="cb1e9-164">`[ServiceName <String>]`: Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="cb1e9-165">`[SubscriptionId <String>]`: Hämtar prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="cb1e9-166">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="cb1e9-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cb1e9-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cb1e9-167">RELATED LINKS</span></span>
