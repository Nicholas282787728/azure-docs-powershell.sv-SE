---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
ms.openlocfilehash: c84037fd402e5ecea51cc4f60dcddb1873878f5a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261667"
---
# <span data-ttu-id="37fea-101">New-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="37fea-101">New-AzSpringCloud</span></span>

## <span data-ttu-id="37fea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="37fea-102">SYNOPSIS</span></span>
<span data-ttu-id="37fea-103">Skapa en ny tjänst eller uppdatera en utförsel tjänst.</span><span class="sxs-lookup"><span data-stu-id="37fea-103">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="37fea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="37fea-104">SYNTAX</span></span>

```
New-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="37fea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="37fea-105">DESCRIPTION</span></span>
<span data-ttu-id="37fea-106">Skapa en ny tjänst eller uppdatera en utförsel tjänst.</span><span class="sxs-lookup"><span data-stu-id="37fea-106">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="37fea-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="37fea-107">EXAMPLES</span></span>

### <span data-ttu-id="37fea-108">Exempel 1: skapa en fjäder moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="37fea-108">Example 1: Create a spring cloud service.</span></span>
```powershell
PS C:\> New-AzSpringCloud -ResourceGroupName spring-cloud-rp -name spring-cloud-service -Location eastus

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

<span data-ttu-id="37fea-109">Skapa en vår moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="37fea-109">Create a spring cloud service.</span></span>

## <span data-ttu-id="37fea-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="37fea-110">PARAMETERS</span></span>

### <span data-ttu-id="37fea-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37fea-111">-AsJob</span></span>
<span data-ttu-id="37fea-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="37fea-112">Run the command as a job</span></span>

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

### <span data-ttu-id="37fea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37fea-113">-DefaultProfile</span></span>
<span data-ttu-id="37fea-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="37fea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37fea-115">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="37fea-115">-GitPropertyUri</span></span>
<span data-ttu-id="37fea-116">URI för databasen</span><span class="sxs-lookup"><span data-stu-id="37fea-116">URI of the repository</span></span>

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

### <span data-ttu-id="37fea-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="37fea-117">-Location</span></span>
<span data-ttu-id="37fea-118">GEO-platsen för resursen.</span><span class="sxs-lookup"><span data-stu-id="37fea-118">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="37fea-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="37fea-119">-Name</span></span>
<span data-ttu-id="37fea-120">Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="37fea-120">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37fea-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="37fea-121">-NoWait</span></span>
<span data-ttu-id="37fea-122">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="37fea-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="37fea-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37fea-123">-ResourceGroupName</span></span>
<span data-ttu-id="37fea-124">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="37fea-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="37fea-125">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="37fea-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="37fea-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="37fea-126">-SkuName</span></span>
<span data-ttu-id="37fea-127">Namn på SKU</span><span class="sxs-lookup"><span data-stu-id="37fea-127">Name of the Sku</span></span>

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

### <span data-ttu-id="37fea-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="37fea-128">-SkuTier</span></span>
<span data-ttu-id="37fea-129">SKU</span><span class="sxs-lookup"><span data-stu-id="37fea-129">Tier of the Sku</span></span>

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

### <span data-ttu-id="37fea-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="37fea-130">-SubscriptionId</span></span>
<span data-ttu-id="37fea-131">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="37fea-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="37fea-132">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="37fea-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="37fea-133">-Tagg</span><span class="sxs-lookup"><span data-stu-id="37fea-133">-Tag</span></span>
<span data-ttu-id="37fea-134">Taggar för tjänsten som är en lista över de värde par som beskriver resursen.</span><span class="sxs-lookup"><span data-stu-id="37fea-134">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="37fea-135">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="37fea-135">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="37fea-136">Huvud instrument för mål program</span><span class="sxs-lookup"><span data-stu-id="37fea-136">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="37fea-137">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="37fea-137">-TraceEnabled</span></span>
<span data-ttu-id="37fea-138">Anger om spårningsfunktionen ska aktive ras</span><span class="sxs-lookup"><span data-stu-id="37fea-138">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="37fea-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="37fea-139">-Confirm</span></span>
<span data-ttu-id="37fea-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="37fea-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37fea-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37fea-141">-WhatIf</span></span>
<span data-ttu-id="37fea-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="37fea-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37fea-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="37fea-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37fea-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37fea-144">CommonParameters</span></span>
<span data-ttu-id="37fea-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37fea-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37fea-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37fea-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37fea-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="37fea-147">INPUTS</span></span>

## <span data-ttu-id="37fea-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="37fea-148">OUTPUTS</span></span>

### <span data-ttu-id="37fea-149">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. Api20190501Preview. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="37fea-149">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IServiceResource</span></span>

## <span data-ttu-id="37fea-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="37fea-150">NOTES</span></span>

<span data-ttu-id="37fea-151">ALIAS</span><span class="sxs-lookup"><span data-stu-id="37fea-151">ALIASES</span></span>

## <span data-ttu-id="37fea-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="37fea-152">RELATED LINKS</span></span>
