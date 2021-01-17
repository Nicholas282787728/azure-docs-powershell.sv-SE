---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdenyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
ms.openlocfilehash: 22acfc03afa4758c44d6c6f02ac1d734c90a806b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389052"
---
# <span data-ttu-id="25fc0-101">Get-AzDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="25fc0-101">Get-AzDenyAssignment</span></span>

## <span data-ttu-id="25fc0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25fc0-102">SYNOPSIS</span></span>
<span data-ttu-id="25fc0-103">Listar Azure RBAC-neka tilldelningar i det angivna omfånget.</span><span class="sxs-lookup"><span data-stu-id="25fc0-103">Lists Azure RBAC deny assignments at the specified scope.</span></span>
<span data-ttu-id="25fc0-104">Som standard listar alla neka-uppgifter i det valda Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="25fc0-104">By default it lists all deny assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="25fc0-105">Använd respektive parametrar för att visa en lista över nekade tilldelningar till en viss användare, eller för att lista neka tilldelningar för en viss resurs grupp eller resurs.</span><span class="sxs-lookup"><span data-stu-id="25fc0-105">Use respective parameters to list deny assignments to a specific user, or to list deny assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="25fc0-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25fc0-106">SYNTAX</span></span>

### <span data-ttu-id="25fc0-107">EmptyParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="25fc0-107">EmptyParameterSet (Default)</span></span>
```
Get-AzDenyAssignment [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25fc0-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25fc0-108">ObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25fc0-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25fc0-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25fc0-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25fc0-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25fc0-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25fc0-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25fc0-112">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="25fc0-112">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25fc0-113">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="25fc0-113">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25fc0-114">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="25fc0-114">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25fc0-115">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="25fc0-115">SignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25fc0-116">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="25fc0-116">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25fc0-117">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="25fc0-117">ResourceWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25fc0-118">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="25fc0-118">ScopeWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25fc0-119">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="25fc0-119">SPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25fc0-120">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="25fc0-120">ResourceGroupParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25fc0-121">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="25fc0-121">ResourceParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25fc0-122">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="25fc0-122">ScopeParameterSet</span></span>
```
Get-AzDenyAssignment -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25fc0-123">DenyAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25fc0-123">DenyAssignmentIdParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -Id <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25fc0-124">DenyAssignmentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="25fc0-124">DenyAssignmentNameParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -DenyAssignmentName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25fc0-125">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25fc0-125">DESCRIPTION</span></span>
<span data-ttu-id="25fc0-126">Använd kommandot Get-AzDenyAssignment om du vill visa alla neka-uppgifter som är giltiga för ett område.</span><span class="sxs-lookup"><span data-stu-id="25fc0-126">Use the Get-AzDenyAssignment command to list all deny assignments that are effective on a scope.</span></span>
<span data-ttu-id="25fc0-127">Utan parametrar returnerar detta kommando alla neka-tilldelningar under prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="25fc0-127">Without any parameters, this command returns all the deny assignments made under the subscription.</span></span>
<span data-ttu-id="25fc0-128">Den här listan kan filtreras med hjälp av filtrerings parametrar för huvud kontot, neka tilldelningens namn och omfattning.</span><span class="sxs-lookup"><span data-stu-id="25fc0-128">This list can  be filtered using filtering parameters for principal, deny assignment name and scope.</span></span>
<span data-ttu-id="25fc0-129">Ange en användare med hjälp av SignInName eller Azure AD ObjectId-parametrar.</span><span class="sxs-lookup"><span data-stu-id="25fc0-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="25fc0-130">Om du vill ange en säkerhets grupp använder du Azure AD ObjectId-parameter.</span><span class="sxs-lookup"><span data-stu-id="25fc0-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="25fc0-131">Och om du vill ange ett Azure AD-program använder du ServicePrincipalName-eller ObjectId-parametrar.</span><span class="sxs-lookup"><span data-stu-id="25fc0-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="25fc0-132">Omfattningen som åtkomst nekas för kan anges.</span><span class="sxs-lookup"><span data-stu-id="25fc0-132">The scope at which access is being denied may be specified.</span></span>
<span data-ttu-id="25fc0-133">Det är standardinställningen för det valda abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="25fc0-133">It defaults to the selected subscription.</span></span>
<span data-ttu-id="25fc0-134">Omfattningen av uppgiften neka kan anges med hjälp av någon av följande parameter kombinationer a.</span><span class="sxs-lookup"><span data-stu-id="25fc0-134">The scope of the deny assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="25fc0-135">Scope-det här är det fullt kvalificerade intervallet från och med/Subscriptions/ \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="25fc0-135">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="25fc0-136">Detta filtrerar nekade tilldelningar i det specifika området, t. ex.</span><span class="sxs-lookup"><span data-stu-id="25fc0-136">This will filter deny assignments that are effective at that particular scope i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="25fc0-137">h.</span><span class="sxs-lookup"><span data-stu-id="25fc0-137">b.</span></span>
<span data-ttu-id="25fc0-138">ResourceGroupName-namnet på en resurs grupp under prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="25fc0-138">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="25fc0-139">Då filtreras tilldelningarna effektivt i den angivna resurs gruppen, t. ex.</span><span class="sxs-lookup"><span data-stu-id="25fc0-139">This will filter assignments effective at the specified resource group i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="25fc0-140">f.</span><span class="sxs-lookup"><span data-stu-id="25fc0-140">c.</span></span>
<span data-ttu-id="25fc0-141">ResourceName, ResourceType, ResourceGroupName och (valfritt) ParentResource-identifierar en viss resurs under prenumerationen och filtrerar neka tilldelningar i den resurs omfattningen.</span><span class="sxs-lookup"><span data-stu-id="25fc0-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter deny assignments effective at that resource scope.</span></span>
<span data-ttu-id="25fc0-142">Använd växeln ExpandPrincipalGroups för att avgöra vilken åtkomst som nekas för en viss användare i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="25fc0-142">To determine what access is denied for a particular user in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="25fc0-143">Här listas alla nekade tilldelningar som har tilldelats användaren, och till de grupper som användaren är medlem i.</span><span class="sxs-lookup"><span data-stu-id="25fc0-143">This will list all deny assignments assigned to the user, and to the groups that the user is member of.</span></span>

