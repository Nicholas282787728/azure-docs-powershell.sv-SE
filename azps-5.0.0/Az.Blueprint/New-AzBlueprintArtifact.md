---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
ms.openlocfilehash: 7a6910e18b966c49ee6c766f06fddc88f903914f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269334"
---
# <span data-ttu-id="3aeec-101">New-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="3aeec-101">New-AzBlueprintArtifact</span></span>

## <span data-ttu-id="3aeec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3aeec-102">SYNOPSIS</span></span>
<span data-ttu-id="3aeec-103">Skapa en ny artefakt och spara den i en skiss.</span><span class="sxs-lookup"><span data-stu-id="3aeec-103">Create a new artifact and save it within a blueprint definition.</span></span>

## <span data-ttu-id="3aeec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3aeec-104">SYNTAX</span></span>

### <span data-ttu-id="3aeec-105">CreateTemplateArtifact (standard)</span><span class="sxs-lookup"><span data-stu-id="3aeec-105">CreateTemplateArtifact (Default)</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3aeec-106">CreateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="3aeec-106">CreateArtifactByInputFile</span></span>
```
New-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3aeec-107">CreateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="3aeec-107">CreateRoleAssignmentArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3aeec-108">CreatePolicyArtifact</span><span class="sxs-lookup"><span data-stu-id="3aeec-108">CreatePolicyArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3aeec-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3aeec-109">DESCRIPTION</span></span>
<span data-ttu-id="3aeec-110">Skapa en ny artefakt.</span><span class="sxs-lookup"><span data-stu-id="3aeec-110">Create a new artifact.</span></span> <span data-ttu-id="3aeec-111">Det finns två sätt att skapa en artefakt: antingen via en artefakt-JSON som en indatafil eller genom att ange infogade parametrar för artefakten.</span><span class="sxs-lookup"><span data-stu-id="3aeec-111">There are two ways to create an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="3aeec-112">Även om JSON-metoden inte kräver en typ av artefakten för att den infogade parameter metoden kräver att en användare anger typen av artefakt med parametern type.</span><span class="sxs-lookup"><span data-stu-id="3aeec-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="3aeec-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3aeec-113">EXAMPLES</span></span>

### <span data-ttu-id="3aeec-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3aeec-114">Example 1</span></span>
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

<span data-ttu-id="3aeec-115">Skapa en ny artefakt genom en artefakt-JSON-fil.</span><span class="sxs-lookup"><span data-stu-id="3aeec-115">Create a new artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="3aeec-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3aeec-116">Example 2</span></span>
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

<span data-ttu-id="3aeec-117">Skapa en ny artefakt genom infogade parametrar.</span><span class="sxs-lookup"><span data-stu-id="3aeec-117">Create a new artifact through inline parameters.</span></span>

### <span data-ttu-id="3aeec-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="3aeec-118">Example 3</span></span>
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

<span data-ttu-id="3aeec-119">Skapa en ny artefakt via en ARM-mallfil.</span><span class="sxs-lookup"><span data-stu-id="3aeec-119">Create a new artifact through an ARM template file.</span></span>

## <span data-ttu-id="3aeec-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3aeec-120">PARAMETERS</span></span>

### <span data-ttu-id="3aeec-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="3aeec-121">-ArtifactFile</span></span>
<span data-ttu-id="3aeec-122">Plats för artefakt filen i JSON-format på disk.</span><span class="sxs-lookup"><span data-stu-id="3aeec-122">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aeec-123">-Skiss</span><span class="sxs-lookup"><span data-stu-id="3aeec-123">-Blueprint</span></span>
<span data-ttu-id="3aeec-124">Skiss objekt.</span><span class="sxs-lookup"><span data-stu-id="3aeec-124">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3aeec-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aeec-125">-DefaultProfile</span></span>
<span data-ttu-id="3aeec-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3aeec-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3aeec-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="3aeec-127">-DependsOn</span></span>
<span data-ttu-id="3aeec-128">Lista över namn på artefakter som måste skapas innan aktuell artefakt skapas.</span><span class="sxs-lookup"><span data-stu-id="3aeec-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aeec-129">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="3aeec-129">-Description</span></span>
<span data-ttu-id="3aeec-130">Beskrivning av artefakten.</span><span class="sxs-lookup"><span data-stu-id="3aeec-130">Description of the artifact.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aeec-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="3aeec-131">-Name</span></span>
<span data-ttu-id="3aeec-132">Namn på artefakten</span><span class="sxs-lookup"><span data-stu-id="3aeec-132">Name of the artifact</span></span>

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

### <span data-ttu-id="3aeec-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="3aeec-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="3aeec-134">Definitions-ID för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="3aeec-134">Definition Id of the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aeec-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="3aeec-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="3aeec-136">En hash-profil för överföring till princip definitionens artefakt.</span><span class="sxs-lookup"><span data-stu-id="3aeec-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aeec-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3aeec-137">-ResourceGroupName</span></span>
<span data-ttu-id="3aeec-138">Namnet på den resurs grupp som artefakten ska vara under.</span><span class="sxs-lookup"><span data-stu-id="3aeec-138">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aeec-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="3aeec-139">-RoleDefinitionId</span></span>
<span data-ttu-id="3aeec-140">Lista över roll definitioner</span><span class="sxs-lookup"><span data-stu-id="3aeec-140">List of role definition</span></span>

```yaml
Type: System.String
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aeec-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="3aeec-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="3aeec-142">Lista över huvud-ID: n för roll definitioner.</span><span class="sxs-lookup"><span data-stu-id="3aeec-142">List of role definition principal ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aeec-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="3aeec-143">-TemplateFile</span></span>
<span data-ttu-id="3aeec-144">Plats för ARM-mallfilen på disk.</span><span class="sxs-lookup"><span data-stu-id="3aeec-144">Location of the ARM template file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aeec-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="3aeec-145">-TemplateParameterFile</span></span>
<span data-ttu-id="3aeec-146">Placering av parameter filen för ARM-mallen på disk.</span><span class="sxs-lookup"><span data-stu-id="3aeec-146">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aeec-147">– Skriv</span><span class="sxs-lookup"><span data-stu-id="3aeec-147">-Type</span></span>
<span data-ttu-id="3aeec-148">Typ av artefakt.</span><span class="sxs-lookup"><span data-stu-id="3aeec-148">Type of the artifact.</span></span>
<span data-ttu-id="3aeec-149">Det finns 3 typer som stöds: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="3aeec-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aeec-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3aeec-150">-Confirm</span></span>
<span data-ttu-id="3aeec-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3aeec-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3aeec-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3aeec-152">-WhatIf</span></span>
<span data-ttu-id="3aeec-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3aeec-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3aeec-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3aeec-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3aeec-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aeec-155">CommonParameters</span></span>
<span data-ttu-id="3aeec-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3aeec-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aeec-157">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3aeec-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aeec-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3aeec-158">INPUTS</span></span>

### <span data-ttu-id="3aeec-159">System. String</span><span class="sxs-lookup"><span data-stu-id="3aeec-159">System.String</span></span>

### <span data-ttu-id="3aeec-160">Microsoft. Azure. commands. skissa. Models. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="3aeec-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="3aeec-161">Microsoft. Azure. commands. skissa. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="3aeec-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="3aeec-162">System. Collections. Generic. list ' 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="3aeec-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="3aeec-163">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="3aeec-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3aeec-164">System. string []</span><span class="sxs-lookup"><span data-stu-id="3aeec-164">System.String[]</span></span>

## <span data-ttu-id="3aeec-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3aeec-165">OUTPUTS</span></span>

### <span data-ttu-id="3aeec-166">Microsoft. Azure. Management. skiss. Models. artefakt</span><span class="sxs-lookup"><span data-stu-id="3aeec-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="3aeec-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3aeec-167">NOTES</span></span>

## <span data-ttu-id="3aeec-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3aeec-168">RELATED LINKS</span></span>
