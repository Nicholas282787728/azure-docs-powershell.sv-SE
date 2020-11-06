---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/update-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
ms.openlocfilehash: 5fb8c8f71366dd9fd0a2c6b12fc023c1ce3ccf9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583139"
---
# <span data-ttu-id="add32-101">Update-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="add32-101">Update-AzureRmMlWebService</span></span>

## <span data-ttu-id="add32-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="add32-102">SYNOPSIS</span></span>
<span data-ttu-id="add32-103">Uppdaterar egenskaper för en befintlig webb tjänst resurs.</span><span class="sxs-lookup"><span data-stu-id="add32-103">Updates properties of an existing web service resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="add32-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="add32-104">SYNTAX</span></span>

### <span data-ttu-id="add32-105">UpdateFromParameters</span><span class="sxs-lookup"><span data-stu-id="add32-105">UpdateFromParameters</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="add32-106">UpdateFromObject</span><span class="sxs-lookup"><span data-stu-id="add32-106">UpdateFromObject</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="add32-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="add32-107">DESCRIPTION</span></span>
<span data-ttu-id="add32-108">Med Update-AzureRmMlWebService cmdlet kan du uppdatera icke-statiska egenskaper för en webb tjänst.</span><span class="sxs-lookup"><span data-stu-id="add32-108">The Update-AzureRmMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="add32-109">Cmdleten fungerar som en korrigerings åtgärd.</span><span class="sxs-lookup"><span data-stu-id="add32-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="add32-110">Skicka bara de egenskaper som du vill ändra.</span><span class="sxs-lookup"><span data-stu-id="add32-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="add32-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="add32-111">EXAMPLES</span></span>

### <span data-ttu-id="add32-112">--------------------------Exempel 1: argument för selektiv uppdatering--------------------------</span><span class="sxs-lookup"><span data-stu-id="add32-112">--------------------------  Example 1: Selective update arguments  --------------------------</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="add32-113">Här ändrar vi beskrivningen, den primära åtkomst tangenten och aktiverar diagnostikprogrammet för alla spårningar under körningen för webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="add32-113">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="add32-114">--------------------------Exempel 2: uppdatering baserad på en webb tjänst instans--------------------------</span><span class="sxs-lookup"><span data-stu-id="add32-114">--------------------------  Example 2: Update based on a web service instance  --------------------------</span></span>
```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="add32-115">I exemplet skapas först en webb tjänst definition som bara innehåller de fält som ska uppdateras och sedan anropar Update-AzureRmMlWebService för att tillämpa dem med hjälp av parametern ServiceUpdates.</span><span class="sxs-lookup"><span data-stu-id="add32-115">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzureRmMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="add32-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="add32-116">PARAMETERS</span></span>

### <span data-ttu-id="add32-117">-Till gångar</span><span class="sxs-lookup"><span data-stu-id="add32-117">-Assets</span></span>
<span data-ttu-id="add32-118">Den uppsättning till till gångar (till exempel moduler, data mängder) som utgör webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="add32-118">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

```yaml
Type: Hashtable
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="add32-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="add32-119">-DefaultProfile</span></span>
<span data-ttu-id="add32-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="add32-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="add32-121">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="add32-121">-Description</span></span>
<span data-ttu-id="add32-122">Det nya värdet för webb tjänstens beskrivning.</span><span class="sxs-lookup"><span data-stu-id="add32-122">The new value for the web service's description.</span></span>
<span data-ttu-id="add32-123">Detta visas i tjänstens Swagger API-schema.</span><span class="sxs-lookup"><span data-stu-id="add32-123">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: String
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="add32-124">-Diagnostik</span><span class="sxs-lookup"><span data-stu-id="add32-124">-Diagnostics</span></span>
<span data-ttu-id="add32-125">Inställningar som styr insamling av diagnos spår för webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="add32-125">The settings that control the diagnostics traces collection for the web service.</span></span>

```yaml
Type: DiagnosticsConfiguration
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="add32-126">-Force</span><span class="sxs-lookup"><span data-stu-id="add32-126">-Force</span></span>
<span data-ttu-id="add32-127">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="add32-127">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="add32-128">-Inmatning</span><span class="sxs-lookup"><span data-stu-id="add32-128">-Input</span></span>
<span data-ttu-id="add32-129">Definitionen för webb tjänstens indata, som Swagger schema konstruktion.</span><span class="sxs-lookup"><span data-stu-id="add32-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="add32-130">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="add32-130">-IsReadOnly</span></span>
<span data-ttu-id="add32-131">Anger att den här webb tjänsten är skrivskyddad.</span><span class="sxs-lookup"><span data-stu-id="add32-131">Specifies that this web serviceis readonly.</span></span>
<span data-ttu-id="add32-132">När du har angett kan webb tjänsten längre uppdateras, inklusive ändring av värdet för den här egenskapen och kan bara tas bort.</span><span class="sxs-lookup"><span data-stu-id="add32-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="add32-133">-Tangenter</span><span class="sxs-lookup"><span data-stu-id="add32-133">-Keys</span></span>
<span data-ttu-id="add32-134">Uppdaterar en eller båda åtkomst nycklar som används för att autentisera samtal i tjänstens runtime API: er.</span><span class="sxs-lookup"><span data-stu-id="add32-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

```yaml
Type: WebServiceKeys
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="add32-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="add32-135">-Name</span></span>
<span data-ttu-id="add32-136">Namnet på webb tjänst resursen som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="add32-136">The name of the web service resource to be updated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="add32-137">-Utdata</span><span class="sxs-lookup"><span data-stu-id="add32-137">-Output</span></span>
<span data-ttu-id="add32-138">Definitionen för webb tjänstens resultat, som Swagger schema konstruktion.</span><span class="sxs-lookup"><span data-stu-id="add32-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="add32-139">-Paketera</span><span class="sxs-lookup"><span data-stu-id="add32-139">-Package</span></span>
<span data-ttu-id="add32-140">Definitionen av grafsystemet som definierar den här webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="add32-140">The definition of the graph package that defines this web service.</span></span>

