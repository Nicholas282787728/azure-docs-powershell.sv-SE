---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
ms.openlocfilehash: e63171f3d4497bf558a4349ff013726e24b079f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747117"
---
# <span data-ttu-id="6f15d-101">New-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6f15d-101">New-AzManagementGroup</span></span>

## <span data-ttu-id="6f15d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f15d-102">SYNOPSIS</span></span>
<span data-ttu-id="6f15d-103">Skapar en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="6f15d-103">Creates a Management Group</span></span>

## <span data-ttu-id="6f15d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f15d-104">SYNTAX</span></span>

### <span data-ttu-id="6f15d-105">GroupOperations (standard)</span><span class="sxs-lookup"><span data-stu-id="6f15d-105">GroupOperations (Default)</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f15d-106">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="6f15d-106">ParentGroupObject</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f15d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f15d-107">DESCRIPTION</span></span>
<span data-ttu-id="6f15d-108">Cmdleten **New-AzManagementGroup** skapar en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="6f15d-108">The **New-AzManagementGroup** cmdlet creates a management group.</span></span>

## <span data-ttu-id="6f15d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f15d-109">EXAMPLES</span></span>

### <span data-ttu-id="6f15d-110">Exempel 1: skapa en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="6f15d-110">Example 1: Create a Management Group</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 11:06:27 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/14307de0-5e6f-46cf-b2ba-64a062964d30
ParentName        : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentDisplayName : 14307de0-5e6f-46cf-b2ba-64a062964d30
```

<span data-ttu-id="6f15d-111">Skapa en ny grupp med `DisplayName` och `ParentId` Ange som `null` .</span><span class="sxs-lookup"><span data-stu-id="6f15d-111">Creation of a new group with `DisplayName` and `ParentId` set to `null`.</span></span> <span data-ttu-id="6f15d-112">Det `DisplayName` kommer att vara samma som `GroupName` och den överordnade gruppen blir då innehavaren.</span><span class="sxs-lookup"><span data-stu-id="6f15d-112">The `DisplayName` will be same as the `GroupName` and the parent of the group will be the tenant.</span></span>  

### <span data-ttu-id="6f15d-113">Exempel 2: skapa en hanterings grupp med ett visnings namn</span><span class="sxs-lookup"><span data-stu-id="6f15d-113">Example 2: Create a Management Group with a display name</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 11:06:27 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/14307de0-5e6f-46cf-b2ba-64a062964d30
ParentName        : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentDisplayName : 14307de0-5e6f-46cf-b2ba-64a062964d30
```

<span data-ttu-id="6f15d-114">I det här fallet blir den överordnade för gruppen innehavaren och `DisplayName` kommer att anges till det angivna värdet.</span><span class="sxs-lookup"><span data-stu-id="6f15d-114">In this case, the parent of the group will be the tenant and the `DisplayName` will be set to the value given.</span></span>

### <span data-ttu-id="6f15d-115">Exempel 3: skapa en hanterings grupp med ett överordnat och ett visnings namn</span><span class="sxs-lookup"><span data-stu-id="6f15d-115">Example 3: Create a Management Group with a parent and a display name</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="6f15d-116">Exempel 4: skapa en hanterings grupp med en överordnad (med ett överordnat objekt)</span><span class="sxs-lookup"><span data-stu-id="6f15d-116">Example 4: Create a Management Group with a parent (using a parent object)</span></span>
```
PS C:\> $parentObject = Get-AzManagementGroup -GroupName "TestGroupParent"
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

## <span data-ttu-id="6f15d-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f15d-117">PARAMETERS</span></span>

### <span data-ttu-id="6f15d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f15d-118">-DefaultProfile</span></span>
<span data-ttu-id="6f15d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6f15d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f15d-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6f15d-120">-DisplayName</span></span>
<span data-ttu-id="6f15d-121">Visnings namn för hanterings gruppen</span><span class="sxs-lookup"><span data-stu-id="6f15d-121">Display Name of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f15d-122">-Grupp namn</span><span class="sxs-lookup"><span data-stu-id="6f15d-122">-GroupName</span></span>
<span data-ttu-id="6f15d-123">Hanterings grupp-ID</span><span class="sxs-lookup"><span data-stu-id="6f15d-123">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f15d-124">-</span><span class="sxs-lookup"><span data-stu-id="6f15d-124">-ParentId</span></span>
<span data-ttu-id="6f15d-125">Överordnat ID för hanterings gruppen</span><span class="sxs-lookup"><span data-stu-id="6f15d-125">Parent Id of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f15d-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6f15d-126">-ParentObject</span></span>
<span data-ttu-id="6f15d-127">Överordnat objekt</span><span class="sxs-lookup"><span data-stu-id="6f15d-127">Parent Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f15d-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6f15d-128">-Confirm</span></span>
<span data-ttu-id="6f15d-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6f15d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f15d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f15d-130">-WhatIf</span></span>
<span data-ttu-id="6f15d-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6f15d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f15d-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6f15d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f15d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f15d-133">CommonParameters</span></span>
<span data-ttu-id="6f15d-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f15d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f15d-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f15d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f15d-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f15d-136">INPUTS</span></span>

### <span data-ttu-id="6f15d-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="6f15d-137">None</span></span>

## <span data-ttu-id="6f15d-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f15d-138">OUTPUTS</span></span>

### <span data-ttu-id="6f15d-139">Microsoft. Azure. commands. Resources. Models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6f15d-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="6f15d-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f15d-140">NOTES</span></span>

## <span data-ttu-id="6f15d-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f15d-141">RELATED LINKS</span></span>

[<span data-ttu-id="6f15d-142">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6f15d-142">Remove-AzManagementGroup</span></span>](./Remove-AzManagementGroup.md)

[<span data-ttu-id="6f15d-143">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6f15d-143">Update-AzManagementGroup</span></span>](./Update-AzManagementGroup.md)

[<span data-ttu-id="6f15d-144">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6f15d-144">Get-AzManagementGroup</span></span>](./Get-AzManagementGroup.md)