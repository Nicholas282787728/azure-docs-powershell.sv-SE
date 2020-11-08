---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
ms.openlocfilehash: b19653570c7bfbf62cb94107bb2fa354a9fda3f1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270271"
---
# <span data-ttu-id="85e17-101">New-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="85e17-101">New-AzTemplateSpec</span></span>

## <span data-ttu-id="85e17-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="85e17-102">SYNOPSIS</span></span>
<span data-ttu-id="85e17-103">Skapar en ny mall-spec.</span><span class="sxs-lookup"><span data-stu-id="85e17-103">Creates a new Template Spec.</span></span>

## <span data-ttu-id="85e17-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="85e17-104">SYNTAX</span></span>

### <span data-ttu-id="85e17-105">FromJsonStringParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="85e17-105">FromJsonStringParameterSet (Default)</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateJson <String> [-VersionDescription <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85e17-106">FromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="85e17-106">FromJsonFileParameterSet</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateFile <String> [-VersionDescription <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85e17-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="85e17-107">DESCRIPTION</span></span>
<span data-ttu-id="85e17-108">Skapar en ny mall för Specifikations version med det angivna innehållet i mallen.</span><span class="sxs-lookup"><span data-stu-id="85e17-108">Creates a new Template Spec version with the specified ARM Template content.</span></span> <span data-ttu-id="85e17-109">Innehållet kan antingen komma från en RAW JSON-sträng (med hjälp av **FromJsonStringParameterSet** parameter uppsättning) eller från en angiven JSON-fil (med **FromJsonFileParameterSet** -parameter uppsättning).</span><span class="sxs-lookup"><span data-stu-id="85e17-109">The content can either come from a raw JSON string (using **FromJsonStringParameterSet** parameter set) or from a specified JSON file (using **FromJsonFileParameterSet** parameter set).</span></span>  

<span data-ttu-id="85e17-110">Om du inte redan har en specifikation för rotzonen skapas den tillsammans med Specifikations versionen för mallen.</span><span class="sxs-lookup"><span data-stu-id="85e17-110">If the root Template Spec does not already exist it will be created along with the Template Spec version.</span></span> <span data-ttu-id="85e17-111">Om det redan finns en mall med det angivna namnet uppdateras den och den angivna versionen (alla andra befintliga versioner kommer att bevaras).</span><span class="sxs-lookup"><span data-stu-id="85e17-111">If a Template Spec already exists with the given name, it and the specified version will be updated (any other existing versions will be preserved).</span></span>

## <span data-ttu-id="85e17-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="85e17-112">EXAMPLES</span></span>

### <span data-ttu-id="85e17-113">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="85e17-113">Example 1:</span></span>
```powershell
PS C:\> $templateJson = @"
{
    "$schema": "http://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "resources": []
}
"@
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v1.0' -Location 'West US' -TemplateJson $templateJson
```

<span data-ttu-id="85e17-114">Skapar en ny mall för Specifikations version "v 1.0" i en mappinformationsmall med namnet "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="85e17-114">Creates a new Template Spec version "v1.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="85e17-115">Den angivna versionen är $templateJson som versions mal len för ARM-mallen.</span><span class="sxs-lookup"><span data-stu-id="85e17-115">The specified version will have $templateJson as the version's ARM Template content.</span></span>

 <span data-ttu-id="85e17-116">**Obs!** Mallen ARM i exemplet är inte en-op eftersom den inte innehåller några faktiska resurser.</span><span class="sxs-lookup"><span data-stu-id="85e17-116">**Note:** The ARM Template in the example is a no-op as it contains no actual resources.</span></span>

