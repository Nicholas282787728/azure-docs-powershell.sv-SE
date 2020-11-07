---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
ms.openlocfilehash: 9db953cf4c02497fd3056a57ed7b71a78687411d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758312"
---
# <span data-ttu-id="c5a3a-101">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c5a3a-101">Get-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="c5a3a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c5a3a-102">SYNOPSIS</span></span>
<span data-ttu-id="c5a3a-103">Visar alla Azure RBAC-roller som är tillgängliga för tilldelning.</span><span class="sxs-lookup"><span data-stu-id="c5a3a-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5a3a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c5a3a-104">SYNTAX</span></span>

### <span data-ttu-id="c5a3a-105">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5a3a-105">RoleDefinitionNameParameterSet</span></span>
```
Get-AzureRmRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5a3a-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5a3a-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5a3a-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5a3a-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzureRmRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5a3a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c5a3a-108">DESCRIPTION</span></span>
<span data-ttu-id="c5a3a-109">Använd kommandot Get-AzureRmRoleDefinition med ett visst rollnamn för att visa dess uppgifter.</span><span class="sxs-lookup"><span data-stu-id="c5a3a-109">Use the Get-AzureRmRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="c5a3a-110">Om du vill kontrol lera enskilda operationer som en roll ger åtkomst till granskar du åtgärderna och NotActions egenskaper för rollen.</span><span class="sxs-lookup"><span data-stu-id="c5a3a-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="c5a3a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c5a3a-111">EXAMPLES</span></span>

### <span data-ttu-id="c5a3a-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c5a3a-112">Example 1</span></span>
```
PS C:\> Get-AzureRmRoleDefinition -Name Reader
```

<span data-ttu-id="c5a3a-113">Hämta roll definitionen för läsaren</span><span class="sxs-lookup"><span data-stu-id="c5a3a-113">Get the Reader role definition</span></span>

### <span data-ttu-id="c5a3a-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c5a3a-114">Example 2</span></span>
```
PS C:\> Get-AzureRmRoleDefinition
```

<span data-ttu-id="c5a3a-115">Visar alla definitioner för en RBAC-roll</span><span class="sxs-lookup"><span data-stu-id="c5a3a-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="c5a3a-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c5a3a-116">PARAMETERS</span></span>

### <span data-ttu-id="c5a3a-117">-Anpassad</span><span class="sxs-lookup"><span data-stu-id="c5a3a-117">-Custom</span></span>
<span data-ttu-id="c5a3a-118">Om det här alternativet anges visas bara de anpassade roller som skapats i katalogen.</span><span class="sxs-lookup"><span data-stu-id="c5a3a-118">If specified, only displays the custom created roles in the directory.</span></span>

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

### <span data-ttu-id="c5a3a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5a3a-119">-DefaultProfile</span></span>
<span data-ttu-id="c5a3a-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c5a3a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5a3a-121">-ID</span><span class="sxs-lookup"><span data-stu-id="c5a3a-121">-Id</span></span>
<span data-ttu-id="c5a3a-122">Rollcenter-ID.</span><span class="sxs-lookup"><span data-stu-id="c5a3a-122">Role definition Id.</span></span>

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

### <span data-ttu-id="c5a3a-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="c5a3a-123">-Name</span></span>
<span data-ttu-id="c5a3a-124">Namn på rollnamn.</span><span class="sxs-lookup"><span data-stu-id="c5a3a-124">Role definition name.</span></span>
<span data-ttu-id="c5a3a-125">Till exempel: läsare, deltagare och virtuell dator deltagare.</span><span class="sxs-lookup"><span data-stu-id="c5a3a-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

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

### <span data-ttu-id="c5a3a-126">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="c5a3a-126">-Scope</span></span>
<span data-ttu-id="c5a3a-127">Definitions omfång för roll.</span><span class="sxs-lookup"><span data-stu-id="c5a3a-127">Role definition scope.</span></span>

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

### <span data-ttu-id="c5a3a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5a3a-128">CommonParameters</span></span>
<span data-ttu-id="c5a3a-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5a3a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5a3a-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5a3a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5a3a-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c5a3a-131">INPUTS</span></span>

### <span data-ttu-id="c5a3a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c5a3a-132">System.String</span></span>
<span data-ttu-id="c5a3a-133">Parametrar: scope (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c5a3a-133">Parameters: Scope (ByValue)</span></span>

### <span data-ttu-id="c5a3a-134">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c5a3a-134">System.Guid</span></span>

### <span data-ttu-id="c5a3a-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c5a3a-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c5a3a-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c5a3a-136">OUTPUTS</span></span>

### <span data-ttu-id="c5a3a-137">Microsoft. Azure. kommandon. sources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c5a3a-137">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="c5a3a-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c5a3a-138">NOTES</span></span>
<span data-ttu-id="c5a3a-139">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="c5a3a-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="c5a3a-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c5a3a-140">RELATED LINKS</span></span>

[<span data-ttu-id="c5a3a-141">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c5a3a-141">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="c5a3a-142">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c5a3a-142">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="c5a3a-143">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c5a3a-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="c5a3a-144">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c5a3a-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

