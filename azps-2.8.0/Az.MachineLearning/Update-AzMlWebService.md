---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
ms.openlocfilehash: a4c8e2687fd525b32ef3a9da3684a3da9f3c5717
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743676"
---
# <span data-ttu-id="db662-101">Update-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="db662-101">Update-AzMlWebService</span></span>

## <span data-ttu-id="db662-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db662-102">SYNOPSIS</span></span>
<span data-ttu-id="db662-103">Uppdaterar egenskaper för en befintlig webb tjänst resurs.</span><span class="sxs-lookup"><span data-stu-id="db662-103">Updates properties of an existing web service resource.</span></span>

## <span data-ttu-id="db662-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db662-104">SYNTAX</span></span>

### <span data-ttu-id="db662-105">UpdateFromParameters</span><span class="sxs-lookup"><span data-stu-id="db662-105">UpdateFromParameters</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db662-106">UpdateFromObject</span><span class="sxs-lookup"><span data-stu-id="db662-106">UpdateFromObject</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db662-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db662-107">DESCRIPTION</span></span>
<span data-ttu-id="db662-108">Med Update-AzMlWebService cmdlet kan du uppdatera icke-statiska egenskaper för en webb tjänst.</span><span class="sxs-lookup"><span data-stu-id="db662-108">The Update-AzMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="db662-109">Cmdleten fungerar som en korrigerings åtgärd.</span><span class="sxs-lookup"><span data-stu-id="db662-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="db662-110">Skicka bara de egenskaper som du vill ändra.</span><span class="sxs-lookup"><span data-stu-id="db662-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="db662-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db662-111">EXAMPLES</span></span>

### <span data-ttu-id="db662-112">Exempel 1: argument för selektiv uppdatering</span><span class="sxs-lookup"><span data-stu-id="db662-112">Example 1: Selective update arguments</span></span>
```
Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="db662-113">Här ändrar vi beskrivningen, den primära åtkomst tangenten och aktiverar diagnostikprogrammet för alla spårningar under körningen för webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="db662-113">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="db662-114">Exempel 2: uppdatering baserad på en webb tjänst instans</span><span class="sxs-lookup"><span data-stu-id="db662-114">Example 2: Update based on a web service instance</span></span>
```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="db662-115">I exemplet skapas först en webb tjänst definition som bara innehåller de fält som ska uppdateras och sedan anropar Update-AzMlWebService för att tillämpa dem med hjälp av parametern ServiceUpdates.</span><span class="sxs-lookup"><span data-stu-id="db662-115">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="db662-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db662-116">PARAMETERS</span></span>

### <span data-ttu-id="db662-117">-Till gångar</span><span class="sxs-lookup"><span data-stu-id="db662-117">-Assets</span></span>
<span data-ttu-id="db662-118">Den uppsättning till till gångar (till exempel moduler, data mängder) som utgör webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="db662-118">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db662-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db662-119">-DefaultProfile</span></span>
<span data-ttu-id="db662-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="db662-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db662-121">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="db662-121">-Description</span></span>
<span data-ttu-id="db662-122">Det nya värdet för webb tjänstens beskrivning.</span><span class="sxs-lookup"><span data-stu-id="db662-122">The new value for the web service's description.</span></span>
<span data-ttu-id="db662-123">Detta visas i tjänstens Swagger API-schema.</span><span class="sxs-lookup"><span data-stu-id="db662-123">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db662-124">-Diagnostik</span><span class="sxs-lookup"><span data-stu-id="db662-124">-Diagnostics</span></span>
<span data-ttu-id="db662-125">Inställningar som styr insamling av diagnos spår för webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="db662-125">The settings that control the diagnostics traces collection for the web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.DiagnosticsConfiguration
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db662-126">-Force</span><span class="sxs-lookup"><span data-stu-id="db662-126">-Force</span></span>
<span data-ttu-id="db662-127">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="db662-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="db662-128">-Inmatning</span><span class="sxs-lookup"><span data-stu-id="db662-128">-Input</span></span>
<span data-ttu-id="db662-129">Definitionen för webb tjänstens indata, som Swagger schema konstruktion.</span><span class="sxs-lookup"><span data-stu-id="db662-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db662-130">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="db662-130">-IsReadOnly</span></span>
<span data-ttu-id="db662-131">Anger att den här webb tjänsten är skrivskyddad.</span><span class="sxs-lookup"><span data-stu-id="db662-131">Specifies that this web service is readonly.</span></span>
<span data-ttu-id="db662-132">När du har angett kan webb tjänsten längre uppdateras, inklusive ändring av värdet för den här egenskapen och kan bara tas bort.</span><span class="sxs-lookup"><span data-stu-id="db662-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db662-133">-Tangenter</span><span class="sxs-lookup"><span data-stu-id="db662-133">-Keys</span></span>
<span data-ttu-id="db662-134">Uppdaterar en eller båda åtkomst nycklar som används för att autentisera samtal i tjänstens runtime API: er.</span><span class="sxs-lookup"><span data-stu-id="db662-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db662-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="db662-135">-Name</span></span>
<span data-ttu-id="db662-136">Namnet på webb tjänst resursen som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="db662-136">The name of the web service resource to be updated.</span></span>

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

