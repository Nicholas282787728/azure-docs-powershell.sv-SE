---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
ms.openlocfilehash: ff2911c1fd8e49e5057c13c086f68a2b3489ad2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270268"
---
# <span data-ttu-id="e07ad-101">Set-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="e07ad-101">Set-AzTemplateSpec</span></span>

## <span data-ttu-id="e07ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e07ad-102">SYNOPSIS</span></span>
<span data-ttu-id="e07ad-103">Ändrar en mallens spec.</span><span class="sxs-lookup"><span data-stu-id="e07ad-103">Modifies a Template Spec.</span></span>

## <span data-ttu-id="e07ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e07ad-104">SYNTAX</span></span>

### <span data-ttu-id="e07ad-105">FromJsonStringParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e07ad-105">FromJsonStringParameterSet (Default)</span></span>
```
Set-AzTemplateSpec [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e07ad-106">UpdateByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e07ad-106">UpdateByIdParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> [-Description <String>] [-DisplayName <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e07ad-107">UpdateVersionByIdFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="e07ad-107">UpdateVersionByIdFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e07ad-108">UpdateVersionByIdFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="e07ad-108">UpdateVersionByIdFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e07ad-109">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e07ad-109">UpdateByNameParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e07ad-110">UpdateVersionByNameFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="e07ad-110">UpdateVersionByNameFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e07ad-111">UpdateVersionByNameFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="e07ad-111">UpdateVersionByNameFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e07ad-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e07ad-112">DESCRIPTION</span></span>
<span data-ttu-id="e07ad-113">Ändrar en Templace-spec. Om det angivna namnet och/eller den specifika versionen av mallen inte redan finns skapas den.</span><span class="sxs-lookup"><span data-stu-id="e07ad-113">Modifies a Templace Spec. If the Template Spec with the specified name and/or specific version does not already exist, it will be created.</span></span>

<span data-ttu-id="e07ad-114">När du ändrar innehållet i en mal Linies spec-mall kan innehållet antingen komma från en RAW JSON-sträng (med **UpdateVersionByNameFromJsonParameterSet** parameter uppsättning) eller från en angiven JSON-fil (med **UpdateVersionByNameFromJsonFileParameterSet** parameter uppsättning).</span><span class="sxs-lookup"><span data-stu-id="e07ad-114">When modifying a Template Spec version's ARM Template content, the content can either come from a raw JSON string (using **UpdateVersionByNameFromJsonParameterSet** parameter set) or from a specified JSON file (using **UpdateVersionByNameFromJsonFileParameterSet** parameter set).</span></span>

## <span data-ttu-id="e07ad-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e07ad-115">EXAMPLES</span></span>

### <span data-ttu-id="e07ad-116">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="e07ad-116">Example 1:</span></span>
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

<span data-ttu-id="e07ad-117">Ändrar version "v 1.0" för en mall med namnet "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="e07ad-117">Modifies version "v1.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="e07ad-118">Den angivna versionen är $templateJson som versions mal len för ARM-mallen.</span><span class="sxs-lookup"><span data-stu-id="e07ad-118">The specified version will have $templateJson as the version's ARM Template content.</span></span> <span data-ttu-id="e07ad-119">Om specifikation och/eller version av rot mal len inte redan finns kommer de att skapas.</span><span class="sxs-lookup"><span data-stu-id="e07ad-119">If the root Template Spec and/or version do not already exist they will be created.</span></span>


<span data-ttu-id="e07ad-120">**Anmärkningar**</span><span class="sxs-lookup"><span data-stu-id="e07ad-120">**Notes:**</span></span> 

* <span data-ttu-id="e07ad-121">Mallen ARM i exemplet är inte en-op eftersom den inte innehåller några faktiska resurser.</span><span class="sxs-lookup"><span data-stu-id="e07ad-121">The ARM Template in the example is a no-op as it contains no actual resources.</span></span>
* <span data-ttu-id="e07ad-122">Plats är endast nödvändig när mallen för mallar inte redan finns</span><span class="sxs-lookup"><span data-stu-id="e07ad-122">Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="e07ad-123">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="e07ad-123">Example 2:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="e07ad-124">Ändrar version "v 2.0" för en mall med namnet "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="e07ad-124">Modifies version "v2.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="e07ad-125">Den angivna versionen kommer att få innehållet från den lokala filen "myTemplateContent.jspå" som versionens ARM-mallens innehåll.</span><span class="sxs-lookup"><span data-stu-id="e07ad-125">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span> <span data-ttu-id="e07ad-126">Om specifikation och/eller version av rot mal len inte redan finns kommer de att skapas.</span><span class="sxs-lookup"><span data-stu-id="e07ad-126">If the root Template Spec and/or version do not already exist they will be created.</span></span>

<span data-ttu-id="e07ad-127">**Obs!** Plats är endast nödvändig när mallen för mallar inte redan finns</span><span class="sxs-lookup"><span data-stu-id="e07ad-127">**Note:** Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="e07ad-128">Exempel 3:</span><span class="sxs-lookup"><span data-stu-id="e07ad-128">Example 3:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec'  -Location 'West US' -Description 'My updated Template Spec'
```

