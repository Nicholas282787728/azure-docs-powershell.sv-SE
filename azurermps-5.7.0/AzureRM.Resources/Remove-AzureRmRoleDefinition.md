---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
ms.openlocfilehash: ae4f8e11ac213943d8cfcec162b43abde60fe753
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583055"
---
# <span data-ttu-id="dc686-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="dc686-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="dc686-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dc686-102">SYNOPSIS</span></span>
<span data-ttu-id="dc686-103">Tar bort en anpassad roll i Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="dc686-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="dc686-104">Rollen som ska tas bort anges med egenskapen ID för rollen.</span><span class="sxs-lookup"><span data-stu-id="dc686-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="dc686-105">Borttagningen Miss lyckas om det finns befintliga roll tilldelningar för den anpassade rollen.</span><span class="sxs-lookup"><span data-stu-id="dc686-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc686-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dc686-106">SYNTAX</span></span>

### <span data-ttu-id="dc686-107">RoleDefinitionIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="dc686-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc686-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc686-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc686-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dc686-109">DESCRIPTION</span></span>
<span data-ttu-id="dc686-110">Remove-AzureRmRoleDefinition cmdlet tar bort en anpassad roll i Azure Role-Based Access-kontroll.</span><span class="sxs-lookup"><span data-stu-id="dc686-110">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="dc686-111">Ange ID-parametern för en befintlig anpassad roll för att ta bort den anpassade rollen.</span><span class="sxs-lookup"><span data-stu-id="dc686-111">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="dc686-112">Remove-AzureRmRoleDefinition uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="dc686-112">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="dc686-113">Om du inte vill att frågan ska visas använder du parametern Force.</span><span class="sxs-lookup"><span data-stu-id="dc686-113">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="dc686-114">Om det finns befintliga roll tilldelningar för den anpassade rollen som ska tas bort Miss lyckas borttagningen.</span><span class="sxs-lookup"><span data-stu-id="dc686-114">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="dc686-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dc686-115">EXAMPLES</span></span>

### <span data-ttu-id="dc686-116">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dc686-116">Example 1</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="dc686-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="dc686-117">Example 2</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="dc686-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dc686-118">PARAMETERS</span></span>

### <span data-ttu-id="dc686-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc686-119">-DefaultProfile</span></span>
<span data-ttu-id="dc686-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="dc686-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc686-121">-Force</span><span class="sxs-lookup"><span data-stu-id="dc686-121">-Force</span></span>
<span data-ttu-id="dc686-122">Om det här alternativet anges behöver du inte bekräfta en bekräftelse innan den anpassade rollen tas bort</span><span class="sxs-lookup"><span data-stu-id="dc686-122">If set, does not prompt for a confirmation before deleting the custom role</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc686-123">-ID</span><span class="sxs-lookup"><span data-stu-id="dc686-123">-Id</span></span>
<span data-ttu-id="dc686-124">ID för den roll definition som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="dc686-124">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="dc686-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="dc686-125">-Name</span></span>
<span data-ttu-id="dc686-126">Namn på den roll definition som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="dc686-126">Name of the Role definition to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc686-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc686-127">-PassThru</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc686-128">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="dc686-128">-Scope</span></span>
<span data-ttu-id="dc686-129">Definitions omfång för roll.</span><span class="sxs-lookup"><span data-stu-id="dc686-129">Role definition scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc686-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dc686-130">-Confirm</span></span>
<span data-ttu-id="dc686-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dc686-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc686-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc686-132">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc686-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc686-133">CommonParameters</span></span>
<span data-ttu-id="dc686-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc686-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc686-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc686-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc686-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dc686-136">INPUTS</span></span>

### <span data-ttu-id="dc686-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="dc686-137">None</span></span>
<span data-ttu-id="dc686-138">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="dc686-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dc686-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dc686-139">OUTPUTS</span></span>

### <span data-ttu-id="dc686-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dc686-140">System.Boolean</span></span>

## <span data-ttu-id="dc686-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dc686-141">NOTES</span></span>
<span data-ttu-id="dc686-142">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="dc686-142">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="dc686-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dc686-143">RELATED LINKS</span></span>

[<span data-ttu-id="dc686-144">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="dc686-144">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="dc686-145">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="dc686-145">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="dc686-146">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="dc686-146">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

