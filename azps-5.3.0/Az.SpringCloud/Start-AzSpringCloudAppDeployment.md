---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/start-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Start-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Start-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 7cab91bf5c7e95258f17a73da4e2b177e30444c9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419747"
---
# <span data-ttu-id="b6af0-101">Start-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="b6af0-101">Start-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="b6af0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6af0-102">SYNOPSIS</span></span>
<span data-ttu-id="b6af0-103">Starta distributionen.</span><span class="sxs-lookup"><span data-stu-id="b6af0-103">Start the deployment.</span></span>

## <span data-ttu-id="b6af0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6af0-104">SYNTAX</span></span>

### <span data-ttu-id="b6af0-105">Start (standard)</span><span class="sxs-lookup"><span data-stu-id="b6af0-105">Start (Default)</span></span>
```
Start-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b6af0-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b6af0-106">StartViaIdentity</span></span>
```
Start-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b6af0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6af0-107">DESCRIPTION</span></span>
<span data-ttu-id="b6af0-108">Starta distributionen.</span><span class="sxs-lookup"><span data-stu-id="b6af0-108">Start the deployment.</span></span>

## <span data-ttu-id="b6af0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6af0-109">EXAMPLES</span></span>

### <span data-ttu-id="b6af0-110">Exempel 1: starta våren Cloud service med namn.</span><span class="sxs-lookup"><span data-stu-id="b6af0-110">Example 1: Start Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Start-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="b6af0-111">Starta vår moln tjänst efter namn.</span><span class="sxs-lookup"><span data-stu-id="b6af0-111">Start Spring Cloud Service by name.</span></span>

### <span data-ttu-id="b6af0-112">Exempel 2: starta vår moln tjänst från en pipe.</span><span class="sxs-lookup"><span data-stu-id="b6af0-112">Example 2: Start Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Start-AzSpringCloud
```

<span data-ttu-id="b6af0-113">Starta vår moln tjänst från en pipe.</span><span class="sxs-lookup"><span data-stu-id="b6af0-113">Start Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="b6af0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6af0-114">PARAMETERS</span></span>

### <span data-ttu-id="b6af0-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="b6af0-115">-AppName</span></span>
<span data-ttu-id="b6af0-116">Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="b6af0-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="b6af0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6af0-117">-AsJob</span></span>
<span data-ttu-id="b6af0-118">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="b6af0-118">Run the command as a job</span></span>

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

### <span data-ttu-id="b6af0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6af0-119">-DefaultProfile</span></span>
<span data-ttu-id="b6af0-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b6af0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6af0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6af0-121">-InputObject</span></span>
<span data-ttu-id="b6af0-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="b6af0-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b6af0-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="b6af0-123">-Name</span></span>
<span data-ttu-id="b6af0-124">Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="b6af0-124">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="b6af0-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b6af0-125">-NoWait</span></span>
<span data-ttu-id="b6af0-126">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="b6af0-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b6af0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6af0-127">-PassThru</span></span>
<span data-ttu-id="b6af0-128">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="b6af0-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b6af0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6af0-129">-ResourceGroupName</span></span>
<span data-ttu-id="b6af0-130">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="b6af0-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b6af0-131">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="b6af0-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b6af0-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b6af0-132">-ServiceName</span></span>
<span data-ttu-id="b6af0-133">Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="b6af0-133">The name of the Service resource.</span></span>

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

### <span data-ttu-id="b6af0-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6af0-134">-SubscriptionId</span></span>
<span data-ttu-id="b6af0-135">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="b6af0-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b6af0-136">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="b6af0-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b6af0-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b6af0-137">-Confirm</span></span>
<span data-ttu-id="b6af0-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b6af0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6af0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6af0-139">-WhatIf</span></span>
<span data-ttu-id="b6af0-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b6af0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6af0-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b6af0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6af0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6af0-142">CommonParameters</span></span>
<span data-ttu-id="b6af0-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6af0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6af0-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6af0-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6af0-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6af0-145">INPUTS</span></span>

### <span data-ttu-id="b6af0-146">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="b6af0-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="b6af0-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6af0-147">OUTPUTS</span></span>

### <span data-ttu-id="b6af0-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b6af0-148">System.Boolean</span></span>

## <span data-ttu-id="b6af0-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6af0-149">NOTES</span></span>

<span data-ttu-id="b6af0-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b6af0-150">ALIASES</span></span>

<span data-ttu-id="b6af0-151">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="b6af0-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b6af0-152">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="b6af0-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b6af0-153">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b6af0-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b6af0-154">INPUTOBJECT <ISpringCloudIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="b6af0-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b6af0-155">`[AppName <String>]`: Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="b6af0-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="b6af0-156">`[BindingName <String>]`: Namnet på bindnings resursen.</span><span class="sxs-lookup"><span data-stu-id="b6af0-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="b6af0-157">`[CertificateName <String>]`: Namnet på certifikat resursen.</span><span class="sxs-lookup"><span data-stu-id="b6af0-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="b6af0-158">`[DeploymentName <String>]`: Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="b6af0-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="b6af0-159">`[DomainName <String>]`: Namnet på den anpassade domän resursen.</span><span class="sxs-lookup"><span data-stu-id="b6af0-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="b6af0-160">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="b6af0-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b6af0-161">`[Location <String>]`: regionen</span><span class="sxs-lookup"><span data-stu-id="b6af0-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="b6af0-162">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="b6af0-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b6af0-163">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="b6af0-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b6af0-164">`[ServiceName <String>]`: Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="b6af0-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="b6af0-165">`[SubscriptionId <String>]`: Hämtar prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="b6af0-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="b6af0-166">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="b6af0-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b6af0-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6af0-167">RELATED LINKS</span></span>