<span data-ttu-id="e07ad-129">Ändrar beskrivningen av mallen "myTemplateSpec" i resurs gruppen "myRG".</span><span class="sxs-lookup"><span data-stu-id="e07ad-129">Modifies the description of the Template Spec named "myTemplateSpec" in resource group "myRG".</span></span> <span data-ttu-id="e07ad-130">Om mallens spec inte redan finns kommer den att skapas.</span><span class="sxs-lookup"><span data-stu-id="e07ad-130">If the Template Spec does not already exist it will be created.</span></span>

<span data-ttu-id="e07ad-131">**Obs!** Plats är endast nödvändig när mallen för mallar inte redan finns</span><span class="sxs-lookup"><span data-stu-id="e07ad-131">**Note:** Location is only required when the Template Spec does not already exist</span></span>

## <span data-ttu-id="e07ad-132">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e07ad-132">PARAMETERS</span></span>

### <span data-ttu-id="e07ad-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e07ad-133">-DefaultProfile</span></span>
<span data-ttu-id="e07ad-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e07ad-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e07ad-135">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="e07ad-135">-Description</span></span>
<span data-ttu-id="e07ad-136">Beskrivningen av mallens spec.</span><span class="sxs-lookup"><span data-stu-id="e07ad-136">The description of the template spec.</span></span>

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

### <span data-ttu-id="e07ad-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e07ad-137">-DisplayName</span></span>
<span data-ttu-id="e07ad-138">Visnings namnet på mallens spec.</span><span class="sxs-lookup"><span data-stu-id="e07ad-138">The display name of the template spec.</span></span>

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

### <span data-ttu-id="e07ad-139">-Plats</span><span class="sxs-lookup"><span data-stu-id="e07ad-139">-Location</span></span>
<span data-ttu-id="e07ad-140">Platsen för mallens spec. Endast obligatoriskt om mallens spec inte redan finns.</span><span class="sxs-lookup"><span data-stu-id="e07ad-140">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="e07ad-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="e07ad-141">-Name</span></span>
<span data-ttu-id="e07ad-142">Namnet på mallens spec.</span><span class="sxs-lookup"><span data-stu-id="e07ad-142">The name of the template spec.</span></span>

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

### <span data-ttu-id="e07ad-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e07ad-143">-ResourceGroupName</span></span>
<span data-ttu-id="e07ad-144">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e07ad-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="e07ad-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e07ad-145">-ResourceId</span></span>
<span data-ttu-id="e07ad-146">Fullständigt resurs-ID för mallens spec. exempel:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="e07ad-146">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="e07ad-147">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="e07ad-147">-TemplateFile</span></span>
<span data-ttu-id="e07ad-148">Fil Sök vägen till den lokala Azure Resource Manager-mallens JSON-fil.</span><span class="sxs-lookup"><span data-stu-id="e07ad-148">The file path to the local Azure Resource Manager template JSON file.</span></span>

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

### <span data-ttu-id="e07ad-149">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="e07ad-149">-TemplateJson</span></span>
<span data-ttu-id="e07ad-150">Azure Resource Manager-mallens JSON.</span><span class="sxs-lookup"><span data-stu-id="e07ad-150">The Azure Resource Manager template JSON.</span></span>

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

### <span data-ttu-id="e07ad-151">-Version</span><span class="sxs-lookup"><span data-stu-id="e07ad-151">-Version</span></span>
<span data-ttu-id="e07ad-152">Versionen av mallens spec.</span><span class="sxs-lookup"><span data-stu-id="e07ad-152">The version of the template spec.</span></span>

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

### <span data-ttu-id="e07ad-153">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="e07ad-153">-VersionDescription</span></span>
<span data-ttu-id="e07ad-154">Beskrivning av versionen.</span><span class="sxs-lookup"><span data-stu-id="e07ad-154">The description of the version.</span></span>

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

### <span data-ttu-id="e07ad-155">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e07ad-155">-Confirm</span></span>
<span data-ttu-id="e07ad-156">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e07ad-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e07ad-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e07ad-157">-WhatIf</span></span>
<span data-ttu-id="e07ad-158">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e07ad-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e07ad-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e07ad-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e07ad-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e07ad-160">CommonParameters</span></span>
<span data-ttu-id="e07ad-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e07ad-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e07ad-162">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e07ad-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e07ad-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e07ad-163">INPUTS</span></span>

### <span data-ttu-id="e07ad-164">System. String</span><span class="sxs-lookup"><span data-stu-id="e07ad-164">System.String</span></span>

## <span data-ttu-id="e07ad-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e07ad-165">OUTPUTS</span></span>

### <span data-ttu-id="e07ad-166">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="e07ad-166">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="e07ad-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e07ad-167">NOTES</span></span>

## <span data-ttu-id="e07ad-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e07ad-168">RELATED LINKS</span></span>
