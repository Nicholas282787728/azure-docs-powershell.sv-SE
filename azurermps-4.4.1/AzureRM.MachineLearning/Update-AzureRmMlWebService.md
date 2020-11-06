---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
ms.openlocfilehash: 75f94e5c93f81fa88dd33c3c0b94cb2b36ca291f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580575"
---
# <span data-ttu-id="c9303-101">Update-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="c9303-101">Update-AzureRmMlWebService</span></span>

## <span data-ttu-id="c9303-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c9303-102">SYNOPSIS</span></span>
<span data-ttu-id="c9303-103">Uppdaterar egenskaper för en befintlig webb tjänst resurs.</span><span class="sxs-lookup"><span data-stu-id="c9303-103">Updates properties of an existing web service resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9303-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c9303-104">SYNTAX</span></span>

### <span data-ttu-id="c9303-105">Uppdatera specifika egenskaper för.</span><span class="sxs-lookup"><span data-stu-id="c9303-105">Update specific properties of the .</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9303-106">Skapa en ny Azure ML-webtjänst från en webb tjänst instans definition.</span><span class="sxs-lookup"><span data-stu-id="c9303-106">Create a new Azure ML webservice from a WebService instance definition.</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9303-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c9303-107">DESCRIPTION</span></span>
<span data-ttu-id="c9303-108">Med Update-AzureRmMlWebService cmdlet kan du uppdatera icke-statiska egenskaper för en webb tjänst.</span><span class="sxs-lookup"><span data-stu-id="c9303-108">The Update-AzureRmMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="c9303-109">Cmdleten fungerar som en korrigerings åtgärd.</span><span class="sxs-lookup"><span data-stu-id="c9303-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="c9303-110">Skicka bara de egenskaper som du vill ändra.</span><span class="sxs-lookup"><span data-stu-id="c9303-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="c9303-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c9303-111">EXAMPLES</span></span>

### <span data-ttu-id="c9303-112">--------------------------Exempel 1: argument för selektiv uppdatering--------------------------</span><span class="sxs-lookup"><span data-stu-id="c9303-112">--------------------------  Example 1: Selective update arguments  --------------------------</span></span>
<span data-ttu-id="c9303-113">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="c9303-113">@{paragraph=PS C:\\\>}</span></span>





```
Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="c9303-114">Här ändrar vi beskrivningen, den primära åtkomst tangenten och aktiverar diagnostikprogrammet för alla spårningar under körningen för webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c9303-114">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="c9303-115">--------------------------Exempel 2: uppdatering baserad på en webb tjänst instans--------------------------</span><span class="sxs-lookup"><span data-stu-id="c9303-115">--------------------------  Example 2: Update based on a web service instance  --------------------------</span></span>
<span data-ttu-id="c9303-116">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="c9303-116">@{paragraph=PS C:\\\>}</span></span>





```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="c9303-117">I exemplet skapas först en webb tjänst definition som bara innehåller de fält som ska uppdateras och sedan anropar Update-AzureRmMlWebService för att tillämpa dem med hjälp av parametern ServiceUpdates.</span><span class="sxs-lookup"><span data-stu-id="c9303-117">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzureRmMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="c9303-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c9303-118">PARAMETERS</span></span>

### <span data-ttu-id="c9303-119">-Till gångar</span><span class="sxs-lookup"><span data-stu-id="c9303-119">-Assets</span></span>
<span data-ttu-id="c9303-120">Den uppsättning till till gångar (till exempel moduler, data mängder) som utgör webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c9303-120">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9303-121">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="c9303-121">-Description</span></span>
<span data-ttu-id="c9303-122">Det nya värdet för webb tjänstens beskrivning.</span><span class="sxs-lookup"><span data-stu-id="c9303-122">The new value for the web service's description.</span></span>
<span data-ttu-id="c9303-123">Detta visas i tjänstens Swagger API-schema.</span><span class="sxs-lookup"><span data-stu-id="c9303-123">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9303-124">-Diagnostik</span><span class="sxs-lookup"><span data-stu-id="c9303-124">-Diagnostics</span></span>
<span data-ttu-id="c9303-125">Inställningar som styr insamling av diagnos spår för webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c9303-125">The settings that control the diagnostics traces collection for the web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.DiagnosticsConfiguration
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9303-126">-Force</span><span class="sxs-lookup"><span data-stu-id="c9303-126">-Force</span></span>
<span data-ttu-id="c9303-127">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c9303-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c9303-128">-Inmatning</span><span class="sxs-lookup"><span data-stu-id="c9303-128">-Input</span></span>
<span data-ttu-id="c9303-129">Definitionen för webb tjänstens indata, som Swagger schema konstruktion.</span><span class="sxs-lookup"><span data-stu-id="c9303-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9303-130">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="c9303-130">-IsReadOnly</span></span>
<span data-ttu-id="c9303-131">Anger att den här webb tjänsten är skrivskyddad.</span><span class="sxs-lookup"><span data-stu-id="c9303-131">Specifies that this web serviceis readonly.</span></span>
<span data-ttu-id="c9303-132">När du har angett kan webb tjänsten längre uppdateras, inklusive ändring av värdet för den här egenskapen och kan bara tas bort.</span><span class="sxs-lookup"><span data-stu-id="c9303-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9303-133">-Tangenter</span><span class="sxs-lookup"><span data-stu-id="c9303-133">-Keys</span></span>
<span data-ttu-id="c9303-134">Uppdaterar en eller båda åtkomst nycklar som används för att autentisera samtal i tjänstens runtime API: er.</span><span class="sxs-lookup"><span data-stu-id="c9303-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9303-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="c9303-135">-Name</span></span>
<span data-ttu-id="c9303-136">Namnet på webb tjänst resursen som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="c9303-136">The name of the web service resource to be updated.</span></span>

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

