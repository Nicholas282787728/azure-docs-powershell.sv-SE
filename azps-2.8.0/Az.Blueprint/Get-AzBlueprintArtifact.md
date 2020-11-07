---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
ms.openlocfilehash: 94a0ff1d4e16748b769f51303fb397da7e029026
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745374"
---
# <span data-ttu-id="5fd3c-101">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="5fd3c-101">Get-AzBlueprintArtifact</span></span>

## <span data-ttu-id="5fd3c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5fd3c-102">SYNOPSIS</span></span>
<span data-ttu-id="5fd3c-103">Hämta artefakter från en skiss definition.</span><span class="sxs-lookup"><span data-stu-id="5fd3c-103">Retrieve artifacts from a blueprint definition.</span></span>

## <span data-ttu-id="5fd3c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5fd3c-104">SYNTAX</span></span>

```
Get-AzBlueprintArtifact [-Name <String>] -Blueprint <PSBlueprintBase> [-BlueprintVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fd3c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5fd3c-105">DESCRIPTION</span></span>
<span data-ttu-id="5fd3c-106">Hämta artefakter från en skiss definition.</span><span class="sxs-lookup"><span data-stu-id="5fd3c-106">Retrieve artifacts from a blueprint definition.</span></span> <span data-ttu-id="5fd3c-107">Om du inte anger en version av ritnings definitionen hämtas utkastet.</span><span class="sxs-lookup"><span data-stu-id="5fd3c-107">If a blueprint definition version is not specified, the draft version is retrieved.</span></span> <span data-ttu-id="5fd3c-108">Om det inte finns någon utkast version returneras den senaste publicerade utkasts definitionen.</span><span class="sxs-lookup"><span data-stu-id="5fd3c-108">In the case where there is no draft version, the latest published blueprint definition is returned.</span></span>

## <span data-ttu-id="5fd3c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5fd3c-109">EXAMPLES</span></span>

### <span data-ttu-id="5fd3c-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5fd3c-110">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Get-AzBlueprintArtifact -Blueprint $bp 

DisplayName        : Audit use of classic virtual machines
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1d84d5fb-01f6-4d12-ba4f-4a26081d403d
Parameters         : {[effect, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : SimpleBlueprintRG
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/3ab44511-0228-4275-9641-7e93e6f34178
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 3ab44511-0228-4275-9641-7e93e6f34178

DisplayName        : Enforce tag and its value
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1e30110a-5ceb-460c-a204-c1c3969c6d62
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/0e1593da-47d5-4b75-800c-9a797dd23192
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 0e1593da-47d5-4b75-800c-9a797dd23192

```

<span data-ttu-id="5fd3c-111">Hämta artefakter från en skiss definition...</span><span class="sxs-lookup"><span data-stu-id="5fd3c-111">Retrieve artifacts from a blueprint definition..</span></span> 

## <span data-ttu-id="5fd3c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5fd3c-112">PARAMETERS</span></span>

### <span data-ttu-id="5fd3c-113">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="5fd3c-113">-ArtifactFile</span></span>
<span data-ttu-id="5fd3c-114">Plats för artefakt filen i JSON-format på disk.</span><span class="sxs-lookup"><span data-stu-id="5fd3c-114">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd3c-115">-Skiss</span><span class="sxs-lookup"><span data-stu-id="5fd3c-115">-Blueprint</span></span>
<span data-ttu-id="5fd3c-116">Skiss objekt.</span><span class="sxs-lookup"><span data-stu-id="5fd3c-116">Blueprint object.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: ArtifactsByBlueprint, UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSBlueprintBase
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd3c-117">-BlueprintVersion</span><span class="sxs-lookup"><span data-stu-id="5fd3c-117">-BlueprintVersion</span></span>
<span data-ttu-id="5fd3c-118">Den version av skissen som du vill hämta artefakterna från.</span><span class="sxs-lookup"><span data-stu-id="5fd3c-118">Version of the blueprint to get the artifacts from.</span></span>