```yaml
Type: GraphPackage
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="add32-141">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="add32-141">-Parameters</span></span>
<span data-ttu-id="add32-142">Uppsättningen globala parameter värden som har definierats för webb tjänsten, med namn som standard för globala parametrar \> .</span><span class="sxs-lookup"><span data-stu-id="add32-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="add32-143">Om inget standardvärde anges anses parametern vara obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="add32-143">If no default value is specified, the parameter is considered to be required.</span></span>

```yaml
Type: Hashtable
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="add32-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="add32-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="add32-145">Uppdateringar för konfiguration av tjänstens slut punkt för tjänste tid.</span><span class="sxs-lookup"><span data-stu-id="add32-145">Updates for the configuration of the service's realtime endpoint.</span></span>

```yaml
Type: RealtimeConfiguration
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="add32-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="add32-146">-ResourceGroupName</span></span>
<span data-ttu-id="add32-147">Resurs gruppen som innehåller webb tjänsten som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="add32-147">The resource group that contains the web service to be updated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="add32-148">-ServiceUpdates</span><span class="sxs-lookup"><span data-stu-id="add32-148">-ServiceUpdates</span></span>
<span data-ttu-id="add32-149">En uppsättning uppdateringar som ska tillämpas på webb tjänsten som tillhandahålls som webb tjänst definitions instans.</span><span class="sxs-lookup"><span data-stu-id="add32-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="add32-150">Endast icke-statiska fält ändras.</span><span class="sxs-lookup"><span data-stu-id="add32-150">Only non-static fields are modified.</span></span>

```yaml
Type: WebService
Parameter Sets: UpdateFromObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="add32-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="add32-151">-StorageAccountKey</span></span>
<span data-ttu-id="add32-152">Roterar snabb tangenten för det lagrings konto som är associerat med webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="add32-152">Rotates the access key for the storage account associated with the web service.</span></span>

```yaml
Type: String
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="add32-153">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="add32-153">-Title</span></span>
<span data-ttu-id="add32-154">Det nya värdet för webb tjänstens titel.</span><span class="sxs-lookup"><span data-stu-id="add32-154">The new value for the web service's title.</span></span>
<span data-ttu-id="add32-155">Detta visas i tjänstens Swagger API-schema.</span><span class="sxs-lookup"><span data-stu-id="add32-155">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: String
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="add32-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="add32-156">-Confirm</span></span>
<span data-ttu-id="add32-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="add32-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="add32-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="add32-158">-WhatIf</span></span>
<span data-ttu-id="add32-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="add32-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="add32-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="add32-160">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="add32-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="add32-161">CommonParameters</span></span>
<span data-ttu-id="add32-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="add32-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="add32-163">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="add32-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="add32-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="add32-164">INPUTS</span></span>

### <span data-ttu-id="add32-165">Webb tjänst</span><span class="sxs-lookup"><span data-stu-id="add32-165">WebService</span></span>
<span data-ttu-id="add32-166">Parametern ' ServiceUpdates ' godkänner värdet för typen "WebService" från pipeline</span><span class="sxs-lookup"><span data-stu-id="add32-166">Parameter 'ServiceUpdates' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="add32-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="add32-167">OUTPUTS</span></span>

### <span data-ttu-id="add32-168">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="add32-168">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="add32-169">En sammanfattning av Azure Machine Learning web service.</span><span class="sxs-lookup"><span data-stu-id="add32-169">A summary description of the Azure Machine Learning web service.</span></span>
<span data-ttu-id="add32-170">Liknar beskrivningen som returneras när du anropar Get-AzureRmMlWebService cmdlet på en befintlig webb tjänst.</span><span class="sxs-lookup"><span data-stu-id="add32-170">Similar to the description returned by calling the Get-AzureRmMlWebService cmdlet on an existing web service.</span></span>
<span data-ttu-id="add32-171">Den här beskrivningen innehåller inte känsliga egenskaper som lagrings kontots autentiseringsuppgifter och tjänstens åtkomst nycklar.</span><span class="sxs-lookup"><span data-stu-id="add32-171">This description does not contain sensitive properties such as storage account's credentials and the service's access keys.</span></span>

## <span data-ttu-id="add32-172">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="add32-172">NOTES</span></span>
<span data-ttu-id="add32-173">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="add32-173">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="add32-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="add32-174">RELATED LINKS</span></span>

