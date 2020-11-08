---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzRoleDefinition.md
ms.openlocfilehash: f31a09f0d148d25796e157eb300a6f5918dade44
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923805"
---
# <span data-ttu-id="b8a0e-101">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b8a0e-101">Remove-AzRoleDefinition</span></span>

## <span data-ttu-id="b8a0e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8a0e-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a0e-103">Tar bort en anpassad roll i Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="b8a0e-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="b8a0e-104">Rollen som ska tas bort anges med egenskapen ID för rollen.</span><span class="sxs-lookup"><span data-stu-id="b8a0e-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="b8a0e-105">Borttagningen Miss lyckas om det finns befintliga roll tilldelningar för den anpassade rollen.</span><span class="sxs-lookup"><span data-stu-id="b8a0e-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

## <span data-ttu-id="b8a0e-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8a0e-106">SYNTAX</span></span>

### <span data-ttu-id="b8a0e-107">RoleDefinitionIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b8a0e-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8a0e-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8a0e-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8a0e-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8a0e-109">InputObjectParameterSet</span></span>
```
Remove-AzRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8a0e-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8a0e-110">DESCRIPTION</span></span>
<span data-ttu-id="b8a0e-111">Remove-AzRoleDefinition cmdlet tar bort en anpassad roll i Azure Role-Based Access-kontroll.</span><span class="sxs-lookup"><span data-stu-id="b8a0e-111">The Remove-AzRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="b8a0e-112">Ange ID-parametern för en befintlig anpassad roll för att ta bort den anpassade rollen.</span><span class="sxs-lookup"><span data-stu-id="b8a0e-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="b8a0e-113">Remove-AzRoleDefinition uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="b8a0e-113">By default, Remove-AzRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="b8a0e-114">Om du inte vill att frågan ska visas använder du parametern Force.</span><span class="sxs-lookup"><span data-stu-id="b8a0e-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="b8a0e-115">Om det finns befintliga roll tilldelningar för den anpassade rollen som ska tas bort Miss lyckas borttagningen.</span><span class="sxs-lookup"><span data-stu-id="b8a0e-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="b8a0e-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8a0e-116">EXAMPLES</span></span>

### <span data-ttu-id="b8a0e-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b8a0e-117">Example 1</span></span>
```
Get-AzRoleDefinition -Name "Virtual Machine Operator" | Remove-AzRoleDefinition
```

### <span data-ttu-id="b8a0e-118">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b8a0e-118">Example 2</span></span>
```
Remove-AzRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="b8a0e-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8a0e-119">PARAMETERS</span></span>

### <span data-ttu-id="b8a0e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8a0e-120">-DefaultProfile</span></span>
<span data-ttu-id="b8a0e-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b8a0e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8a0e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b8a0e-122">-Force</span></span>
<span data-ttu-id="b8a0e-123">Om det här alternativet anges behöver du inte bekräfta en bekräftelse innan den anpassade rollen tas bort</span><span class="sxs-lookup"><span data-stu-id="b8a0e-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="b8a0e-124">-ID</span><span class="sxs-lookup"><span data-stu-id="b8a0e-124">-Id</span></span>
<span data-ttu-id="b8a0e-125">ID för den roll definition som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="b8a0e-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="b8a0e-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8a0e-126">-InputObject</span></span>
<span data-ttu-id="b8a0e-127">Objektet som representerar den roll definition som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b8a0e-127">The object representing the role definition to be removed.</span></span>

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

### <span data-ttu-id="b8a0e-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="b8a0e-128">-Name</span></span>
<span data-ttu-id="b8a0e-129">Namn på den roll definition som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b8a0e-129">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="b8a0e-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8a0e-130">-PassThru</span></span>
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

### <span data-ttu-id="b8a0e-131">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="b8a0e-131">-Scope</span></span>
<span data-ttu-id="b8a0e-132">Definitions omfång för roll.</span><span class="sxs-lookup"><span data-stu-id="b8a0e-132">Role definition scope.</span></span>

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

### <span data-ttu-id="b8a0e-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b8a0e-133">-Confirm</span></span>
<span data-ttu-id="b8a0e-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b8a0e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8a0e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8a0e-135">-WhatIf</span></span>
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

### <span data-ttu-id="b8a0e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a0e-136">CommonParameters</span></span>
<span data-ttu-id="b8a0e-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8a0e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a0e-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8a0e-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a0e-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8a0e-139">INPUTS</span></span>

### <span data-ttu-id="b8a0e-140">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b8a0e-140">System.Guid</span></span>

### <span data-ttu-id="b8a0e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b8a0e-141">System.String</span></span>

### <span data-ttu-id="b8a0e-142">Microsoft. Azure. kommandon. sources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b8a0e-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="b8a0e-143">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b8a0e-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="b8a0e-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8a0e-144">OUTPUTS</span></span>

### <span data-ttu-id="b8a0e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b8a0e-145">System.Boolean</span></span>

## <span data-ttu-id="b8a0e-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8a0e-146">NOTES</span></span>
<span data-ttu-id="b8a0e-147">Nyckelord: Azure, AZ, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="b8a0e-147">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b8a0e-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8a0e-148">RELATED LINKS</span></span>

[<span data-ttu-id="b8a0e-149">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b8a0e-149">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="b8a0e-150">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b8a0e-150">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="b8a0e-151">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b8a0e-151">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)
