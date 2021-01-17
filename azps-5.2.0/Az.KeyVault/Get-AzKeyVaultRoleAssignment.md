---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: c610339bf90069f30d6107d46fc92fd896d6816c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388413"
---
# <span data-ttu-id="0934f-101">Get-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0934f-101">Get-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="0934f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0934f-102">SYNOPSIS</span></span>
<span data-ttu-id="0934f-103">Hämta eller lista roll tilldelningar för en hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="0934f-103">Get or list role assignments of a managed HSM.</span></span> <span data-ttu-id="0934f-104">Använd respektive parametrar för att lista tilldelningar till en viss användare eller en roll definition.</span><span class="sxs-lookup"><span data-stu-id="0934f-104">Use respective parameters to list assignments to a specific user or a role definition.</span></span>

## <span data-ttu-id="0934f-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0934f-105">SYNTAX</span></span>

### <span data-ttu-id="0934f-106">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="0934f-106">List (Default)</span></span>
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-RoleDefinitionName <String>]
 [-RoleDefinitionId <String>] [-ObjectId <String>] [-SignInName <String>] [-ApplicationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0934f-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="0934f-107">GetByName</span></span>
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0934f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0934f-108">DESCRIPTION</span></span>
<span data-ttu-id="0934f-109">Använd `Get-AzKeyVaultRoleAssignment` kommandot för att visa en lista över alla roll tilldelningar som är effektiva för ett scope.</span><span class="sxs-lookup"><span data-stu-id="0934f-109">Use the `Get-AzKeyVaultRoleAssignment` command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="0934f-110">Utan parametrar returnerar detta kommando alla roll tilldelningar som har gjorts under den hanterade HSM.</span><span class="sxs-lookup"><span data-stu-id="0934f-110">Without any parameters, this command returns all the role assignments made under the managed HSM.</span></span>
<span data-ttu-id="0934f-111">Den här listan kan filtreras med hjälp av filtrerings parametrar för huvud-, roll-och omfattning.</span><span class="sxs-lookup"><span data-stu-id="0934f-111">This list can be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="0934f-112">Uppgiftens ämne måste anges.</span><span class="sxs-lookup"><span data-stu-id="0934f-112">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="0934f-113">Ange en användare med hjälp av SignInName eller Azure AD ObjectId-parametrar.</span><span class="sxs-lookup"><span data-stu-id="0934f-113">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="0934f-114">Om du vill ange en säkerhets grupp använder du Azure AD ObjectId-parameter.</span><span class="sxs-lookup"><span data-stu-id="0934f-114">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="0934f-115">Om du vill ange ett Azure AD-program använder du ApplicationId-eller ObjectId-parametrar.</span><span class="sxs-lookup"><span data-stu-id="0934f-115">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="0934f-116">Rollen som tilldelas måste anges med parametern RoleDefinitionName eller RoleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="0934f-116">The role that is being assigned must be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>
<span data-ttu-id="0934f-117">Omfattningen där åtkomst ges kan anges.</span><span class="sxs-lookup"><span data-stu-id="0934f-117">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="0934f-118">Den är som standard "/".</span><span class="sxs-lookup"><span data-stu-id="0934f-118">It defaults to "/".</span></span>

## <span data-ttu-id="0934f-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0934f-119">EXAMPLES</span></span>

### <span data-ttu-id="0934f-120">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0934f-120">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Administrator  User 1 (user1@microsoft.com)     User       /
Managed HSM Crypto Auditor User 2 (user2@microsoft.com)     User       /keys
Managed HSM Backup         User 2 (user2@microsoft.com)     User       /
Managed HSM Administrator  User 2 (user2@microsoft.com)     User       /
```

<span data-ttu-id="0934f-121">I det här exemplet visas alla roll tilldelningar för "myHsm" i alla omfattningar.</span><span class="sxs-lookup"><span data-stu-id="0934f-121">This example lists all role assignments of "myHsm" on all the scope.</span></span>

### <span data-ttu-id="0934f-122">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0934f-122">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com -Scope "/keys"

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Crypto Auditor User 1 (user1@microsoft.com)     User       /keys
Managed HSM Backup         User 1 (user1@microsoft.com)     User       /keys
```

<span data-ttu-id="0934f-123">I det här exemplet listas alla roll tilldelningar för "myHsm" i omfattningen "/Keys" och filtrerar resultatet efter användarens inloggnings namn.</span><span class="sxs-lookup"><span data-stu-id="0934f-123">This example lists all role assignments of "myHsm" on "/keys" scope and filters the result by user sign-in name.</span></span>

## <span data-ttu-id="0934f-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0934f-124">PARAMETERS</span></span>

### <span data-ttu-id="0934f-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="0934f-125">-ApplicationId</span></span>
<span data-ttu-id="0934f-126">App-SPN.</span><span class="sxs-lookup"><span data-stu-id="0934f-126">The app SPN.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: SPN, ServicePrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0934f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0934f-127">-DefaultProfile</span></span>
<span data-ttu-id="0934f-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0934f-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0934f-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="0934f-129">-HsmName</span></span>
<span data-ttu-id="0934f-130">Namn på HSM.</span><span class="sxs-lookup"><span data-stu-id="0934f-130">Name of the HSM.</span></span>

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

### <span data-ttu-id="0934f-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0934f-131">-ObjectId</span></span>
<span data-ttu-id="0934f-132">Objekt-ID för användare eller grupp.</span><span class="sxs-lookup"><span data-stu-id="0934f-132">The user or group object id.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0934f-133">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="0934f-133">-RoleAssignmentName</span></span>
<span data-ttu-id="0934f-134">Namn på roll tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="0934f-134">Name of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0934f-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="0934f-135">-RoleDefinitionId</span></span>
<span data-ttu-id="0934f-136">Roll-ID huvudobjektet har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="0934f-136">Role Id the principal is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0934f-137">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="0934f-137">-RoleDefinitionName</span></span>
<span data-ttu-id="0934f-138">Namnet på den RBAC-roll som du vill tilldela huvud delen med.</span><span class="sxs-lookup"><span data-stu-id="0934f-138">Name of the RBAC role to assign the principal with.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0934f-139">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="0934f-139">-Scope</span></span>
<span data-ttu-id="0934f-140">Omfattning som roll tilldelningen eller definitionen gäller för, till exempel., "/" eller "/Keys" eller "/keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="0934f-140">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="0934f-141">'/' används när det utelämnas.</span><span class="sxs-lookup"><span data-stu-id="0934f-141">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="0934f-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="0934f-142">-SignInName</span></span>
<span data-ttu-id="0934f-143">Användaren SignInName.</span><span class="sxs-lookup"><span data-stu-id="0934f-143">The user SignInName.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: Email, UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0934f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0934f-144">CommonParameters</span></span>
<span data-ttu-id="0934f-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0934f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0934f-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0934f-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0934f-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0934f-147">INPUTS</span></span>

### <span data-ttu-id="0934f-148">Ingen</span><span class="sxs-lookup"><span data-stu-id="0934f-148">None</span></span>

## <span data-ttu-id="0934f-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0934f-149">OUTPUTS</span></span>

### <span data-ttu-id="0934f-150">Microsoft. Azure. commands. valv. Models. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0934f-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="0934f-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0934f-151">NOTES</span></span>

## <span data-ttu-id="0934f-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0934f-152">RELATED LINKS</span></span>
