---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
ms.openlocfilehash: 3ac6d0be30075409924c014c27a16b2f4cab21a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103364"
---
# <span data-ttu-id="31f8b-101">Remove-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="31f8b-101">Remove-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="31f8b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="31f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="31f8b-103">Tar bort en Synapse.</span><span class="sxs-lookup"><span data-stu-id="31f8b-103">Deletes a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="31f8b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="31f8b-104">SYNTAX</span></span>

### <span data-ttu-id="31f8b-105">RemoveByWorkspaceNameAndNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="31f8b-105">RemoveByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31f8b-106">RemoveByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31f8b-106">RemoveByWorkspaceNameAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31f8b-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31f8b-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31f8b-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31f8b-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31f8b-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="31f8b-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31f8b-110">RemoveByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31f8b-110">RemoveByWorkspaceObjectAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31f8b-111">RemoveByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="31f8b-111">RemoveByWorkspaceObjectAndNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="31f8b-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31f8b-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="31f8b-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31f8b-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="31f8b-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="31f8b-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31f8b-115">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="31f8b-115">DESCRIPTION</span></span>
<span data-ttu-id="31f8b-116">Cmdleten **Remove-AzSynapseRoleAssignment** tar bort en Azure Synapse-roll tilldelning.</span><span class="sxs-lookup"><span data-stu-id="31f8b-116">The **Remove-AzSynapseRoleAssignment** cmdlet permanently deletes an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="31f8b-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="31f8b-117">EXAMPLES</span></span>

### <span data-ttu-id="31f8b-118">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="31f8b-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="31f8b-119">Det här kommandot tar bort en Azure Synapse med ett roll tilldelnings-ID.</span><span class="sxs-lookup"><span data-stu-id="31f8b-119">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id.</span></span>

### <span data-ttu-id="31f8b-120">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="31f8b-120">Example 2</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="31f8b-121">Det här kommandot tar bort en Azure Synapse med ett rollnamn och ett huvud namn för användaren.</span><span class="sxs-lookup"><span data-stu-id="31f8b-121">This command deletes an Azure Synapse Analytics role assignment with a role name and a user principal name.</span></span>

### <span data-ttu-id="31f8b-122">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="31f8b-122">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseRoleAssignment -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="31f8b-123">Det här kommandot tar bort en Azure Synapse-roll tilldelning med ett roll tilldelnings-ID via pipeline.</span><span class="sxs-lookup"><span data-stu-id="31f8b-123">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id through pipeline.</span></span>

## <span data-ttu-id="31f8b-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="31f8b-124">PARAMETERS</span></span>

### <span data-ttu-id="31f8b-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31f8b-125">-AsJob</span></span>
<span data-ttu-id="31f8b-126">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="31f8b-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31f8b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31f8b-127">-DefaultProfile</span></span>
<span data-ttu-id="31f8b-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="31f8b-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31f8b-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="31f8b-129">-ObjectId</span></span>
<span data-ttu-id="31f8b-130">Azure AD ObjectId för användaren, gruppen eller tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="31f8b-130">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f8b-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31f8b-131">-PassThru</span></span>
<span data-ttu-id="31f8b-132">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="31f8b-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="31f8b-133">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="31f8b-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="31f8b-134">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="31f8b-134">-RoleAssignmentId</span></span>
<span data-ttu-id="31f8b-135">ID för roll tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="31f8b-135">The ID of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndIdParameterSet, RemoveByWorkspaceObjectAndIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f8b-136">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="31f8b-136">-RoleDefinitionId</span></span>
<span data-ttu-id="31f8b-137">ID för rollen som tilldelats huvudobjektet.</span><span class="sxs-lookup"><span data-stu-id="31f8b-137">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f8b-138">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="31f8b-138">-RoleDefinitionName</span></span>
<span data-ttu-id="31f8b-139">Namn på den roll som tilldelats huvudobjektet.</span><span class="sxs-lookup"><span data-stu-id="31f8b-139">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndServicePrincipalNameParameterSet, RemoveByWorkspaceObjectAndNameParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f8b-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="31f8b-140">-ServicePrincipalName</span></span>
<span data-ttu-id="31f8b-141">ServicePrincipalName för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="31f8b-141">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndServicePrincipalNameParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f8b-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="31f8b-142">-SignInName</span></span>
<span data-ttu-id="31f8b-143">E-postadressen eller användarens huvud namn för användaren.</span><span class="sxs-lookup"><span data-stu-id="31f8b-143">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f8b-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="31f8b-144">-WorkspaceName</span></span>
<span data-ttu-id="31f8b-145">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="31f8b-145">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceNameAndIdParameterSet, RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f8b-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="31f8b-146">-WorkspaceObject</span></span>
<span data-ttu-id="31f8b-147">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="31f8b-147">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByWorkspaceObjectAndIdParameterSet, RemoveByWorkspaceObjectAndNameParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31f8b-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="31f8b-148">-Confirm</span></span>
<span data-ttu-id="31f8b-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="31f8b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31f8b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31f8b-150">-WhatIf</span></span>
<span data-ttu-id="31f8b-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="31f8b-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31f8b-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="31f8b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31f8b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31f8b-153">CommonParameters</span></span>
<span data-ttu-id="31f8b-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31f8b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31f8b-155">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31f8b-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31f8b-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="31f8b-156">INPUTS</span></span>

### <span data-ttu-id="31f8b-157">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="31f8b-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="31f8b-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="31f8b-158">OUTPUTS</span></span>

### <span data-ttu-id="31f8b-159">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="31f8b-159">System.Boolean</span></span>

## <span data-ttu-id="31f8b-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="31f8b-160">NOTES</span></span>

## <span data-ttu-id="31f8b-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="31f8b-161">RELATED LINKS</span></span>