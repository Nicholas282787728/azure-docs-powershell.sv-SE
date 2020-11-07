---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
ms.openlocfilehash: 19e2c227e8715d74cd9c33eaacd2807a96a5afc2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747167"
---
# <span data-ttu-id="6c697-101">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6c697-101">Get-AzManagementGroup</span></span>

## <span data-ttu-id="6c697-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6c697-102">SYNOPSIS</span></span>
<span data-ttu-id="6c697-103">Hämtar hanterings grupp (er)</span><span class="sxs-lookup"><span data-stu-id="6c697-103">Gets Management Group(s)</span></span>

## <span data-ttu-id="6c697-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6c697-104">SYNTAX</span></span>

### <span data-ttu-id="6c697-105">ListOperation (standard)</span><span class="sxs-lookup"><span data-stu-id="6c697-105">ListOperation (Default)</span></span>
```
Get-AzManagementGroup [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c697-106">GetOperation</span><span class="sxs-lookup"><span data-stu-id="6c697-106">GetOperation</span></span>
```
Get-AzManagementGroup [-GroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-Expand] [-Recurse]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c697-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6c697-107">DESCRIPTION</span></span>
<span data-ttu-id="6c697-108">Get-AzManagementGroup cmdlet får alla eller en specifik hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="6c697-108">The Get-AzManagementGroup cmdlet Gets all or a specific Management Group.</span></span>

## <span data-ttu-id="6c697-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6c697-109">EXAMPLES</span></span>

### <span data-ttu-id="6c697-110">Exempel 1: Hämta alla hanterings grupper</span><span class="sxs-lookup"><span data-stu-id="6c697-110">Example 1: Get all Management Groups</span></span>
```
PS C:\> Get-AzManagementGroup

Id          : /providers/Microsoft.Management/managementGroups/TestGroup
Type        : /providers/Microsoft.Management/managementGroups
Name        : TestGroup
TenantId    : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName : TestGroupDisplayName

Id          : /providers/Microsoft.Management/managementGroups/TestGroupChild
Type        : /providers/Microsoft.Management/managementGroups
Name        : TestGroupChild
TenantId    : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName : TestGroupChildDisplayName
```

### <span data-ttu-id="6c697-111">Exempel 2: Hämta specifik hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="6c697-111">Example 2: Get specific Management Group</span></span>
```
PS C:\> Get-AzManagementGroup -GroupName TestGroup

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="6c697-112">Exempel 3: Hämta specifik hanterings grupp och första nivån i hierarkin</span><span class="sxs-lookup"><span data-stu-id="6c697-112">Example 3: Get specific Management Group and first level of hierarchy</span></span>
```
PS C:\> $reponse = Get-AzManagementGroup -GroupName TestGroupParent -Expand
PS C:\> $response

Id                : /providers/Microsoft.Management/managementGroups/TestGroupParent
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroupParent
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupParent
UpdatedTime       : 2/1/2018 11:15:46 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
Children          : {TestGroup1DisplayName, TestGroup2DisplayName}

PS C:\> $response.Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestGroup1
Name        : TestGroup1
DisplayName : TestGroup1DisplayName
Children    :
```

<span data-ttu-id="6c697-113">Med `Expand` flaggan kan en navigera mellan `Children` matrisen och få information för varje underordnad.</span><span class="sxs-lookup"><span data-stu-id="6c697-113">With the `Expand` flag, one can navigate through the `Children` array and get details for each child.</span></span> <span data-ttu-id="6c697-114">Ger till exempel `Children[0]` information om gruppen med visnings namn `TestGroup1DisplayName` .</span><span class="sxs-lookup"><span data-stu-id="6c697-114">For example, `Children[0]` will give details for the group with display name `TestGroup1DisplayName`.</span></span>

### <span data-ttu-id="6c697-115">Exempel 4: Hämta specifik hanterings grupp och alla hiearchy</span><span class="sxs-lookup"><span data-stu-id="6c697-115">Example 4: Get specific Management Group and all levels of hiearchy</span></span>
```
PS C:\> $response = Get-AzManagementGroup -GroupName TestGroupParent -Expand -Recurse
PS C:\> $response

Id                : /providers/Microsoft.Management/managementGroups/TestGroupParent
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroupParent
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupParent
UpdatedTime       : 2/1/2018 11:15:46 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
Children          : {TestGroup1DisplayName, TestGroup2DisplayName}

PS C:\> $response.Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestGroup1
Name        : TestGroup1
DisplayName : TestGroup1DisplayName
Children    : {TestRecurseChild}

PS C:\> $response.Children[0].Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestRecurseChild
Name        : TestRecurseChild
DisplayName : TestRecurseChild
Children    :
```

## <span data-ttu-id="6c697-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6c697-116">PARAMETERS</span></span>

### <span data-ttu-id="6c697-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c697-117">-DefaultProfile</span></span>
<span data-ttu-id="6c697-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6c697-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c697-119">-Expandera</span><span class="sxs-lookup"><span data-stu-id="6c697-119">-Expand</span></span>
<span data-ttu-id="6c697-120">Expandera utdata för att visa en lista över underordnade till hanterings gruppen</span><span class="sxs-lookup"><span data-stu-id="6c697-120">Expand the output to list the children of the management group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetOperation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c697-121">-Grupp namn</span><span class="sxs-lookup"><span data-stu-id="6c697-121">-GroupName</span></span>
<span data-ttu-id="6c697-122">Hanterings grupp-ID</span><span class="sxs-lookup"><span data-stu-id="6c697-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c697-123">-Recurse</span><span class="sxs-lookup"><span data-stu-id="6c697-123">-Recurse</span></span>
<span data-ttu-id="6c697-124">Lista över underordnade objekt i hanterings gruppen rekursivt</span><span class="sxs-lookup"><span data-stu-id="6c697-124">Recursively list the children of the management group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetOperation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c697-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6c697-125">-Confirm</span></span>
<span data-ttu-id="6c697-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6c697-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c697-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c697-127">-WhatIf</span></span>
<span data-ttu-id="6c697-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6c697-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c697-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6c697-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c697-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c697-130">CommonParameters</span></span>
<span data-ttu-id="6c697-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c697-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c697-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c697-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c697-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6c697-133">INPUTS</span></span>

### <span data-ttu-id="6c697-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="6c697-134">None</span></span>

## <span data-ttu-id="6c697-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6c697-135">OUTPUTS</span></span>

### <span data-ttu-id="6c697-136">Microsoft. Azure. commands. Resources. Models. ManagementGroups. PSManagementGroupInfo</span><span class="sxs-lookup"><span data-stu-id="6c697-136">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroupInfo</span></span>

### <span data-ttu-id="6c697-137">Microsoft. Azure. commands. Resources. Models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6c697-137">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="6c697-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6c697-138">NOTES</span></span>

## <span data-ttu-id="6c697-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6c697-139">RELATED LINKS</span></span>