---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8C1D738C-825D-4718-AD2A-9CFEAA7DBD3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzRoleAssignment.md
ms.openlocfilehash: d0efa32f8a0eb00d203b0e1be3318cd98ab06ef7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923806"
---
# <span data-ttu-id="0accb-101">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0accb-101">Remove-AzRoleAssignment</span></span>

## <span data-ttu-id="0accb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0accb-102">SYNOPSIS</span></span>
<span data-ttu-id="0accb-103">Tar bort en roll tilldelning till det angivna huvud kontot som har tilldelats en viss roll i ett visst område.</span><span class="sxs-lookup"><span data-stu-id="0accb-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="0accb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0accb-104">SYNTAX</span></span>

### <span data-ttu-id="0accb-105">EmptyParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0accb-105">EmptyParameterSet (Default)</span></span>
```
Remove-AzRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0accb-106">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0accb-106">ResourceWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0accb-107">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0accb-107">ResourceGroupWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0accb-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0accb-108">ScopeWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0accb-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0accb-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0accb-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0accb-110">ResourceWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0accb-111">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0accb-111">ResourceGroupWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0accb-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0accb-112">ScopeWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0accb-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="0accb-113">ResourceWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0accb-114">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="0accb-114">ResourceGroupWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 -RoleDefinitionName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0accb-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="0accb-115">ScopeWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0accb-116">RoleAssignmentParameterSet</span><span class="sxs-lookup"><span data-stu-id="0accb-116">RoleAssignmentParameterSet</span></span>
```
Remove-AzRoleAssignment [-PassThru] [-InputObject] <PSRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0accb-117">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0accb-117">DESCRIPTION</span></span>
<span data-ttu-id="0accb-118">Använd Remove-AzRoleAssignment-cmdleten om du vill återkalla åtkomsten till ett objekt vid givet omfång och med den roll som anges.</span><span class="sxs-lookup"><span data-stu-id="0accb-118">Use the Remove-AzRoleAssignment commandlet to revoke access to any principal at given scope and given role.</span></span>
<span data-ttu-id="0accb-119">Uppgiftens objekt, t. ex.</span><span class="sxs-lookup"><span data-stu-id="0accb-119">The object of the assignment i.e. the principal MUST be specified.</span></span>
<span data-ttu-id="0accb-120">Huvudobjektet kan vara en användare (Använd SignInName-eller ObjectId-parametrar för att identifiera en användare), säkerhets grupp (Använd parametern ObjectId för att identifiera en grupp) eller tjänstens huvud namn (Använd ServicePrincipalName-eller ObjectId-parametrar för att identifiera en ServicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="0accb-120">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ServicePrincipalName or ObjectId parameters to identify a ServicePrincipal.</span></span>
<span data-ttu-id="0accb-121">Rollen som huvudobjektet är tilldelad måste anges med parametern RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="0accb-121">The role that the principal is assigned to MUST be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="0accb-122">Omfattningen av tilldelningen kan anges och om den inte anges, blir standardvärdet för prenumerationens omfattning, d.v.s. det försöker ta bort en uppgift till det angivna huvud kontot och rollen i prenumerations omfattningen.</span><span class="sxs-lookup"><span data-stu-id="0accb-122">The scope of the assignment MAY be specified and if not specified, defaults to the subscription scope i.e. it will try to delete an assignment to the specified principal and role at the subscription scope.</span></span>
<span data-ttu-id="0accb-123">Omfattningen av uppgiften kan anges med hjälp av någon av följande parametrar.</span><span class="sxs-lookup"><span data-stu-id="0accb-123">The scope of the assignment can be specified using one of the following parameters.</span></span>
<span data-ttu-id="0accb-124">kallas.</span><span class="sxs-lookup"><span data-stu-id="0accb-124">a.</span></span>
<span data-ttu-id="0accb-125">Scope-det här är det fullt kvalificerade scopet som börjar med/Subscriptions/ \< subscriptionId \> b.</span><span class="sxs-lookup"><span data-stu-id="0accb-125">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="0accb-126">ResourceGroupName-namnet på en resurs grupp under prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0accb-126">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="0accb-127">f.</span><span class="sxs-lookup"><span data-stu-id="0accb-127">c.</span></span>
<span data-ttu-id="0accb-128">ResourceName, ResourceType, ResourceGroupName och (valfritt) ParentResource-identifierar en viss resurs under prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0accb-128">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription.</span></span>

## <span data-ttu-id="0accb-129">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0accb-129">EXAMPLES</span></span>

### <span data-ttu-id="0accb-130">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0accb-130">Example 1</span></span>
```
PS C:\> Remove-AzRoleAssignment -ResourceGroupName rg1 -SignInName john.doe@contoso.com -RoleDefinitionName Reader
```

<span data-ttu-id="0accb-131">Tar bort en roll tilldelning för john.doe@contoso.com vem som är tilldelad rollen läsare i RG1 resourcegroup-scope.</span><span class="sxs-lookup"><span data-stu-id="0accb-131">Removes a role assignment for john.doe@contoso.com who is assigned to the Reader role at the rg1 resourcegroup scope.</span></span>

### <span data-ttu-id="0accb-132">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0accb-132">Example 2</span></span>
```
PS C:\> Remove-AzRoleAssignment -ObjectId 36f81fc3-b00f-48cd-8218-3879f51ff39f -RoleDefinitionName Reader
```

<span data-ttu-id="0accb-133">Tar bort roll tilldelningen till det grupp huvud konto som identifieras av ObjectId och som har tilldelats rollen läsare.</span><span class="sxs-lookup"><span data-stu-id="0accb-133">Removes the role assignment to the group principal identified by the ObjectId and assigned to the Reader role.</span></span>
<span data-ttu-id="0accb-134">Standardvärdet använder det nuvarande abonnemanget som omfattning för att hitta uppgiften som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="0accb-134">Defaults to using the current subscription as the scope to find the assignment to be deleted.</span></span>

### <span data-ttu-id="0accb-135">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="0accb-135">Example 3</span></span>
```
PS C:\> $roleassignment = Get-AzRoleAssignment |Select-Object -First 1 -Wait
PS C:\> Remove-AzRoleAssignment -InputObject $roleassignment
```

<span data-ttu-id="0accb-136">Tar bort det första roll tilldelnings objekt som hämtas från Get-AzRoleAssignment cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0accb-136">Removes the first role assignment object which is fetched from the Get-AzRoleAssignment commandlet.</span></span>

## <span data-ttu-id="0accb-137">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0accb-137">PARAMETERS</span></span>

### <span data-ttu-id="0accb-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0accb-138">-DefaultProfile</span></span>
<span data-ttu-id="0accb-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0accb-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0accb-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0accb-140">-InputObject</span></span>
<span data-ttu-id="0accb-141">Roll tilldelnings objekt.</span><span class="sxs-lookup"><span data-stu-id="0accb-141">Role Assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0accb-142">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0accb-142">-ObjectId</span></span>
<span data-ttu-id="0accb-143">Azure AD ObjectId för användaren, gruppen eller tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="0accb-143">Azure AD ObjectId of the user, group or service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0accb-144">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="0accb-144">-ParentResource</span></span>
<span data-ttu-id="0accb-145">Den överordnade resursen i hierarkin (av resursen som anges med parametern ResourceName), om det finns någon.</span><span class="sxs-lookup"><span data-stu-id="0accb-145">The parent resource in the hierarchy(of the resource specified using ResourceName parameter), if any.</span></span>
<span data-ttu-id="0accb-146">Måste användas tillsammans med parametrarna ResourceGroupName, ResourceType och ResourceName för att skapa ett hierarkiskt scope i form av en relativ URI som identifierar resursen.</span><span class="sxs-lookup"><span data-stu-id="0accb-146">Must be used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0accb-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0accb-147">-PassThru</span></span>
<span data-ttu-id="0accb-148">Om det här alternativet anges visas den borttagna roll tilldelningen</span><span class="sxs-lookup"><span data-stu-id="0accb-148">If specified, displays the deleted role assignment</span></span>

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

### <span data-ttu-id="0accb-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0accb-149">-ResourceGroupName</span></span>
<span data-ttu-id="0accb-150">Namnet på resurs gruppen som rollen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="0accb-150">The resource group name that the role is assigned to.</span></span>
<span data-ttu-id="0accb-151">Försöker ta bort en tilldelning i den angivna resurs grupps omfattningen.</span><span class="sxs-lookup"><span data-stu-id="0accb-151">Attempts to delete an assignment at the specified resource group scope.</span></span>
<span data-ttu-id="0accb-152">När kommandot används tillsammans med kommandona ResourceName, ResourceType och (valfritt) ParentResource, skapas ett hierarkiskt område i form av en relativ URI som identifierar en resurs.</span><span class="sxs-lookup"><span data-stu-id="0accb-152">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0accb-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0accb-153">-ResourceName</span></span>
<span data-ttu-id="0accb-154">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="0accb-154">The resource name.</span></span>
<span data-ttu-id="0accb-155">T. storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="0accb-155">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="0accb-156">Måste användas tillsammans med ResourceGroupName-, ResourceType-och (valfritt) ParentResource-parametrar för att skapa ett hierarkiskt scope i form av en relativ URI som identifierar resursen och ta bort en tilldelning i det aktuella området.</span><span class="sxs-lookup"><span data-stu-id="0accb-156">Must be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters, to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0accb-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0accb-157">-ResourceType</span></span>
<span data-ttu-id="0accb-158">Resurs typen.</span><span class="sxs-lookup"><span data-stu-id="0accb-158">The resource type.</span></span>
<span data-ttu-id="0accb-159">Till exempel. Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="0accb-159">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="0accb-160">Måste användas tillsammans med ResourceGroupName-, ResourceName-och (valfritt) ParentResource-parametrar för att skapa ett hierarkiskt scope i form av en relativ URI som identifierar resursen och ta bort en tilldelning i resurs omfattningen.</span><span class="sxs-lookup"><span data-stu-id="0accb-160">Must be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that resource scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0accb-161">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="0accb-161">-RoleDefinitionId</span></span>
<span data-ttu-id="0accb-162">ID för den RBAC-roll för vilken tilldelningen ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="0accb-162">Id of the RBAC role for which the assignment needs to be deleted.</span></span>

```yaml
Type: System.Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0accb-163">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="0accb-163">-RoleDefinitionName</span></span>
<span data-ttu-id="0accb-164">Namnet på den RBAC-roll för vilken tilldelningen måste tas bort, till exempel läsare, deltagare, virtuell nätverks administratör osv.</span><span class="sxs-lookup"><span data-stu-id="0accb-164">Name of the RBAC role for which the assignment needs to be deleted i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0accb-165">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="0accb-165">-Scope</span></span>
<span data-ttu-id="0accb-166">Omfattningen för den roll tilldelning som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="0accb-166">The Scope of the role assignment to be deleted.</span></span>
<span data-ttu-id="0accb-167">I formatet för relativ URI.</span><span class="sxs-lookup"><span data-stu-id="0accb-167">In the format of relative URI.</span></span>
<span data-ttu-id="0accb-168">Till exempel "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="0accb-168">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="0accb-169">Om du inte anger något försök att ta bort rollen på prenumerations nivån.</span><span class="sxs-lookup"><span data-stu-id="0accb-169">If not specified, will attempt to delete the role at subscription level.</span></span>
<span data-ttu-id="0accb-170">Om det anges ska det börja med "/Subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="0accb-170">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0accb-171">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="0accb-171">-ServicePrincipalName</span></span>
<span data-ttu-id="0accb-172">ServicePrincipalName för Azure AD-programmet</span><span class="sxs-lookup"><span data-stu-id="0accb-172">The ServicePrincipalName of the Azure AD application</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0accb-173">-SignInName</span><span class="sxs-lookup"><span data-stu-id="0accb-173">-SignInName</span></span>
<span data-ttu-id="0accb-174">E-postadressen eller användarens huvud namn för användaren.</span><span class="sxs-lookup"><span data-stu-id="0accb-174">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0accb-175">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0accb-175">-Confirm</span></span>
<span data-ttu-id="0accb-176">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0accb-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0accb-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0accb-177">-WhatIf</span></span>
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

### <span data-ttu-id="0accb-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0accb-178">CommonParameters</span></span>
<span data-ttu-id="0accb-179">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0accb-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0accb-180">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0accb-180">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0accb-181">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0accb-181">INPUTS</span></span>

### <span data-ttu-id="0accb-182">System. GUID</span><span class="sxs-lookup"><span data-stu-id="0accb-182">System.Guid</span></span>

### <span data-ttu-id="0accb-183">System. String</span><span class="sxs-lookup"><span data-stu-id="0accb-183">System.String</span></span>

### <span data-ttu-id="0accb-184">Microsoft. Azure. kommandon. sources. Models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0accb-184">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>
<span data-ttu-id="0accb-185">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0accb-185">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="0accb-186">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0accb-186">OUTPUTS</span></span>

### <span data-ttu-id="0accb-187">Microsoft. Azure. kommandon. sources. Models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0accb-187">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="0accb-188">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0accb-188">NOTES</span></span>
<span data-ttu-id="0accb-189">Nyckelord: Azure, AZ, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="0accb-189">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="0accb-190">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0accb-190">RELATED LINKS</span></span>

[<span data-ttu-id="0accb-191">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0accb-191">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="0accb-192">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0accb-192">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="0accb-193">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="0accb-193">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

