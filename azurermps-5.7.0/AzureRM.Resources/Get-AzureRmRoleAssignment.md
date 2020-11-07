---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleAssignment.md
ms.openlocfilehash: c6dd17917624d8b2b914ac94c8310358fac03b68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581988"
---
# <span data-ttu-id="0686e-101">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0686e-101">Get-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="0686e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0686e-102">SYNOPSIS</span></span>
<span data-ttu-id="0686e-103">Visar en lista med Azure RBAC-resurstilldelningar för det angivna omfånget.</span><span class="sxs-lookup"><span data-stu-id="0686e-103">Lists Azure RBAC role assignments at the specified scope.</span></span>
<span data-ttu-id="0686e-104">Som standard visar den alla roll tilldelningar i det valda Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="0686e-104">By default it lists all role assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="0686e-105">Använd respektive parametrar för att lista tilldelningar till en viss användare, eller för att lista tilldelningar för en viss resurs grupp eller resurs.</span><span class="sxs-lookup"><span data-stu-id="0686e-105">Use respective parameters to list assignments to a specific user, or to list assignments on a specific resource group or resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0686e-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0686e-106">SYNTAX</span></span>

### <span data-ttu-id="0686e-107">EmptyParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0686e-107">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0686e-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0686e-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0686e-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0686e-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0686e-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0686e-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0686e-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0686e-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0686e-112">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0686e-112">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment [-ObjectId <Guid>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0686e-113">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0686e-113">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0686e-114">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0686e-114">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0686e-115">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0686e-115">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0686e-116">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0686e-116">SignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0686e-117">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="0686e-117">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 [-RoleDefinitionName <String>] [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0686e-118">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="0686e-118">ResourceWithSPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0686e-119">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="0686e-119">ScopeWithSPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0686e-120">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="0686e-120">SPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0686e-121">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="0686e-121">ResourceGroupParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0686e-122">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="0686e-122">ResourceParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0686e-123">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="0686e-123">ScopeParameterSet</span></span>
```
Get-AzureRmRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0686e-124">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0686e-124">DESCRIPTION</span></span>
<span data-ttu-id="0686e-125">Använd kommandot Get-AzureRMRoleAssignment om du vill visa en lista över alla roll tilldelningar som gäller för ett område.</span><span class="sxs-lookup"><span data-stu-id="0686e-125">Use the Get-AzureRMRoleAssignment command to list all role assignments that are effective on a scope.</span></span>

<span data-ttu-id="0686e-126">Utan parametrar returnerar detta kommando alla roll tilldelningar som har gjorts under prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0686e-126">Without any parameters, this command returns all the role assignments made under the subscription.</span></span>
<span data-ttu-id="0686e-127">Den här listan kan filtreras med hjälp av filtrerings parametrar för huvud-, roll-och omfattning.</span><span class="sxs-lookup"><span data-stu-id="0686e-127">This list can  be filtered using filtering parameters for principal, role and scope.</span></span>

<span data-ttu-id="0686e-128">Uppgiftens ämne måste anges.</span><span class="sxs-lookup"><span data-stu-id="0686e-128">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="0686e-129">Ange en användare med hjälp av SignInName eller Azure AD ObjectId-parametrar.</span><span class="sxs-lookup"><span data-stu-id="0686e-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="0686e-130">Om du vill ange en säkerhets grupp använder du Azure AD ObjectId-parameter.</span><span class="sxs-lookup"><span data-stu-id="0686e-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="0686e-131">Och om du vill ange ett Azure AD-program använder du ServicePrincipalName-eller ObjectId-parametrar.</span><span class="sxs-lookup"><span data-stu-id="0686e-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>

<span data-ttu-id="0686e-132">Rollen som tilldelas måste anges med parametern RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="0686e-132">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>

<span data-ttu-id="0686e-133">Omfattningen där åtkomst ges kan anges.</span><span class="sxs-lookup"><span data-stu-id="0686e-133">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="0686e-134">Det är standardinställningen för det valda abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="0686e-134">It defaults to the selected subscription.</span></span> <span data-ttu-id="0686e-135">Omfattningen av uppgiften kan anges med hjälp av någon av följande parameter kombinationer a.</span><span class="sxs-lookup"><span data-stu-id="0686e-135">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="0686e-136">Scope-det här är det fullt kvalificerade intervallet från och med/Subscriptions/ \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="0686e-136">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="0686e-137">Då filtreras de uppgifter som är gällande för det specifika området, t. ex.</span><span class="sxs-lookup"><span data-stu-id="0686e-137">This will filter assignments that are effective at that particular scope i.e. all assignments at that scope and above.</span></span>
<span data-ttu-id="0686e-138">h.</span><span class="sxs-lookup"><span data-stu-id="0686e-138">b.</span></span>
<span data-ttu-id="0686e-139">ResourceGroupName-namnet på en resurs grupp under prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0686e-139">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="0686e-140">Då filtreras tilldelningarna effektivt efter den angivna resurs gruppen c.</span><span class="sxs-lookup"><span data-stu-id="0686e-140">This will filter assignments effective at the specified resource group c.</span></span>
<span data-ttu-id="0686e-141">ResourceName, ResourceType, ResourceGroupName och (valfritt) ParentResource-identifierar en viss resurs under prenumerationen och kommer att kunna filtrera tilldelningarna i den aktuella resurs omfattningen.</span><span class="sxs-lookup"><span data-stu-id="0686e-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter assignments effective at that resource scope.</span></span>

<span data-ttu-id="0686e-142">Använd växeln ExpandPrincipalGroups för att avgöra vilken åtkomst en viss användare har i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0686e-142">To determine what access a particular user has in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="0686e-143">Här listas alla roller som har tilldelats till användaren och till de grupper som användaren är medlem i.</span><span class="sxs-lookup"><span data-stu-id="0686e-143">This will list all roles assigned to the user, and to the groups that the user is member of.</span></span>

<span data-ttu-id="0686e-144">Använd växeln IncludeClassicAdministrators om du även vill visa abonnemangs administratörer och medadministratörer.</span><span class="sxs-lookup"><span data-stu-id="0686e-144">Use the IncludeClassicAdministrators switch to also display the subscription admins and co-admins.</span></span>

## <span data-ttu-id="0686e-145">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0686e-145">EXAMPLES</span></span>

### <span data-ttu-id="0686e-146">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0686e-146">Example 1</span></span>
```
PS C:\> Get-AzureRmRoleAssignment
```

<span data-ttu-id="0686e-147">Lista alla roll tilldelningar i prenumerationen</span><span class="sxs-lookup"><span data-stu-id="0686e-147">List all role assignments in the subscription</span></span>

### <span data-ttu-id="0686e-148">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0686e-148">Example 2</span></span>
```
PS C:\> Get-AzureRmRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com
```

<span data-ttu-id="0686e-149">Hämtar alla roll tilldelningar till en användare john.doe@contoso.com och de grupper som han är medlem i, i testRG omfattning eller ovan.</span><span class="sxs-lookup"><span data-stu-id="0686e-149">Gets all role assignments made to user john.doe@contoso.com, and the groups of which he is member, at the testRG scope or above.</span></span>

### <span data-ttu-id="0686e-150">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="0686e-150">Example 3</span></span>
```
PS C:\> Get-AzureRmRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

