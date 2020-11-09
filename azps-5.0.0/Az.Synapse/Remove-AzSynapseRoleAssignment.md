---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
ms.openlocfilehash: 3ac6d0be30075409924c014c27a16b2f4cab21a0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94326124"
---
# <span data-ttu-id="243df-101">Remove-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="243df-101">Remove-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="243df-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="243df-102">SYNOPSIS</span></span>
<span data-ttu-id="243df-103">Tar bort en Synapse.</span><span class="sxs-lookup"><span data-stu-id="243df-103">Deletes a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="243df-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="243df-104">SYNTAX</span></span>

### <span data-ttu-id="243df-105">RemoveByWorkspaceNameAndNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="243df-105">RemoveByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="243df-106">RemoveByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="243df-106">RemoveByWorkspaceNameAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="243df-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="243df-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="243df-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="243df-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="243df-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="243df-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="243df-110">RemoveByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="243df-110">RemoveByWorkspaceObjectAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="243df-111">RemoveByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="243df-111">RemoveByWorkspaceObjectAndNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="243df-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="243df-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="243df-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="243df-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="243df-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="243df-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="243df-115">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="243df-115">DESCRIPTION</span></span>
<span data-ttu-id="243df-116">Cmdleten **Remove-AzSynapseRoleAssignment** tar bort en Azure Synapse-roll tilldelning.</span><span class="sxs-lookup"><span data-stu-id="243df-116">The **Remove-AzSynapseRoleAssignment** cmdlet permanently deletes an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="243df-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="243df-117">EXAMPLES</span></span>

### <span data-ttu-id="243df-118">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="243df-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="243df-119">Det här kommandot tar bort en Azure Synapse med ett roll tilldelnings-ID.</span><span class="sxs-lookup"><span data-stu-id="243df-119">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id.</span></span>

### <span data-ttu-id="243df-120">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="243df-120">Example 2</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="243df-121">Det här kommandot tar bort en Azure Synapse med ett rollnamn och ett huvud namn för användaren.</span><span class="sxs-lookup"><span data-stu-id="243df-121">This command deletes an Azure Synapse Analytics role assignment with a role name and a user principal name.</span></span>

### <span data-ttu-id="243df-122">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="243df-122">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseRoleAssignment -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="243df-123">Det här kommandot tar bort en Azure Synapse-roll tilldelning med ett roll tilldelnings-ID via pipeline.</span><span class="sxs-lookup"><span data-stu-id="243df-123">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id through pipeline.</span></span>

## <span data-ttu-id="243df-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="243df-124">PARAMETERS</span></span>

### <span data-ttu-id="243df-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="243df-125">-AsJob</span></span>
<span data-ttu-id="243df-126">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="243df-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="243df-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="243df-127">-DefaultProfile</span></span>
<span data-ttu-id="243df-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="243df-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="243df-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="243df-129">-ObjectId</span></span>
<span data-ttu-id="243df-130">Azure AD ObjectId för användaren, gruppen eller tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="243df-130">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

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

### <span data-ttu-id="243df-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="243df-131">-PassThru</span></span>
<span data-ttu-id="243df-132">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="243df-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="243df-133">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="243df-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="243df-134">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="243df-134">-RoleAssignmentId</span></span>
<span data-ttu-id="243df-135">ID för roll tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="243df-135">The ID of the role assignment.</span></span>

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

### <span data-ttu-id="243df-136">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="243df-136">-RoleDefinitionId</span></span>
<span data-ttu-id="243df-137">ID för rollen som tilldelats huvudobjektet.</span><span class="sxs-lookup"><span data-stu-id="243df-137">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="243df-138">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="243df-138">-RoleDefinitionName</span></span>
<span data-ttu-id="243df-139">Namn på den roll som tilldelats huvudobjektet.</span><span class="sxs-lookup"><span data-stu-id="243df-139">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="243df-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="243df-140">-ServicePrincipalName</span></span>
<span data-ttu-id="243df-141">ServicePrincipalName för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="243df-141">The ServicePrincipalName of the service principal.</span></span>

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

### <span data-ttu-id="243df-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="243df-142">-SignInName</span></span>
<span data-ttu-id="243df-143">E-postadressen eller användarens huvud namn för användaren.</span><span class="sxs-lookup"><span data-stu-id="243df-143">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="243df-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="243df-144">-WorkspaceName</span></span>
<span data-ttu-id="243df-145">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="243df-145">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="243df-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="243df-146">-WorkspaceObject</span></span>
<span data-ttu-id="243df-147">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="243df-147">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="243df-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="243df-148">-Confirm</span></span>
<span data-ttu-id="243df-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="243df-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="243df-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="243df-150">-WhatIf</span></span>
<span data-ttu-id="243df-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="243df-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="243df-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="243df-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="243df-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="243df-153">CommonParameters</span></span>
<span data-ttu-id="243df-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="243df-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="243df-155">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="243df-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="243df-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="243df-156">INPUTS</span></span>

### <span data-ttu-id="243df-157">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="243df-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="243df-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="243df-158">OUTPUTS</span></span>

### <span data-ttu-id="243df-159">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="243df-159">System.Boolean</span></span>

## <span data-ttu-id="243df-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="243df-160">NOTES</span></span>

## <span data-ttu-id="243df-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="243df-161">RELATED LINKS</span></span>
