---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
ms.openlocfilehash: 476555b271d58f8e594f0cae1422bcdde1fc46e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756551"
---
# <span data-ttu-id="1c0f9-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1c0f9-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="1c0f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c0f9-102">SYNOPSIS</span></span>
<span data-ttu-id="1c0f9-103">Tar bort en anpassad roll i Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="1c0f9-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="1c0f9-104">Rollen som ska tas bort anges med egenskapen ID för rollen.</span><span class="sxs-lookup"><span data-stu-id="1c0f9-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="1c0f9-105">Borttagningen Miss lyckas om det finns befintliga roll tilldelningar för den anpassade rollen.</span><span class="sxs-lookup"><span data-stu-id="1c0f9-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c0f9-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c0f9-106">SYNTAX</span></span>

### <span data-ttu-id="1c0f9-107">RoleDefinitionIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1c0f9-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c0f9-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c0f9-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c0f9-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c0f9-109">DESCRIPTION</span></span>
<span data-ttu-id="1c0f9-110">Remove-AzureRmRoleDefinition cmdlet tar bort en anpassad roll i Azure Role-Based Access-kontroll.</span><span class="sxs-lookup"><span data-stu-id="1c0f9-110">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="1c0f9-111">Ange ID-parametern för en befintlig anpassad roll för att ta bort den anpassade rollen.</span><span class="sxs-lookup"><span data-stu-id="1c0f9-111">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="1c0f9-112">Remove-AzureRmRoleDefinition uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="1c0f9-112">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="1c0f9-113">Om du inte vill att frågan ska visas använder du parametern Force.</span><span class="sxs-lookup"><span data-stu-id="1c0f9-113">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="1c0f9-114">Om det finns befintliga roll tilldelningar för den anpassade rollen som ska tas bort Miss lyckas borttagningen.</span><span class="sxs-lookup"><span data-stu-id="1c0f9-114">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="1c0f9-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c0f9-115">EXAMPLES</span></span>

### <span data-ttu-id="1c0f9-116">--------------------------Exempel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1c0f9-116">--------------------------  Example 1  --------------------------</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="1c0f9-117">--------------------------Exempel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="1c0f9-117">--------------------------  Example 2  --------------------------</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="1c0f9-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c0f9-118">PARAMETERS</span></span>

### <span data-ttu-id="1c0f9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1c0f9-119">-Force</span></span>
<span data-ttu-id="1c0f9-120">Om det här alternativet anges behöver du inte bekräfta en bekräftelse innan den anpassade rollen tas bort</span><span class="sxs-lookup"><span data-stu-id="1c0f9-120">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="1c0f9-121">-ID</span><span class="sxs-lookup"><span data-stu-id="1c0f9-121">-Id</span></span>
<span data-ttu-id="1c0f9-122">ID för den roll definition som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="1c0f9-122">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="1c0f9-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="1c0f9-123">-Name</span></span>
<span data-ttu-id="1c0f9-124">Namn på den roll definition som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="1c0f9-124">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="1c0f9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c0f9-125">-PassThru</span></span>
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

### <span data-ttu-id="1c0f9-126">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="1c0f9-126">-Scope</span></span>
<span data-ttu-id="1c0f9-127">Definitions omfång för roll.</span><span class="sxs-lookup"><span data-stu-id="1c0f9-127">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c0f9-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1c0f9-128">-Confirm</span></span>
<span data-ttu-id="1c0f9-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1c0f9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c0f9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c0f9-130">-WhatIf</span></span>
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

### <span data-ttu-id="1c0f9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c0f9-131">-DefaultProfile</span></span>
<span data-ttu-id="1c0f9-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1c0f9-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c0f9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c0f9-133">CommonParameters</span></span>
<span data-ttu-id="1c0f9-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c0f9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c0f9-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c0f9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c0f9-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c0f9-136">INPUTS</span></span>

## <span data-ttu-id="1c0f9-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c0f9-137">OUTPUTS</span></span>

### <span data-ttu-id="1c0f9-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1c0f9-138">System.Boolean</span></span>

## <span data-ttu-id="1c0f9-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c0f9-139">NOTES</span></span>
<span data-ttu-id="1c0f9-140">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="1c0f9-140">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="1c0f9-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c0f9-141">RELATED LINKS</span></span>

[<span data-ttu-id="1c0f9-142">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1c0f9-142">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="1c0f9-143">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1c0f9-143">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="1c0f9-144">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1c0f9-144">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