### <span data-ttu-id="c9303-137">-Utdata</span><span class="sxs-lookup"><span data-stu-id="c9303-137">-Output</span></span>
<span data-ttu-id="c9303-138">Definitionen för webb tjänstens resultat, som Swagger schema konstruktion.</span><span class="sxs-lookup"><span data-stu-id="c9303-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9303-139">-Paketera</span><span class="sxs-lookup"><span data-stu-id="c9303-139">-Package</span></span>
<span data-ttu-id="c9303-140">Definitionen av grafsystemet som definierar den här webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c9303-140">The definition of the graph package that defines this web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.GraphPackage
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9303-141">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="c9303-141">-Parameters</span></span>
<span data-ttu-id="c9303-142">Uppsättningen globala parameter värden som har definierats för webb tjänsten, med namn som standard för globala parametrar \> .</span><span class="sxs-lookup"><span data-stu-id="c9303-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="c9303-143">Om inget standardvärde anges anses parametern vara obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="c9303-143">If no default value is specified, the parameter is considered to be required.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9303-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9303-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="c9303-145">Uppdateringar för konfiguration av tjänstens slut punkt för tjänste tid.</span><span class="sxs-lookup"><span data-stu-id="c9303-145">Updates for the configuration of the service's realtime endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.RealtimeConfiguration
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9303-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9303-146">-ResourceGroupName</span></span>
<span data-ttu-id="c9303-147">Resurs gruppen som innehåller webb tjänsten som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="c9303-147">The resource group that contains the web service to be updated.</span></span>

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

### <span data-ttu-id="c9303-148">-ServiceUpdates</span><span class="sxs-lookup"><span data-stu-id="c9303-148">-ServiceUpdates</span></span>
<span data-ttu-id="c9303-149">En uppsättning uppdateringar som ska tillämpas på webb tjänsten som tillhandahålls som webb tjänst definitions instans.</span><span class="sxs-lookup"><span data-stu-id="c9303-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="c9303-150">Endast icke-statiska fält ändras.</span><span class="sxs-lookup"><span data-stu-id="c9303-150">Only non-static fields are modified.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Create a new Azure ML webservice from a WebService instance definition.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9303-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c9303-151">-StorageAccountKey</span></span>
<span data-ttu-id="c9303-152">Roterar snabb tangenten för det lagrings konto som är associerat med webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c9303-152">Rotates the access key for the storage account associated with the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9303-153">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="c9303-153">-Title</span></span>
<span data-ttu-id="c9303-154">Det nya värdet för webb tjänstens titel.</span><span class="sxs-lookup"><span data-stu-id="c9303-154">The new value for the web service's title.</span></span>
<span data-ttu-id="c9303-155">Detta visas i tjänstens Swagger API-schema.</span><span class="sxs-lookup"><span data-stu-id="c9303-155">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9303-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c9303-156">-Confirm</span></span>
<span data-ttu-id="c9303-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c9303-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9303-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9303-158">-WhatIf</span></span>
<span data-ttu-id="c9303-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c9303-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9303-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c9303-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9303-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9303-161">-DefaultProfile</span></span>
<span data-ttu-id="c9303-162">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c9303-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9303-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9303-163">CommonParameters</span></span>
<span data-ttu-id="c9303-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9303-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9303-165">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9303-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9303-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c9303-166">INPUTS</span></span>

### <span data-ttu-id="c9303-167">Webb tjänst</span><span class="sxs-lookup"><span data-stu-id="c9303-167">WebService</span></span>
<span data-ttu-id="c9303-168">Parametern ' ServiceUpdates ' godkänner värdet för typen "WebService" från pipeline</span><span class="sxs-lookup"><span data-stu-id="c9303-168">Parameter 'ServiceUpdates' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="c9303-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c9303-169">OUTPUTS</span></span>

### <span data-ttu-id="c9303-170">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="c9303-170">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="c9303-171">En sammanfattning av Azure Machine Learning web service.</span><span class="sxs-lookup"><span data-stu-id="c9303-171">A summary description of the Azure Machine Learning web service.</span></span>
<span data-ttu-id="c9303-172">Liknar beskrivningen som returneras när du anropar Get-AzureRmMlWebService cmdlet på en befintlig webb tjänst.</span><span class="sxs-lookup"><span data-stu-id="c9303-172">Similar to the description returned by calling the Get-AzureRmMlWebService cmdlet on an existing web service.</span></span>
<span data-ttu-id="c9303-173">Den här beskrivningen innehåller inte känsliga egenskaper som lagrings kontots autentiseringsuppgifter och tjänstens åtkomst nycklar.</span><span class="sxs-lookup"><span data-stu-id="c9303-173">This description does not contain sensitive properties such as storage account's credentials and the service's access keys.</span></span>

## <span data-ttu-id="c9303-174">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c9303-174">NOTES</span></span>
<span data-ttu-id="c9303-175">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="c9303-175">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="c9303-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c9303-176">RELATED LINKS</span></span>

