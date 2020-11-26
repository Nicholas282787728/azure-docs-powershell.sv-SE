---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/new-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 37538cddb7654b665b2b2dd4935414a2cb76b45a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94262959"
---
# <span data-ttu-id="b318b-101">New-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="b318b-101">New-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="b318b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b318b-102">SYNOPSIS</span></span>
<span data-ttu-id="b318b-103">Skapa en ny distribution eller uppdatera en avslutnings distribution.</span><span class="sxs-lookup"><span data-stu-id="b318b-103">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="b318b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b318b-104">SYNTAX</span></span>

```
New-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b318b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b318b-105">DESCRIPTION</span></span>
<span data-ttu-id="b318b-106">Skapa en ny distribution eller uppdatera en avslutnings distribution.</span><span class="sxs-lookup"><span data-stu-id="b318b-106">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="b318b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b318b-107">EXAMPLES</span></span>

### <span data-ttu-id="b318b-108">Exempel 1: exempel 1: skapa en introduktion till moln distribution.</span><span class="sxs-lookup"><span data-stu-id="b318b-108">Example 1: Example 1: Create a spring cloud deployment.</span></span>
```powershell
PS C:\> New-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rp -name spring-cloud-service -AppName gateway -DeploymentName default

Active                               : False
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-6bd6f87954-nl2wl}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : <default>
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="b318b-109">Skapa en vår distribution av fjäder moln.</span><span class="sxs-lookup"><span data-stu-id="b318b-109">Create a spring cloud deployment.</span></span>

## <span data-ttu-id="b318b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b318b-110">PARAMETERS</span></span>

### <span data-ttu-id="b318b-111">-AppName</span><span class="sxs-lookup"><span data-stu-id="b318b-111">-AppName</span></span>
<span data-ttu-id="b318b-112">Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="b318b-112">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b318b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b318b-113">-AsJob</span></span>
<span data-ttu-id="b318b-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="b318b-114">Run the command as a job</span></span>

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

### <span data-ttu-id="b318b-115">-CPU</span><span class="sxs-lookup"><span data-stu-id="b318b-115">-Cpu</span></span>
<span data-ttu-id="b318b-116">Nödvändig processor</span><span class="sxs-lookup"><span data-stu-id="b318b-116">Required CPU</span></span>

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

### <span data-ttu-id="b318b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b318b-117">-DefaultProfile</span></span>
<span data-ttu-id="b318b-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b318b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b318b-119">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="b318b-119">-EnvironmentVariable</span></span>
<span data-ttu-id="b318b-120">Uppsättning miljövariabler</span><span class="sxs-lookup"><span data-stu-id="b318b-120">Collection of environment variables</span></span>

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

### <span data-ttu-id="b318b-121">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="b318b-121">-JvmOption</span></span>
<span data-ttu-id="b318b-122">Parametern JVM</span><span class="sxs-lookup"><span data-stu-id="b318b-122">JVM parameter</span></span>

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

### <span data-ttu-id="b318b-123">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="b318b-123">-MemoryInGb</span></span>
<span data-ttu-id="b318b-124">Nödvändig minnes storlek i GB</span><span class="sxs-lookup"><span data-stu-id="b318b-124">Required Memory size in GB</span></span>

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

### <span data-ttu-id="b318b-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="b318b-125">-Name</span></span>
<span data-ttu-id="b318b-126">Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="b318b-126">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b318b-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b318b-127">-NoWait</span></span>
<span data-ttu-id="b318b-128">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="b318b-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b318b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b318b-129">-ResourceGroupName</span></span>
<span data-ttu-id="b318b-130">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="b318b-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b318b-131">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="b318b-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b318b-132">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="b318b-132">-RuntimeVersion</span></span>
<span data-ttu-id="b318b-133">Kör tids version</span><span class="sxs-lookup"><span data-stu-id="b318b-133">Runtime version</span></span>

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

### <span data-ttu-id="b318b-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b318b-134">-ServiceName</span></span>
<span data-ttu-id="b318b-135">Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="b318b-135">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b318b-136">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="b318b-136">-SourceArtifactSelector</span></span>
<span data-ttu-id="b318b-137">Väljaren för den artefakt som ska användas för distribution av projekt med flera moduler.</span><span class="sxs-lookup"><span data-stu-id="b318b-137">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="b318b-138">Det här ska Bethe relativa sökvägen till målobjektet/projektet.</span><span class="sxs-lookup"><span data-stu-id="b318b-138">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="b318b-139">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="b318b-139">-SourceRelativePath</span></span>
<span data-ttu-id="b318b-140">Relativ sökväg för lagrings platsen som innehåller källan</span><span class="sxs-lookup"><span data-stu-id="b318b-140">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="b318b-141">-SourceType</span><span class="sxs-lookup"><span data-stu-id="b318b-141">-SourceType</span></span>
<span data-ttu-id="b318b-142">Typ av källa som laddats upp</span><span class="sxs-lookup"><span data-stu-id="b318b-142">Type of the source uploaded</span></span>

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

### <span data-ttu-id="b318b-143">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="b318b-143">-SourceVersion</span></span>
<span data-ttu-id="b318b-144">Version av källan</span><span class="sxs-lookup"><span data-stu-id="b318b-144">Version of the source</span></span>

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

### <span data-ttu-id="b318b-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b318b-145">-SubscriptionId</span></span>
<span data-ttu-id="b318b-146">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="b318b-146">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b318b-147">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="b318b-147">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b318b-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b318b-148">-Confirm</span></span>
<span data-ttu-id="b318b-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b318b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b318b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b318b-150">-WhatIf</span></span>
<span data-ttu-id="b318b-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b318b-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b318b-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b318b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b318b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b318b-153">CommonParameters</span></span>
<span data-ttu-id="b318b-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b318b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b318b-155">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b318b-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b318b-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b318b-156">INPUTS</span></span>

## <span data-ttu-id="b318b-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b318b-157">OUTPUTS</span></span>

### <span data-ttu-id="b318b-158">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. Api20200701. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="b318b-158">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="b318b-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b318b-159">NOTES</span></span>

<span data-ttu-id="b318b-160">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b318b-160">ALIASES</span></span>

## <span data-ttu-id="b318b-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b318b-161">RELATED LINKS</span></span>
