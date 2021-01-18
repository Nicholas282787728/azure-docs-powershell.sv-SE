---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
ms.openlocfilehash: bdef58db8dcda735a7a8c08350b806c9fd00cf21
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522299"
---
# <span data-ttu-id="c44de-101">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c44de-101">Update-AzManagementGroup</span></span>

## <span data-ttu-id="c44de-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c44de-102">SYNOPSIS</span></span>
<span data-ttu-id="c44de-103">Uppdaterar en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="c44de-103">Updates a Management Group</span></span>

## <span data-ttu-id="c44de-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c44de-104">SYNTAX</span></span>

### <span data-ttu-id="c44de-105">GroupOperations (standard)</span><span class="sxs-lookup"><span data-stu-id="c44de-105">GroupOperations (Default)</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c44de-106">ParentAndManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="c44de-106">ParentAndManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c44de-107">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="c44de-107">ManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c44de-108">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="c44de-108">ParentGroupObject</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c44de-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c44de-109">DESCRIPTION</span></span>
<span data-ttu-id="c44de-110">Cmdleten **Update-AzManagementGroup** **uppdaterar värdet för** namn eller **DisplayName** för en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="c44de-110">The **Update-AzManagementGroup** cmdlet updates the **ParentId** or **DisplayName** for a Management Group.</span></span>

## <span data-ttu-id="c44de-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c44de-111">EXAMPLES</span></span>

### <span data-ttu-id="c44de-112">Exempel 1: uppdatera namnet på en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="c44de-112">Example 1: Update a Management Group's Display Name</span></span>
```
PS C:\> Update-AzManagementGroup -Group "TestGroup" -DisplayName "New Display Name"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : New Display Name
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
```

### <span data-ttu-id="c44de-113">Exempel 2: uppdatera chef för en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="c44de-113">Example 2: Update a Management Group's Parent</span></span>
```
PS C:\> Update-AzManagementGroup -Group "TestGroup" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="c44de-114">Exempel 3: uppdatera en hanterings grupp efter ledning PSManagementGroup-objekt</span><span class="sxs-lookup"><span data-stu-id="c44de-114">Example 3: Update a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Update-AzManagementGroup -DisplayName "TestDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestDisplayName
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="c44de-115">Exempel 4: uppdatera en hanterings grupps förälder med ParentObject</span><span class="sxs-lookup"><span data-stu-id="c44de-115">Example 4: Update a Management Group's parent using the ParentObject</span></span>
```
PS C:\> $parentObject = Get-AzManagementGroup -GroupName "TestGroupParent"
PS C:\> Update-AzManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

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

## <span data-ttu-id="c44de-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c44de-116">PARAMETERS</span></span>

### <span data-ttu-id="c44de-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c44de-117">-DefaultProfile</span></span>
<span data-ttu-id="c44de-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c44de-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c44de-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c44de-119">-DisplayName</span></span>
<span data-ttu-id="c44de-120">Visnings namn för hanterings gruppen</span><span class="sxs-lookup"><span data-stu-id="c44de-120">Display Name of the management group</span></span>

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

### <span data-ttu-id="c44de-121">-Grupp namn</span><span class="sxs-lookup"><span data-stu-id="c44de-121">-GroupName</span></span>
<span data-ttu-id="c44de-122">Hanterings grupp-ID</span><span class="sxs-lookup"><span data-stu-id="c44de-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations, ParentGroupObject
Aliases: GroupId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44de-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c44de-123">-InputObject</span></span>
<span data-ttu-id="c44de-124">Infoga objekt från get-samtalet</span><span class="sxs-lookup"><span data-stu-id="c44de-124">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentAndManagementGroupObject, ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c44de-125">-</span><span class="sxs-lookup"><span data-stu-id="c44de-125">-ParentId</span></span>
<span data-ttu-id="c44de-126">Överordnat ID för hanterings gruppen</span><span class="sxs-lookup"><span data-stu-id="c44de-126">Parent Id of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations, ManagementGroupObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44de-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c44de-127">-ParentObject</span></span>
<span data-ttu-id="c44de-128">Infoga objekt från get-samtalet</span><span class="sxs-lookup"><span data-stu-id="c44de-128">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentAndManagementGroupObject, ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44de-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c44de-129">-Confirm</span></span>
<span data-ttu-id="c44de-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c44de-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c44de-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c44de-131">-WhatIf</span></span>
<span data-ttu-id="c44de-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c44de-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c44de-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c44de-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c44de-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c44de-134">CommonParameters</span></span>
<span data-ttu-id="c44de-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c44de-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c44de-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c44de-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c44de-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c44de-137">INPUTS</span></span>

### <span data-ttu-id="c44de-138">Microsoft. Azure. commands. Resources. Models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c44de-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="c44de-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c44de-139">OUTPUTS</span></span>

### <span data-ttu-id="c44de-140">Microsoft. Azure. commands. Resources. Models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c44de-140">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="c44de-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c44de-141">NOTES</span></span>

## <span data-ttu-id="c44de-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c44de-142">RELATED LINKS</span></span>
