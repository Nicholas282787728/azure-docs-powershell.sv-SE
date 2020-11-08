---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
ms.openlocfilehash: 7187994ca1e6e6ba9da3980be2e75b7b4ad1a877
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103277"
---
# <span data-ttu-id="28486-101">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="28486-101">Set-AzBlueprintArtifact</span></span>

## <span data-ttu-id="28486-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="28486-102">SYNOPSIS</span></span>
<span data-ttu-id="28486-103">Uppdatera en artefakt i en skiss definition.</span><span class="sxs-lookup"><span data-stu-id="28486-103">Update an artifact in a blueprint definition.</span></span>

## <span data-ttu-id="28486-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="28486-104">SYNTAX</span></span>

### <span data-ttu-id="28486-105">UpdateTemplateArtifact (standard)</span><span class="sxs-lookup"><span data-stu-id="28486-105">UpdateTemplateArtifact (Default)</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28486-106">UpdateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="28486-106">UpdateArtifactByInputFile</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28486-107">UpdateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="28486-107">UpdateRoleAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28486-108">UpdatePolicyAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="28486-108">UpdatePolicyAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28486-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="28486-109">DESCRIPTION</span></span>
<span data-ttu-id="28486-110">Uppdatera en artefakt.</span><span class="sxs-lookup"><span data-stu-id="28486-110">Update an artifact.</span></span> <span data-ttu-id="28486-111">Det finns två sätt att uppdatera en artefakt: antingen via en artefakt-JSON som en indatafil eller genom att ange infogade parametrar för artefakten.</span><span class="sxs-lookup"><span data-stu-id="28486-111">There are two ways to update an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="28486-112">Även om JSON-metoden inte kräver en typ av artefakten för att den infogade parameter metoden kräver att en användare anger typen av artefakt med parametern type.</span><span class="sxs-lookup"><span data-stu-id="28486-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="28486-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="28486-113">EXAMPLES</span></span>

### <span data-ttu-id="28486-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="28486-114">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Name PolicyStorage -Blueprint $bp -ArtifactFile C:\PolicyAssignmentStorageTag.json

DisplayName        :
Description        : Apply storage tag and the parameter also used by the template to resource groups
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/AppNetwork/artifacts/PolicyAssignmentStorageTag
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : PolicyAssignmentStorageTag
```

<span data-ttu-id="28486-115">Uppdatera en artefakt via en artefakt-JSON-fil.</span><span class="sxs-lookup"><span data-stu-id="28486-115">Update an artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="28486-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="28486-116">Example 2</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Type PolicyAssignmentArtifact -Name "ApplyTag-RG" -Blueprint $bp -PolicyDefinitionId "/providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71" -PolicyDefinitionParameter @{tagName="[parameters('tagName')]"; tagValue="[parameters('tagValue')]"} -ResourceGroupName storageRG

DisplayName        : ApplyTag-RG
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71
Parameters         : {[tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagName,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : storageRG
Id                 : /subscriptions/28cbf98f-381d-4425-9ac4-cf342dab9753/providers/Microsoft.Blueprint/blueprints/AppNetwork/
                     artifacts/ApplyTag-RG
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : ApplyTag-RG
```

<span data-ttu-id="28486-117">Uppdatera en artefakt genom infogade parametrar.</span><span class="sxs-lookup"><span data-stu-id="28486-117">Update an artifact through inline parameters.</span></span>

### <span data-ttu-id="28486-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="28486-118">Example 3</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Type TemplateArtifact -Name storage-account -Blueprint $bp -TemplateFile C:\StorageAccountArmTemplate.json -ResourceGroup "storageRG" -TemplateParameterFile C:\Workspace\BlueprintTemplates\RestTemplatesSomeInline\StorageAccountParameters.json

