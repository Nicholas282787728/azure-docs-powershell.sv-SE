---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/remove-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
ms.openlocfilehash: 6f3b3006bfb51a90d5919c4cba2e2bc4295d4a76
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526520"
---
# <span data-ttu-id="4773a-101">Remove-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="4773a-101">Remove-AzContainerGroup</span></span>

## <span data-ttu-id="4773a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4773a-102">SYNOPSIS</span></span>
<span data-ttu-id="4773a-103">Tar bort en behållar grupp.</span><span class="sxs-lookup"><span data-stu-id="4773a-103">Removes a container group.</span></span>

## <span data-ttu-id="4773a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4773a-104">SYNTAX</span></span>

### <span data-ttu-id="4773a-105">RemoveContainerGroupByResourceGroupAndNameParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4773a-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4773a-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="4773a-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzContainerGroup -InputObject <PSContainerGroup> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4773a-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="4773a-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4773a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4773a-108">DESCRIPTION</span></span>
<span data-ttu-id="4773a-109">Cmdleten **Remove-AzContainerGroup** tar bort en behållar grupp.</span><span class="sxs-lookup"><span data-stu-id="4773a-109">The **Remove-AzContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="4773a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4773a-110">EXAMPLES</span></span>

### <span data-ttu-id="4773a-111">Exempel 1: tar bort en behållar grupp</span><span class="sxs-lookup"><span data-stu-id="4773a-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="4773a-112">Det här kommandot tar bort den angivna behållar gruppen.</span><span class="sxs-lookup"><span data-stu-id="4773a-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="4773a-113">Exempel 2: tar bort en behållar grupp efter ledning</span><span class="sxs-lookup"><span data-stu-id="4773a-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="4773a-114">Det här kommandot tar bort en behållar grupp efter dragning.</span><span class="sxs-lookup"><span data-stu-id="4773a-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="4773a-115">Exempel 3: tar bort en behållar grupp efter resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="4773a-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="4773a-116">Det här kommandot tar bort en behållar grupp efter resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="4773a-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="4773a-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4773a-117">PARAMETERS</span></span>

### <span data-ttu-id="4773a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4773a-118">-DefaultProfile</span></span>
<span data-ttu-id="4773a-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4773a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4773a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4773a-120">-InputObject</span></span>
<span data-ttu-id="4773a-121">Behållar gruppen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="4773a-121">The container group to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: RemoveContainerGroupByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4773a-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="4773a-122">-Name</span></span>
<span data-ttu-id="4773a-123">Namn på behållar gruppen.</span><span class="sxs-lookup"><span data-stu-id="4773a-123">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4773a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4773a-124">-PassThru</span></span>
<span data-ttu-id="4773a-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4773a-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4773a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4773a-126">-ResourceGroupName</span></span>
<span data-ttu-id="4773a-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4773a-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4773a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4773a-128">-ResourceId</span></span>
<span data-ttu-id="4773a-129">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="4773a-129">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4773a-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4773a-130">-Confirm</span></span>
<span data-ttu-id="4773a-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4773a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4773a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4773a-132">-WhatIf</span></span>
<span data-ttu-id="4773a-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4773a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4773a-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4773a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4773a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4773a-135">CommonParameters</span></span>
<span data-ttu-id="4773a-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4773a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4773a-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4773a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4773a-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4773a-138">INPUTS</span></span>

### <span data-ttu-id="4773a-139">Microsoft. Azure. commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="4773a-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="4773a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4773a-140">System.String</span></span>

## <span data-ttu-id="4773a-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4773a-141">OUTPUTS</span></span>

### <span data-ttu-id="4773a-142">Microsoft. Azure. commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="4773a-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="4773a-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4773a-143">NOTES</span></span>

## <span data-ttu-id="4773a-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4773a-144">RELATED LINKS</span></span>
