---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
ms.openlocfilehash: 681cbc620a5c6067102dfe2a67f20dd9edc42046
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407144"
---
# <span data-ttu-id="838c9-101">Set-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="838c9-101">Set-AzTemplateSpec</span></span>

## <span data-ttu-id="838c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="838c9-102">SYNOPSIS</span></span>
<span data-ttu-id="838c9-103">Ändrar en mallens spec.</span><span class="sxs-lookup"><span data-stu-id="838c9-103">Modifies a Template Spec.</span></span>

## <span data-ttu-id="838c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="838c9-104">SYNTAX</span></span>

### <span data-ttu-id="838c9-105">FromJsonStringParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="838c9-105">FromJsonStringParameterSet (Default)</span></span>
```
Set-AzTemplateSpec [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="838c9-106">UpdateByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="838c9-106">UpdateByIdParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> [-Description <String>] [-DisplayName <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="838c9-107">UpdateVersionByIdFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="838c9-107">UpdateVersionByIdFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="838c9-108">UpdateVersionByIdFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="838c9-108">UpdateVersionByIdFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="838c9-109">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="838c9-109">UpdateByNameParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="838c9-110">UpdateVersionByNameFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="838c9-110">UpdateVersionByNameFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="838c9-111">UpdateVersionByNameFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="838c9-111">UpdateVersionByNameFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="838c9-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="838c9-112">DESCRIPTION</span></span>
<span data-ttu-id="838c9-113">Ändrar en Templace-spec. Om det angivna namnet och/eller den specifika versionen av mallen inte redan finns skapas den.</span><span class="sxs-lookup"><span data-stu-id="838c9-113">Modifies a Templace Spec. If the Template Spec with the specified name and/or specific version does not already exist, it will be created.</span></span>

<span data-ttu-id="838c9-114">När du ändrar innehållet i en mal Linies spec-mall kan innehållet antingen komma från en RAW JSON-sträng (med **UpdateVersionByNameFromJsonParameterSet** parameter uppsättning) eller från en angiven JSON-fil (med **UpdateVersionByNameFromJsonFileParameterSet** parameter uppsättning).</span><span class="sxs-lookup"><span data-stu-id="838c9-114">When modifying a Template Spec version's ARM Template content, the content can either come from a raw JSON string (using **UpdateVersionByNameFromJsonParameterSet** parameter set) or from a specified JSON file (using **UpdateVersionByNameFromJsonFileParameterSet** parameter set).</span></span>

## <span data-ttu-id="838c9-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="838c9-115">EXAMPLES</span></span>

### <span data-ttu-id="838c9-116">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="838c9-116">Example 1:</span></span>
```powershell
PS C:\> $templateJson = @"
{
    "$schema": "http://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "resources": []
}
"@
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v1.0' -Location 'West US' -TemplateJson $templateJson
```

<span data-ttu-id="838c9-117">Ändrar version "v 1.0" för en mall med namnet "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="838c9-117">Modifies version "v1.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="838c9-118">Den angivna versionen är $templateJson som versions mal len för ARM-mallen.</span><span class="sxs-lookup"><span data-stu-id="838c9-118">The specified version will have $templateJson as the version's ARM Template content.</span></span> <span data-ttu-id="838c9-119">Om specifikation och/eller version av rot mal len inte redan finns kommer de att skapas.</span><span class="sxs-lookup"><span data-stu-id="838c9-119">If the root Template Spec and/or version do not already exist they will be created.</span></span>


<span data-ttu-id="838c9-120">**Anmärkningar**</span><span class="sxs-lookup"><span data-stu-id="838c9-120">**Notes:**</span></span> 

* <span data-ttu-id="838c9-121">Mallen ARM i exemplet är inte en-op eftersom den inte innehåller några faktiska resurser.</span><span class="sxs-lookup"><span data-stu-id="838c9-121">The ARM Template in the example is a no-op as it contains no actual resources.</span></span>
* <span data-ttu-id="838c9-122">Plats är endast nödvändig när mallen för mallar inte redan finns</span><span class="sxs-lookup"><span data-stu-id="838c9-122">Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="838c9-123">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="838c9-123">Example 2:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="838c9-124">Ändrar version "v 2.0" för en mall med namnet "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="838c9-124">Modifies version "v2.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="838c9-125">Den angivna versionen kommer att få innehållet från den lokala filen "myTemplateContent.jspå" som versionens ARM-mallens innehåll.</span><span class="sxs-lookup"><span data-stu-id="838c9-125">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span> <span data-ttu-id="838c9-126">Om specifikation och/eller version av rot mal len inte redan finns kommer de att skapas.</span><span class="sxs-lookup"><span data-stu-id="838c9-126">If the root Template Spec and/or version do not already exist they will be created.</span></span>

<span data-ttu-id="838c9-127">**Obs!** Plats är endast nödvändig när mallen för mallar inte redan finns</span><span class="sxs-lookup"><span data-stu-id="838c9-127">**Note:** Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="838c9-128">Exempel 3:</span><span class="sxs-lookup"><span data-stu-id="838c9-128">Example 3:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec'  -Location 'West US' -Description 'My updated Template Spec'
```

