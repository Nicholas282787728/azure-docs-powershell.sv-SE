---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
ms.openlocfilehash: d1fe464078c41d07f0d40024c06c4d5f88358470
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919297"
---
# <span data-ttu-id="b2659-101">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b2659-101">New-AzRoleAssignment</span></span>

## <span data-ttu-id="b2659-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b2659-102">SYNOPSIS</span></span>
<span data-ttu-id="b2659-103">Tilldelar den angivna RBAC-rollen till den angivna huvud delen, vid det angivna omfånget.</span><span class="sxs-lookup"><span data-stu-id="b2659-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="b2659-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b2659-104">SYNTAX</span></span>

### <span data-ttu-id="b2659-105">EmptyParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b2659-105">EmptyParameterSet (Default)</span></span>
```
New-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2659-106">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2659-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2659-107">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2659-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2659-108">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2659-108">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -Scope <String> -RoleDefinitionId <Guid> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2659-109">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2659-109">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2659-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2659-110">ResourceWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2659-111">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2659-111">ScopeWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2659-112">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2659-112">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2659-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2659-113">ResourceWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2659-114">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2659-114">ScopeWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> [-Scope <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2659-115">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b2659-115">DESCRIPTION</span></span>
<span data-ttu-id="b2659-116">Använd kommandot New-AzRoleAssignment för att ge åtkomst.</span><span class="sxs-lookup"><span data-stu-id="b2659-116">Use the New-AzRoleAssignment command to grant access.</span></span>
<span data-ttu-id="b2659-117">Åtkomst beviljas genom att den lämpliga RBAC-rollen tilldelas till dem vid rätt scope.</span><span class="sxs-lookup"><span data-stu-id="b2659-117">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="b2659-118">Om du vill bevilja åtkomst till hela abonnemanget tilldelar du en roll i prenumerations omfattningen.</span><span class="sxs-lookup"><span data-stu-id="b2659-118">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="b2659-119">Om du vill bevilja åtkomst till en viss resurs grupp i en prenumeration tilldelar du en roll i resurs gruppens omfattning.</span><span class="sxs-lookup"><span data-stu-id="b2659-119">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>
<span data-ttu-id="b2659-120">Uppgiftens ämne måste anges.</span><span class="sxs-lookup"><span data-stu-id="b2659-120">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="b2659-121">Ange en användare med hjälp av SignInName eller Azure AD ObjectId-parametrar.</span><span class="sxs-lookup"><span data-stu-id="b2659-121">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="b2659-122">Om du vill ange en säkerhets grupp använder du Azure AD ObjectId-parameter.</span><span class="sxs-lookup"><span data-stu-id="b2659-122">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="b2659-123">Om du vill ange ett Azure AD-program använder du ApplicationId-eller ObjectId-parametrar.</span><span class="sxs-lookup"><span data-stu-id="b2659-123">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="b2659-124">Rollen som tilldelas måste anges med parametern RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="b2659-124">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="b2659-125">Omfattningen där åtkomst ges kan anges.</span><span class="sxs-lookup"><span data-stu-id="b2659-125">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="b2659-126">Det är standardinställningen för det valda abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b2659-126">It defaults to the selected subscription.</span></span> <span data-ttu-id="b2659-127">Omfattningen av uppgiften kan anges med hjälp av någon av följande parameter kombinationer a.</span><span class="sxs-lookup"><span data-stu-id="b2659-127">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="b2659-128">Scope-det här är det fullt kvalificerade scopet som börjar med/Subscriptions/ \< subscriptionId \> b.</span><span class="sxs-lookup"><span data-stu-id="b2659-128">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="b2659-129">ResourceGroupName – om du vill bevilja åtkomst till den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b2659-129">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="b2659-130">f.</span><span class="sxs-lookup"><span data-stu-id="b2659-130">c.</span></span>
<span data-ttu-id="b2659-131">ResourceName, ResourceType, ResourceGroupName och (valfritt) ParentResource-för att ange en viss resurs i en resurs grupp för att bevilja åtkomst till.</span><span class="sxs-lookup"><span data-stu-id="b2659-131">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="b2659-132">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b2659-132">EXAMPLES</span></span>

### <span data-ttu-id="b2659-133">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b2659-133">Example 1</span></span>
```
PS C:\> New-AzRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader -AllowDelegation
```

<span data-ttu-id="b2659-134">Ge läsare rollen åtkomst till en användare i en resurs grupp omfattning med den roll tilldelning som är tillgänglig för delegering</span><span class="sxs-lookup"><span data-stu-id="b2659-134">Grant Reader role access to a user at a resource group scope with the Role Assignment being available for delegation</span></span>

### <span data-ttu-id="b2659-135">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b2659-135">Example 2</span></span>
```
PS C:\> Get-AzADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           Id
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="b2659-136">Bevilja åtkomst till en säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="b2659-136">Grant access to a security group</span></span>