### <span data-ttu-id="db662-137">-Utdata</span><span class="sxs-lookup"><span data-stu-id="db662-137">-Output</span></span>
<span data-ttu-id="db662-138">Definitionen för webb tjänstens resultat, som Swagger schema konstruktion.</span><span class="sxs-lookup"><span data-stu-id="db662-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db662-139">-Paketera</span><span class="sxs-lookup"><span data-stu-id="db662-139">-Package</span></span>
<span data-ttu-id="db662-140">Definitionen av grafsystemet som definierar den här webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="db662-140">The definition of the graph package that defines this web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.GraphPackage
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db662-141">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="db662-141">-Parameters</span></span>
<span data-ttu-id="db662-142">Uppsättningen globala parameter värden som har definierats för webb tjänsten, med namn som standard för globala parametrar \> .</span><span class="sxs-lookup"><span data-stu-id="db662-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="db662-143">Om inget standardvärde anges anses parametern vara obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="db662-143">If no default value is specified, the parameter is considered to be required.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db662-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="db662-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="db662-145">Uppdateringar för konfiguration av tjänstens slut punkt för tjänste tid.</span><span class="sxs-lookup"><span data-stu-id="db662-145">Updates for the configuration of the service's realtime endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.RealtimeConfiguration
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db662-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db662-146">-ResourceGroupName</span></span>
<span data-ttu-id="db662-147">Resurs gruppen som innehåller webb tjänsten som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="db662-147">The resource group that contains the web service to be updated.</span></span>

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

### <span data-ttu-id="db662-148">-ServiceUpdates</span><span class="sxs-lookup"><span data-stu-id="db662-148">-ServiceUpdates</span></span>
<span data-ttu-id="db662-149">En uppsättning uppdateringar som ska tillämpas på webb tjänsten som tillhandahålls som webb tjänst definitions instans.</span><span class="sxs-lookup"><span data-stu-id="db662-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="db662-150">Endast icke-statiska fält ändras.</span><span class="sxs-lookup"><span data-stu-id="db662-150">Only non-static fields are modified.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: UpdateFromObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db662-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="db662-151">-StorageAccountKey</span></span>
<span data-ttu-id="db662-152">Roterar snabb tangenten för det lagrings konto som är associerat med webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="db662-152">Rotates the access key for the storage account associated with the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db662-153">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="db662-153">-Title</span></span>
<span data-ttu-id="db662-154">Det nya värdet för webb tjänstens titel.</span><span class="sxs-lookup"><span data-stu-id="db662-154">The new value for the web service's title.</span></span>
<span data-ttu-id="db662-155">Detta visas i tjänstens Swagger API-schema.</span><span class="sxs-lookup"><span data-stu-id="db662-155">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db662-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="db662-156">-Confirm</span></span>
<span data-ttu-id="db662-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="db662-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db662-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db662-158">-WhatIf</span></span>
<span data-ttu-id="db662-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="db662-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db662-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="db662-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db662-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db662-161">CommonParameters</span></span>
<span data-ttu-id="db662-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db662-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db662-163">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db662-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db662-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db662-164">INPUTS</span></span>

### <span data-ttu-id="db662-165">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="db662-165">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="db662-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db662-166">OUTPUTS</span></span>

### <span data-ttu-id="db662-167">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="db662-167">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="db662-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db662-168">NOTES</span></span>
<span data-ttu-id="db662-169">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="db662-169">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="db662-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db662-170">RELATED LINKS</span></span>