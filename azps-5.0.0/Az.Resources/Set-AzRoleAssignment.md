---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleAssignment.md
ms.openlocfilehash: 9342ea2486c28a44ba7ff4a22f21619846ac7010
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273038"
---
# <span data-ttu-id="ad0c3-101">Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ad0c3-101">Set-AzRoleAssignment</span></span>

## <span data-ttu-id="ad0c3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad0c3-102">SYNOPSIS</span></span>
<span data-ttu-id="ad0c3-103">Uppdatera en befintlig roll tilldelning.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-103">Update an existing Role Assignment.</span></span>

## <span data-ttu-id="ad0c3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad0c3-104">SYNTAX</span></span>

### <span data-ttu-id="ad0c3-105">RoleAssignmentParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ad0c3-105">RoleAssignmentParameterSet (Default)</span></span>
```
Set-AzRoleAssignment -InputObject <PSRoleAssignment> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad0c3-106">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad0c3-106">InputFileParameterSet</span></span>
```
Set-AzRoleAssignment -InputFile <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad0c3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad0c3-107">DESCRIPTION</span></span>
<span data-ttu-id="ad0c3-108">Använd kommandot New-AzRoleAssignment om du vill ändra en befintlig uppgift.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-108">Use the New-AzRoleAssignment command to modify an existing assignment.</span></span>  
<span data-ttu-id="ad0c3-109">Beskrivningar kan vara en giltig sträng och diferentiate från varandra.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-109">Descriptions can be any valid string, use that to diferentiate from one another.</span></span>  
<span data-ttu-id="ad0c3-110">om villkoret anges villkors versionen måste du ange det men om du uppdaterar ett villkor som inte behövs.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-110">if Condition is set Condition Version has to be set as well but if you're updating a Condition that is not necesary.</span></span>
<span data-ttu-id="ad0c3-111">Villkors versionen kan uppgraderas från 1,0 till 2,0, men kan inte nedgraderas.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-111">Condition Version can be upgraded from 1.0 to 2.0 but it can't not be downgraded back.</span></span> <span data-ttu-id="ad0c3-112">Var försiktig eftersom 2,0 inte är retrocompatible med 1,0.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-112">Be cautious as 2.0 is not retrocompatible with 1.0.</span></span>

## <span data-ttu-id="ad0c3-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad0c3-113">EXAMPLES</span></span>

### <span data-ttu-id="ad0c3-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ad0c3-114">Example 1</span></span>
```powershell
$ConditionVersion = "2.0"
  $Description = "This is a new role assignment for John"
  $Condition = "@Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'"

  $roleAssignment = Get-AzRoleAssignment -Scope "/subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg" -PrincipalId "0c0f6cdc-90dd-4664-83c0-a0d986c4c604"
  $roleAssignment.Description = $Description
  $roleAssignment.Condition = $Condition
  $roleAssignment.ConditionVersion = $ConditionVersion

  Set-AzRoleAssignment -InputObject $roleAssignment -PassThru

  RoleAssignmentId   : /providers/Microsoft.Management/managementGroups/1273adef-00a3
                     -4086-a51a-dbcce1857d36/providers/Microsoft.Authorization/role
                     Assignments/926c2a76-be19-4281-94de-38777629b9dc
  Scope              : /subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg
  DisplayName        : John Doe
  SignInName         : John.Doe@Contoso.com
  RoleDefinitionName : Owner
  RoleDefinitionId   : 8e3af657-a8ff-443c-a75c-2fe8c4bcb635
  ObjectId           : 0c0f6cdc-90dd-4664-83c0-a0d986c4c604
  ObjectType         : User
  CanDelegate        : False
  Description        : This is a new role assignment for John
  ConditionVersion   : 2.0
  Condition          : @Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'
```

<span data-ttu-id="ad0c3-115">Uppdatera en befintlig roll tilldelning genom att ändra ett objekt</span><span class="sxs-lookup"><span data-stu-id="ad0c3-115">Update an existing role assignment by modifying an object</span></span>

### <span data-ttu-id="ad0c3-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ad0c3-116">Example 2</span></span>
```powershell
Set-AzRoleAssignment -InputFile "C:\RoleAssignments\example.json" -PassThru

  RoleAssignmentId   : /providers/Microsoft.Management/managementGroups/1273adef-00a3
                     -4086-a51a-dbcce1857d36/providers/Microsoft.Authorization/role
                     Assignments/926c2a76-be19-4281-94de-38777629b9dc
  Scope              : /subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg
  DisplayName        : John Doe
  SignInName         : John.Doe@Contoso.com
  RoleDefinitionName : Owner
  RoleDefinitionId   : 8e3af657-a8ff-443c-a75c-2fe8c4bcb635
  ObjectId           : 0c0f6cdc-90dd-4664-83c0-a0d986c4c604
  ObjectType         : User
  CanDelegate        : False
  Description        : This is a new role assignment for John
  ConditionVersion   : 2.0
  Condition          : @Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'
```

<span data-ttu-id="ad0c3-117">Uppdatera en befintlig roll tilldelning med hjälp av en fil</span><span class="sxs-lookup"><span data-stu-id="ad0c3-117">Update an existing role assignment by using a file</span></span>

## <span data-ttu-id="ad0c3-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad0c3-118">PARAMETERS</span></span>

### <span data-ttu-id="ad0c3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad0c3-119">-DefaultProfile</span></span>
<span data-ttu-id="ad0c3-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad0c3-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="ad0c3-121">-InputFile</span></span>
<span data-ttu-id="ad0c3-122">Fil namn som innehåller en enda roll definition.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-122">File name containing a single role definition.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad0c3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad0c3-123">-InputObject</span></span>
<span data-ttu-id="ad0c3-124">Roll tilldelning.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-124">Role Assignment.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad0c3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad0c3-125">-PassThru</span></span>
<span data-ttu-id="ad0c3-126">Om det anges visas den uppdaterade roll tilldelningen</span><span class="sxs-lookup"><span data-stu-id="ad0c3-126">If specified, displays the updated role assignment</span></span>

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

### <span data-ttu-id="ad0c3-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ad0c3-127">-Confirm</span></span>
<span data-ttu-id="ad0c3-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad0c3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad0c3-129">-WhatIf</span></span>
<span data-ttu-id="ad0c3-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad0c3-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad0c3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad0c3-132">CommonParameters</span></span>
<span data-ttu-id="ad0c3-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad0c3-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad0c3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad0c3-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad0c3-135">INPUTS</span></span>

### <span data-ttu-id="ad0c3-136">Microsoft. Azure. kommandon. sources. Models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ad0c3-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="ad0c3-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad0c3-137">OUTPUTS</span></span>

### <span data-ttu-id="ad0c3-138">Microsoft. Azure. kommandon. sources. Models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ad0c3-138">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="ad0c3-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad0c3-139">NOTES</span></span>

## <span data-ttu-id="ad0c3-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad0c3-140">RELATED LINKS</span></span>
