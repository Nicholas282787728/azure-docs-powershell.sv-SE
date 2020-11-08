---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsmroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmRoleAssignment.md
ms.openlocfilehash: 038049af40d84b678da12a57918328b3b0725127
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263014"
---
# <span data-ttu-id="6205f-101">Remove-AzManagedHsmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6205f-101">Remove-AzManagedHsmRoleAssignment</span></span>

## <span data-ttu-id="6205f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6205f-102">SYNOPSIS</span></span>
<span data-ttu-id="6205f-103">Tar bort en roll tilldelning till det angivna huvud kontot som har tilldelats en viss roll i ett visst område.</span><span class="sxs-lookup"><span data-stu-id="6205f-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="6205f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6205f-104">SYNTAX</span></span>

### <span data-ttu-id="6205f-105">DefinitionNameSignInName (standard)</span><span class="sxs-lookup"><span data-stu-id="6205f-105">DefinitionNameSignInName (Default)</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6205f-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="6205f-106">DefinitionNameApplicationId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6205f-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="6205f-107">DefinitionNameObjectId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6205f-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="6205f-108">DefinitionIdApplicationId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6205f-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="6205f-109">DefinitionIdObjectId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6205f-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="6205f-110">DefinitionIdSignInName</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6205f-111">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6205f-111">RemoveByNameParameterSet</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] [-PassThru]
 -RoleAssignmentName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6205f-112">InputObject</span><span class="sxs-lookup"><span data-stu-id="6205f-112">InputObject</span></span>
```
Remove-AzManagedHsmRoleAssignment [-Scope <String>] [-PassThru] -InputObject <PSKeyVaultRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6205f-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6205f-113">DESCRIPTION</span></span>
<span data-ttu-id="6205f-114">Använd `Remove-AzManagedHsmRoleAssignment` cmdleten för att återkalla åtkomsten till ett objekt i ett givet scope och en given roll.</span><span class="sxs-lookup"><span data-stu-id="6205f-114">Use the `Remove-AzManagedHsmRoleAssignment` cmdlet to revoke access to any principal at given scope and given role.</span></span> <span data-ttu-id="6205f-115">Uppgiftens objekt, t. ex.</span><span class="sxs-lookup"><span data-stu-id="6205f-115">The object of the assignment i.e. the principal MUST be specified.</span></span> <span data-ttu-id="6205f-116">Huvudobjektet kan vara en användare (Använd SignInName-eller ObjectId-parametrar för att identifiera en användare), säkerhets grupp (Använd parametern ObjectId för att identifiera en grupp) eller tjänstens huvud namn (Använd ApplicationId-eller ObjectId-parametrar för att identifiera en ServicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="6205f-116">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ApplicationId or ObjectId parameters to identify a ServicePrincipal.</span></span> <span data-ttu-id="6205f-117">Rollen som huvudobjektet är tilldelad måste anges med parametern RoleDefinitionName eller RoleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="6205f-117">The role that the principal is assigned to MUST be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>

## <span data-ttu-id="6205f-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6205f-118">EXAMPLES</span></span>

### <span data-ttu-id="6205f-119">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6205f-119">Example 1</span></span>
```powershell
PS C:\> Remove-AzManagedHsmRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com -Scope "/keys"
```

<span data-ttu-id="6205f-120">I det här exemplet återkallas rollen hanterad HSM-princip administratör "i user1@microsoft.com /Keys".</span><span class="sxs-lookup"><span data-stu-id="6205f-120">This example revokes "Managed HSM Policy Administrator" role of "user1@microsoft.com" at "/keys" scope.</span></span>

### <span data-ttu-id="6205f-121">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6205f-121">Example 2</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com | Remove-AzManagedHsmRoleAssignment
```

<span data-ttu-id="6205f-122">I det här exemplet dras alla roller för " user1@microsoft.com " i alla omfattningar.</span><span class="sxs-lookup"><span data-stu-id="6205f-122">This example revokes all roles of "user1@microsoft.com" at all scopes.</span></span>

