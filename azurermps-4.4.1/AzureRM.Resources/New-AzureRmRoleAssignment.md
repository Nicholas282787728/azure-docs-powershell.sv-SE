---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleAssignment.md
ms.openlocfilehash: c3988727e8afd54dddea9719c348222c41f47503
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577511"
---
# <span data-ttu-id="29d70-101">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="29d70-101">New-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="29d70-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29d70-102">SYNOPSIS</span></span>
<span data-ttu-id="29d70-103">Tilldelar den angivna RBAC-rollen till den angivna huvud delen, vid det angivna omfånget.</span><span class="sxs-lookup"><span data-stu-id="29d70-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29d70-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29d70-104">SYNTAX</span></span>

### <span data-ttu-id="29d70-105">EmptyParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="29d70-105">EmptyParameterSet (Default)</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -Scope <String> -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29d70-106">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="29d70-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29d70-107">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="29d70-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29d70-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="29d70-108">ScopeWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29d70-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="29d70-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -Scope <String> -RoleDefinitionId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29d70-110">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="29d70-110">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29d70-111">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="29d70-111">ResourceWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29d70-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="29d70-112">ScopeWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29d70-113">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="29d70-113">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 -RoleDefinitionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29d70-114">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="29d70-114">ResourceWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29d70-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="29d70-115">ScopeWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29d70-116">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29d70-116">DESCRIPTION</span></span>
<span data-ttu-id="29d70-117">Använd kommandot New-AzureRMRoleAssignment för att ge åtkomst.</span><span class="sxs-lookup"><span data-stu-id="29d70-117">Use the New-AzureRMRoleAssignment command to grant access.</span></span>
<span data-ttu-id="29d70-118">Åtkomst beviljas genom att den lämpliga RBAC-rollen tilldelas till dem vid rätt scope.</span><span class="sxs-lookup"><span data-stu-id="29d70-118">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="29d70-119">Om du vill bevilja åtkomst till hela abonnemanget tilldelar du en roll i prenumerations omfattningen.</span><span class="sxs-lookup"><span data-stu-id="29d70-119">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="29d70-120">Om du vill bevilja åtkomst till en viss resurs grupp i en prenumeration tilldelar du en roll i resurs gruppens omfattning.</span><span class="sxs-lookup"><span data-stu-id="29d70-120">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>

<span data-ttu-id="29d70-121">Uppgiftens ämne måste anges.</span><span class="sxs-lookup"><span data-stu-id="29d70-121">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="29d70-122">Ange en användare med hjälp av SignInName eller Azure AD ObjectId-parametrar.</span><span class="sxs-lookup"><span data-stu-id="29d70-122">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="29d70-123">Om du vill ange en säkerhets grupp använder du Azure AD ObjectId-parameter.</span><span class="sxs-lookup"><span data-stu-id="29d70-123">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="29d70-124">Och om du vill ange ett Azure AD-program använder du ServicePrincipalName-eller ObjectId-parametrar.</span><span class="sxs-lookup"><span data-stu-id="29d70-124">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>

<span data-ttu-id="29d70-125">Rollen som tilldelas måste anges med parametern RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="29d70-125">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>

<span data-ttu-id="29d70-126">Omfattningen där åtkomst ges kan anges.</span><span class="sxs-lookup"><span data-stu-id="29d70-126">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="29d70-127">Det är standardinställningen för det valda abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="29d70-127">It defaults to the selected subscription.</span></span> <span data-ttu-id="29d70-128">Omfattningen av uppgiften kan anges med hjälp av någon av följande parameter kombinationer a.</span><span class="sxs-lookup"><span data-stu-id="29d70-128">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="29d70-129">Scope-det här är det fullt kvalificerade scopet som börjar med/Subscriptions/ \<subscriptionId\> b.</span><span class="sxs-lookup"><span data-stu-id="29d70-129">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="29d70-130">ResourceGroupName – om du vill bevilja åtkomst till den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="29d70-130">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="29d70-131">f.</span><span class="sxs-lookup"><span data-stu-id="29d70-131">c.</span></span>
<span data-ttu-id="29d70-132">ResourceName, ResourceType, ResourceGroupName och (valfritt) ParentResource-för att ange en viss resurs i en resurs grupp för att bevilja åtkomst till.</span><span class="sxs-lookup"><span data-stu-id="29d70-132">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="29d70-133">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29d70-133">EXAMPLES</span></span>

### <span data-ttu-id="29d70-134">--------------------------Exempel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="29d70-134">--------------------------  Example 1  --------------------------</span></span>
```
PS C:\> New-AzureRmRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader
```

<span data-ttu-id="29d70-135">Ge läsare rollen åtkomst till en användare i en resurs grupps omfattning</span><span class="sxs-lookup"><span data-stu-id="29d70-135">Grant Reader role access to a user at a resource group scope</span></span>