```yaml
Type: String
Parameter Sets: ArtifactsByBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd3c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fd3c-119">-DefaultProfile</span></span>
<span data-ttu-id="5fd3c-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5fd3c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd3c-121">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="5fd3c-121">-DependsOn</span></span>
<span data-ttu-id="5fd3c-122">Lista över namn på artefakter som måste skapas innan aktuell artefakt skapas.</span><span class="sxs-lookup"><span data-stu-id="5fd3c-122">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd3c-123">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="5fd3c-123">-Description</span></span>
<span data-ttu-id="5fd3c-124">Beskrivning av artefakten.</span><span class="sxs-lookup"><span data-stu-id="5fd3c-124">Description of the artifact.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd3c-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="5fd3c-125">-Name</span></span>
<span data-ttu-id="5fd3c-126">Namn på artefakten</span><span class="sxs-lookup"><span data-stu-id="5fd3c-126">Name of the artifact</span></span>

```yaml
Type: String
Parameter Sets: ArtifactsByBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: CreateArtifactByInputFile, UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd3c-127">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="5fd3c-127">-PolicyDefinitionId</span></span>
<span data-ttu-id="5fd3c-128">Definitions-ID för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="5fd3c-128">Definition Id of the policy definition.</span></span>

```yaml
Type: String
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd3c-129">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="5fd3c-129">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="5fd3c-130">En hash-profil för överföring till princip definitionens artefakt.</span><span class="sxs-lookup"><span data-stu-id="5fd3c-130">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: Hashtable
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd3c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fd3c-131">-ResourceGroupName</span></span>
<span data-ttu-id="5fd3c-132">Namnet på den resurs grupp som artefakten ska vara under.</span><span class="sxs-lookup"><span data-stu-id="5fd3c-132">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd3c-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="5fd3c-133">-RoleDefinitionId</span></span>
<span data-ttu-id="5fd3c-134">Lista över roll definitioner</span><span class="sxs-lookup"><span data-stu-id="5fd3c-134">List of role definition</span></span>

```yaml
Type: String
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd3c-135">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="5fd3c-135">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="5fd3c-136">Lista över huvud-ID: n för roll definitioner.</span><span class="sxs-lookup"><span data-stu-id="5fd3c-136">List of role definition principal ids.</span></span>

```yaml
Type: String[]
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd3c-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="5fd3c-137">-TemplateFile</span></span>
<span data-ttu-id="5fd3c-138">Plats för ARM-mallfilen på disk.</span><span class="sxs-lookup"><span data-stu-id="5fd3c-138">Location of the ARM template file on disk.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd3c-139">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="5fd3c-139">-TemplateParameterFile</span></span>
<span data-ttu-id="5fd3c-140">Placering av parameter filen för ARM-mallen på disk.</span><span class="sxs-lookup"><span data-stu-id="5fd3c-140">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd3c-141">– Skriv</span><span class="sxs-lookup"><span data-stu-id="5fd3c-141">-Type</span></span>
<span data-ttu-id="5fd3c-142">Typ av artefakt.</span><span class="sxs-lookup"><span data-stu-id="5fd3c-142">Type of the artifact.</span></span>
<span data-ttu-id="5fd3c-143">Det finns 3 typer som stöds: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="5fd3c-143">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: PSArtifactKind
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd3c-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5fd3c-144">-Confirm</span></span>
<span data-ttu-id="5fd3c-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5fd3c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fd3c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fd3c-146">-WhatIf</span></span>
<span data-ttu-id="5fd3c-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5fd3c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fd3c-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5fd3c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fd3c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fd3c-149">CommonParameters</span></span>
<span data-ttu-id="5fd3c-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fd3c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5fd3c-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fd3c-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fd3c-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5fd3c-152">INPUTS</span></span>

### <span data-ttu-id="5fd3c-153">System. String</span><span class="sxs-lookup"><span data-stu-id="5fd3c-153">System.String</span></span>

### <span data-ttu-id="5fd3c-154">Microsoft. Azure. commands. skissa. Models. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="5fd3c-154">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="5fd3c-155">Microsoft. Azure. commands. skissa. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="5fd3c-155">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="5fd3c-156">System. Collections. Generic. list ' 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="5fd3c-156">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="5fd3c-157">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="5fd3c-157">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5fd3c-158">System. string []</span><span class="sxs-lookup"><span data-stu-id="5fd3c-158">System.String[]</span></span>

## <span data-ttu-id="5fd3c-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5fd3c-159">OUTPUTS</span></span>

### <span data-ttu-id="5fd3c-160">Microsoft. Azure. commands. skissa. Models. PSBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="5fd3c-160">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span></span>

## <span data-ttu-id="5fd3c-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5fd3c-161">NOTES</span></span>

## <span data-ttu-id="5fd3c-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5fd3c-162">RELATED LINKS</span></span>
