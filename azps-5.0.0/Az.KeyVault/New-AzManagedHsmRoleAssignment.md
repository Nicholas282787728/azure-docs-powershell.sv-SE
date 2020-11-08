---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azmanagedhsmroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsmRoleAssignment.md
ms.openlocfilehash: 3b02bf3471546c9b6bc68d0ded109133341d20bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263029"
---
# <span data-ttu-id="b1616-101">New-AzManagedHsmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b1616-101">New-AzManagedHsmRoleAssignment</span></span>

## <span data-ttu-id="b1616-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b1616-102">SYNOPSIS</span></span>
<span data-ttu-id="b1616-103">Tilldelar den angivna RBAC-rollen till den angivna huvud delen, vid det angivna omfånget.</span><span class="sxs-lookup"><span data-stu-id="b1616-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="b1616-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b1616-104">SYNTAX</span></span>

### <span data-ttu-id="b1616-105">DefinitionNameSignInName (standard)</span><span class="sxs-lookup"><span data-stu-id="b1616-105">DefinitionNameSignInName (Default)</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1616-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="b1616-106">DefinitionNameApplicationId</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1616-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="b1616-107">DefinitionNameObjectId</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1616-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="b1616-108">DefinitionIdApplicationId</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1616-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="b1616-109">DefinitionIdObjectId</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1616-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="b1616-110">DefinitionIdSignInName</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1616-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b1616-111">DESCRIPTION</span></span>
<span data-ttu-id="b1616-112">Använd `New-AzManagedHsmRoleAssignment` kommandot för att ge åtkomst.</span><span class="sxs-lookup"><span data-stu-id="b1616-112">Use the `New-AzManagedHsmRoleAssignment` command to grant access.</span></span>
<span data-ttu-id="b1616-113">Åtkomst beviljas genom att den lämpliga RBAC-rollen tilldelas till dem vid rätt scope.</span><span class="sxs-lookup"><span data-stu-id="b1616-113">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="b1616-114">Uppgiftens ämne måste anges.</span><span class="sxs-lookup"><span data-stu-id="b1616-114">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="b1616-115">Ange en användare med hjälp av SignInName eller Azure AD ObjectId-parametrar.</span><span class="sxs-lookup"><span data-stu-id="b1616-115">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="b1616-116">Om du vill ange en säkerhets grupp använder du Azure AD ObjectId-parameter.</span><span class="sxs-lookup"><span data-stu-id="b1616-116">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="b1616-117">Om du vill ange ett Azure AD-program använder du ApplicationId-eller ObjectId-parametrar.</span><span class="sxs-lookup"><span data-stu-id="b1616-117">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="b1616-118">Rollen som tilldelas måste anges med RoleDefinitionName PR RoleDefinitionId-parametern.</span><span class="sxs-lookup"><span data-stu-id="b1616-118">The role that is being assigned must be specified using the RoleDefinitionName pr RoleDefinitionId parameter.</span></span> <span data-ttu-id="b1616-119">Omfattningen där åtkomst ges kan anges.</span><span class="sxs-lookup"><span data-stu-id="b1616-119">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="b1616-120">Det är standardinställningen för det valda abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b1616-120">It defaults to the selected subscription.</span></span>

## <span data-ttu-id="b1616-121">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b1616-121">EXAMPLES</span></span>

### <span data-ttu-id="b1616-122">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b1616-122">Example 1</span></span>
```powershell
PS C:\> New-AzManagedHsmRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com

RoleDefinitionName               DisplayName                    ObjectType Scope
------------------               -----------                    ---------- -----
Managed HSM Policy Administrator User 1 (user1@microsoft.com)   User       /
```

<span data-ttu-id="b1616-123">I det här exemplet tilldelas rollen "hanterad HSM-princip administratör" till användaren " user1@microsoft.com " högst upp.</span><span class="sxs-lookup"><span data-stu-id="b1616-123">This example assigns role "Managed HSM Policy Administrator" to user "user1@microsoft.com" at top scope.</span></span>

## <span data-ttu-id="b1616-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b1616-124">PARAMETERS</span></span>

### <span data-ttu-id="b1616-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b1616-125">-ApplicationId</span></span>
<span data-ttu-id="b1616-126">App-SPN.</span><span class="sxs-lookup"><span data-stu-id="b1616-126">The app SPN.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameApplicationId, DefinitionIdApplicationId
Aliases: SPN, ServicePrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1616-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1616-127">-DefaultProfile</span></span>
<span data-ttu-id="b1616-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b1616-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1616-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="b1616-129">-HsmName</span></span>
<span data-ttu-id="b1616-130">Namn på HSM.</span><span class="sxs-lookup"><span data-stu-id="b1616-130">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1616-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b1616-131">-ObjectId</span></span>
<span data-ttu-id="b1616-132">Objekt-ID för användare eller grupp.</span><span class="sxs-lookup"><span data-stu-id="b1616-132">The user or group object id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameObjectId, DefinitionIdObjectId
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1616-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="b1616-133">-RoleDefinitionId</span></span>
<span data-ttu-id="b1616-134">Roll-ID huvudobjektet har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="b1616-134">Role Id the principal is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionIdApplicationId, DefinitionIdObjectId, DefinitionIdSignInName
Aliases: RoleId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1616-135">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="b1616-135">-RoleDefinitionName</span></span>
<span data-ttu-id="b1616-136">Namnet på den RBAC-roll som du vill tilldela huvud delen med.</span><span class="sxs-lookup"><span data-stu-id="b1616-136">Name of the RBAC role to assign the principal with.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionNameApplicationId, DefinitionNameObjectId
Aliases: RoleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1616-137">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="b1616-137">-Scope</span></span>
<span data-ttu-id="b1616-138">Omfattning som roll tilldelningen eller definitionen gäller för, till exempel., "/" eller "/Keys" eller "/keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="b1616-138">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="b1616-139">'/' används när det utelämnas.</span><span class="sxs-lookup"><span data-stu-id="b1616-139">'/' is used when omitted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1616-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="b1616-140">-SignInName</span></span>
<span data-ttu-id="b1616-141">Användaren SignInName.</span><span class="sxs-lookup"><span data-stu-id="b1616-141">The user SignInName.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionIdSignInName
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1616-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b1616-142">-Confirm</span></span>
<span data-ttu-id="b1616-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b1616-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1616-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1616-144">-WhatIf</span></span>
<span data-ttu-id="b1616-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b1616-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1616-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b1616-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1616-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1616-147">CommonParameters</span></span>
<span data-ttu-id="b1616-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1616-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1616-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1616-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1616-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b1616-150">INPUTS</span></span>

### <span data-ttu-id="b1616-151">Ingen</span><span class="sxs-lookup"><span data-stu-id="b1616-151">None</span></span>

## <span data-ttu-id="b1616-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b1616-152">OUTPUTS</span></span>

### <span data-ttu-id="b1616-153">Microsoft. Azure. commands. valv. Models. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b1616-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="b1616-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b1616-154">NOTES</span></span>

## <span data-ttu-id="b1616-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b1616-155">RELATED LINKS</span></span>