### <span data-ttu-id="29d70-136">--------------------------Exempel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="29d70-136">--------------------------  Example 2  --------------------------</span></span>
```
PS C:\> Get-AzureRMADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           ObjectId
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzureRmRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="29d70-137">Bevilja åtkomst till en säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="29d70-137">Grant access to a security group</span></span>

### <span data-ttu-id="29d70-138">--------------------------Exempel 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="29d70-138">--------------------------  Example 3  --------------------------</span></span>
```
PS C:\> New-AzureRmRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="29d70-139">Bevilja åtkomst till en användare på en resurs (webbplats)</span><span class="sxs-lookup"><span data-stu-id="29d70-139">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="29d70-140">--------------------------Exempel 4--------------------------</span><span class="sxs-lookup"><span data-stu-id="29d70-140">--------------------------  Example 4  --------------------------</span></span>
```
PS C:\> New-AzureRMRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="29d70-141">Bevilja åtkomst till en grupp på en kapslad resurs (delnät)</span><span class="sxs-lookup"><span data-stu-id="29d70-141">Grant access to a group at a nested resource (subnet)</span></span>

## <span data-ttu-id="29d70-142">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29d70-142">PARAMETERS</span></span>

### <span data-ttu-id="29d70-143">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="29d70-143">-ObjectId</span></span>
<span data-ttu-id="29d70-144">Azure AD ObjectID för användaren, gruppen eller tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="29d70-144">Azure AD Objectid of the user, group or service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29d70-145">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="29d70-145">-ParentResource</span></span>
<span data-ttu-id="29d70-146">Den överordnade resursen i hierarkin (av resursen som anges med parametern ResourceName).</span><span class="sxs-lookup"><span data-stu-id="29d70-146">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="29d70-147">Bör endast användas tillsammans med parametrarna ResourceGroupName, ResourceType och ResourceName för att konstruera ett hierarkiskt scope i form av en relativ URI som identifierar en resurs.</span><span class="sxs-lookup"><span data-stu-id="29d70-147">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="29d70-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29d70-148">-ResourceGroupName</span></span>
<span data-ttu-id="29d70-149">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="29d70-149">The resource group name.</span></span>
<span data-ttu-id="29d70-150">Skapar en tilldelning som gäller för den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="29d70-150">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="29d70-151">När kommandot används tillsammans med kommandona ResourceName, ResourceType och (valfritt) ParentResource, skapas ett hierarkiskt område i form av en relativ URI som identifierar en resurs.</span><span class="sxs-lookup"><span data-stu-id="29d70-151">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="29d70-152">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="29d70-152">-ResourceName</span></span>
<span data-ttu-id="29d70-153">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="29d70-153">The resource name.</span></span>
<span data-ttu-id="29d70-154">T. storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="29d70-154">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="29d70-155">Bör endast användas tillsammans med ResourceGroupName-, ResourceType-och (valfritt) ParentResource-parametrar för att skapa ett hierarkiskt scope i form av en relativ URI som identifierar en resurs.</span><span class="sxs-lookup"><span data-stu-id="29d70-155">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="29d70-156">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="29d70-156">-ResourceType</span></span>
<span data-ttu-id="29d70-157">Resurs typen.</span><span class="sxs-lookup"><span data-stu-id="29d70-157">The resource type.</span></span>
<span data-ttu-id="29d70-158">Till exempel. Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="29d70-158">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="29d70-159">Bör endast användas tillsammans med ParentResource-parametrar (ResourceGroupName, ResourceName och (valfritt) för att skapa ett hierarkiskt scope i form av en relativ URI som identifierar en resurs.</span><span class="sxs-lookup"><span data-stu-id="29d70-159">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="29d70-160">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="29d70-160">-RoleDefinitionId</span></span>
<span data-ttu-id="29d70-161">ID för den RBAC-roll som måste tilldelas huvudobjektet.</span><span class="sxs-lookup"><span data-stu-id="29d70-161">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="29d70-162">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="29d70-162">-RoleDefinitionName</span></span>
<span data-ttu-id="29d70-163">Namnet på den RBAC-roll som måste tilldelas den huvudansvarige, till exempel läsare, deltagare, virtuell nätverks administratör, etc.</span><span class="sxs-lookup"><span data-stu-id="29d70-163">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29d70-164">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="29d70-164">-Scope</span></span>
<span data-ttu-id="29d70-165">Omfattningen av roll tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="29d70-165">The Scope of the role assignment.</span></span>
<span data-ttu-id="29d70-166">I formatet för relativ URI.</span><span class="sxs-lookup"><span data-stu-id="29d70-166">In the format of relative URI.</span></span>
<span data-ttu-id="29d70-167">Till exempel "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="29d70-167">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="29d70-168">Om det inte anges skapas roll tilldelningen på prenumerations nivå.</span><span class="sxs-lookup"><span data-stu-id="29d70-168">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="29d70-169">Om det anges ska det börja med "/Subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="29d70-169">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29d70-170">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="29d70-170">-ServicePrincipalName</span></span>
<span data-ttu-id="29d70-171">ServicePrincipalName för Azure AD-programmet</span><span class="sxs-lookup"><span data-stu-id="29d70-171">The ServicePrincipalName of the Azure AD application</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29d70-172">-SignInName</span><span class="sxs-lookup"><span data-stu-id="29d70-172">-SignInName</span></span>
<span data-ttu-id="29d70-173">E-postadressen eller användarens huvud namn för användaren.</span><span class="sxs-lookup"><span data-stu-id="29d70-173">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="29d70-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29d70-174">-DefaultProfile</span></span>
<span data-ttu-id="29d70-175">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="29d70-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29d70-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29d70-176">CommonParameters</span></span>
<span data-ttu-id="29d70-177">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29d70-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29d70-178">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29d70-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29d70-179">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29d70-179">INPUTS</span></span>

## <span data-ttu-id="29d70-180">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29d70-180">OUTPUTS</span></span>

### <span data-ttu-id="29d70-181">Microsoft. Azure. kommandon. sources. Models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="29d70-181">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="29d70-182">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29d70-182">NOTES</span></span>
<span data-ttu-id="29d70-183">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="29d70-183">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="29d70-184">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29d70-184">RELATED LINKS</span></span>

[<span data-ttu-id="29d70-185">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="29d70-185">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="29d70-186">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="29d70-186">Remove-AzureRmRoleAssignment</span></span>](./Remove-AzureRmRoleAssignment.md)

[<span data-ttu-id="29d70-187">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="29d70-187">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