## <span data-ttu-id="25fc0-144">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25fc0-144">EXAMPLES</span></span>

### <span data-ttu-id="25fc0-145">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="25fc0-145">Example 1</span></span>

<span data-ttu-id="25fc0-146">Lista alla neka-uppgifter i prenumerationen</span><span class="sxs-lookup"><span data-stu-id="25fc0-146">List all deny assignments in the subscription</span></span>

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

### <span data-ttu-id="25fc0-147">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="25fc0-147">Example 2</span></span>

<span data-ttu-id="25fc0-148">Hämtar alla neka-tilldelningar till användaren john.doe@contoso.com i omfattningen testRG och senare.</span><span class="sxs-lookup"><span data-stu-id="25fc0-148">Gets all deny assignments made to user john.doe@contoso.com at the scope testRG and above.</span></span>

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

### <span data-ttu-id="25fc0-149">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="25fc0-149">Example 3</span></span>

<span data-ttu-id="25fc0-150">Får alla neka-tilldelningar för det angivna tjänst säkerhets objekt</span><span class="sxs-lookup"><span data-stu-id="25fc0-150">Gets all deny assignments of the specified service principal</span></span>

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

### <span data-ttu-id="25fc0-151">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="25fc0-151">Example 4</span></span>

<span data-ttu-id="25fc0-152">Nekar tilldelningar på webbplats omfattningen ' site1 '.</span><span class="sxs-lookup"><span data-stu-id="25fc0-152">Gets deny assignments at the 'site1' website scope.</span></span>

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

## <span data-ttu-id="25fc0-153">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25fc0-153">PARAMETERS</span></span>