DisplayName   : storage-account
Description   :
DependsOn     :
Template      : {$schema, contentVersion, parameters, variables...}
Parameters    : {}
ResourceGroup : storageRG
Id            : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/AppNetwork/artifacts/storage-account
Type          : Microsoft.Blueprint/blueprints/artifacts
Name          : storage-account
```

<span data-ttu-id="28486-119">Uppdatera en artefakt via en ARM-mallfil.</span><span class="sxs-lookup"><span data-stu-id="28486-119">Update an artifact through an ARM template file.</span></span>

## <span data-ttu-id="28486-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="28486-120">PARAMETERS</span></span>

### <span data-ttu-id="28486-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="28486-121">-ArtifactFile</span></span>
<span data-ttu-id="28486-122">Plats för artefakt filen i JSON-format på disk.</span><span class="sxs-lookup"><span data-stu-id="28486-122">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28486-123">-Skiss</span><span class="sxs-lookup"><span data-stu-id="28486-123">-Blueprint</span></span>
<span data-ttu-id="28486-124">Skiss objekt.</span><span class="sxs-lookup"><span data-stu-id="28486-124">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28486-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28486-125">-DefaultProfile</span></span>
<span data-ttu-id="28486-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="28486-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28486-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="28486-127">-DependsOn</span></span>
<span data-ttu-id="28486-128">Lista över namn på artefakter som måste skapas innan aktuell artefakt skapas.</span><span class="sxs-lookup"><span data-stu-id="28486-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28486-129">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="28486-129">-Description</span></span>
<span data-ttu-id="28486-130">Beskrivning av artefakten.</span><span class="sxs-lookup"><span data-stu-id="28486-130">Description of the artifact.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28486-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="28486-131">-Name</span></span>
<span data-ttu-id="28486-132">Namn på artefakten</span><span class="sxs-lookup"><span data-stu-id="28486-132">Name of the artifact</span></span>

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

### <span data-ttu-id="28486-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="28486-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="28486-134">Definitions-ID för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="28486-134">Definition Id of the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28486-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="28486-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="28486-136">En hash-profil för överföring till princip definitionens artefakt.</span><span class="sxs-lookup"><span data-stu-id="28486-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28486-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28486-137">-ResourceGroupName</span></span>
<span data-ttu-id="28486-138">Namnet på den resurs grupp som artefakten ska vara under.</span><span class="sxs-lookup"><span data-stu-id="28486-138">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28486-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="28486-139">-RoleDefinitionId</span></span>
<span data-ttu-id="28486-140">Lista över roll definitioner</span><span class="sxs-lookup"><span data-stu-id="28486-140">List of role definition</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28486-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="28486-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="28486-142">Lista över huvud-ID: n för roll definitioner.</span><span class="sxs-lookup"><span data-stu-id="28486-142">List of role definition principal ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28486-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="28486-143">-TemplateFile</span></span>
<span data-ttu-id="28486-144">Plats för ARM-mallfilen på disk.</span><span class="sxs-lookup"><span data-stu-id="28486-144">Location of the ARM template file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28486-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="28486-145">-TemplateParameterFile</span></span>
<span data-ttu-id="28486-146">Placering av parameter filen för ARM-mallen på disk.</span><span class="sxs-lookup"><span data-stu-id="28486-146">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28486-147">– Skriv</span><span class="sxs-lookup"><span data-stu-id="28486-147">-Type</span></span>
<span data-ttu-id="28486-148">Typ av artefakt.</span><span class="sxs-lookup"><span data-stu-id="28486-148">Type of the artifact.</span></span>
<span data-ttu-id="28486-149">Det finns 3 typer som stöds: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="28486-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28486-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="28486-150">-Confirm</span></span>
<span data-ttu-id="28486-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="28486-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28486-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28486-152">-WhatIf</span></span>
<span data-ttu-id="28486-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="28486-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28486-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="28486-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28486-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28486-155">CommonParameters</span></span>
<span data-ttu-id="28486-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28486-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28486-157">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28486-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28486-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="28486-158">INPUTS</span></span>

### <span data-ttu-id="28486-159">System. String</span><span class="sxs-lookup"><span data-stu-id="28486-159">System.String</span></span>

### <span data-ttu-id="28486-160">Microsoft. Azure. commands. skissa. Models. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="28486-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="28486-161">Microsoft. Azure. commands. skissa. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="28486-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="28486-162">System. Collections. Generic. list ' 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="28486-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="28486-163">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="28486-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="28486-164">System. string []</span><span class="sxs-lookup"><span data-stu-id="28486-164">System.String[]</span></span>

## <span data-ttu-id="28486-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="28486-165">OUTPUTS</span></span>

### <span data-ttu-id="28486-166">Microsoft. Azure. Management. skiss. Models. artefakt</span><span class="sxs-lookup"><span data-stu-id="28486-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="28486-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="28486-167">NOTES</span></span>

## <span data-ttu-id="28486-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="28486-168">RELATED LINKS</span></span>
