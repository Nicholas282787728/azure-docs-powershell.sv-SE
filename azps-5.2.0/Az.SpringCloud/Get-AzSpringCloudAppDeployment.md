---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 3accf4b622f77edb0e3d0cea6fe67bbc1db9ff6c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413011"
---
# <span data-ttu-id="83ab6-101">Get-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="83ab6-101">Get-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="83ab6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="83ab6-102">SYNOPSIS</span></span>
<span data-ttu-id="83ab6-103">Skaffa en distribution och dess egenskaper.</span><span class="sxs-lookup"><span data-stu-id="83ab6-103">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="83ab6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="83ab6-104">SYNTAX</span></span>

### <span data-ttu-id="83ab6-105">List1 (standard)</span><span class="sxs-lookup"><span data-stu-id="83ab6-105">List1 (Default)</span></span>
```
Get-AzSpringCloudAppDeployment -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="83ab6-106">Lära</span><span class="sxs-lookup"><span data-stu-id="83ab6-106">Get</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="83ab6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="83ab6-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="83ab6-108">Förteckning</span><span class="sxs-lookup"><span data-stu-id="83ab6-108">List</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="83ab6-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="83ab6-109">DESCRIPTION</span></span>
<span data-ttu-id="83ab6-110">Skaffa en distribution och dess egenskaper.</span><span class="sxs-lookup"><span data-stu-id="83ab6-110">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="83ab6-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="83ab6-111">EXAMPLES</span></span>

### <span data-ttu-id="83ab6-112">Exempel 1: Hämta Deploymeng till vår moln efter namn.</span><span class="sxs-lookup"><span data-stu-id="83ab6-112">Example 1: Get Spring Cloud App Deploymeng by name.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
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

<span data-ttu-id="83ab6-113">Skaffa ett Deploymeng efter namn.</span><span class="sxs-lookup"><span data-stu-id="83ab6-113">Get Spring Cloud App Deploymeng by name.</span></span>

### <span data-ttu-id="83ab6-114">Exempel 2: Visa en lista över alla distributioner under en viss fjäder moln app.</span><span class="sxs-lookup"><span data-stu-id="83ab6-114">Example 2: List all the deployment under a given spring cloud app.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
Name    Type
----    ----
default Microsoft.AppPlatform/Spring/apps/deployments
prod    Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="83ab6-115">Visa en lista över alla distributioner under en viss fjäder moln app.</span><span class="sxs-lookup"><span data-stu-id="83ab6-115">List all the deployment under a given spring cloud app.</span></span>

## <span data-ttu-id="83ab6-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="83ab6-116">PARAMETERS</span></span>

### <span data-ttu-id="83ab6-117">-AppName</span><span class="sxs-lookup"><span data-stu-id="83ab6-117">-AppName</span></span>
<span data-ttu-id="83ab6-118">Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="83ab6-118">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ab6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83ab6-119">-DefaultProfile</span></span>
<span data-ttu-id="83ab6-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="83ab6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83ab6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83ab6-121">-InputObject</span></span>
<span data-ttu-id="83ab6-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="83ab6-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83ab6-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="83ab6-123">-Name</span></span>
<span data-ttu-id="83ab6-124">Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="83ab6-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ab6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83ab6-125">-ResourceGroupName</span></span>
<span data-ttu-id="83ab6-126">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="83ab6-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="83ab6-127">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="83ab6-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ab6-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="83ab6-128">-ServiceName</span></span>
<span data-ttu-id="83ab6-129">Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="83ab6-129">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ab6-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83ab6-130">-SubscriptionId</span></span>
<span data-ttu-id="83ab6-131">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="83ab6-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="83ab6-132">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="83ab6-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ab6-133">-Version</span><span class="sxs-lookup"><span data-stu-id="83ab6-133">-Version</span></span>
<span data-ttu-id="83ab6-134">Version av distributionerna som ska listas</span><span class="sxs-lookup"><span data-stu-id="83ab6-134">Version of the deployments to be listed</span></span>

```yaml
Type: System.String[]
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ab6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83ab6-135">CommonParameters</span></span>
<span data-ttu-id="83ab6-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83ab6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83ab6-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83ab6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83ab6-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="83ab6-138">INPUTS</span></span>

### <span data-ttu-id="83ab6-139">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="83ab6-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="83ab6-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="83ab6-140">OUTPUTS</span></span>

### <span data-ttu-id="83ab6-141">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. Api20200701. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="83ab6-141">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="83ab6-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="83ab6-142">NOTES</span></span>

<span data-ttu-id="83ab6-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="83ab6-143">ALIASES</span></span>

<span data-ttu-id="83ab6-144">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="83ab6-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="83ab6-145">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="83ab6-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="83ab6-146">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="83ab6-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="83ab6-147">INPUTOBJECT <ISpringCloudIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="83ab6-147">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="83ab6-148">`[AppName <String>]`: Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="83ab6-148">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="83ab6-149">`[BindingName <String>]`: Namnet på bindnings resursen.</span><span class="sxs-lookup"><span data-stu-id="83ab6-149">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="83ab6-150">`[CertificateName <String>]`: Namnet på certifikat resursen.</span><span class="sxs-lookup"><span data-stu-id="83ab6-150">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="83ab6-151">`[DeploymentName <String>]`: Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="83ab6-151">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="83ab6-152">`[DomainName <String>]`: Namnet på den anpassade domän resursen.</span><span class="sxs-lookup"><span data-stu-id="83ab6-152">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="83ab6-153">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="83ab6-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="83ab6-154">`[Location <String>]`: regionen</span><span class="sxs-lookup"><span data-stu-id="83ab6-154">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="83ab6-155">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="83ab6-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="83ab6-156">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="83ab6-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="83ab6-157">`[ServiceName <String>]`: Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="83ab6-157">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="83ab6-158">`[SubscriptionId <String>]`: Hämtar prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="83ab6-158">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="83ab6-159">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="83ab6-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="83ab6-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="83ab6-160">RELATED LINKS</span></span>

