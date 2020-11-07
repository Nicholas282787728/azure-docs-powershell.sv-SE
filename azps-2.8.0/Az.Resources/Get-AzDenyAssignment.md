---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdenyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
ms.openlocfilehash: 745df057c7c111bdca7cc30ac0864e15905ffd6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919340"
---
# <span data-ttu-id="8d557-101">Get-AzDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="8d557-101">Get-AzDenyAssignment</span></span>

## <span data-ttu-id="8d557-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8d557-102">SYNOPSIS</span></span>
<span data-ttu-id="8d557-103">Listar Azure RBAC-neka tilldelningar i det angivna omfånget.</span><span class="sxs-lookup"><span data-stu-id="8d557-103">Lists Azure RBAC deny assignments at the specified scope.</span></span>
<span data-ttu-id="8d557-104">Som standard listar alla neka-uppgifter i det valda Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8d557-104">By default it lists all deny assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="8d557-105">Använd respektive parametrar för att visa en lista över nekade tilldelningar till en viss användare, eller för att lista neka tilldelningar för en viss resurs grupp eller resurs.</span><span class="sxs-lookup"><span data-stu-id="8d557-105">Use respective parameters to list deny assignments to a specific user, or to list deny assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="8d557-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8d557-106">SYNTAX</span></span>

### <span data-ttu-id="8d557-107">EmptyParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8d557-107">EmptyParameterSet (Default)</span></span>
```
Get-AzDenyAssignment [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d557-108">DenyAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d557-108">DenyAssignmentIdParameterSet</span></span>
```
Get-AzDenyAssignment -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d557-109">DenyAssignmentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d557-109">DenyAssignmentNameParameterSet</span></span>
```
Get-AzDenyAssignment -DenyAssignmentName <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d557-110">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d557-110">ObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d557-111">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d557-111">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d557-112">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d557-112">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d557-113">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d557-113">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d557-114">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d557-114">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d557-115">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d557-115">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d557-116">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d557-116">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d557-117">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d557-117">SignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d557-118">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d557-118">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d557-119">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d557-119">ResourceWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d557-120">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d557-120">ScopeWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d557-121">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d557-121">SPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d557-122">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d557-122">ResourceGroupParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d557-123">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d557-123">ResourceParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d557-124">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d557-124">ScopeParameterSet</span></span>
```
Get-AzDenyAssignment -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d557-125">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8d557-125">DESCRIPTION</span></span>
<span data-ttu-id="8d557-126">Använd kommandot Get-AzDenyAssignment om du vill visa alla neka-uppgifter som är giltiga för ett område.</span><span class="sxs-lookup"><span data-stu-id="8d557-126">Use the Get-AzDenyAssignment command to list all deny assignments that are effective on a scope.</span></span>
<span data-ttu-id="8d557-127">Utan parametrar returnerar detta kommando alla neka-tilldelningar under prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8d557-127">Without any parameters, this command returns all the deny assignments made under the subscription.</span></span>
<span data-ttu-id="8d557-128">Den här listan kan filtreras med hjälp av filtrerings parametrar för huvud kontot, neka tilldelningens namn och omfattning.</span><span class="sxs-lookup"><span data-stu-id="8d557-128">This list can  be filtered using filtering parameters for principal, deny assignment name and scope.</span></span>
<span data-ttu-id="8d557-129">Ange en användare med hjälp av SignInName eller Azure AD ObjectId-parametrar.</span><span class="sxs-lookup"><span data-stu-id="8d557-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="8d557-130">Om du vill ange en säkerhets grupp använder du Azure AD ObjectId-parameter.</span><span class="sxs-lookup"><span data-stu-id="8d557-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="8d557-131">Och om du vill ange ett Azure AD-program använder du ServicePrincipalName-eller ObjectId-parametrar.</span><span class="sxs-lookup"><span data-stu-id="8d557-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="8d557-132">Omfattningen som åtkomst nekas för kan anges.</span><span class="sxs-lookup"><span data-stu-id="8d557-132">The scope at which access is being denied may be specified.</span></span>
<span data-ttu-id="8d557-133">Det är standardinställningen för det valda abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8d557-133">It defaults to the selected subscription.</span></span>
<span data-ttu-id="8d557-134">Omfattningen av uppgiften neka kan anges med hjälp av någon av följande parameter kombinationer a.</span><span class="sxs-lookup"><span data-stu-id="8d557-134">The scope of the deny assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="8d557-135">Scope-det här är det fullt kvalificerade scopet som börjar med/Subscriptions/ \< subscriptionId \> .</span><span class="sxs-lookup"><span data-stu-id="8d557-135">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="8d557-136">Detta filtrerar nekade tilldelningar i det specifika området, t. ex.</span><span class="sxs-lookup"><span data-stu-id="8d557-136">This will filter deny assignments that are effective at that particular scope i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="8d557-137">h.</span><span class="sxs-lookup"><span data-stu-id="8d557-137">b.</span></span>
<span data-ttu-id="8d557-138">ResourceGroupName-namnet på en resurs grupp under prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8d557-138">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="8d557-139">Då filtreras tilldelningarna effektivt i den angivna resurs gruppen, t. ex.</span><span class="sxs-lookup"><span data-stu-id="8d557-139">This will filter assignments effective at the specified resource group i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="8d557-140">f.</span><span class="sxs-lookup"><span data-stu-id="8d557-140">c.</span></span>
<span data-ttu-id="8d557-141">ResourceName, ResourceType, ResourceGroupName och (valfritt) ParentResource-identifierar en viss resurs under prenumerationen och filtrerar neka tilldelningar i den resurs omfattningen.</span><span class="sxs-lookup"><span data-stu-id="8d557-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter deny assignments effective at that resource scope.</span></span>
<span data-ttu-id="8d557-142">Använd växeln ExpandPrincipalGroups för att avgöra vilken åtkomst som nekas för en viss användare i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8d557-142">To determine what access is denied for a particular user in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="8d557-143">Här listas alla nekade tilldelningar som har tilldelats användaren, och till de grupper som användaren är medlem i.</span><span class="sxs-lookup"><span data-stu-id="8d557-143">This will list all deny assignments assigned to the user, and to the groups that the user is member of.</span></span>

