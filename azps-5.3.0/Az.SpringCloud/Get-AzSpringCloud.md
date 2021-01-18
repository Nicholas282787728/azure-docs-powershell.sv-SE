---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
ms.openlocfilehash: 39324dc0f85ca4d6f9c3498fae92c340e2113dad
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523014"
---
# <span data-ttu-id="8e243-101">Get-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="8e243-101">Get-AzSpringCloud</span></span>

## <span data-ttu-id="8e243-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8e243-102">SYNOPSIS</span></span>
<span data-ttu-id="8e243-103">Skaffa en tjänst och dess egenskaper.</span><span class="sxs-lookup"><span data-stu-id="8e243-103">Get a Service and its properties.</span></span>

## <span data-ttu-id="8e243-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8e243-104">SYNTAX</span></span>

### <span data-ttu-id="8e243-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="8e243-105">List (Default)</span></span>
```
Get-AzSpringCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8e243-106">Lära</span><span class="sxs-lookup"><span data-stu-id="8e243-106">Get</span></span>
```
Get-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8e243-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8e243-107">GetViaIdentity</span></span>
```
Get-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8e243-108">List1</span><span class="sxs-lookup"><span data-stu-id="8e243-108">List1</span></span>
```
Get-AzSpringCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e243-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8e243-109">DESCRIPTION</span></span>
<span data-ttu-id="8e243-110">Skaffa en tjänst och dess egenskaper.</span><span class="sxs-lookup"><span data-stu-id="8e243-110">Get a Service and its properties.</span></span>

## <span data-ttu-id="8e243-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8e243-111">EXAMPLES</span></span>

### <span data-ttu-id="8e243-112">Exempel 1: skaffa vår moln tjänst efter namn</span><span class="sxs-lookup"><span data-stu-id="8e243-112">Example 1: Get Spring Cloud Service by name</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
ConfigServerPropertiesErrorCode                  :
ConfigServerPropertiesErrorMessage               :
ConfigServerPropertyState                        : Succeeded
GitPropertyHostKey                               :
GitPropertyHostKeyAlgorithm                      :
GitPropertyLabel                                 :
GitPropertyPassword                              :
GitPropertyPrivateKey                            :
GitPropertyRepository                            :
GitPropertySearchPath                            :
GitPropertyStrictHostKeyChecking                 :
GitPropertyUri                                   :
GitPropertyUsername                              :
Id                                               : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service
Location                                         : eastus
Name                                             : spring-cloud-service
NetworkProfileAppNetworkResourceGroup            :
NetworkProfileAppSubnetId                        :
NetworkProfileServiceCidr                        :
NetworkProfileServiceRuntimeNetworkResourceGroup :
NetworkProfileServiceRuntimeSubnetId             :
ProvisioningState                                : Succeeded
ServiceId                                        : e5e964885b4146b1a91e9bfc17971ee5
SkuCapacity                                      :
SkuName                                          : S0
SkuTier                                          : Standard
Tag                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TrackedResourceTags
TraceAppInsightInstrumentationKey                :
TraceEnabled                                     : False
TraceErrorCode                                   :
TraceErrorMessage                                :
TraceState                                       : Succeeded
Type                                             : Microsoft.AppPlatform/Spring
Version                                          : 2
ConfigServerGitProperty                          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerGitProperty
ConfigServerProperty                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerProperties
ConfigServerPropertyConfigServer                 : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerSettings
ConfigServerPropertyError                        : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
NetworkProfile                                   : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.NetworkProfile
Property                                         : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ClusterResourceProperties
Sku                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Sku
Trace                                            : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TraceProperties
TraceError                                       : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
```

<span data-ttu-id="8e243-113">Skaffa vår moln tjänst med namn</span><span class="sxs-lookup"><span data-stu-id="8e243-113">Get Spring Cloud Service by name</span></span>

### <span data-ttu-id="8e243-114">Exempel 2: lista alla våren-moln tjänster under resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8e243-114">Example 2: List all the spring cloud service under the resource group.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg
Location Name                Type
-------- ----                ----
eastus   spring-cloud-rg Microsoft.AppPlatform/Spring
```

<span data-ttu-id="8e243-115">Lista alla våren-moln tjänster under resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8e243-115">List all the spring cloud service under the resource group.</span></span>

## <span data-ttu-id="8e243-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8e243-116">PARAMETERS</span></span>

### <span data-ttu-id="8e243-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e243-117">-DefaultProfile</span></span>
<span data-ttu-id="8e243-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8e243-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e243-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e243-119">-InputObject</span></span>
<span data-ttu-id="8e243-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="8e243-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8e243-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="8e243-121">-Name</span></span>
<span data-ttu-id="8e243-122">Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="8e243-122">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e243-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e243-123">-ResourceGroupName</span></span>
<span data-ttu-id="8e243-124">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="8e243-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8e243-125">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="8e243-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e243-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8e243-126">-SubscriptionId</span></span>
<span data-ttu-id="8e243-127">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8e243-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="8e243-128">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="8e243-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8e243-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e243-129">CommonParameters</span></span>
<span data-ttu-id="8e243-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e243-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e243-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e243-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e243-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8e243-132">INPUTS</span></span>

### <span data-ttu-id="8e243-133">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="8e243-133">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="8e243-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8e243-134">OUTPUTS</span></span>

### <span data-ttu-id="8e243-135">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. Api20200701. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="8e243-135">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="8e243-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8e243-136">NOTES</span></span>

<span data-ttu-id="8e243-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8e243-137">ALIASES</span></span>

<span data-ttu-id="8e243-138">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="8e243-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8e243-139">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="8e243-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8e243-140">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8e243-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8e243-141">INPUTOBJECT <ISpringCloudIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="8e243-141">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8e243-142">`[AppName <String>]`: Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="8e243-142">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="8e243-143">`[BindingName <String>]`: Namnet på bindnings resursen.</span><span class="sxs-lookup"><span data-stu-id="8e243-143">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="8e243-144">`[CertificateName <String>]`: Namnet på certifikat resursen.</span><span class="sxs-lookup"><span data-stu-id="8e243-144">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="8e243-145">`[DeploymentName <String>]`: Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="8e243-145">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="8e243-146">`[DomainName <String>]`: Namnet på den anpassade domän resursen.</span><span class="sxs-lookup"><span data-stu-id="8e243-146">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="8e243-147">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="8e243-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8e243-148">`[Location <String>]`: regionen</span><span class="sxs-lookup"><span data-stu-id="8e243-148">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="8e243-149">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="8e243-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="8e243-150">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="8e243-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="8e243-151">`[ServiceName <String>]`: Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="8e243-151">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="8e243-152">`[SubscriptionId <String>]`: Hämtar prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8e243-152">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="8e243-153">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="8e243-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8e243-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8e243-154">RELATED LINKS</span></span>