<span data-ttu-id="0686e-151">Hämtar alla roll tilldelningar för den angivna tjänstens huvud namn</span><span class="sxs-lookup"><span data-stu-id="0686e-151">Gets all role assignments of the specified service principal</span></span>

### <span data-ttu-id="0686e-152">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="0686e-152">Example 4</span></span>
```
PS C:\> Get-AzureRmRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="0686e-153">Hämtar roll tilldelningar på webbplats omfattningen ' site1 '.</span><span class="sxs-lookup"><span data-stu-id="0686e-153">Gets role assignments at the 'site1' website scope.</span></span>

## <span data-ttu-id="0686e-154">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0686e-154">PARAMETERS</span></span>

### <span data-ttu-id="0686e-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0686e-155">-DefaultProfile</span></span>
<span data-ttu-id="0686e-156">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0686e-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0686e-157">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="0686e-157">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="0686e-158">Om du anger det här alternativet returneras roller direkt tilldelade till användaren och till de grupper som användaren är medlem i (transitivt).</span><span class="sxs-lookup"><span data-stu-id="0686e-158">If specified, returns roles directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="0686e-159">Stöds endast för en användares huvud.</span><span class="sxs-lookup"><span data-stu-id="0686e-159">Supported only for a user principal.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ObjectIdParameterSet, SignInNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0686e-160">-IncludeClassicAdministrators</span><span class="sxs-lookup"><span data-stu-id="0686e-160">-IncludeClassicAdministrators</span></span>
<span data-ttu-id="0686e-161">Om det här anges kan du även lista de administratörer som är klassiska (medadministratörer, tjänst administratörer och andra).</span><span class="sxs-lookup"><span data-stu-id="0686e-161">If specified, also lists subscription classic administrators (co-admins, service admins, etc.) role assignments.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0686e-162">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0686e-162">-ObjectId</span></span>
<span data-ttu-id="0686e-163">Azure AD ObjectId för användaren, gruppen eller tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="0686e-163">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="0686e-164">Filtrerar alla uppgifter som görs till det angivna huvudobjektet.</span><span class="sxs-lookup"><span data-stu-id="0686e-164">Filters all assignments that are made to the specified principal.</span></span>

```yaml
Type: Guid
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0686e-165">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="0686e-165">-ParentResource</span></span>
<span data-ttu-id="0686e-166">Den överordnade resursen i hierarkin för den resurs som anges med parametern ResourceName.</span><span class="sxs-lookup"><span data-stu-id="0686e-166">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="0686e-167">Måste användas tillsammans med parametrarna ResourceGroupName, ResourceType och ResourceName.</span><span class="sxs-lookup"><span data-stu-id="0686e-167">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0686e-168">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0686e-168">-ResourceGroupName</span></span>
<span data-ttu-id="0686e-169">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="0686e-169">The resource group name.</span></span>
<span data-ttu-id="0686e-170">Visar de roll tilldelningar som gäller för den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0686e-170">Lists role assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="0686e-171">När kommandot används tillsammans med parametrarna ResourceName, ResourceType och ParentResource visas tilldelningarna effektivt i resurser i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0686e-171">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists assignments effective at resources within the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0686e-172">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0686e-172">-ResourceName</span></span>
<span data-ttu-id="0686e-173">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="0686e-173">The resource name.</span></span>
<span data-ttu-id="0686e-174">T. storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="0686e-174">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="0686e-175">Måste användas tillsammans med ResourceGroupName-, ResourceType-och (valfritt) ParentResource-parametrar.</span><span class="sxs-lookup"><span data-stu-id="0686e-175">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0686e-176">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0686e-176">-ResourceType</span></span>
<span data-ttu-id="0686e-177">Resurs typen.</span><span class="sxs-lookup"><span data-stu-id="0686e-177">The resource type.</span></span>
<span data-ttu-id="0686e-178">Till exempel. Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="0686e-178">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="0686e-179">Måste användas tillsammans med ResourceGroupName, ResourceName och (valfritt) ParentResource-parametrar.</span><span class="sxs-lookup"><span data-stu-id="0686e-179">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0686e-180">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="0686e-180">-RoleDefinitionId</span></span>
<span data-ttu-id="0686e-181">ID för rollen som tilldelats huvudobjektet.</span><span class="sxs-lookup"><span data-stu-id="0686e-181">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="0686e-182">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="0686e-182">-RoleDefinitionName</span></span>
<span data-ttu-id="0686e-183">Roll som är tilldelad till den huvudansvarige, till exempel läsare, deltagare, virtuell nätverks administratör etc.</span><span class="sxs-lookup"><span data-stu-id="0686e-183">Role that is assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: String
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0686e-184">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="0686e-184">-Scope</span></span>
<span data-ttu-id="0686e-185">Omfattningen av roll tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="0686e-185">The Scope of the role assignment.</span></span>
<span data-ttu-id="0686e-186">I formatet för relativ URI.</span><span class="sxs-lookup"><span data-stu-id="0686e-186">In the format of relative URI.</span></span>
<span data-ttu-id="0686e-187">T./subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="0686e-187">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="0686e-188">Det måste börja med "/Subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="0686e-188">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="0686e-189">Kommandot filtrerar alla uppgifter som är giltiga för det aktuella området.</span><span class="sxs-lookup"><span data-stu-id="0686e-189">The command filters all assignments that are effective at that scope.</span></span>

