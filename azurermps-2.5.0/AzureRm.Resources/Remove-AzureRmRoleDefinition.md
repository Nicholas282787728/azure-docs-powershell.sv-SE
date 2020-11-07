---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroledefinition
schema: 2.0.0
ms.openlocfilehash: 90b7b0b1d7909210d86ec1d5ac6b465f6e9fb239
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930466"
---
# <span data-ttu-id="34e6a-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="34e6a-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="34e6a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="34e6a-102">SYNOPSIS</span></span>
<span data-ttu-id="34e6a-103">Tar bort en anpassad roll i Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="34e6a-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="34e6a-104">Rollen som ska tas bort anges med egenskapen ID för rollen.</span><span class="sxs-lookup"><span data-stu-id="34e6a-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="34e6a-105">Borttagningen Miss lyckas om det finns befintliga roll tilldelningar för den anpassade rollen.</span><span class="sxs-lookup"><span data-stu-id="34e6a-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34e6a-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="34e6a-106">SYNTAX</span></span>

### <span data-ttu-id="34e6a-107">RoleDefinitionIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="34e6a-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34e6a-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="34e6a-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34e6a-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34e6a-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34e6a-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="34e6a-110">DESCRIPTION</span></span>
<span data-ttu-id="34e6a-111">Remove-AzureRmRoleDefinition cmdlet tar bort en anpassad roll i Azure Role-Based Access-kontroll.</span><span class="sxs-lookup"><span data-stu-id="34e6a-111">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="34e6a-112">Ange ID-parametern för en befintlig anpassad roll för att ta bort den anpassade rollen.</span><span class="sxs-lookup"><span data-stu-id="34e6a-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="34e6a-113">Remove-AzureRmRoleDefinition uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="34e6a-113">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="34e6a-114">Om du inte vill att frågan ska visas använder du parametern Force.</span><span class="sxs-lookup"><span data-stu-id="34e6a-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="34e6a-115">Om det finns befintliga roll tilldelningar för den anpassade rollen som ska tas bort Miss lyckas borttagningen.</span><span class="sxs-lookup"><span data-stu-id="34e6a-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="34e6a-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="34e6a-116">EXAMPLES</span></span>

### <span data-ttu-id="34e6a-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="34e6a-117">Example 1</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="34e6a-118">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="34e6a-118">Example 2</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="34e6a-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="34e6a-119">PARAMETERS</span></span>

### <span data-ttu-id="34e6a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34e6a-120">-DefaultProfile</span></span>
<span data-ttu-id="34e6a-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="34e6a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34e6a-122">-Force</span><span class="sxs-lookup"><span data-stu-id="34e6a-122">-Force</span></span>
<span data-ttu-id="34e6a-123">Om det här alternativet anges behöver du inte bekräfta en bekräftelse innan den anpassade rollen tas bort</span><span class="sxs-lookup"><span data-stu-id="34e6a-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="34e6a-124">-ID</span><span class="sxs-lookup"><span data-stu-id="34e6a-124">-Id</span></span>
<span data-ttu-id="34e6a-125">ID för den roll definition som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="34e6a-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="34e6a-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34e6a-126">-InputObject</span></span>
<span data-ttu-id="34e6a-127">Objektet som representerar den roll definition som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="34e6a-127">The object representing the role definition to be removed.</span></span>

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

### <span data-ttu-id="34e6a-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="34e6a-128">-Name</span></span>
<span data-ttu-id="34e6a-129">Namn på den roll definition som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="34e6a-129">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="34e6a-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34e6a-130">-PassThru</span></span>
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

### <span data-ttu-id="34e6a-131">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="34e6a-131">-Scope</span></span>
<span data-ttu-id="34e6a-132">Definitions omfång för roll.</span><span class="sxs-lookup"><span data-stu-id="34e6a-132">Role definition scope.</span></span>

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

### <span data-ttu-id="34e6a-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="34e6a-133">-Confirm</span></span>
<span data-ttu-id="34e6a-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="34e6a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34e6a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34e6a-135">-WhatIf</span></span>
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

### <span data-ttu-id="34e6a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34e6a-136">CommonParameters</span></span>
<span data-ttu-id="34e6a-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34e6a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34e6a-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34e6a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34e6a-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="34e6a-139">INPUTS</span></span>

### <span data-ttu-id="34e6a-140">System. GUID</span><span class="sxs-lookup"><span data-stu-id="34e6a-140">System.Guid</span></span>

### <span data-ttu-id="34e6a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="34e6a-141">System.String</span></span>

### <span data-ttu-id="34e6a-142">Microsoft. Azure. kommandon. sources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="34e6a-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="34e6a-143">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="34e6a-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="34e6a-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="34e6a-144">OUTPUTS</span></span>

### <span data-ttu-id="34e6a-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="34e6a-145">System.Boolean</span></span>

## <span data-ttu-id="34e6a-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="34e6a-146">NOTES</span></span>
<span data-ttu-id="34e6a-147">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="34e6a-147">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="34e6a-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="34e6a-148">RELATED LINKS</span></span>

[<span data-ttu-id="34e6a-149">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="34e6a-149">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="34e6a-150">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="34e6a-150">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="34e6a-151">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="34e6a-151">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

