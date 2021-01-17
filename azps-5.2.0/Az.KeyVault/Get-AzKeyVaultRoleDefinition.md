---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
ms.openlocfilehash: 6e4f58c355296a281a9ecbef21d7eca754bf41c0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388419"
---
# <span data-ttu-id="91d21-101">Get-AzKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="91d21-101">Get-AzKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="91d21-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="91d21-102">SYNOPSIS</span></span>
<span data-ttu-id="91d21-103">List roll definitioner för en viss hanterad HSM i ett angivet omfång.</span><span class="sxs-lookup"><span data-stu-id="91d21-103">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="91d21-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="91d21-104">SYNTAX</span></span>

### <span data-ttu-id="91d21-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="91d21-105">Interactive (Default)</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91d21-106">ByName</span><span class="sxs-lookup"><span data-stu-id="91d21-106">ByName</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91d21-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="91d21-107">DESCRIPTION</span></span>
<span data-ttu-id="91d21-108">List roll definitioner för en viss hanterad HSM i ett angivet omfång.</span><span class="sxs-lookup"><span data-stu-id="91d21-108">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="91d21-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="91d21-109">EXAMPLES</span></span>

### <span data-ttu-id="91d21-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="91d21-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleDefinition -HsmName myHsm -Scope "/keys"

RoleName                              Description Permissions
--------                              ----------- -----------
Managed HSM Administrator                         1 permission(s)
Managed HSM Crypto Officer                        1 permission(s)
Managed HSM Crypto User                           1 permission(s)
Managed HSM Policy Administrator                  1 permission(s)
Managed HSM Crypto Auditor                        1 permission(s)
Managed HSM Crypto Service Encryption             1 permission(s)
Managed HSM Backup                                1 permission(s)
```

<span data-ttu-id="91d21-111">I exemplet visas alla roller i "/Keys"-området.</span><span class="sxs-lookup"><span data-stu-id="91d21-111">The example lists all the roles at "/keys" scope.</span></span>

### <span data-ttu-id="91d21-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="91d21-112">Example 2</span></span>
```powershell
PS C:\> $backupRole = Get-AzKeyVaultRoleDefinition -HsmName myHsm -RoleDefinitionName "managed hsm backup"

PS C:\> $backupRole.Permissions

AllowedActions DeniedActions AllowedDataActions DeniedDataActions
-------------- ------------- ------------------ -----------------
0 action(s)    0 action(s)   3 action(s)        0 action(s)

PS C:\> $backupRole.Permissions.AllowedDataActions

Microsoft.KeyVault/managedHsm/backup/start/action
Microsoft.KeyVault/managedHsm/backup/status/action
Microsoft.KeyVault/managedHsm/keys/backup/action

RoleName                              Description Permissions
--------                              ----------- -----------
Managed HSM Administrator                         1 permission(s)
Managed HSM Crypto Officer                        1 permission(s)
Managed HSM Crypto User                           1 permission(s)
Managed HSM Policy Administrator                  1 permission(s)
Managed HSM Crypto Auditor                        1 permission(s)
Managed HSM Crypto Service Encryption             1 permission(s)
Managed HSM Backup                                1 permission(s)
```

<span data-ttu-id="91d21-113">Exemplet får rollen "hanterad HSM-säkerhetskopiering" och kontrollerar dess behörigheter.</span><span class="sxs-lookup"><span data-stu-id="91d21-113">The example gets the "Managed HSM Backup" role and inspects its permissions.</span></span>

## <span data-ttu-id="91d21-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="91d21-114">PARAMETERS</span></span>

### <span data-ttu-id="91d21-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91d21-115">-DefaultProfile</span></span>
<span data-ttu-id="91d21-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="91d21-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91d21-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="91d21-117">-HsmName</span></span>
<span data-ttu-id="91d21-118">Namn på HSM.</span><span class="sxs-lookup"><span data-stu-id="91d21-118">Name of the HSM.</span></span>

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

### <span data-ttu-id="91d21-119">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="91d21-119">-RoleDefinitionName</span></span>
<span data-ttu-id="91d21-120">Namn på den roll definition som ska visas.</span><span class="sxs-lookup"><span data-stu-id="91d21-120">Name of the role definition to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: RoleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91d21-121">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="91d21-121">-Scope</span></span>
<span data-ttu-id="91d21-122">Omfattning som roll tilldelningen eller definitionen gäller för, till exempel., "/" eller "/Keys" eller "/keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="91d21-122">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="91d21-123">'/' används när det utelämnas.</span><span class="sxs-lookup"><span data-stu-id="91d21-123">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="91d21-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91d21-124">CommonParameters</span></span>
<span data-ttu-id="91d21-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91d21-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91d21-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91d21-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91d21-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="91d21-127">INPUTS</span></span>

### <span data-ttu-id="91d21-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="91d21-128">None</span></span>

## <span data-ttu-id="91d21-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="91d21-129">OUTPUTS</span></span>

### <span data-ttu-id="91d21-130">Microsoft. Azure. commands. valv. Models. PSKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="91d21-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="91d21-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="91d21-131">NOTES</span></span>

## <span data-ttu-id="91d21-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="91d21-132">RELATED LINKS</span></span>
