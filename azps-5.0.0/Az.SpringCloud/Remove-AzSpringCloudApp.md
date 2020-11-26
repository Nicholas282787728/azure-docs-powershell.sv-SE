---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
ms.openlocfilehash: e363a7bedc891c736f06b60c093483010e6b261d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94262953"
---
# <span data-ttu-id="68583-101">Remove-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="68583-101">Remove-AzSpringCloudApp</span></span>

## <span data-ttu-id="68583-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="68583-102">SYNOPSIS</span></span>
<span data-ttu-id="68583-103">Åtgärd att ta bort ett program.</span><span class="sxs-lookup"><span data-stu-id="68583-103">Operation to delete an App.</span></span>

## <span data-ttu-id="68583-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="68583-104">SYNTAX</span></span>

### <span data-ttu-id="68583-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="68583-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="68583-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="68583-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="68583-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="68583-107">DESCRIPTION</span></span>
<span data-ttu-id="68583-108">Åtgärd att ta bort ett program.</span><span class="sxs-lookup"><span data-stu-id="68583-108">Operation to delete an App.</span></span>

## <span data-ttu-id="68583-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="68583-109">EXAMPLES</span></span>

### <span data-ttu-id="68583-110">Exempel 1: ta bort programmet våren med namn.</span><span class="sxs-lookup"><span data-stu-id="68583-110">Example 1: Remove Spring Cloud App by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
```

<span data-ttu-id="68583-111">Ta bort vår moln app efter namn.</span><span class="sxs-lookup"><span data-stu-id="68583-111">Remove Spring Cloud App by name.</span></span>

### <span data-ttu-id="68583-112">Exempel 2: ta bort programmet våren från en pipe.</span><span class="sxs-lookup"><span data-stu-id="68583-112">Example 2: Remove Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Remove-AzSpringCloudApp
```

<span data-ttu-id="68583-113">Ta bort programmet våren från en pipe.</span><span class="sxs-lookup"><span data-stu-id="68583-113">Remove Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="68583-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="68583-114">PARAMETERS</span></span>

### <span data-ttu-id="68583-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68583-115">-AsJob</span></span>
<span data-ttu-id="68583-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="68583-116">Run the command as a job</span></span>

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

### <span data-ttu-id="68583-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68583-117">-DefaultProfile</span></span>
<span data-ttu-id="68583-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="68583-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68583-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68583-119">-InputObject</span></span>
<span data-ttu-id="68583-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="68583-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="68583-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="68583-121">-Name</span></span>
<span data-ttu-id="68583-122">Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="68583-122">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68583-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="68583-123">-NoWait</span></span>
<span data-ttu-id="68583-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="68583-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="68583-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68583-125">-PassThru</span></span>
<span data-ttu-id="68583-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="68583-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="68583-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68583-127">-ResourceGroupName</span></span>
<span data-ttu-id="68583-128">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="68583-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="68583-129">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="68583-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="68583-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="68583-130">-ServiceName</span></span>
<span data-ttu-id="68583-131">Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="68583-131">The name of the Service resource.</span></span>

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

### <span data-ttu-id="68583-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="68583-132">-SubscriptionId</span></span>
<span data-ttu-id="68583-133">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="68583-133">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="68583-134">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="68583-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="68583-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="68583-135">-Confirm</span></span>
<span data-ttu-id="68583-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="68583-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68583-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68583-137">-WhatIf</span></span>
<span data-ttu-id="68583-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="68583-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68583-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="68583-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68583-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68583-140">CommonParameters</span></span>
<span data-ttu-id="68583-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68583-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68583-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68583-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68583-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="68583-143">INPUTS</span></span>

### <span data-ttu-id="68583-144">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="68583-144">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="68583-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="68583-145">OUTPUTS</span></span>

### <span data-ttu-id="68583-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="68583-146">System.Boolean</span></span>

## <span data-ttu-id="68583-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="68583-147">NOTES</span></span>

<span data-ttu-id="68583-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="68583-148">ALIASES</span></span>

<span data-ttu-id="68583-149">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="68583-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="68583-150">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="68583-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="68583-151">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="68583-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="68583-152">INPUTOBJECT <ISpringCloudIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="68583-152">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="68583-153">`[AppName <String>]`: Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="68583-153">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="68583-154">`[BindingName <String>]`: Namnet på bindnings resursen.</span><span class="sxs-lookup"><span data-stu-id="68583-154">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="68583-155">`[CertificateName <String>]`: Namnet på certifikat resursen.</span><span class="sxs-lookup"><span data-stu-id="68583-155">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="68583-156">`[DeploymentName <String>]`: Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="68583-156">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="68583-157">`[DomainName <String>]`: Namnet på den anpassade domän resursen.</span><span class="sxs-lookup"><span data-stu-id="68583-157">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="68583-158">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="68583-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="68583-159">`[Location <String>]`: regionen</span><span class="sxs-lookup"><span data-stu-id="68583-159">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="68583-160">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="68583-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="68583-161">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="68583-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="68583-162">`[ServiceName <String>]`: Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="68583-162">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="68583-163">`[SubscriptionId <String>]`: Hämtar prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="68583-163">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="68583-164">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="68583-164">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="68583-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="68583-165">RELATED LINKS</span></span>
