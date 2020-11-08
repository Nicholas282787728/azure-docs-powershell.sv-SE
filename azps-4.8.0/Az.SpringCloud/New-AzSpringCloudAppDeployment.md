---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/new-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 0669371f589722e3da18e554df98dbf7d193ccc8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261656"
---
# <span data-ttu-id="40ac8-101">New-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="40ac8-101">New-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="40ac8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="40ac8-102">SYNOPSIS</span></span>
<span data-ttu-id="40ac8-103">Skapa en ny distribution eller uppdatera en avslutnings distribution.</span><span class="sxs-lookup"><span data-stu-id="40ac8-103">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="40ac8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="40ac8-104">SYNTAX</span></span>

```
New-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-InstanceCount <Int32>] [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="40ac8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="40ac8-105">DESCRIPTION</span></span>
<span data-ttu-id="40ac8-106">Skapa en ny distribution eller uppdatera en avslutnings distribution.</span><span class="sxs-lookup"><span data-stu-id="40ac8-106">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="40ac8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="40ac8-107">EXAMPLES</span></span>

### <span data-ttu-id="40ac8-108">Exempel 1: exempel 1: skapa en introduktion till moln distribution.</span><span class="sxs-lookup"><span data-stu-id="40ac8-108">Example 1: Example 1: Create a spring cloud deployment.</span></span>
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

<span data-ttu-id="40ac8-109">Skapa en vår distribution av fjäder moln.</span><span class="sxs-lookup"><span data-stu-id="40ac8-109">Create a spring cloud deployment.</span></span>

## <span data-ttu-id="40ac8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="40ac8-110">PARAMETERS</span></span>

### <span data-ttu-id="40ac8-111">-AppName</span><span class="sxs-lookup"><span data-stu-id="40ac8-111">-AppName</span></span>
<span data-ttu-id="40ac8-112">Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="40ac8-112">The name of the App resource.</span></span>

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

### <span data-ttu-id="40ac8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40ac8-113">-AsJob</span></span>
<span data-ttu-id="40ac8-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="40ac8-114">Run the command as a job</span></span>

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

### <span data-ttu-id="40ac8-115">-CPU</span><span class="sxs-lookup"><span data-stu-id="40ac8-115">-Cpu</span></span>
<span data-ttu-id="40ac8-116">Nödvändig processor</span><span class="sxs-lookup"><span data-stu-id="40ac8-116">Required CPU</span></span>

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

### <span data-ttu-id="40ac8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40ac8-117">-DefaultProfile</span></span>
<span data-ttu-id="40ac8-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="40ac8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40ac8-119">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="40ac8-119">-EnvironmentVariable</span></span>
<span data-ttu-id="40ac8-120">Uppsättning miljövariabler</span><span class="sxs-lookup"><span data-stu-id="40ac8-120">Collection of environment variables</span></span>

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

### <span data-ttu-id="40ac8-121">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="40ac8-121">-InstanceCount</span></span>
<span data-ttu-id="40ac8-122">Antal förekomster</span><span class="sxs-lookup"><span data-stu-id="40ac8-122">Instance count</span></span>

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

### <span data-ttu-id="40ac8-123">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="40ac8-123">-JvmOption</span></span>
<span data-ttu-id="40ac8-124">Parametern JVM</span><span class="sxs-lookup"><span data-stu-id="40ac8-124">JVM parameter</span></span>

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

### <span data-ttu-id="40ac8-125">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="40ac8-125">-MemoryInGb</span></span>
<span data-ttu-id="40ac8-126">Nödvändig minnes storlek i GB</span><span class="sxs-lookup"><span data-stu-id="40ac8-126">Required Memory size in GB</span></span>

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

### <span data-ttu-id="40ac8-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="40ac8-127">-Name</span></span>
<span data-ttu-id="40ac8-128">Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="40ac8-128">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="40ac8-129">-Nowait</span><span class="sxs-lookup"><span data-stu-id="40ac8-129">-NoWait</span></span>
<span data-ttu-id="40ac8-130">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="40ac8-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="40ac8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40ac8-131">-ResourceGroupName</span></span>
<span data-ttu-id="40ac8-132">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="40ac8-132">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="40ac8-133">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="40ac8-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="40ac8-134">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="40ac8-134">-RuntimeVersion</span></span>
<span data-ttu-id="40ac8-135">Kör tids version</span><span class="sxs-lookup"><span data-stu-id="40ac8-135">Runtime version</span></span>

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

### <span data-ttu-id="40ac8-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="40ac8-136">-ServiceName</span></span>
<span data-ttu-id="40ac8-137">Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="40ac8-137">The name of the Service resource.</span></span>

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

### <span data-ttu-id="40ac8-138">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="40ac8-138">-SourceArtifactSelector</span></span>
<span data-ttu-id="40ac8-139">Väljaren för den artefakt som ska användas för distribution av projekt med flera moduler.</span><span class="sxs-lookup"><span data-stu-id="40ac8-139">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="40ac8-140">Det här ska Bethe relativa sökvägen till målobjektet/projektet.</span><span class="sxs-lookup"><span data-stu-id="40ac8-140">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="40ac8-141">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="40ac8-141">-SourceRelativePath</span></span>
<span data-ttu-id="40ac8-142">Relativ sökväg för lagrings platsen som innehåller källan</span><span class="sxs-lookup"><span data-stu-id="40ac8-142">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="40ac8-143">-SourceType</span><span class="sxs-lookup"><span data-stu-id="40ac8-143">-SourceType</span></span>
<span data-ttu-id="40ac8-144">Typ av källa som laddats upp</span><span class="sxs-lookup"><span data-stu-id="40ac8-144">Type of the source uploaded</span></span>

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

### <span data-ttu-id="40ac8-145">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="40ac8-145">-SourceVersion</span></span>
<span data-ttu-id="40ac8-146">Version av källan</span><span class="sxs-lookup"><span data-stu-id="40ac8-146">Version of the source</span></span>

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

### <span data-ttu-id="40ac8-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="40ac8-147">-SubscriptionId</span></span>
<span data-ttu-id="40ac8-148">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="40ac8-148">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="40ac8-149">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="40ac8-149">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="40ac8-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="40ac8-150">-Confirm</span></span>
<span data-ttu-id="40ac8-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="40ac8-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40ac8-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40ac8-152">-WhatIf</span></span>
<span data-ttu-id="40ac8-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="40ac8-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40ac8-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="40ac8-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40ac8-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40ac8-155">CommonParameters</span></span>
<span data-ttu-id="40ac8-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40ac8-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40ac8-157">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40ac8-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40ac8-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="40ac8-158">INPUTS</span></span>

## <span data-ttu-id="40ac8-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="40ac8-159">OUTPUTS</span></span>

### <span data-ttu-id="40ac8-160">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. Api20190501Preview. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="40ac8-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="40ac8-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="40ac8-161">NOTES</span></span>

<span data-ttu-id="40ac8-162">ALIAS</span><span class="sxs-lookup"><span data-stu-id="40ac8-162">ALIASES</span></span>

## <span data-ttu-id="40ac8-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="40ac8-163">RELATED LINKS</span></span>

