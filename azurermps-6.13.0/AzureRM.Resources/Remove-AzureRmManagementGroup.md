---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroup.md
ms.openlocfilehash: 7f19e45f96dbeac1470fbcc67a7db319589ad390
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582555"
---
# <span data-ttu-id="36f74-101">Remove-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="36f74-101">Remove-AzureRmManagementGroup</span></span>

## <span data-ttu-id="36f74-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36f74-102">SYNOPSIS</span></span>
<span data-ttu-id="36f74-103">Tar bort en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="36f74-103">Removes a Management Group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36f74-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36f74-104">SYNTAX</span></span>

### <span data-ttu-id="36f74-105">GroupOperations (standard)</span><span class="sxs-lookup"><span data-stu-id="36f74-105">GroupOperations (Default)</span></span>
```
Remove-AzureRmManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36f74-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="36f74-106">ManagementGroupObject</span></span>
```
Remove-AzureRmManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36f74-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36f74-107">DESCRIPTION</span></span>
<span data-ttu-id="36f74-108">Cmdleten **Remove-AzureRmManagementGroup** tar bort en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="36f74-108">The **Remove-AzureRmManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="36f74-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36f74-109">EXAMPLES</span></span>

### <span data-ttu-id="36f74-110">Exempel 1 – ta bort en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="36f74-110">Example 1 - Remove a Management Group</span></span>
```
PS C:\> Remove-AzureRmManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="36f74-111">Exempel 2 – ta bort en hanterings grupp efter rör PSManagementGroup-objekt</span><span class="sxs-lookup"><span data-stu-id="36f74-111">Example 2 - Remove a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-Remove-AzureRmManagementGroup -GroupName "TestGroup" | Remove-AzureRmManagementGroup
```

## <span data-ttu-id="36f74-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36f74-112">PARAMETERS</span></span>

### <span data-ttu-id="36f74-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36f74-113">-DefaultProfile</span></span>
<span data-ttu-id="36f74-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="36f74-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36f74-115">-Grupp namn</span><span class="sxs-lookup"><span data-stu-id="36f74-115">-GroupName</span></span>
<span data-ttu-id="36f74-116">Hanterings grupp-ID</span><span class="sxs-lookup"><span data-stu-id="36f74-116">Management Group Id</span></span>

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

### <span data-ttu-id="36f74-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36f74-117">-InputObject</span></span>
<span data-ttu-id="36f74-118">Infoga objekt från get-samtalet</span><span class="sxs-lookup"><span data-stu-id="36f74-118">Input Object from the Get call</span></span>

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

### <span data-ttu-id="36f74-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36f74-119">-PassThru</span></span>
<span data-ttu-id="36f74-120">Retur `true` vid lyckad körning</span><span class="sxs-lookup"><span data-stu-id="36f74-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="36f74-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="36f74-121">-Confirm</span></span>
<span data-ttu-id="36f74-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="36f74-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36f74-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36f74-123">-WhatIf</span></span>
<span data-ttu-id="36f74-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="36f74-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36f74-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="36f74-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36f74-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36f74-126">CommonParameters</span></span>
<span data-ttu-id="36f74-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36f74-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36f74-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36f74-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36f74-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36f74-129">INPUTS</span></span>

### <span data-ttu-id="36f74-130">Microsoft. Azure. commands. Resources. Models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="36f74-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>
<span data-ttu-id="36f74-131">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="36f74-131">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="36f74-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36f74-132">OUTPUTS</span></span>

### <span data-ttu-id="36f74-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="36f74-133">System.Boolean</span></span>

## <span data-ttu-id="36f74-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36f74-134">NOTES</span></span>

## <span data-ttu-id="36f74-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36f74-135">RELATED LINKS</span></span>
