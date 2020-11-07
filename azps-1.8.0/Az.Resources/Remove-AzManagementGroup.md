---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: cbc6be671669b3db8af41c0e5de4333b811e271a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747070"
---
# <span data-ttu-id="6b44d-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6b44d-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="6b44d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6b44d-102">SYNOPSIS</span></span>
<span data-ttu-id="6b44d-103">Tar bort en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="6b44d-103">Removes a Management Group</span></span>

## <span data-ttu-id="6b44d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6b44d-104">SYNTAX</span></span>

### <span data-ttu-id="6b44d-105">GroupOperations (standard)</span><span class="sxs-lookup"><span data-stu-id="6b44d-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b44d-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="6b44d-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b44d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6b44d-107">DESCRIPTION</span></span>
<span data-ttu-id="6b44d-108">Cmdleten **Remove-AzManagementGroup** tar bort en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="6b44d-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="6b44d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6b44d-109">EXAMPLES</span></span>

### <span data-ttu-id="6b44d-110">Exempel 1 – ta bort en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="6b44d-110">Example 1 - Remove a Management Group</span></span>
```
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="6b44d-111">Exempel 2 – ta bort en hanterings grupp efter rör PSManagementGroup-objekt</span><span class="sxs-lookup"><span data-stu-id="6b44d-111">Example 2 - Remove a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-Remove-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="6b44d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6b44d-112">PARAMETERS</span></span>

### <span data-ttu-id="6b44d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b44d-113">-DefaultProfile</span></span>
<span data-ttu-id="6b44d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6b44d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b44d-115">-Grupp namn</span><span class="sxs-lookup"><span data-stu-id="6b44d-115">-GroupName</span></span>
<span data-ttu-id="6b44d-116">Hanterings grupp-ID</span><span class="sxs-lookup"><span data-stu-id="6b44d-116">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b44d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b44d-117">-InputObject</span></span>
<span data-ttu-id="6b44d-118">Infoga objekt från get-samtalet</span><span class="sxs-lookup"><span data-stu-id="6b44d-118">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b44d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b44d-119">-PassThru</span></span>
<span data-ttu-id="6b44d-120">Retur `true` vid lyckad körning</span><span class="sxs-lookup"><span data-stu-id="6b44d-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="6b44d-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6b44d-121">-Confirm</span></span>
<span data-ttu-id="6b44d-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6b44d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b44d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b44d-123">-WhatIf</span></span>
<span data-ttu-id="6b44d-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6b44d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b44d-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6b44d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b44d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b44d-126">CommonParameters</span></span>
<span data-ttu-id="6b44d-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b44d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b44d-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b44d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b44d-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6b44d-129">INPUTS</span></span>

### <span data-ttu-id="6b44d-130">Microsoft. Azure. commands. Resources. Models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6b44d-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="6b44d-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6b44d-131">OUTPUTS</span></span>

### <span data-ttu-id="6b44d-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6b44d-132">System.Boolean</span></span>

## <span data-ttu-id="6b44d-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6b44d-133">NOTES</span></span>

## <span data-ttu-id="6b44d-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6b44d-134">RELATED LINKS</span></span>