### <span data-ttu-id="b2659-137">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="b2659-137">Example 3</span></span>
```
PS C:\> New-AzRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="b2659-138">Bevilja åtkomst till en användare på en resurs (webbplats)</span><span class="sxs-lookup"><span data-stu-id="b2659-138">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="b2659-139">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="b2659-139">Example 4</span></span>
```
PS C:\> New-AzRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="b2659-140">Bevilja åtkomst till en grupp på en kapslad resurs (delnät)</span><span class="sxs-lookup"><span data-stu-id="b2659-140">Grant access to a group at a nested resource (subnet)</span></span>

### <span data-ttu-id="b2659-141">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="b2659-141">Example 5</span></span>
```
PS C:\> $servicePrincipal = New-AzADServicePrincipal -DisplayName "testServiceprincipal"
PS C:\> New-AzRoleAssignment -RoleDefinitionName "Reader" -ApplicationId $servicePrincipal.ApplicationId
```

<span data-ttu-id="b2659-142">Ge läsare åtkomst till ett tjänst huvud konto</span><span class="sxs-lookup"><span data-stu-id="b2659-142">Grant reader access to a service principal</span></span>

## <span data-ttu-id="b2659-143">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b2659-143">PARAMETERS</span></span>

### <span data-ttu-id="b2659-144">-AllowDelegation</span><span class="sxs-lookup"><span data-stu-id="b2659-144">-AllowDelegation</span></span>
<span data-ttu-id="b2659-145">Delegerings flaggan när du skapar en roll tilldelning.</span><span class="sxs-lookup"><span data-stu-id="b2659-145">The delegation flag while creating a Role assignment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2659-146">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b2659-146">-ApplicationId</span></span>
<span data-ttu-id="b2659-147">Program-ID för ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b2659-147">The Application ID of the ServicePrincipal</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN, ServicePrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2659-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2659-148">-DefaultProfile</span></span>
<span data-ttu-id="b2659-149">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b2659-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2659-150">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b2659-150">-ObjectId</span></span>
<span data-ttu-id="b2659-151">Azure AD ObjectID för användaren, gruppen eller tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="b2659-151">Azure AD Objectid of the user, group or service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2659-152">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="b2659-152">-ParentResource</span></span>
<span data-ttu-id="b2659-153">Den överordnade resursen i hierarkin (av resursen som anges med parametern ResourceName).</span><span class="sxs-lookup"><span data-stu-id="b2659-153">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="b2659-154">Bör endast användas tillsammans med parametrarna ResourceGroupName, ResourceType och ResourceName för att konstruera ett hierarkiskt scope i form av en relativ URI som identifierar en resurs.</span><span class="sxs-lookup"><span data-stu-id="b2659-154">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="b2659-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2659-155">-ResourceGroupName</span></span>
<span data-ttu-id="b2659-156">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b2659-156">The resource group name.</span></span>
<span data-ttu-id="b2659-157">Skapar en tilldelning som gäller för den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b2659-157">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="b2659-158">När kommandot används tillsammans med kommandona ResourceName, ResourceType och (valfritt) ParentResource, skapas ett hierarkiskt område i form av en relativ URI som identifierar en resurs.</span><span class="sxs-lookup"><span data-stu-id="b2659-158">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2659-159">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b2659-159">-ResourceName</span></span>
<span data-ttu-id="b2659-160">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="b2659-160">The resource name.</span></span>
<span data-ttu-id="b2659-161">T. storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="b2659-161">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="b2659-162">Bör endast användas tillsammans med ResourceGroupName-, ResourceType-och (valfritt) ParentResource-parametrar för att skapa ett hierarkiskt scope i form av en relativ URI som identifierar en resurs.</span><span class="sxs-lookup"><span data-stu-id="b2659-162">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="b2659-163">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b2659-163">-ResourceType</span></span>
<span data-ttu-id="b2659-164">Resurs typen.</span><span class="sxs-lookup"><span data-stu-id="b2659-164">The resource type.</span></span>
<span data-ttu-id="b2659-165">Till exempel. Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="b2659-165">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="b2659-166">Bör endast användas tillsammans med ParentResource-parametrar (ResourceGroupName, ResourceName och (valfritt) för att skapa ett hierarkiskt scope i form av en relativ URI som identifierar en resurs.</span><span class="sxs-lookup"><span data-stu-id="b2659-166">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="b2659-167">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="b2659-167">-RoleDefinitionId</span></span>
<span data-ttu-id="b2659-168">ID för den RBAC-roll som måste tilldelas huvudobjektet.</span><span class="sxs-lookup"><span data-stu-id="b2659-168">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="b2659-169">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="b2659-169">-RoleDefinitionName</span></span>
<span data-ttu-id="b2659-170">Namnet på den RBAC-roll som måste tilldelas den huvudansvarige, till exempel läsare, deltagare, virtuell nätverks administratör, etc.</span><span class="sxs-lookup"><span data-stu-id="b2659-170">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2659-171">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="b2659-171">-Scope</span></span>
<span data-ttu-id="b2659-172">Omfattningen av roll tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="b2659-172">The Scope of the role assignment.</span></span>
<span data-ttu-id="b2659-173">I formatet för relativ URI.</span><span class="sxs-lookup"><span data-stu-id="b2659-173">In the format of relative URI.</span></span>
<span data-ttu-id="b2659-174">Till exempel "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="b2659-174">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="b2659-175">Om det inte anges skapas roll tilldelningen på prenumerations nivå.</span><span class="sxs-lookup"><span data-stu-id="b2659-175">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="b2659-176">Om det anges ska det börja med "/Subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="b2659-176">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2659-177">-SignInName</span><span class="sxs-lookup"><span data-stu-id="b2659-177">-SignInName</span></span>
<span data-ttu-id="b2659-178">E-postadressen eller användarens huvud namn för användaren.</span><span class="sxs-lookup"><span data-stu-id="b2659-178">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2659-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2659-179">CommonParameters</span></span>
<span data-ttu-id="b2659-180">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2659-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2659-181">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2659-181">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2659-182">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b2659-182">INPUTS</span></span>

### <span data-ttu-id="b2659-183">System. String</span><span class="sxs-lookup"><span data-stu-id="b2659-183">System.String</span></span>

### <span data-ttu-id="b2659-184">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b2659-184">System.Guid</span></span>

## <span data-ttu-id="b2659-185">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b2659-185">OUTPUTS</span></span>

### <span data-ttu-id="b2659-186">Microsoft. Azure. kommandon. sources. Models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b2659-186">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="b2659-187">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b2659-187">NOTES</span></span>
<span data-ttu-id="b2659-188">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="b2659-188">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b2659-189">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b2659-189">RELATED LINKS</span></span>

[<span data-ttu-id="b2659-190">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b2659-190">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="b2659-191">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b2659-191">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="b2659-192">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b2659-192">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)
