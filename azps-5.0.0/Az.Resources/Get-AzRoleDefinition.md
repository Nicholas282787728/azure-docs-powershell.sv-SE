---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: 5cd9a76f71f63b1d16003cce467d2d91eddc5b04
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322907"
---
# <span data-ttu-id="f4bef-101">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f4bef-101">Get-AzRoleDefinition</span></span>

## <span data-ttu-id="f4bef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f4bef-102">SYNOPSIS</span></span>
<span data-ttu-id="f4bef-103">Visar alla Azure RBAC-roller som är tillgängliga för tilldelning.</span><span class="sxs-lookup"><span data-stu-id="f4bef-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

## <span data-ttu-id="f4bef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f4bef-104">SYNTAX</span></span>

### <span data-ttu-id="f4bef-105">RoleDefinitionNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f4bef-105">RoleDefinitionNameParameterSet (Default)</span></span>
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4bef-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4bef-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4bef-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4bef-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4bef-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f4bef-108">DESCRIPTION</span></span>
<span data-ttu-id="f4bef-109">Använd kommandot Get-AzRoleDefinition med ett visst rollnamn för att visa dess uppgifter.</span><span class="sxs-lookup"><span data-stu-id="f4bef-109">Use the Get-AzRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="f4bef-110">Om du vill kontrol lera enskilda operationer som en roll ger åtkomst till granskar du åtgärderna och NotActions egenskaper för rollen.</span><span class="sxs-lookup"><span data-stu-id="f4bef-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="f4bef-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f4bef-111">EXAMPLES</span></span>

### <span data-ttu-id="f4bef-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f4bef-112">Example 1</span></span>
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

<span data-ttu-id="f4bef-113">Hämta roll definitionen för läsaren</span><span class="sxs-lookup"><span data-stu-id="f4bef-113">Get the Reader role definition</span></span>

### <span data-ttu-id="f4bef-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f4bef-114">Example 2</span></span>
```
PS C:\> Get-AzRoleDefinition
```

<span data-ttu-id="f4bef-115">Visar alla definitioner för en RBAC-roll</span><span class="sxs-lookup"><span data-stu-id="f4bef-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="f4bef-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f4bef-116">PARAMETERS</span></span>

### <span data-ttu-id="f4bef-117">-Anpassad</span><span class="sxs-lookup"><span data-stu-id="f4bef-117">-Custom</span></span>
<span data-ttu-id="f4bef-118">Om det här alternativet anges visas bara de anpassade roller som skapats i katalogen.</span><span class="sxs-lookup"><span data-stu-id="f4bef-118">If specified, only displays the custom created roles in the directory.</span></span>

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

### <span data-ttu-id="f4bef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4bef-119">-DefaultProfile</span></span>
<span data-ttu-id="f4bef-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f4bef-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4bef-121">-ID</span><span class="sxs-lookup"><span data-stu-id="f4bef-121">-Id</span></span>
<span data-ttu-id="f4bef-122">Rollcenter-ID.</span><span class="sxs-lookup"><span data-stu-id="f4bef-122">Role definition Id.</span></span>

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

### <span data-ttu-id="f4bef-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="f4bef-123">-Name</span></span>
<span data-ttu-id="f4bef-124">Namn på rollnamn.</span><span class="sxs-lookup"><span data-stu-id="f4bef-124">Role definition name.</span></span>
<span data-ttu-id="f4bef-125">Till exempel: läsare, deltagare och virtuell dator deltagare.</span><span class="sxs-lookup"><span data-stu-id="f4bef-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

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

### <span data-ttu-id="f4bef-126">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="f4bef-126">-Scope</span></span>
<span data-ttu-id="f4bef-127">Definitions omfång för roll.</span><span class="sxs-lookup"><span data-stu-id="f4bef-127">Role definition scope.</span></span>

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

### <span data-ttu-id="f4bef-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4bef-128">CommonParameters</span></span>
<span data-ttu-id="f4bef-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4bef-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4bef-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4bef-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4bef-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f4bef-131">INPUTS</span></span>

### <span data-ttu-id="f4bef-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f4bef-132">System.String</span></span>

### <span data-ttu-id="f4bef-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f4bef-133">System.Guid</span></span>

### <span data-ttu-id="f4bef-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f4bef-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f4bef-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f4bef-135">OUTPUTS</span></span>

### <span data-ttu-id="f4bef-136">Microsoft. Azure. kommandon. sources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f4bef-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="f4bef-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f4bef-137">NOTES</span></span>
<span data-ttu-id="f4bef-138">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="f4bef-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="f4bef-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f4bef-139">RELATED LINKS</span></span>

[<span data-ttu-id="f4bef-140">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f4bef-140">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="f4bef-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f4bef-141">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="f4bef-142">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f4bef-142">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="f4bef-143">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f4bef-143">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

