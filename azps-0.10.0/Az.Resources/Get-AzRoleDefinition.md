---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: d43ec874af02d57abedddb1b49b3cc8723af5c2e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923977"
---
# <span data-ttu-id="31c02-101">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="31c02-101">Get-AzRoleDefinition</span></span>

## <span data-ttu-id="31c02-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="31c02-102">SYNOPSIS</span></span>
<span data-ttu-id="31c02-103">Visar alla Azure RBAC-roller som är tillgängliga för tilldelning.</span><span class="sxs-lookup"><span data-stu-id="31c02-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

## <span data-ttu-id="31c02-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="31c02-104">SYNTAX</span></span>

### <span data-ttu-id="31c02-105">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="31c02-105">RoleDefinitionNameParameterSet</span></span>
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31c02-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31c02-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31c02-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="31c02-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31c02-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="31c02-108">DESCRIPTION</span></span>
<span data-ttu-id="31c02-109">Använd kommandot Get-AzRoleDefinition med ett visst rollnamn för att visa dess uppgifter.</span><span class="sxs-lookup"><span data-stu-id="31c02-109">Use the Get-AzRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="31c02-110">Om du vill kontrol lera enskilda operationer som en roll ger åtkomst till granskar du åtgärderna och NotActions egenskaper för rollen.</span><span class="sxs-lookup"><span data-stu-id="31c02-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="31c02-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="31c02-111">EXAMPLES</span></span>

### <span data-ttu-id="31c02-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="31c02-112">Example 1</span></span>
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

<span data-ttu-id="31c02-113">Hämta roll definitionen för läsaren</span><span class="sxs-lookup"><span data-stu-id="31c02-113">Get the Reader role definition</span></span>

### <span data-ttu-id="31c02-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="31c02-114">Example 2</span></span>
```
PS C:\> Get-AzRoleDefinition
```

<span data-ttu-id="31c02-115">Visar alla definitioner för en RBAC-roll</span><span class="sxs-lookup"><span data-stu-id="31c02-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="31c02-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="31c02-116">PARAMETERS</span></span>

### <span data-ttu-id="31c02-117">-Anpassad</span><span class="sxs-lookup"><span data-stu-id="31c02-117">-Custom</span></span>
<span data-ttu-id="31c02-118">Om det här alternativet anges visas bara de anpassade roller som skapats i katalogen.</span><span class="sxs-lookup"><span data-stu-id="31c02-118">If specified, only displays the custom created roles in the directory.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RoleDefinitionCustomParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c02-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31c02-119">-DefaultProfile</span></span>
<span data-ttu-id="31c02-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="31c02-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31c02-121">-ID</span><span class="sxs-lookup"><span data-stu-id="31c02-121">-Id</span></span>
<span data-ttu-id="31c02-122">Rollcenter-ID.</span><span class="sxs-lookup"><span data-stu-id="31c02-122">Role definition Id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c02-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="31c02-123">-Name</span></span>
<span data-ttu-id="31c02-124">Namn på rollnamn.</span><span class="sxs-lookup"><span data-stu-id="31c02-124">Role definition name.</span></span>
<span data-ttu-id="31c02-125">Till exempel: läsare, deltagare och virtuell dator deltagare.</span><span class="sxs-lookup"><span data-stu-id="31c02-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c02-126">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="31c02-126">-Scope</span></span>
<span data-ttu-id="31c02-127">Definitions omfång för roll.</span><span class="sxs-lookup"><span data-stu-id="31c02-127">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31c02-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31c02-128">CommonParameters</span></span>
<span data-ttu-id="31c02-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31c02-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31c02-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31c02-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31c02-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="31c02-131">INPUTS</span></span>

### <span data-ttu-id="31c02-132">System. String</span><span class="sxs-lookup"><span data-stu-id="31c02-132">System.String</span></span>
<span data-ttu-id="31c02-133">Parametrar: scope (ByValue)</span><span class="sxs-lookup"><span data-stu-id="31c02-133">Parameters: Scope (ByValue)</span></span>

### <span data-ttu-id="31c02-134">System. GUID</span><span class="sxs-lookup"><span data-stu-id="31c02-134">System.Guid</span></span>

### <span data-ttu-id="31c02-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="31c02-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="31c02-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="31c02-136">OUTPUTS</span></span>

### <span data-ttu-id="31c02-137">Microsoft. Azure. kommandon. sources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="31c02-137">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="31c02-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="31c02-138">NOTES</span></span>
<span data-ttu-id="31c02-139">Nyckelord: Azure, AZ, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="31c02-139">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="31c02-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="31c02-140">RELATED LINKS</span></span>

[<span data-ttu-id="31c02-141">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="31c02-141">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="31c02-142">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="31c02-142">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="31c02-143">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="31c02-143">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="31c02-144">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="31c02-144">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

