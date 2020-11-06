---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleAssignment.md
ms.openlocfilehash: 746dc2c7665cf41dc8d70bf7b16f667c6e22ef89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575524"
---
# <span data-ttu-id="58c34-101">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="58c34-101">New-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="58c34-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="58c34-102">SYNOPSIS</span></span>
<span data-ttu-id="58c34-103">Tilldelar den angivna RBAC-rollen till den angivna huvud delen, vid det angivna omfånget.</span><span class="sxs-lookup"><span data-stu-id="58c34-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58c34-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="58c34-104">SYNTAX</span></span>

### <span data-ttu-id="58c34-105">EmptyParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="58c34-105">EmptyParameterSet (Default)</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -Scope <String> -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58c34-106">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58c34-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58c34-107">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58c34-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58c34-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58c34-108">ScopeWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58c34-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58c34-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -Scope <String> -RoleDefinitionId <Guid> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58c34-110">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="58c34-110">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58c34-111">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="58c34-111">ResourceWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58c34-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="58c34-112">ScopeWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58c34-113">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="58c34-113">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58c34-114">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="58c34-114">ResourceWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58c34-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="58c34-115">ScopeWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ApplicationId <String> [-Scope <String>] -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58c34-116">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="58c34-116">DESCRIPTION</span></span>
<span data-ttu-id="58c34-117">Använd kommandot New-AzureRMRoleAssignment för att ge åtkomst.</span><span class="sxs-lookup"><span data-stu-id="58c34-117">Use the New-AzureRMRoleAssignment command to grant access.</span></span>
<span data-ttu-id="58c34-118">Åtkomst beviljas genom att den lämpliga RBAC-rollen tilldelas till dem vid rätt scope.</span><span class="sxs-lookup"><span data-stu-id="58c34-118">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="58c34-119">Om du vill bevilja åtkomst till hela abonnemanget tilldelar du en roll i prenumerations omfattningen.</span><span class="sxs-lookup"><span data-stu-id="58c34-119">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="58c34-120">Om du vill bevilja åtkomst till en viss resurs grupp i en prenumeration tilldelar du en roll i resurs gruppens omfattning.</span><span class="sxs-lookup"><span data-stu-id="58c34-120">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>

<span data-ttu-id="58c34-121">Uppgiftens ämne måste anges.</span><span class="sxs-lookup"><span data-stu-id="58c34-121">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="58c34-122">Ange en användare med hjälp av SignInName eller Azure AD ObjectId-parametrar.</span><span class="sxs-lookup"><span data-stu-id="58c34-122">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="58c34-123">Om du vill ange en säkerhets grupp använder du Azure AD ObjectId-parameter.</span><span class="sxs-lookup"><span data-stu-id="58c34-123">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="58c34-124">Om du vill ange ett Azure AD-program använder du ApplicationId-eller ObjectId-parametrar.</span><span class="sxs-lookup"><span data-stu-id="58c34-124">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>

<span data-ttu-id="58c34-125">Rollen som tilldelas måste anges med parametern RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="58c34-125">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>

<span data-ttu-id="58c34-126">Omfattningen där åtkomst ges kan anges.</span><span class="sxs-lookup"><span data-stu-id="58c34-126">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="58c34-127">Det är standardinställningen för det valda abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="58c34-127">It defaults to the selected subscription.</span></span> <span data-ttu-id="58c34-128">Omfattningen av uppgiften kan anges med hjälp av någon av följande parameter kombinationer a.</span><span class="sxs-lookup"><span data-stu-id="58c34-128">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="58c34-129">Scope-det här är det fullt kvalificerade scopet som börjar med/Subscriptions/ \<subscriptionId\> b.</span><span class="sxs-lookup"><span data-stu-id="58c34-129">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="58c34-130">ResourceGroupName – om du vill bevilja åtkomst till den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="58c34-130">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="58c34-131">f.</span><span class="sxs-lookup"><span data-stu-id="58c34-131">c.</span></span>
<span data-ttu-id="58c34-132">ResourceName, ResourceType, ResourceGroupName och (valfritt) ParentResource-för att ange en viss resurs i en resurs grupp för att bevilja åtkomst till.</span><span class="sxs-lookup"><span data-stu-id="58c34-132">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="58c34-133">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="58c34-133">EXAMPLES</span></span>

