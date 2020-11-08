---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
ms.openlocfilehash: f91747d7c48521a9a14906cd873df564fadc4aa7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103492"
---
# <span data-ttu-id="da890-101">Remove-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="da890-101">Remove-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="da890-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="da890-102">SYNOPSIS</span></span>
<span data-ttu-id="da890-103">Åtgärd för att ta bort en distribution.</span><span class="sxs-lookup"><span data-stu-id="da890-103">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="da890-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="da890-104">SYNTAX</span></span>

### <span data-ttu-id="da890-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="da890-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="da890-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="da890-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="da890-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="da890-107">DESCRIPTION</span></span>
<span data-ttu-id="da890-108">Åtgärd för att ta bort en distribution.</span><span class="sxs-lookup"><span data-stu-id="da890-108">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="da890-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="da890-109">EXAMPLES</span></span>

### <span data-ttu-id="da890-110">Exempel 1: ta bort vår moln distribution efter namn.</span><span class="sxs-lookup"><span data-stu-id="da890-110">Example 1: Remove Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="da890-111">Ta bort vår moln distribution efter namn.</span><span class="sxs-lookup"><span data-stu-id="da890-111">Remove Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="da890-112">Exempel 2: ta bort vår moln distribution från pipe.</span><span class="sxs-lookup"><span data-stu-id="da890-112">Example 2: Remove Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Remove-AzSpringCloudAppDeployment
```

<span data-ttu-id="da890-113">Ta bort vår moln distribution från pipe.</span><span class="sxs-lookup"><span data-stu-id="da890-113">Remove Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="da890-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="da890-114">PARAMETERS</span></span>

### <span data-ttu-id="da890-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="da890-115">-AppName</span></span>
<span data-ttu-id="da890-116">Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="da890-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da890-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da890-117">-DefaultProfile</span></span>
<span data-ttu-id="da890-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="da890-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da890-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da890-119">-InputObject</span></span>
<span data-ttu-id="da890-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="da890-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da890-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="da890-121">-Name</span></span>
<span data-ttu-id="da890-122">Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="da890-122">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da890-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da890-123">-PassThru</span></span>
<span data-ttu-id="da890-124">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="da890-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="da890-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da890-125">-ResourceGroupName</span></span>
<span data-ttu-id="da890-126">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="da890-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="da890-127">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="da890-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da890-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="da890-128">-ServiceName</span></span>
<span data-ttu-id="da890-129">Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="da890-129">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da890-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da890-130">-SubscriptionId</span></span>
<span data-ttu-id="da890-131">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="da890-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="da890-132">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="da890-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da890-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="da890-133">-Confirm</span></span>
<span data-ttu-id="da890-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="da890-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da890-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da890-135">-WhatIf</span></span>
<span data-ttu-id="da890-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="da890-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da890-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="da890-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da890-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da890-138">CommonParameters</span></span>
<span data-ttu-id="da890-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da890-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da890-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da890-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da890-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="da890-141">INPUTS</span></span>

### <span data-ttu-id="da890-142">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="da890-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="da890-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="da890-143">OUTPUTS</span></span>

### <span data-ttu-id="da890-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="da890-144">System.Boolean</span></span>

## <span data-ttu-id="da890-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="da890-145">NOTES</span></span>

<span data-ttu-id="da890-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="da890-146">ALIASES</span></span>

<span data-ttu-id="da890-147">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="da890-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="da890-148">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="da890-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="da890-149">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="da890-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="da890-150">INPUTOBJECT <ISpringCloudIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="da890-150">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="da890-151">`[AppName <String>]`: Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="da890-151">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="da890-152">`[BindingName <String>]`: Namnet på bindnings resursen.</span><span class="sxs-lookup"><span data-stu-id="da890-152">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="da890-153">`[CertificateName <String>]`: Namnet på certifikat resursen.</span><span class="sxs-lookup"><span data-stu-id="da890-153">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="da890-154">`[DeploymentName <String>]`: Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="da890-154">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="da890-155">`[DomainName <String>]`: Namnet på den anpassade domän resursen.</span><span class="sxs-lookup"><span data-stu-id="da890-155">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="da890-156">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="da890-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="da890-157">`[Location <String>]`: regionen</span><span class="sxs-lookup"><span data-stu-id="da890-157">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="da890-158">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="da890-158">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="da890-159">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="da890-159">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="da890-160">`[ServiceName <String>]`: Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="da890-160">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="da890-161">`[SubscriptionId <String>]`: Hämtar prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="da890-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="da890-162">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="da890-162">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="da890-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="da890-163">RELATED LINKS</span></span>

