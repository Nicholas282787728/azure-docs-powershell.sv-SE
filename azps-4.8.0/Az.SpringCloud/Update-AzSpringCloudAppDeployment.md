---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: f19383959e2a342555c7a741524e687b7bac37a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261012"
---
# <span data-ttu-id="0c97d-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="0c97d-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="0c97d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0c97d-102">SYNOPSIS</span></span>
<span data-ttu-id="0c97d-103">Åtgärd för att uppdatera en avsluta distribution.</span><span class="sxs-lookup"><span data-stu-id="0c97d-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="0c97d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0c97d-104">SYNTAX</span></span>

### <span data-ttu-id="0c97d-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="0c97d-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-InstanceCount <Int32>] [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0c97d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0c97d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-InstanceCount <Int32>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0c97d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0c97d-107">DESCRIPTION</span></span>
<span data-ttu-id="0c97d-108">Åtgärd för att uppdatera en avsluta distribution.</span><span class="sxs-lookup"><span data-stu-id="0c97d-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="0c97d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0c97d-109">EXAMPLES</span></span>

### <span data-ttu-id="0c97d-110">Exempel 1: uppdatera vår moln distribution efter namn.</span><span class="sxs-lookup"><span data-stu-id="0c97d-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
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

<span data-ttu-id="0c97d-111">Uppdatera vår moln distribution efter namn.</span><span class="sxs-lookup"><span data-stu-id="0c97d-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="0c97d-112">Exempel 2: uppdatera vår moln distribution från en pipe.</span><span class="sxs-lookup"><span data-stu-id="0c97d-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
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

<span data-ttu-id="0c97d-113">Uppdatera vår moln distribution från pipe.</span><span class="sxs-lookup"><span data-stu-id="0c97d-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="0c97d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0c97d-114">PARAMETERS</span></span>

### <span data-ttu-id="0c97d-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="0c97d-115">-AppName</span></span>
<span data-ttu-id="0c97d-116">Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="0c97d-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="0c97d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c97d-117">-AsJob</span></span>
<span data-ttu-id="0c97d-118">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="0c97d-118">Run the command as a job</span></span>

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

### <span data-ttu-id="0c97d-119">-CPU</span><span class="sxs-lookup"><span data-stu-id="0c97d-119">-Cpu</span></span>
<span data-ttu-id="0c97d-120">Nödvändig processor</span><span class="sxs-lookup"><span data-stu-id="0c97d-120">Required CPU</span></span>

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

### <span data-ttu-id="0c97d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c97d-121">-DefaultProfile</span></span>
<span data-ttu-id="0c97d-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0c97d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c97d-123">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="0c97d-123">-EnvironmentVariable</span></span>
<span data-ttu-id="0c97d-124">Uppsättning miljövariabler</span><span class="sxs-lookup"><span data-stu-id="0c97d-124">Collection of environment variables</span></span>

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

### <span data-ttu-id="0c97d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c97d-125">-InputObject</span></span>
<span data-ttu-id="0c97d-126">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="0c97d-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0c97d-127">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="0c97d-127">-InstanceCount</span></span>
<span data-ttu-id="0c97d-128">Antal förekomster</span><span class="sxs-lookup"><span data-stu-id="0c97d-128">Instance count</span></span>

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

### <span data-ttu-id="0c97d-129">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="0c97d-129">-JvmOption</span></span>
<span data-ttu-id="0c97d-130">Parametern JVM</span><span class="sxs-lookup"><span data-stu-id="0c97d-130">JVM parameter</span></span>

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

### <span data-ttu-id="0c97d-131">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="0c97d-131">-MemoryInGb</span></span>
<span data-ttu-id="0c97d-132">Nödvändig minnes storlek i GB</span><span class="sxs-lookup"><span data-stu-id="0c97d-132">Required Memory size in GB</span></span>

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

### <span data-ttu-id="0c97d-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="0c97d-133">-Name</span></span>
<span data-ttu-id="0c97d-134">Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="0c97d-134">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="0c97d-135">-Nowait</span><span class="sxs-lookup"><span data-stu-id="0c97d-135">-NoWait</span></span>
<span data-ttu-id="0c97d-136">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="0c97d-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0c97d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c97d-137">-ResourceGroupName</span></span>
<span data-ttu-id="0c97d-138">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="0c97d-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="0c97d-139">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="0c97d-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="0c97d-140">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="0c97d-140">-RuntimeVersion</span></span>
<span data-ttu-id="0c97d-141">Kör tids version</span><span class="sxs-lookup"><span data-stu-id="0c97d-141">Runtime version</span></span>

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