### <span data-ttu-id="25fc0-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25fc0-154">-DefaultProfile</span></span>
<span data-ttu-id="25fc0-155">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="25fc0-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25fc0-156">-DenyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="25fc0-156">-DenyAssignmentName</span></span>
<span data-ttu-id="25fc0-157">Namn på neka-tilldelning.</span><span class="sxs-lookup"><span data-stu-id="25fc0-157">Name of the deny assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: DenyAssignmentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25fc0-158">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="25fc0-158">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="25fc0-159">Om det här alternativet anges nekar du de uppgifter som är direkt tilldelade till användaren och till de grupper som användaren är medlem i (transitivt).</span><span class="sxs-lookup"><span data-stu-id="25fc0-159">If specified, returns deny assignments directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="25fc0-160">Stöds endast för en användares huvud.</span><span class="sxs-lookup"><span data-stu-id="25fc0-160">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="25fc0-161">-ID</span><span class="sxs-lookup"><span data-stu-id="25fc0-161">-Id</span></span>
<span data-ttu-id="25fc0-162">Neka tilldelnings-ID.</span><span class="sxs-lookup"><span data-stu-id="25fc0-162">Deny assignment id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: DenyAssignmentIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25fc0-163">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="25fc0-163">-ObjectId</span></span>
<span data-ttu-id="25fc0-164">Azure AD ObjectId för användaren, gruppen eller tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="25fc0-164">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="25fc0-165">Filtrerar alla neka-uppgifter som görs till det angivna huvudobjektet.</span><span class="sxs-lookup"><span data-stu-id="25fc0-165">Filters all deny assignments that are made to the specified principal.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25fc0-166">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="25fc0-166">-ParentResource</span></span>
<span data-ttu-id="25fc0-167">Den överordnade resursen i hierarkin för den resurs som anges med parametern ResourceName.</span><span class="sxs-lookup"><span data-stu-id="25fc0-167">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="25fc0-168">Måste användas tillsammans med parametrarna ResourceGroupName, ResourceType och ResourceName.</span><span class="sxs-lookup"><span data-stu-id="25fc0-168">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="25fc0-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25fc0-169">-ResourceGroupName</span></span>
<span data-ttu-id="25fc0-170">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="25fc0-170">The resource group name.</span></span>
<span data-ttu-id="25fc0-171">Listor för att neka tilldelningar som gäller för den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="25fc0-171">Lists deny assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="25fc0-172">När kommandot används tillsammans med kommandona ResourceName, ResourceType och ParentResource visas de Tillåt tilldelningar som gäller för resurser i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="25fc0-172">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists deny assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="25fc0-173">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="25fc0-173">-ResourceName</span></span>
<span data-ttu-id="25fc0-174">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="25fc0-174">The resource name.</span></span>
<span data-ttu-id="25fc0-175">T. storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="25fc0-175">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="25fc0-176">Måste användas tillsammans med ResourceGroupName-, ResourceType-och (valfritt) ParentResource-parametrar.</span><span class="sxs-lookup"><span data-stu-id="25fc0-176">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="25fc0-177">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="25fc0-177">-ResourceType</span></span>
<span data-ttu-id="25fc0-178">Resurs typen.</span><span class="sxs-lookup"><span data-stu-id="25fc0-178">The resource type.</span></span>
<span data-ttu-id="25fc0-179">Till exempel. Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="25fc0-179">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="25fc0-180">Måste användas tillsammans med ResourceGroupName, ResourceName och (valfritt) ParentResource-parametrar.</span><span class="sxs-lookup"><span data-stu-id="25fc0-180">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="25fc0-181">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="25fc0-181">-Scope</span></span>
<span data-ttu-id="25fc0-182">Omfattningen av roll tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="25fc0-182">The Scope of the role assignment.</span></span>
<span data-ttu-id="25fc0-183">I formatet för relativ URI.</span><span class="sxs-lookup"><span data-stu-id="25fc0-183">In the format of relative URI.</span></span>
<span data-ttu-id="25fc0-184">T./subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="25fc0-184">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="25fc0-185">Det måste börja med "/Subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="25fc0-185">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="25fc0-186">Kommandot filtrerar alla de tilldelningar som är giltiga för det aktuella området.</span><span class="sxs-lookup"><span data-stu-id="25fc0-186">The command filters all deny assignments that are effective at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, DenyAssignmentIdParameterSet, DenyAssignmentNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="25fc0-187">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="25fc0-187">-ServicePrincipalName</span></span>
<span data-ttu-id="25fc0-188">ServicePrincipalName för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="25fc0-188">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="25fc0-189">Filtrerar alla neka-uppgifter som görs till det angivna Azure AD-programmet.</span><span class="sxs-lookup"><span data-stu-id="25fc0-189">Filters all deny assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="25fc0-190">-SignInName</span><span class="sxs-lookup"><span data-stu-id="25fc0-190">-SignInName</span></span>
<span data-ttu-id="25fc0-191">E-postadressen eller användarens huvud namn för användaren.</span><span class="sxs-lookup"><span data-stu-id="25fc0-191">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="25fc0-192">Filtrerar alla neka-uppgifter som görs till angiven användare.</span><span class="sxs-lookup"><span data-stu-id="25fc0-192">Filters all deny assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="25fc0-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25fc0-193">CommonParameters</span></span>
<span data-ttu-id="25fc0-194">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25fc0-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25fc0-195">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25fc0-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25fc0-196">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25fc0-196">INPUTS</span></span>

### <span data-ttu-id="25fc0-197">System. GUID</span><span class="sxs-lookup"><span data-stu-id="25fc0-197">System.Guid</span></span>

### <span data-ttu-id="25fc0-198">System. String</span><span class="sxs-lookup"><span data-stu-id="25fc0-198">System.String</span></span>

## <span data-ttu-id="25fc0-199">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25fc0-199">OUTPUTS</span></span>

### <span data-ttu-id="25fc0-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="25fc0-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span></span>

## <span data-ttu-id="25fc0-201">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25fc0-201">NOTES</span></span>
<span data-ttu-id="25fc0-202">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="25fc0-202">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="25fc0-203">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25fc0-203">RELATED LINKS</span></span>
