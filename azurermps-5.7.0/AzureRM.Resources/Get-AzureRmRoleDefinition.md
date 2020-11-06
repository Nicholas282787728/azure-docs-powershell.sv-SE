---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
ms.openlocfilehash: c1850cdc410df064a97950bb38f3734657649467
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581987"
---
# <span data-ttu-id="b29ef-101">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b29ef-101">Get-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="b29ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b29ef-102">SYNOPSIS</span></span>
<span data-ttu-id="b29ef-103">Visar alla Azure RBAC-roller som är tillgängliga för tilldelning.</span><span class="sxs-lookup"><span data-stu-id="b29ef-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b29ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b29ef-104">SYNTAX</span></span>

### <span data-ttu-id="b29ef-105">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b29ef-105">RoleDefinitionNameParameterSet</span></span>
```
Get-AzureRmRoleDefinition [[-Name] <String>] [-Scope <String>] [-AtScopeAndBelow]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b29ef-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b29ef-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b29ef-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="b29ef-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzureRmRoleDefinition [-Scope <String>] [-Custom] [-AtScopeAndBelow]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b29ef-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b29ef-108">DESCRIPTION</span></span>
<span data-ttu-id="b29ef-109">Använd kommandot Get-AzureRmRoleDefinition med ett visst rollnamn för att visa dess uppgifter.</span><span class="sxs-lookup"><span data-stu-id="b29ef-109">Use the Get-AzureRmRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="b29ef-110">Om du vill kontrol lera enskilda operationer som en roll ger åtkomst till granskar du åtgärderna och NotActions egenskaper för rollen.</span><span class="sxs-lookup"><span data-stu-id="b29ef-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="b29ef-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b29ef-111">EXAMPLES</span></span>

### <span data-ttu-id="b29ef-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b29ef-112">Example 1</span></span>
```
PS C:\> Get-AzureRmRoleDefinition -Name Reader
```

<span data-ttu-id="b29ef-113">Hämta roll definitionen för läsaren</span><span class="sxs-lookup"><span data-stu-id="b29ef-113">Get the Reader role definition</span></span>

### <span data-ttu-id="b29ef-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b29ef-114">Example 2</span></span>
```
PS C:\> Get-AzureRmRoleDefinition
```

<span data-ttu-id="b29ef-115">Visar alla definitioner för en RBAC-roll</span><span class="sxs-lookup"><span data-stu-id="b29ef-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="b29ef-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b29ef-116">PARAMETERS</span></span>

### <span data-ttu-id="b29ef-117">-AtScopeAndBelow</span><span class="sxs-lookup"><span data-stu-id="b29ef-117">-AtScopeAndBelow</span></span>
<span data-ttu-id="b29ef-118">Visar alla roll definitioner.</span><span class="sxs-lookup"><span data-stu-id="b29ef-118">If specified, displays all role definitions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RoleDefinitionNameParameterSet, RoleDefinitionCustomParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b29ef-119">-Anpassad</span><span class="sxs-lookup"><span data-stu-id="b29ef-119">-Custom</span></span>
<span data-ttu-id="b29ef-120">Om det här alternativet anges visas bara de anpassade roller som skapats i katalogen.</span><span class="sxs-lookup"><span data-stu-id="b29ef-120">If specified, only displays the custom created roles in the directory.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RoleDefinitionCustomParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b29ef-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b29ef-121">-DefaultProfile</span></span>
<span data-ttu-id="b29ef-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b29ef-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b29ef-123">-ID</span><span class="sxs-lookup"><span data-stu-id="b29ef-123">-Id</span></span>
<span data-ttu-id="b29ef-124">Rollcenter-ID.</span><span class="sxs-lookup"><span data-stu-id="b29ef-124">Role definition Id.</span></span>

```yaml
Type: Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b29ef-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="b29ef-125">-Name</span></span>
<span data-ttu-id="b29ef-126">Namn på rollnamn.</span><span class="sxs-lookup"><span data-stu-id="b29ef-126">Role definition name.</span></span>
<span data-ttu-id="b29ef-127">Till exempel: läsare, deltagare och virtuell dator deltagare.</span><span class="sxs-lookup"><span data-stu-id="b29ef-127">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

```yaml
Type: String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b29ef-128">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="b29ef-128">-Scope</span></span>
<span data-ttu-id="b29ef-129">Definitions omfång för roll.</span><span class="sxs-lookup"><span data-stu-id="b29ef-129">Role definition scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b29ef-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b29ef-130">CommonParameters</span></span>
<span data-ttu-id="b29ef-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b29ef-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b29ef-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b29ef-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b29ef-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b29ef-133">INPUTS</span></span>

### <span data-ttu-id="b29ef-134">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="b29ef-134">String</span></span>
<span data-ttu-id="b29ef-135">Parametern ' scope ' godkänner värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="b29ef-135">Parameter 'Scope' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="b29ef-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b29ef-136">OUTPUTS</span></span>

### <span data-ttu-id="b29ef-137">System. Collections. Generic. list ' 1 [Microsoft. Azure. kommandon. Resources. Authorization. PSRoleDefinition]</span><span class="sxs-lookup"><span data-stu-id="b29ef-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition]</span></span>

## <span data-ttu-id="b29ef-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b29ef-138">NOTES</span></span>
<span data-ttu-id="b29ef-139">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="b29ef-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b29ef-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b29ef-140">RELATED LINKS</span></span>

[<span data-ttu-id="b29ef-141">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b29ef-141">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="b29ef-142">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b29ef-142">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="b29ef-143">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b29ef-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="b29ef-144">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b29ef-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

