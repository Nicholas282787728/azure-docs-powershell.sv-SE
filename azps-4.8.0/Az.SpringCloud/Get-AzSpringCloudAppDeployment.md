---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
ms.openlocfilehash: d33f649d71a8fb3f4a112ac77937f37d867a24c4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261668"
---
# <span data-ttu-id="56f8b-101">Get-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="56f8b-101">Get-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="56f8b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="56f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="56f8b-103">Skaffa en distribution och dess egenskaper.</span><span class="sxs-lookup"><span data-stu-id="56f8b-103">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="56f8b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="56f8b-104">SYNTAX</span></span>

### <span data-ttu-id="56f8b-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="56f8b-105">List (Default)</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="56f8b-106">Lära</span><span class="sxs-lookup"><span data-stu-id="56f8b-106">Get</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="56f8b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="56f8b-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="56f8b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="56f8b-108">DESCRIPTION</span></span>
<span data-ttu-id="56f8b-109">Skaffa en distribution och dess egenskaper.</span><span class="sxs-lookup"><span data-stu-id="56f8b-109">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="56f8b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="56f8b-110">EXAMPLES</span></span>

### <span data-ttu-id="56f8b-111">Exempel 1: Hämta Deploymeng till vår moln efter namn.</span><span class="sxs-lookup"><span data-stu-id="56f8b-111">Example 1: Get Spring Cloud App Deploymeng by name.</span></span>
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

<span data-ttu-id="56f8b-112">Skaffa ett Deploymeng efter namn.</span><span class="sxs-lookup"><span data-stu-id="56f8b-112">Get Spring Cloud App Deploymeng by name.</span></span>

### <span data-ttu-id="56f8b-113">Exempel 2: Visa en lista över alla distributioner under en viss fjäder moln app.</span><span class="sxs-lookup"><span data-stu-id="56f8b-113">Example 2: List all the deployment under a given spring cloud app.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
Name    Type
----    ----
default Microsoft.AppPlatform/Spring/apps/deployments
prod    Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="56f8b-114">Visa en lista över alla distributioner under en viss fjäder moln app.</span><span class="sxs-lookup"><span data-stu-id="56f8b-114">List all the deployment under a given spring cloud app.</span></span>

## <span data-ttu-id="56f8b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="56f8b-115">PARAMETERS</span></span>

### <span data-ttu-id="56f8b-116">-AppName</span><span class="sxs-lookup"><span data-stu-id="56f8b-116">-AppName</span></span>
<span data-ttu-id="56f8b-117">Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="56f8b-117">The name of the App resource.</span></span>

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

### <span data-ttu-id="56f8b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56f8b-118">-DefaultProfile</span></span>
<span data-ttu-id="56f8b-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="56f8b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56f8b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56f8b-120">-InputObject</span></span>
<span data-ttu-id="56f8b-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="56f8b-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="56f8b-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="56f8b-122">-Name</span></span>
<span data-ttu-id="56f8b-123">Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="56f8b-123">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="56f8b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56f8b-124">-ResourceGroupName</span></span>
<span data-ttu-id="56f8b-125">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="56f8b-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="56f8b-126">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="56f8b-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="56f8b-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="56f8b-127">-ServiceName</span></span>
<span data-ttu-id="56f8b-128">Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="56f8b-128">The name of the Service resource.</span></span>

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

### <span data-ttu-id="56f8b-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56f8b-129">-SubscriptionId</span></span>
<span data-ttu-id="56f8b-130">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="56f8b-130">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="56f8b-131">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="56f8b-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f8b-132">-Version</span><span class="sxs-lookup"><span data-stu-id="56f8b-132">-Version</span></span>
<span data-ttu-id="56f8b-133">Version av distributionerna som ska listas</span><span class="sxs-lookup"><span data-stu-id="56f8b-133">Version of the deployments to be listed</span></span>

```yaml
Type: System.String[]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f8b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56f8b-134">CommonParameters</span></span>
<span data-ttu-id="56f8b-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56f8b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56f8b-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56f8b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56f8b-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="56f8b-137">INPUTS</span></span>

### <span data-ttu-id="56f8b-138">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="56f8b-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="56f8b-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="56f8b-139">OUTPUTS</span></span>

### <span data-ttu-id="56f8b-140">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. Api20190501Preview. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="56f8b-140">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="56f8b-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="56f8b-141">NOTES</span></span>

<span data-ttu-id="56f8b-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="56f8b-142">ALIASES</span></span>

<span data-ttu-id="56f8b-143">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="56f8b-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="56f8b-144">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="56f8b-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="56f8b-145">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="56f8b-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="56f8b-146">INPUTOBJECT <ISpringCloudIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="56f8b-146">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="56f8b-147">`[AppName <String>]`: Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="56f8b-147">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="56f8b-148">`[BindingName <String>]`: Namnet på bindnings resursen.</span><span class="sxs-lookup"><span data-stu-id="56f8b-148">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="56f8b-149">`[CertificateName <String>]`: Namnet på certifikat resursen.</span><span class="sxs-lookup"><span data-stu-id="56f8b-149">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="56f8b-150">`[DeploymentName <String>]`: Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="56f8b-150">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="56f8b-151">`[DomainName <String>]`: Namnet på den anpassade domän resursen.</span><span class="sxs-lookup"><span data-stu-id="56f8b-151">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="56f8b-152">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="56f8b-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="56f8b-153">`[Location <String>]`: regionen</span><span class="sxs-lookup"><span data-stu-id="56f8b-153">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="56f8b-154">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="56f8b-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="56f8b-155">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="56f8b-155">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="56f8b-156">`[ServiceName <String>]`: Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="56f8b-156">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="56f8b-157">`[SubscriptionId <String>]`: Hämtar prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="56f8b-157">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="56f8b-158">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="56f8b-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="56f8b-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="56f8b-159">RELATED LINKS</span></span>