<span data-ttu-id="838c9-129">Ändrar beskrivningen av mallen "myTemplateSpec" i resurs gruppen "myRG".</span><span class="sxs-lookup"><span data-stu-id="838c9-129">Modifies the description of the Template Spec named "myTemplateSpec" in resource group "myRG".</span></span> <span data-ttu-id="838c9-130">Om mallens spec inte redan finns kommer den att skapas.</span><span class="sxs-lookup"><span data-stu-id="838c9-130">If the Template Spec does not already exist it will be created.</span></span>

<span data-ttu-id="838c9-131">**Obs!** Plats är endast nödvändig när mallen för mallar inte redan finns</span><span class="sxs-lookup"><span data-stu-id="838c9-131">**Note:** Location is only required when the Template Spec does not already exist</span></span>

## <span data-ttu-id="838c9-132">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="838c9-132">PARAMETERS</span></span>

### <span data-ttu-id="838c9-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="838c9-133">-DefaultProfile</span></span>
<span data-ttu-id="838c9-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="838c9-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="838c9-135">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="838c9-135">-Description</span></span>
<span data-ttu-id="838c9-136">Beskrivningen av mallens spec.</span><span class="sxs-lookup"><span data-stu-id="838c9-136">The description of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838c9-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="838c9-137">-DisplayName</span></span>
<span data-ttu-id="838c9-138">Visnings namnet på mallens spec.</span><span class="sxs-lookup"><span data-stu-id="838c9-138">The display name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838c9-139">-Plats</span><span class="sxs-lookup"><span data-stu-id="838c9-139">-Location</span></span>
<span data-ttu-id="838c9-140">Platsen för mallens spec. Endast obligatoriskt om mallens spec inte redan finns.</span><span class="sxs-lookup"><span data-stu-id="838c9-140">The location of the template spec. Only required if the template spec does not already exist.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838c9-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="838c9-141">-Name</span></span>
<span data-ttu-id="838c9-142">Namnet på mallens spec.</span><span class="sxs-lookup"><span data-stu-id="838c9-142">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838c9-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="838c9-143">-ResourceGroupName</span></span>
<span data-ttu-id="838c9-144">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="838c9-144">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838c9-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="838c9-145">-ResourceId</span></span>
<span data-ttu-id="838c9-146">Fullständigt resurs-ID för mallens spec. exempel:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="838c9-146">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838c9-147">-Tagg</span><span class="sxs-lookup"><span data-stu-id="838c9-147">-Tag</span></span>
<span data-ttu-id="838c9-148">En webb förteckning med taggar för specifikationer och/eller version för mallen</span><span class="sxs-lookup"><span data-stu-id="838c9-148">Hashtable of tags for the template spec and/or version</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="838c9-149">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="838c9-149">-TemplateFile</span></span>
<span data-ttu-id="838c9-150">Fil Sök vägen till den lokala Azure Resource Manager-mallens JSON-fil.</span><span class="sxs-lookup"><span data-stu-id="838c9-150">The file path to the local Azure Resource Manager template JSON file.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByNameFromJsonFileParameterSet
Aliases: InputFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838c9-151">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="838c9-151">-TemplateJson</span></span>
<span data-ttu-id="838c9-152">Azure Resource Manager-mallens JSON.</span><span class="sxs-lookup"><span data-stu-id="838c9-152">The Azure Resource Manager template JSON.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838c9-153">-Version</span><span class="sxs-lookup"><span data-stu-id="838c9-153">-Version</span></span>
<span data-ttu-id="838c9-154">Versionen av mallens spec.</span><span class="sxs-lookup"><span data-stu-id="838c9-154">The version of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838c9-155">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="838c9-155">-VersionDescription</span></span>
<span data-ttu-id="838c9-156">Beskrivning av versionen.</span><span class="sxs-lookup"><span data-stu-id="838c9-156">The description of the version.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838c9-157">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="838c9-157">-Confirm</span></span>
<span data-ttu-id="838c9-158">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="838c9-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="838c9-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="838c9-159">-WhatIf</span></span>
<span data-ttu-id="838c9-160">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="838c9-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="838c9-161">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="838c9-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="838c9-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="838c9-162">CommonParameters</span></span>
<span data-ttu-id="838c9-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="838c9-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="838c9-164">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="838c9-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="838c9-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="838c9-165">INPUTS</span></span>

### <span data-ttu-id="838c9-166">System. String</span><span class="sxs-lookup"><span data-stu-id="838c9-166">System.String</span></span>

## <span data-ttu-id="838c9-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="838c9-167">OUTPUTS</span></span>

### <span data-ttu-id="838c9-168">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="838c9-168">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="838c9-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="838c9-169">NOTES</span></span>

## <span data-ttu-id="838c9-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="838c9-170">RELATED LINKS</span></span>
