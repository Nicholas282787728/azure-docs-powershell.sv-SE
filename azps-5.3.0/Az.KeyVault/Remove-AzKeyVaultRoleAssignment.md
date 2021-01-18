---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: 9e2dd07ac0346cacb99bbcc2e05d47b57ac8ccd6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524106"
---
# <span data-ttu-id="db939-101">Remove-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="db939-101">Remove-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="db939-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db939-102">SYNOPSIS</span></span>
<span data-ttu-id="db939-103">Tar bort en roll tilldelning till det angivna huvud kontot som har tilldelats en viss roll i ett visst område.</span><span class="sxs-lookup"><span data-stu-id="db939-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="db939-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db939-104">SYNTAX</span></span>

### <span data-ttu-id="db939-105">DefinitionNameSignInName (standard)</span><span class="sxs-lookup"><span data-stu-id="db939-105">DefinitionNameSignInName (Default)</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db939-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="db939-106">DefinitionNameApplicationId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db939-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="db939-107">DefinitionNameObjectId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db939-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="db939-108">DefinitionIdApplicationId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db939-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="db939-109">DefinitionIdObjectId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db939-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="db939-110">DefinitionIdSignInName</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db939-111">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="db939-111">RemoveByNameParameterSet</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-PassThru] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db939-112">InputObject</span><span class="sxs-lookup"><span data-stu-id="db939-112">InputObject</span></span>
```
Remove-AzKeyVaultRoleAssignment [-Scope <String>] [-PassThru] -InputObject <PSKeyVaultRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db939-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db939-113">DESCRIPTION</span></span>
<span data-ttu-id="db939-114">Använd `Remove-AzKeyVaultRoleAssignment` cmdleten för att återkalla åtkomsten till ett objekt i ett givet scope och en given roll.</span><span class="sxs-lookup"><span data-stu-id="db939-114">Use the `Remove-AzKeyVaultRoleAssignment` cmdlet to revoke access to any principal at given scope and given role.</span></span> <span data-ttu-id="db939-115">Uppgiftens objekt, t. ex.</span><span class="sxs-lookup"><span data-stu-id="db939-115">The object of the assignment i.e. the principal MUST be specified.</span></span> <span data-ttu-id="db939-116">Huvudobjektet kan vara en användare (Använd SignInName-eller ObjectId-parametrar för att identifiera en användare), säkerhets grupp (Använd parametern ObjectId för att identifiera en grupp) eller tjänstens huvud namn (Använd ApplicationId-eller ObjectId-parametrar för att identifiera en ServicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="db939-116">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ApplicationId or ObjectId parameters to identify a ServicePrincipal.</span></span> <span data-ttu-id="db939-117">Rollen som huvudobjektet är tilldelad måste anges med parametern RoleDefinitionName eller RoleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="db939-117">The role that the principal is assigned to MUST be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>

## <span data-ttu-id="db939-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db939-118">EXAMPLES</span></span>

### <span data-ttu-id="db939-119">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="db939-119">Example 1</span></span>
```powershell
PS C:\> Remove-AzKeyVaultRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com -Scope "/keys"
```

<span data-ttu-id="db939-120">I det här exemplet återkallas rollen hanterad HSM-princip administratör "i user1@microsoft.com /Keys".</span><span class="sxs-lookup"><span data-stu-id="db939-120">This example revokes "Managed HSM Policy Administrator" role of "user1@microsoft.com" at "/keys" scope.</span></span>

### <span data-ttu-id="db939-121">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="db939-121">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com | Remove-AzKeyVaultRoleAssignment
```

<span data-ttu-id="db939-122">I det här exemplet dras alla roller för " user1@microsoft.com " i alla omfattningar.</span><span class="sxs-lookup"><span data-stu-id="db939-122">This example revokes all roles of "user1@microsoft.com" at all scopes.</span></span>

## <span data-ttu-id="db939-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db939-123">PARAMETERS</span></span>

### <span data-ttu-id="db939-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="db939-124">-ApplicationId</span></span>
<span data-ttu-id="db939-125">App-SPN.</span><span class="sxs-lookup"><span data-stu-id="db939-125">The app SPN.</span></span>

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

### <span data-ttu-id="db939-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db939-126">-DefaultProfile</span></span>
<span data-ttu-id="db939-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="db939-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db939-128">-HsmName</span><span class="sxs-lookup"><span data-stu-id="db939-128">-HsmName</span></span>
<span data-ttu-id="db939-129">Namn på HSM.</span><span class="sxs-lookup"><span data-stu-id="db939-129">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionNameApplicationId, DefinitionNameObjectId, DefinitionIdApplicationId, DefinitionIdObjectId, DefinitionIdSignInName, RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db939-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db939-130">-InputObject</span></span>
<span data-ttu-id="db939-131">Roll tilldelnings objekt.</span><span class="sxs-lookup"><span data-stu-id="db939-131">Role assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db939-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="db939-132">-ObjectId</span></span>
<span data-ttu-id="db939-133">Objekt-ID för användare eller grupp.</span><span class="sxs-lookup"><span data-stu-id="db939-133">The user or group object id.</span></span>

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

### <span data-ttu-id="db939-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db939-134">-PassThru</span></span>
<span data-ttu-id="db939-135">Returnera true när HSM återställs.</span><span class="sxs-lookup"><span data-stu-id="db939-135">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="db939-136">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="db939-136">-RoleAssignmentName</span></span>
<span data-ttu-id="db939-137">Namn på roll tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="db939-137">Name of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db939-138">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="db939-138">-RoleDefinitionId</span></span>
<span data-ttu-id="db939-139">Roll-ID huvudobjektet har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="db939-139">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="db939-140">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="db939-140">-RoleDefinitionName</span></span>
<span data-ttu-id="db939-141">Namnet på den RBAC-roll som du vill tilldela huvud delen med.</span><span class="sxs-lookup"><span data-stu-id="db939-141">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="db939-142">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="db939-142">-Scope</span></span>
<span data-ttu-id="db939-143">Omfattning som roll tilldelningen eller definitionen gäller för, till exempel., "/" eller "/Keys" eller "/keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="db939-143">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="db939-144">'/' används när det utelämnas.</span><span class="sxs-lookup"><span data-stu-id="db939-144">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="db939-145">-SignInName</span><span class="sxs-lookup"><span data-stu-id="db939-145">-SignInName</span></span>
<span data-ttu-id="db939-146">Användaren SignInName.</span><span class="sxs-lookup"><span data-stu-id="db939-146">The user SignInName.</span></span>

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

### <span data-ttu-id="db939-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="db939-147">-Confirm</span></span>
<span data-ttu-id="db939-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="db939-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db939-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db939-149">-WhatIf</span></span>
<span data-ttu-id="db939-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="db939-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db939-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="db939-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db939-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db939-152">CommonParameters</span></span>
<span data-ttu-id="db939-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db939-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db939-154">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db939-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db939-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db939-155">INPUTS</span></span>

### <span data-ttu-id="db939-156">Microsoft. Azure. commands. valv. Models. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="db939-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="db939-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db939-157">OUTPUTS</span></span>

### <span data-ttu-id="db939-158">Microsoft. Azure. commands. valv. Models. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="db939-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="db939-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db939-159">NOTES</span></span>

## <span data-ttu-id="db939-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db939-160">RELATED LINKS</span></span>
