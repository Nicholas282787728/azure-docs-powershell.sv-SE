---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: ba31f4d7c81392a30f4f8b9073d967b2a57cfab7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419712"
---
# <span data-ttu-id="c3478-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="c3478-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="c3478-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3478-102">SYNOPSIS</span></span>
<span data-ttu-id="c3478-103">Åtgärd för att uppdatera en avsluta distribution.</span><span class="sxs-lookup"><span data-stu-id="c3478-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="c3478-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3478-104">SYNTAX</span></span>

### <span data-ttu-id="c3478-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="c3478-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c3478-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c3478-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c3478-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3478-107">DESCRIPTION</span></span>
<span data-ttu-id="c3478-108">Åtgärd för att uppdatera en avsluta distribution.</span><span class="sxs-lookup"><span data-stu-id="c3478-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="c3478-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3478-109">EXAMPLES</span></span>

### <span data-ttu-id="c3478-110">Exempel 1: uppdatera vår moln distribution efter namn.</span><span class="sxs-lookup"><span data-stu-id="c3478-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default -SourceRelativePath resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
Active                               : True
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-fb79b6b5d-kvmpz}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="c3478-111">Uppdatera vår moln distribution efter namn.</span><span class="sxs-lookup"><span data-stu-id="c3478-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="c3478-112">Exempel 2: uppdatera vår moln distribution från en pipe.</span><span class="sxs-lookup"><span data-stu-id="c3478-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Update-AzSpringCloudAppDeployment -SourceRelativePath resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
Active                               : True
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-fb79b6b5d-kvmpz}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="c3478-113">Uppdatera vår moln distribution från pipe.</span><span class="sxs-lookup"><span data-stu-id="c3478-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="c3478-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3478-114">PARAMETERS</span></span>

### <span data-ttu-id="c3478-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="c3478-115">-AppName</span></span>
<span data-ttu-id="c3478-116">Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="c3478-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="c3478-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3478-117">-AsJob</span></span>
<span data-ttu-id="c3478-118">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="c3478-118">Run the command as a job</span></span>

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

### <span data-ttu-id="c3478-119">-CPU</span><span class="sxs-lookup"><span data-stu-id="c3478-119">-Cpu</span></span>
<span data-ttu-id="c3478-120">Nödvändig processor</span><span class="sxs-lookup"><span data-stu-id="c3478-120">Required CPU</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3478-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3478-121">-DefaultProfile</span></span>
<span data-ttu-id="c3478-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c3478-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3478-123">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="c3478-123">-EnvironmentVariable</span></span>
<span data-ttu-id="c3478-124">Uppsättning miljövariabler</span><span class="sxs-lookup"><span data-stu-id="c3478-124">Collection of environment variables</span></span>

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

### <span data-ttu-id="c3478-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3478-125">-InputObject</span></span>
<span data-ttu-id="c3478-126">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="c3478-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3478-127">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="c3478-127">-JvmOption</span></span>
<span data-ttu-id="c3478-128">Parametern JVM</span><span class="sxs-lookup"><span data-stu-id="c3478-128">JVM parameter</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3478-129">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="c3478-129">-MemoryInGb</span></span>
<span data-ttu-id="c3478-130">Nödvändig minnes storlek i GB</span><span class="sxs-lookup"><span data-stu-id="c3478-130">Required Memory size in GB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3478-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="c3478-131">-Name</span></span>
<span data-ttu-id="c3478-132">Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="c3478-132">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3478-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c3478-133">-NoWait</span></span>
<span data-ttu-id="c3478-134">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="c3478-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c3478-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3478-135">-ResourceGroupName</span></span>
<span data-ttu-id="c3478-136">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="c3478-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c3478-137">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="c3478-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c3478-138">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="c3478-138">-RuntimeVersion</span></span>
<span data-ttu-id="c3478-139">Kör tids version</span><span class="sxs-lookup"><span data-stu-id="c3478-139">Runtime version</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Support.RuntimeVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3478-140">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c3478-140">-ServiceName</span></span>
<span data-ttu-id="c3478-141">Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="c3478-141">The name of the Service resource.</span></span>

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

### <span data-ttu-id="c3478-142">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="c3478-142">-SourceArtifactSelector</span></span>
<span data-ttu-id="c3478-143">Väljaren för den artefakt som ska användas för distribution av projekt med flera moduler.</span><span class="sxs-lookup"><span data-stu-id="c3478-143">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="c3478-144">Det här ska Bethe relativa sökvägen till målobjektet/projektet.</span><span class="sxs-lookup"><span data-stu-id="c3478-144">This should bethe relative path to the target module/project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3478-145">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="c3478-145">-SourceRelativePath</span></span>
<span data-ttu-id="c3478-146">Relativ sökväg för lagrings platsen som innehåller källan</span><span class="sxs-lookup"><span data-stu-id="c3478-146">Relative path of the storage which stores the source</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3478-147">-SourceType</span><span class="sxs-lookup"><span data-stu-id="c3478-147">-SourceType</span></span>
<span data-ttu-id="c3478-148">Typ av källa som laddats upp</span><span class="sxs-lookup"><span data-stu-id="c3478-148">Type of the source uploaded</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Support.UserSourceType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3478-149">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="c3478-149">-SourceVersion</span></span>
<span data-ttu-id="c3478-150">Version av källan</span><span class="sxs-lookup"><span data-stu-id="c3478-150">Version of the source</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3478-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c3478-151">-SubscriptionId</span></span>
<span data-ttu-id="c3478-152">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c3478-152">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c3478-153">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="c3478-153">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c3478-154">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c3478-154">-Confirm</span></span>
<span data-ttu-id="c3478-155">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c3478-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3478-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3478-156">-WhatIf</span></span>
<span data-ttu-id="c3478-157">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c3478-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3478-158">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c3478-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3478-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3478-159">CommonParameters</span></span>
<span data-ttu-id="c3478-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3478-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3478-161">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3478-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3478-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3478-162">INPUTS</span></span>

### <span data-ttu-id="c3478-163">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="c3478-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="c3478-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3478-164">OUTPUTS</span></span>

### <span data-ttu-id="c3478-165">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. Api20200701. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="c3478-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="c3478-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3478-166">NOTES</span></span>

<span data-ttu-id="c3478-167">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c3478-167">ALIASES</span></span>

<span data-ttu-id="c3478-168">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="c3478-168">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c3478-169">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="c3478-169">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c3478-170">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c3478-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c3478-171">INPUTOBJECT <ISpringCloudIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="c3478-171">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c3478-172">`[AppName <String>]`: Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="c3478-172">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="c3478-173">`[BindingName <String>]`: Namnet på bindnings resursen.</span><span class="sxs-lookup"><span data-stu-id="c3478-173">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="c3478-174">`[CertificateName <String>]`: Namnet på certifikat resursen.</span><span class="sxs-lookup"><span data-stu-id="c3478-174">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="c3478-175">`[DeploymentName <String>]`: Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="c3478-175">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="c3478-176">`[DomainName <String>]`: Namnet på den anpassade domän resursen.</span><span class="sxs-lookup"><span data-stu-id="c3478-176">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="c3478-177">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="c3478-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c3478-178">`[Location <String>]`: regionen</span><span class="sxs-lookup"><span data-stu-id="c3478-178">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="c3478-179">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="c3478-179">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="c3478-180">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="c3478-180">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="c3478-181">`[ServiceName <String>]`: Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="c3478-181">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="c3478-182">`[SubscriptionId <String>]`: Hämtar prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c3478-182">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="c3478-183">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="c3478-183">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c3478-184">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3478-184">RELATED LINKS</span></span>