## <span data-ttu-id="6205f-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6205f-123">PARAMETERS</span></span>

### <span data-ttu-id="6205f-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="6205f-124">-ApplicationId</span></span>
<span data-ttu-id="6205f-125">App-SPN.</span><span class="sxs-lookup"><span data-stu-id="6205f-125">The app SPN.</span></span>

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

### <span data-ttu-id="6205f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6205f-126">-DefaultProfile</span></span>
<span data-ttu-id="6205f-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6205f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6205f-128">-HsmName</span><span class="sxs-lookup"><span data-stu-id="6205f-128">-HsmName</span></span>
<span data-ttu-id="6205f-129">Namn på HSM.</span><span class="sxs-lookup"><span data-stu-id="6205f-129">Name of the HSM.</span></span>

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

### <span data-ttu-id="6205f-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6205f-130">-InputObject</span></span>
<span data-ttu-id="6205f-131">Roll tilldelnings objekt.</span><span class="sxs-lookup"><span data-stu-id="6205f-131">Role assignment object.</span></span>

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

### <span data-ttu-id="6205f-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6205f-132">-ObjectId</span></span>
<span data-ttu-id="6205f-133">Objekt-ID för användare eller grupp.</span><span class="sxs-lookup"><span data-stu-id="6205f-133">The user or group object id.</span></span>

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

### <span data-ttu-id="6205f-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6205f-134">-PassThru</span></span>
<span data-ttu-id="6205f-135">Returnera true när HSM återställs.</span><span class="sxs-lookup"><span data-stu-id="6205f-135">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="6205f-136">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="6205f-136">-RoleAssignmentName</span></span>
<span data-ttu-id="6205f-137">Namn på roll tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="6205f-137">Name of the role assignment.</span></span>

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

### <span data-ttu-id="6205f-138">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="6205f-138">-RoleDefinitionId</span></span>
<span data-ttu-id="6205f-139">Roll-ID huvudobjektet har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="6205f-139">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="6205f-140">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="6205f-140">-RoleDefinitionName</span></span>
<span data-ttu-id="6205f-141">Namnet på den RBAC-roll som du vill tilldela huvud delen med.</span><span class="sxs-lookup"><span data-stu-id="6205f-141">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="6205f-142">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="6205f-142">-Scope</span></span>
<span data-ttu-id="6205f-143">Omfattning som roll tilldelningen eller definitionen gäller för, till exempel., "/" eller "/Keys" eller "/keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="6205f-143">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="6205f-144">'/' används när det utelämnas.</span><span class="sxs-lookup"><span data-stu-id="6205f-144">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="6205f-145">-SignInName</span><span class="sxs-lookup"><span data-stu-id="6205f-145">-SignInName</span></span>
<span data-ttu-id="6205f-146">Användaren SignInName.</span><span class="sxs-lookup"><span data-stu-id="6205f-146">The user SignInName.</span></span>

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

### <span data-ttu-id="6205f-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6205f-147">-Confirm</span></span>
<span data-ttu-id="6205f-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6205f-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6205f-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6205f-149">-WhatIf</span></span>
<span data-ttu-id="6205f-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6205f-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6205f-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6205f-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6205f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6205f-152">CommonParameters</span></span>
<span data-ttu-id="6205f-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6205f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6205f-154">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6205f-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6205f-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6205f-155">INPUTS</span></span>

### <span data-ttu-id="6205f-156">Microsoft. Azure. commands. valv. Models. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6205f-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="6205f-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6205f-157">OUTPUTS</span></span>

### <span data-ttu-id="6205f-158">Microsoft. Azure. commands. valv. Models. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6205f-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="6205f-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6205f-159">NOTES</span></span>

## <span data-ttu-id="6205f-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6205f-160">RELATED LINKS</span></span>