### <span data-ttu-id="0c97d-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0c97d-142">-ServiceName</span></span>
<span data-ttu-id="0c97d-143">Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="0c97d-143">The name of the Service resource.</span></span>

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

### <span data-ttu-id="0c97d-144">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="0c97d-144">-SourceArtifactSelector</span></span>
<span data-ttu-id="0c97d-145">Väljaren för den artefakt som ska användas för distribution av projekt med flera moduler.</span><span class="sxs-lookup"><span data-stu-id="0c97d-145">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="0c97d-146">Det här ska Bethe relativa sökvägen till målobjektet/projektet.</span><span class="sxs-lookup"><span data-stu-id="0c97d-146">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="0c97d-147">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="0c97d-147">-SourceRelativePath</span></span>
<span data-ttu-id="0c97d-148">Relativ sökväg för lagrings platsen som innehåller källan</span><span class="sxs-lookup"><span data-stu-id="0c97d-148">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="0c97d-149">-SourceType</span><span class="sxs-lookup"><span data-stu-id="0c97d-149">-SourceType</span></span>
<span data-ttu-id="0c97d-150">Typ av källa som laddats upp</span><span class="sxs-lookup"><span data-stu-id="0c97d-150">Type of the source uploaded</span></span>

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

### <span data-ttu-id="0c97d-151">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="0c97d-151">-SourceVersion</span></span>
<span data-ttu-id="0c97d-152">Version av källan</span><span class="sxs-lookup"><span data-stu-id="0c97d-152">Version of the source</span></span>

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

### <span data-ttu-id="0c97d-153">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0c97d-153">-SubscriptionId</span></span>
<span data-ttu-id="0c97d-154">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0c97d-154">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="0c97d-155">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="0c97d-155">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0c97d-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0c97d-156">-Confirm</span></span>
<span data-ttu-id="0c97d-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0c97d-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c97d-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c97d-158">-WhatIf</span></span>
<span data-ttu-id="0c97d-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0c97d-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c97d-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0c97d-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c97d-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c97d-161">CommonParameters</span></span>
<span data-ttu-id="0c97d-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c97d-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c97d-163">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c97d-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c97d-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0c97d-164">INPUTS</span></span>

### <span data-ttu-id="0c97d-165">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="0c97d-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="0c97d-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0c97d-166">OUTPUTS</span></span>

### <span data-ttu-id="0c97d-167">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. Api20190501Preview. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="0c97d-167">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="0c97d-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0c97d-168">NOTES</span></span>

<span data-ttu-id="0c97d-169">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0c97d-169">ALIASES</span></span>

<span data-ttu-id="0c97d-170">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="0c97d-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0c97d-171">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="0c97d-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0c97d-172">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0c97d-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0c97d-173">INPUTOBJECT <ISpringCloudIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="0c97d-173">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0c97d-174">`[AppName <String>]`: Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="0c97d-174">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="0c97d-175">`[BindingName <String>]`: Namnet på bindnings resursen.</span><span class="sxs-lookup"><span data-stu-id="0c97d-175">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="0c97d-176">`[CertificateName <String>]`: Namnet på certifikat resursen.</span><span class="sxs-lookup"><span data-stu-id="0c97d-176">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="0c97d-177">`[DeploymentName <String>]`: Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="0c97d-177">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="0c97d-178">`[DomainName <String>]`: Namnet på den anpassade domän resursen.</span><span class="sxs-lookup"><span data-stu-id="0c97d-178">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="0c97d-179">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="0c97d-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0c97d-180">`[Location <String>]`: regionen</span><span class="sxs-lookup"><span data-stu-id="0c97d-180">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="0c97d-181">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="0c97d-181">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="0c97d-182">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="0c97d-182">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="0c97d-183">`[ServiceName <String>]`: Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="0c97d-183">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="0c97d-184">`[SubscriptionId <String>]`: Hämtar prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0c97d-184">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="0c97d-185">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="0c97d-185">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0c97d-186">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0c97d-186">RELATED LINKS</span></span>