### <span data-ttu-id="58c34-134">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="58c34-134">Example 1</span></span>
```
PS C:\> New-AzureRmRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader -AllowDelegation
```

<span data-ttu-id="58c34-135">Ge läsare rollen åtkomst till en användare i en resurs grupp omfattning med den roll tilldelning som är tillgänglig för delegering</span><span class="sxs-lookup"><span data-stu-id="58c34-135">Grant Reader role access to a user at a resource group scope with the Role Assignment being available for delegation</span></span>

### <span data-ttu-id="58c34-136">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="58c34-136">Example 2</span></span>
```
PS C:\> Get-AzureRMADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           ObjectId
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzureRmRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="58c34-137">Bevilja åtkomst till en säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="58c34-137">Grant access to a security group</span></span>

### <span data-ttu-id="58c34-138">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="58c34-138">Example 3</span></span>
```
PS C:\> New-AzureRmRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="58c34-139">Bevilja åtkomst till en användare på en resurs (webbplats)</span><span class="sxs-lookup"><span data-stu-id="58c34-139">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="58c34-140">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="58c34-140">Example 4</span></span>
```
PS C:\> New-AzureRMRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="58c34-141">Bevilja åtkomst till en grupp på en kapslad resurs (delnät)</span><span class="sxs-lookup"><span data-stu-id="58c34-141">Grant access to a group at a nested resource (subnet)</span></span>

### <span data-ttu-id="58c34-142">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="58c34-142">Example 5</span></span>
```
PS C:\> $servicePrincipal = New-AzureRmADServicePrincipal -DisplayName "testServiceprincipal"
PS C:\> New-AzureRmRoleAssignment -RoleDefinitionName "Reader" -ApplicationId $servicePrincipal.ApplicationId
```

<span data-ttu-id="58c34-143">Ge läsare åtkomst till ett tjänst huvud konto</span><span class="sxs-lookup"><span data-stu-id="58c34-143">Grant reader access to a service principal</span></span>

## <span data-ttu-id="58c34-144">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="58c34-144">PARAMETERS</span></span>

### <span data-ttu-id="58c34-145">-AllowDelegation</span><span class="sxs-lookup"><span data-stu-id="58c34-145">-AllowDelegation</span></span>
<span data-ttu-id="58c34-146">Delegerings flaggan när du skapar en roll tilldelning.</span><span class="sxs-lookup"><span data-stu-id="58c34-146">The delegation flag while creating a Role assignment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c34-147">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="58c34-147">-ApplicationId</span></span>
<span data-ttu-id="58c34-148">Program-ID för ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="58c34-148">The Application ID of the ServicePrincipal</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN, ServicePrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58c34-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58c34-149">-DefaultProfile</span></span>
<span data-ttu-id="58c34-150">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="58c34-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c34-151">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="58c34-151">-ObjectId</span></span>
<span data-ttu-id="58c34-152">Azure AD ObjectID för användaren, gruppen eller tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="58c34-152">Azure AD Objectid of the user, group or service principal.</span></span>

```yaml
Type: Guid
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58c34-153">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="58c34-153">-ParentResource</span></span>
<span data-ttu-id="58c34-154">Den överordnade resursen i hierarkin (av resursen som anges med parametern ResourceName).</span><span class="sxs-lookup"><span data-stu-id="58c34-154">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="58c34-155">Bör endast användas tillsammans med parametrarna ResourceGroupName, ResourceType och ResourceName för att konstruera ett hierarkiskt scope i form av en relativ URI som identifierar en resurs.</span><span class="sxs-lookup"><span data-stu-id="58c34-155">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58c34-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58c34-156">-ResourceGroupName</span></span>
<span data-ttu-id="58c34-157">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="58c34-157">The resource group name.</span></span>
<span data-ttu-id="58c34-158">Skapar en tilldelning som gäller för den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="58c34-158">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="58c34-159">När kommandot används tillsammans med kommandona ResourceName, ResourceType och (valfritt) ParentResource, skapas ett hierarkiskt område i form av en relativ URI som identifierar en resurs.</span><span class="sxs-lookup"><span data-stu-id="58c34-159">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58c34-160">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="58c34-160">-ResourceName</span></span>
<span data-ttu-id="58c34-161">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="58c34-161">The resource name.</span></span>
<span data-ttu-id="58c34-162">T. storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="58c34-162">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="58c34-163">Bör endast användas tillsammans med ResourceGroupName-, ResourceType-och (valfritt) ParentResource-parametrar för att skapa ett hierarkiskt scope i form av en relativ URI som identifierar en resurs.</span><span class="sxs-lookup"><span data-stu-id="58c34-163">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58c34-164">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="58c34-164">-ResourceType</span></span>
<span data-ttu-id="58c34-165">Resurs typen.</span><span class="sxs-lookup"><span data-stu-id="58c34-165">The resource type.</span></span>
<span data-ttu-id="58c34-166">Till exempel. Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="58c34-166">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="58c34-167">Bör endast användas tillsammans med ParentResource-parametrar (ResourceGroupName, ResourceName och (valfritt) för att skapa ett hierarkiskt scope i form av en relativ URI som identifierar en resurs.</span><span class="sxs-lookup"><span data-stu-id="58c34-167">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58c34-168">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="58c34-168">-RoleDefinitionId</span></span>
<span data-ttu-id="58c34-169">ID för den RBAC-roll som måste tilldelas huvudobjektet.</span><span class="sxs-lookup"><span data-stu-id="58c34-169">Id of the RBAC role that needs to be assigned to the principal.</span></span>

```yaml
Type: Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58c34-170">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="58c34-170">-RoleDefinitionName</span></span>
<span data-ttu-id="58c34-171">Namnet på den RBAC-roll som måste tilldelas den huvudansvarige, till exempel läsare, deltagare, virtuell nätverks administratör, etc.</span><span class="sxs-lookup"><span data-stu-id="58c34-171">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58c34-172">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="58c34-172">-Scope</span></span>
<span data-ttu-id="58c34-173">Omfattningen av roll tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="58c34-173">The Scope of the role assignment.</span></span>
<span data-ttu-id="58c34-174">I formatet för relativ URI.</span><span class="sxs-lookup"><span data-stu-id="58c34-174">In the format of relative URI.</span></span>
<span data-ttu-id="58c34-175">Till exempel "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="58c34-175">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="58c34-176">Om det inte anges skapas roll tilldelningen på prenumerations nivå.</span><span class="sxs-lookup"><span data-stu-id="58c34-176">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="58c34-177">Om det anges ska det börja med "/Subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="58c34-177">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: String
Parameter Sets: EmptyParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58c34-178">-SignInName</span><span class="sxs-lookup"><span data-stu-id="58c34-178">-SignInName</span></span>
<span data-ttu-id="58c34-179">E-postadressen eller användarens huvud namn för användaren.</span><span class="sxs-lookup"><span data-stu-id="58c34-179">The email address or the user principal name of the user.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58c34-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58c34-180">CommonParameters</span></span>
<span data-ttu-id="58c34-181">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58c34-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58c34-182">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58c34-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58c34-183">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="58c34-183">INPUTS</span></span>

### <span data-ttu-id="58c34-184">Ingen</span><span class="sxs-lookup"><span data-stu-id="58c34-184">None</span></span>
<span data-ttu-id="58c34-185">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="58c34-185">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="58c34-186">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="58c34-186">OUTPUTS</span></span>

### <span data-ttu-id="58c34-187">Microsoft. Azure. kommandon. sources. Models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="58c34-187">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="58c34-188">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="58c34-188">NOTES</span></span>
<span data-ttu-id="58c34-189">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="58c34-189">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="58c34-190">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="58c34-190">RELATED LINKS</span></span>

[<span data-ttu-id="58c34-191">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="58c34-191">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="58c34-192">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="58c34-192">Remove-AzureRmRoleAssignment</span></span>](./Remove-AzureRmRoleAssignment.md)

[<span data-ttu-id="58c34-193">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="58c34-193">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)