```yaml
Type: String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet, ScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0686e-190">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="0686e-190">-ServicePrincipalName</span></span>
<span data-ttu-id="0686e-191">ServicePrincipalName för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="0686e-191">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="0686e-192">Filtrerar alla uppgifter som görs till det angivna Azure AD-programmet.</span><span class="sxs-lookup"><span data-stu-id="0686e-192">Filters all assignments that are made to the specified Azure AD application.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0686e-193">-SignInName</span><span class="sxs-lookup"><span data-stu-id="0686e-193">-SignInName</span></span>
<span data-ttu-id="0686e-194">E-postadressen eller användarens huvud namn för användaren.</span><span class="sxs-lookup"><span data-stu-id="0686e-194">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="0686e-195">Filtrerar alla uppgifter som görs till angiven användare.</span><span class="sxs-lookup"><span data-stu-id="0686e-195">Filters all assignments that are made to the specified user.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0686e-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0686e-196">CommonParameters</span></span>
<span data-ttu-id="0686e-197">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0686e-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0686e-198">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0686e-198">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0686e-199">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0686e-199">INPUTS</span></span>

### <span data-ttu-id="0686e-200">Ingen</span><span class="sxs-lookup"><span data-stu-id="0686e-200">None</span></span>
<span data-ttu-id="0686e-201">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="0686e-201">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0686e-202">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0686e-202">OUTPUTS</span></span>

### <span data-ttu-id="0686e-203">System. Collections. Generic. list ' 1 [Microsoft. Azure. kommandon. Resources. Authorization. PSRoleAssignment]</span><span class="sxs-lookup"><span data-stu-id="0686e-203">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment]</span></span>

## <span data-ttu-id="0686e-204">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0686e-204">NOTES</span></span>
<span data-ttu-id="0686e-205">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="0686e-205">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="0686e-206">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0686e-206">RELATED LINKS</span></span>

[<span data-ttu-id="0686e-207">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0686e-207">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="0686e-208">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0686e-208">Remove-AzureRmRoleAssignment</span></span>](./Remove-AzureRmRoleAssignment.md)

[<span data-ttu-id="0686e-209">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="0686e-209">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)
