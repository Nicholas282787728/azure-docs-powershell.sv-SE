---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
ms.openlocfilehash: a2bd64daf4b9895de3ef8ca12ff0fec7295cd094
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419771"
---
# <span data-ttu-id="176b0-101">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="176b0-101">Remove-AzRoleDefinition</span></span>

## <span data-ttu-id="176b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="176b0-102">SYNOPSIS</span></span>
<span data-ttu-id="176b0-103">Tar bort en anpassad roll i Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="176b0-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="176b0-104">Rollen som ska tas bort anges med egenskapen ID för rollen.</span><span class="sxs-lookup"><span data-stu-id="176b0-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="176b0-105">Borttagningen Miss lyckas om det finns befintliga roll tilldelningar för den anpassade rollen.</span><span class="sxs-lookup"><span data-stu-id="176b0-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

## <span data-ttu-id="176b0-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="176b0-106">SYNTAX</span></span>

### <span data-ttu-id="176b0-107">RoleDefinitionIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="176b0-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="176b0-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="176b0-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="176b0-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="176b0-109">InputObjectParameterSet</span></span>
```
Remove-AzRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="176b0-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="176b0-110">DESCRIPTION</span></span>
<span data-ttu-id="176b0-111">Remove-AzRoleDefinition cmdlet tar bort en anpassad roll i Azure Role-Based Access-kontroll.</span><span class="sxs-lookup"><span data-stu-id="176b0-111">The Remove-AzRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="176b0-112">Ange ID-parametern för en befintlig anpassad roll för att ta bort den anpassade rollen.</span><span class="sxs-lookup"><span data-stu-id="176b0-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="176b0-113">Remove-AzRoleDefinition uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="176b0-113">By default, Remove-AzRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="176b0-114">Om du inte vill att frågan ska visas använder du parametern Force.</span><span class="sxs-lookup"><span data-stu-id="176b0-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="176b0-115">Om det finns befintliga roll tilldelningar för den anpassade rollen som ska tas bort Miss lyckas borttagningen.</span><span class="sxs-lookup"><span data-stu-id="176b0-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="176b0-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="176b0-116">EXAMPLES</span></span>

### <span data-ttu-id="176b0-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="176b0-117">Example 1</span></span>
```
Get-AzRoleDefinition -Name "Virtual Machine Operator" | Remove-AzRoleDefinition
```

### <span data-ttu-id="176b0-118">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="176b0-118">Example 2</span></span>
```
Remove-AzRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="176b0-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="176b0-119">PARAMETERS</span></span>

### <span data-ttu-id="176b0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="176b0-120">-DefaultProfile</span></span>
<span data-ttu-id="176b0-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="176b0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="176b0-122">-Force</span><span class="sxs-lookup"><span data-stu-id="176b0-122">-Force</span></span>
<span data-ttu-id="176b0-123">Om det här alternativet anges behöver du inte bekräfta en bekräftelse innan den anpassade rollen tas bort</span><span class="sxs-lookup"><span data-stu-id="176b0-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="176b0-124">-ID</span><span class="sxs-lookup"><span data-stu-id="176b0-124">-Id</span></span>
<span data-ttu-id="176b0-125">ID för den roll definition som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="176b0-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="176b0-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="176b0-126">-InputObject</span></span>
<span data-ttu-id="176b0-127">Objektet som representerar den roll definition som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="176b0-127">The object representing the role definition to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="176b0-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="176b0-128">-Name</span></span>
<span data-ttu-id="176b0-129">Namn på den roll definition som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="176b0-129">Name of the Role definition to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="176b0-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="176b0-130">-PassThru</span></span>
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

### <span data-ttu-id="176b0-131">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="176b0-131">-Scope</span></span>
<span data-ttu-id="176b0-132">Definitions omfång för roll.</span><span class="sxs-lookup"><span data-stu-id="176b0-132">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionIdParameterSet, RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="176b0-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="176b0-133">-Confirm</span></span>
<span data-ttu-id="176b0-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="176b0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="176b0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="176b0-135">-WhatIf</span></span>
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

### <span data-ttu-id="176b0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="176b0-136">CommonParameters</span></span>
<span data-ttu-id="176b0-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="176b0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="176b0-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="176b0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="176b0-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="176b0-139">INPUTS</span></span>

### <span data-ttu-id="176b0-140">System. GUID</span><span class="sxs-lookup"><span data-stu-id="176b0-140">System.Guid</span></span>

### <span data-ttu-id="176b0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="176b0-141">System.String</span></span>

### <span data-ttu-id="176b0-142">Microsoft. Azure. kommandon. sources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="176b0-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="176b0-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="176b0-143">OUTPUTS</span></span>

### <span data-ttu-id="176b0-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="176b0-144">System.Boolean</span></span>

## <span data-ttu-id="176b0-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="176b0-145">NOTES</span></span>
<span data-ttu-id="176b0-146">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="176b0-146">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="176b0-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="176b0-147">RELATED LINKS</span></span>

[<span data-ttu-id="176b0-148">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="176b0-148">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="176b0-149">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="176b0-149">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="176b0-150">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="176b0-150">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