### <span data-ttu-id="85e17-117">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="85e17-117">Example 2:</span></span>
```powershell
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="85e17-118">Skapar en ny mall för Specifikations version "v 2.0" i en mappinformationsmall med namnet "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="85e17-118">Creates a new Template Spec version "v2.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="85e17-119">Den angivna versionen kommer att få innehållet från den lokala filen "myTemplateContent.jspå" som versionens ARM-mallens innehåll.</span><span class="sxs-lookup"><span data-stu-id="85e17-119">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span>

## <span data-ttu-id="85e17-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="85e17-120">PARAMETERS</span></span>

### <span data-ttu-id="85e17-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85e17-121">-DefaultProfile</span></span>
<span data-ttu-id="85e17-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="85e17-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85e17-123">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="85e17-123">-Description</span></span>
<span data-ttu-id="85e17-124">Beskrivningen av mallens spec.</span><span class="sxs-lookup"><span data-stu-id="85e17-124">The description of the template spec.</span></span>

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

### <span data-ttu-id="85e17-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="85e17-125">-DisplayName</span></span>
<span data-ttu-id="85e17-126">Visnings namnet på mallens spec.</span><span class="sxs-lookup"><span data-stu-id="85e17-126">The display name of the template spec.</span></span>

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

### <span data-ttu-id="85e17-127">-Force</span><span class="sxs-lookup"><span data-stu-id="85e17-127">-Force</span></span>
<span data-ttu-id="85e17-128">Fråga inte efter bekräftelse när en befintlig version skrivs över.</span><span class="sxs-lookup"><span data-stu-id="85e17-128">Do not ask for confirmation when overwriting an existing version.</span></span>

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

### <span data-ttu-id="85e17-129">-Plats</span><span class="sxs-lookup"><span data-stu-id="85e17-129">-Location</span></span>
<span data-ttu-id="85e17-130">Platsen för mallens spec. Endast obligatoriskt om mallens spec inte redan finns.</span><span class="sxs-lookup"><span data-stu-id="85e17-130">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="85e17-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="85e17-131">-Name</span></span>
<span data-ttu-id="85e17-132">Namnet på mallens spec.</span><span class="sxs-lookup"><span data-stu-id="85e17-132">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e17-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85e17-133">-ResourceGroupName</span></span>
<span data-ttu-id="85e17-134">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="85e17-134">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e17-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="85e17-135">-TemplateFile</span></span>
<span data-ttu-id="85e17-136">Fil Sök vägen till den lokala Azure Resource Manager-mallens JSON-fil.</span><span class="sxs-lookup"><span data-stu-id="85e17-136">The file path to the local Azure Resource Manager template JSON file.</span></span>

```yaml
Type: System.String
Parameter Sets: FromJsonFileParameterSet
Aliases: InputFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e17-137">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="85e17-137">-TemplateJson</span></span>
<span data-ttu-id="85e17-138">Azure Resource Manager-mallens JSON.</span><span class="sxs-lookup"><span data-stu-id="85e17-138">The Azure Resource Manager template JSON.</span></span>

```yaml
Type: System.String
Parameter Sets: FromJsonStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e17-139">-Version</span><span class="sxs-lookup"><span data-stu-id="85e17-139">-Version</span></span>
<span data-ttu-id="85e17-140">Versionen av mallens spec.</span><span class="sxs-lookup"><span data-stu-id="85e17-140">The version of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e17-141">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="85e17-141">-VersionDescription</span></span>
<span data-ttu-id="85e17-142">Beskrivning av versionen.</span><span class="sxs-lookup"><span data-stu-id="85e17-142">The description of the version.</span></span>

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

### <span data-ttu-id="85e17-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="85e17-143">-Confirm</span></span>
<span data-ttu-id="85e17-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="85e17-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85e17-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85e17-145">-WhatIf</span></span>
<span data-ttu-id="85e17-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="85e17-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85e17-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="85e17-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85e17-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85e17-148">CommonParameters</span></span>
<span data-ttu-id="85e17-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85e17-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85e17-150">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85e17-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85e17-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="85e17-151">INPUTS</span></span>

### <span data-ttu-id="85e17-152">System. String</span><span class="sxs-lookup"><span data-stu-id="85e17-152">System.String</span></span>

## <span data-ttu-id="85e17-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="85e17-153">OUTPUTS</span></span>

### <span data-ttu-id="85e17-154">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="85e17-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="85e17-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="85e17-155">NOTES</span></span>

## <span data-ttu-id="85e17-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="85e17-156">RELATED LINKS</span></span>
