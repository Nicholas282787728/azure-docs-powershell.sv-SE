---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
ms.openlocfilehash: bf96dc0818b978c6c759d363c9d3e2637f27b704
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100711"
---
# <span data-ttu-id="6f530-101">Get-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6f530-101">Get-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="6f530-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f530-102">SYNOPSIS</span></span>
<span data-ttu-id="6f530-103">Hämtar en Synapse.</span><span class="sxs-lookup"><span data-stu-id="6f530-103">Gets a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="6f530-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f530-104">SYNTAX</span></span>

### <span data-ttu-id="6f530-105">GetByWorkspaceNameAndNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6f530-105">GetByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-SignInName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f530-106">GetByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f530-106">GetByWorkspaceNameAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f530-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f530-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f530-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f530-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f530-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f530-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>]
 [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f530-110">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f530-110">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f530-111">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f530-111">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f530-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f530-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f530-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f530-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f530-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f530-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f530-115">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f530-115">DESCRIPTION</span></span>
<span data-ttu-id="6f530-116">Cmdleten **Get-AzSynapseRoleAssignment** har en Azure Synapse-roll tilldelning.</span><span class="sxs-lookup"><span data-stu-id="6f530-116">The **Get-AzSynapseRoleAssignment** cmdlet gets a Azure Synapse Analytics Role Assignment.</span></span>
<span data-ttu-id="6f530-117">Om du inte anger en roll definition eller ett huvud namn för användaren får denna cmdlet all roll tilldelning.</span><span class="sxs-lookup"><span data-stu-id="6f530-117">If you do not specify a role definition or a user principal name, this cmdlet gets all role assignment.</span></span>

## <span data-ttu-id="6f530-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f530-118">EXAMPLES</span></span>

### <span data-ttu-id="6f530-119">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6f530-119">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="6f530-120">Det här kommandot får alla roll tilldelningar under en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="6f530-120">This command gets all role assignments under a workspace.</span></span>

### <span data-ttu-id="6f530-121">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6f530-121">Example 2</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole
```

<span data-ttu-id="6f530-122">Det här kommandot får alla roll tilldelningar under arbets ytans ContosoWorkspace med roll namn ContosoRole.</span><span class="sxs-lookup"><span data-stu-id="6f530-122">This command gets all role assignments under workspace ContosoWorkspace with role name ContosoRole.</span></span>

### <span data-ttu-id="6f530-123">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="6f530-123">Example 3</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="6f530-124">Det här kommandot får en roll tilldelning under arbets ytans ContosoWorkspace med roll namn ContosoRole och användarens huvud namn ContosoName.</span><span class="sxs-lookup"><span data-stu-id="6f530-124">This command gets a role assignment under workspace ContosoWorkspace with role name ContosoRole and user principal name ContosoName.</span></span>

### <span data-ttu-id="6f530-125">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="6f530-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleAssignment
```

<span data-ttu-id="6f530-126">Det här kommandot får alla roll tilldelningar under en arbets yta genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="6f530-126">This command gets all role assignments under a workspace through pipeline.</span></span>

## <span data-ttu-id="6f530-127">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f530-127">PARAMETERS</span></span>

### <span data-ttu-id="6f530-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f530-128">-DefaultProfile</span></span>
<span data-ttu-id="6f530-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6f530-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f530-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6f530-130">-ObjectId</span></span>
<span data-ttu-id="6f530-131">Azure AD ObjectId för användaren, gruppen eller tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="6f530-131">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f530-132">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="6f530-132">-RoleAssignmentId</span></span>
<span data-ttu-id="6f530-133">ID för roll tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="6f530-133">The ID of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndAssignmentIdParameterSet, GetByWorkspaceObjectAndAssignmentIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f530-134">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="6f530-134">-RoleDefinitionId</span></span>
<span data-ttu-id="6f530-135">ID för rollen som tilldelats huvudobjektet.</span><span class="sxs-lookup"><span data-stu-id="6f530-135">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f530-136">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="6f530-136">-RoleDefinitionName</span></span>
<span data-ttu-id="6f530-137">Namn på den roll som tilldelats huvudobjektet.</span><span class="sxs-lookup"><span data-stu-id="6f530-137">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndServicePrincipalNameParameterSet, GetByWorkspaceObjectAndNameParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f530-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="6f530-138">-ServicePrincipalName</span></span>
<span data-ttu-id="6f530-139">ServicePrincipalName för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="6f530-139">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f530-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="6f530-140">-SignInName</span></span>
<span data-ttu-id="6f530-141">E-postadressen eller användarens huvud namn för användaren.</span><span class="sxs-lookup"><span data-stu-id="6f530-141">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f530-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6f530-142">-WorkspaceName</span></span>
<span data-ttu-id="6f530-143">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="6f530-143">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceNameAndAssignmentIdParameterSet, GetByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f530-144">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6f530-144">-WorkspaceObject</span></span>
<span data-ttu-id="6f530-145">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="6f530-145">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByWorkspaceObjectAndNameParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndAssignmentIdParameterSet, GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f530-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f530-146">CommonParameters</span></span>
<span data-ttu-id="6f530-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f530-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f530-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f530-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f530-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f530-149">INPUTS</span></span>

### <span data-ttu-id="6f530-150">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6f530-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6f530-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f530-151">OUTPUTS</span></span>

### <span data-ttu-id="6f530-152">Microsoft. Azure. commands. Synapse. Models. PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="6f530-152">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="6f530-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f530-153">NOTES</span></span>

## <span data-ttu-id="6f530-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f530-154">RELATED LINKS</span></span>