## <span data-ttu-id="8d557-144">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8d557-144">EXAMPLES</span></span>

### <span data-ttu-id="8d557-145">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8d557-145">Example 1</span></span>

<span data-ttu-id="8d557-146">Lista alla neka-uppgifter i prenumerationen</span><span class="sxs-lookup"><span data-stu-id="8d557-146">List all deny assignments in the subscription</span></span>

```
PS C:\> Get-AzDenyAssignment
Id                      : 22704996-fbd0-4ab1-8625-722d897825d2
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  All Principals
                          ObjectType:   SystemDefined
                          ObjectId:     00000000-0000-0000-0000-000000000000
                          }
ExcludePrincipals       : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
IsSystemProtected       : True

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  PowershellTestingApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="8d557-147">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8d557-147">Example 2</span></span>

<span data-ttu-id="8d557-148">Hämtar alla neka-tilldelningar till användaren john.doe@contoso.com i omfattningen testRG och senare.</span><span class="sxs-lookup"><span data-stu-id="8d557-148">Gets all deny assignments made to user john.doe@contoso.com at the scope testRG and above.</span></span>

```
PS C:\> Get-AzDenyAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com

Id                      : 22704996-fbd0-4ab1-8625-722d897825d2
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  john.doe
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  john.doe
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  PowershellTestingApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="8d557-149">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="8d557-149">Example 3</span></span>

<span data-ttu-id="8d557-150">Får alla neka-tilldelningar för det angivna tjänst säkerhets objekt</span><span class="sxs-lookup"><span data-stu-id="8d557-150">Gets all deny assignments of the specified service principal</span></span>

```
PS C:\> Get-AzDenyAssignment -ServicePrincipalName 'http://testapp1.com'

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 94e3d9da-3700-4113-aab4-15f6c173d794
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/testRG/providers/Microsoft.Web/sites/site1
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="8d557-151">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="8d557-151">Example 4</span></span>

<span data-ttu-id="8d557-152">Nekar tilldelningar på webbplats omfattningen ' site1 '.</span><span class="sxs-lookup"><span data-stu-id="8d557-152">Gets deny assignments at the 'site1' website scope.</span></span>

```
PS C:\> Get-AzDenyAssignment -Scope '/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/testRG/providers/Microsoft.Web/sites/site1'

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 94e3d9da-3700-4113-aab4-15f6c173d794
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/testRG/providers/Microsoft.Web/sites/site1
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

