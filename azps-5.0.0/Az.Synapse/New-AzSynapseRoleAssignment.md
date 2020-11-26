---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
ms.openlocfilehash: 6fdb2a51354df01c308629eaedb09cba3a8d2fdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269547"
---
# <span data-ttu-id="d0b34-101">New-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d0b34-101">New-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="d0b34-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0b34-102">SYNOPSIS</span></span>
<span data-ttu-id="d0b34-103">Skapar en Synapse.</span><span class="sxs-lookup"><span data-stu-id="d0b34-103">Creates a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="d0b34-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0b34-104">SYNTAX</span></span>

### <span data-ttu-id="d0b34-105">NewByWorkspaceNameAndNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d0b34-105">NewByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0b34-106">NewByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0b34-106">NewByWorkspaceNameAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0b34-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0b34-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0b34-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0b34-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ServicePrincipalName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0b34-109">NewByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0b34-109">NewByWorkspaceObjectAndNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0b34-110">NewByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0b34-110">NewByWorkspaceObjectAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0b34-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0b34-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String> -ObjectId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0b34-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0b34-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0b34-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0b34-113">DESCRIPTION</span></span>
<span data-ttu-id="d0b34-114">Cmdleten **New-AzSynapseRoleAssignment** skapar en Azure Synapse-roll tilldelning.</span><span class="sxs-lookup"><span data-stu-id="d0b34-114">The **New-AzSynapseRoleAssignment** cmdlet creates an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="d0b34-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0b34-115">EXAMPLES</span></span>

### <span data-ttu-id="d0b34-116">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d0b34-116">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="d0b34-117">Det här kommandot tilldelar ContosoRole till den användare vars huvud namn är ContosoName.</span><span class="sxs-lookup"><span data-stu-id="d0b34-117">This command assigns ContosoRole to the user whose principal name is ContosoName.</span></span>

### <span data-ttu-id="d0b34-118">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d0b34-118">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseRoleAssignment -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="d0b34-119">Det här kommandot tilldelar ContosoRole till den användare vars huvud namn är ContosoName genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="d0b34-119">This command assigns ContosoRole to the user whose principal name is ContosoName through pipeline.</span></span>

## <span data-ttu-id="d0b34-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0b34-120">PARAMETERS</span></span>

### <span data-ttu-id="d0b34-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0b34-121">-AsJob</span></span>
<span data-ttu-id="d0b34-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d0b34-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0b34-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0b34-123">-DefaultProfile</span></span>
<span data-ttu-id="d0b34-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d0b34-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0b34-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d0b34-125">-ObjectId</span></span>
<span data-ttu-id="d0b34-126">Azure AD ObjectId för användaren, gruppen eller tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="d0b34-126">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0b34-127">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="d0b34-127">-RoleDefinitionId</span></span>
<span data-ttu-id="d0b34-128">ID för rollen som tilldelats huvudobjektet.</span><span class="sxs-lookup"><span data-stu-id="d0b34-128">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0b34-129">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="d0b34-129">-RoleDefinitionName</span></span>
<span data-ttu-id="d0b34-130">Namn på den roll som tilldelats huvudobjektet.</span><span class="sxs-lookup"><span data-stu-id="d0b34-130">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndServicePrincipalNameParameterSet, NewByWorkspaceObjectAndNameParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0b34-131">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d0b34-131">-ServicePrincipalName</span></span>
<span data-ttu-id="d0b34-132">ServicePrincipalName för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="d0b34-132">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndServicePrincipalNameParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0b34-133">-SignInName</span><span class="sxs-lookup"><span data-stu-id="d0b34-133">-SignInName</span></span>
<span data-ttu-id="d0b34-134">E-postadressen eller användarens huvud namn för användaren.</span><span class="sxs-lookup"><span data-stu-id="d0b34-134">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0b34-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d0b34-135">-WorkspaceName</span></span>
<span data-ttu-id="d0b34-136">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="d0b34-136">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0b34-137">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d0b34-137">-WorkspaceObject</span></span>
<span data-ttu-id="d0b34-138">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="d0b34-138">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByWorkspaceObjectAndNameParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0b34-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d0b34-139">-Confirm</span></span>
<span data-ttu-id="d0b34-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d0b34-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0b34-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0b34-141">-WhatIf</span></span>
<span data-ttu-id="d0b34-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d0b34-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0b34-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d0b34-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0b34-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0b34-144">CommonParameters</span></span>
<span data-ttu-id="d0b34-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0b34-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0b34-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0b34-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0b34-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0b34-147">INPUTS</span></span>

### <span data-ttu-id="d0b34-148">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d0b34-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d0b34-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0b34-149">OUTPUTS</span></span>

### <span data-ttu-id="d0b34-150">Microsoft. Azure. commands. Synapse. Models. PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="d0b34-150">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="d0b34-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0b34-151">NOTES</span></span>

## <span data-ttu-id="d0b34-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0b34-152">RELATED LINKS</span></span>