```

## <span data-ttu-id="8d557-153">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8d557-153">PARAMETERS</span></span>

### <span data-ttu-id="8d557-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d557-154">-DefaultProfile</span></span>
<span data-ttu-id="8d557-155">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8d557-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d557-156">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="8d557-156">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="8d557-157">Om det här alternativet anges nekar du de uppgifter som är direkt tilldelade till användaren och till de grupper som användaren är medlem i (transitivt).</span><span class="sxs-lookup"><span data-stu-id="8d557-157">If specified, returns deny assignments directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="8d557-158">Stöds endast för en användares huvud.</span><span class="sxs-lookup"><span data-stu-id="8d557-158">Supported only for a user principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ObjectIdParameterSet, SignInNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d557-159">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8d557-159">-ObjectId</span></span>
<span data-ttu-id="8d557-160">Azure AD ObjectId för användaren, gruppen eller tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="8d557-160">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="8d557-161">Filtrerar alla neka-uppgifter som görs till det angivna huvudobjektet.</span><span class="sxs-lookup"><span data-stu-id="8d557-161">Filters all deny assignments that are made to the specified principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d557-162">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="8d557-162">-ParentResource</span></span>
<span data-ttu-id="8d557-163">Den överordnade resursen i hierarkin för den resurs som anges med parametern ResourceName.</span><span class="sxs-lookup"><span data-stu-id="8d557-163">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="8d557-164">Måste användas tillsammans med parametrarna ResourceGroupName, ResourceType och ResourceName.</span><span class="sxs-lookup"><span data-stu-id="8d557-164">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d557-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d557-165">-ResourceGroupName</span></span>
<span data-ttu-id="8d557-166">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="8d557-166">The resource group name.</span></span>
<span data-ttu-id="8d557-167">Listor för att neka tilldelningar som gäller för den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8d557-167">Lists deny assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="8d557-168">När kommandot används tillsammans med kommandona ResourceName, ResourceType och ParentResource visas de Tillåt tilldelningar som gäller för resurser i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8d557-168">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists deny assignments effective at resources within the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d557-169">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8d557-169">-ResourceName</span></span>
<span data-ttu-id="8d557-170">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="8d557-170">The resource name.</span></span>
<span data-ttu-id="8d557-171">T. storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="8d557-171">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="8d557-172">Måste användas tillsammans med ResourceGroupName-, ResourceType-och (valfritt) ParentResource-parametrar.</span><span class="sxs-lookup"><span data-stu-id="8d557-172">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d557-173">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8d557-173">-ResourceType</span></span>
<span data-ttu-id="8d557-174">Resurs typen.</span><span class="sxs-lookup"><span data-stu-id="8d557-174">The resource type.</span></span>
<span data-ttu-id="8d557-175">Till exempel. Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="8d557-175">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="8d557-176">Måste användas tillsammans med ResourceGroupName, ResourceName och (valfritt) ParentResource-parametrar.</span><span class="sxs-lookup"><span data-stu-id="8d557-176">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d557-177">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="8d557-177">-Scope</span></span>
<span data-ttu-id="8d557-178">Omfattningen av roll tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="8d557-178">The Scope of the role assignment.</span></span>
<span data-ttu-id="8d557-179">I formatet för relativ URI.</span><span class="sxs-lookup"><span data-stu-id="8d557-179">In the format of relative URI.</span></span>
<span data-ttu-id="8d557-180">T./subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="8d557-180">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="8d557-181">Det måste börja med "/Subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="8d557-181">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="8d557-182">Kommandot filtrerar alla de tilldelningar som är giltiga för det aktuella området.</span><span class="sxs-lookup"><span data-stu-id="8d557-182">The command filters all deny assignments that are effective at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet, ScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d557-183">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8d557-183">-ServicePrincipalName</span></span>
<span data-ttu-id="8d557-184">ServicePrincipalName för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="8d557-184">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="8d557-185">Filtrerar alla neka-uppgifter som görs till det angivna Azure AD-programmet.</span><span class="sxs-lookup"><span data-stu-id="8d557-185">Filters all deny assignments that are made to the specified Azure AD application.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d557-186">-SignInName</span><span class="sxs-lookup"><span data-stu-id="8d557-186">-SignInName</span></span>
<span data-ttu-id="8d557-187">E-postadressen eller användarens huvud namn för användaren.</span><span class="sxs-lookup"><span data-stu-id="8d557-187">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="8d557-188">Filtrerar alla neka-uppgifter som görs till angiven användare.</span><span class="sxs-lookup"><span data-stu-id="8d557-188">Filters all deny assignments that are made to the specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d557-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d557-189">CommonParameters</span></span>
<span data-ttu-id="8d557-190">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d557-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d557-191">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d557-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d557-192">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8d557-192">INPUTS</span></span>

### <span data-ttu-id="8d557-193">System. GUID</span><span class="sxs-lookup"><span data-stu-id="8d557-193">System.Guid</span></span>

### <span data-ttu-id="8d557-194">System. String</span><span class="sxs-lookup"><span data-stu-id="8d557-194">System.String</span></span>

## <span data-ttu-id="8d557-195">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8d557-195">OUTPUTS</span></span>

### <span data-ttu-id="8d557-196">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="8d557-196">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span></span>

## <span data-ttu-id="8d557-197">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8d557-197">NOTES</span></span>
<span data-ttu-id="8d557-198">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="8d557-198">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>