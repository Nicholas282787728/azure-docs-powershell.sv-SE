---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/remove-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
ms.openlocfilehash: 6f3b3006bfb51a90d5919c4cba2e2bc4295d4a76
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926301"
---
# <span data-ttu-id="b9c0f-101">Remove-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="b9c0f-101">Remove-AzContainerGroup</span></span>

## <span data-ttu-id="b9c0f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b9c0f-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c0f-103">Tar bort en behållar grupp.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-103">Removes a container group.</span></span>

## <span data-ttu-id="b9c0f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b9c0f-104">SYNTAX</span></span>

### <span data-ttu-id="b9c0f-105">RemoveContainerGroupByResourceGroupAndNameParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b9c0f-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9c0f-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="b9c0f-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzContainerGroup -InputObject <PSContainerGroup> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9c0f-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="b9c0f-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9c0f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b9c0f-108">DESCRIPTION</span></span>
<span data-ttu-id="b9c0f-109">Cmdleten **Remove-AzContainerGroup** tar bort en behållar grupp.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-109">The **Remove-AzContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="b9c0f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b9c0f-110">EXAMPLES</span></span>

### <span data-ttu-id="b9c0f-111">Exempel 1: tar bort en behållar grupp</span><span class="sxs-lookup"><span data-stu-id="b9c0f-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="b9c0f-112">Det här kommandot tar bort den angivna behållar gruppen.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="b9c0f-113">Exempel 2: tar bort en behållar grupp efter ledning</span><span class="sxs-lookup"><span data-stu-id="b9c0f-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="b9c0f-114">Det här kommandot tar bort en behållar grupp efter dragning.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="b9c0f-115">Exempel 3: tar bort en behållar grupp efter resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="b9c0f-116">Det här kommandot tar bort en behållar grupp efter resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="b9c0f-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b9c0f-117">PARAMETERS</span></span>

### <span data-ttu-id="b9c0f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c0f-118">-DefaultProfile</span></span>
<span data-ttu-id="b9c0f-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9c0f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9c0f-120">-InputObject</span></span>
<span data-ttu-id="b9c0f-121">Behållar gruppen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-121">The container group to remove.</span></span>

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

### <span data-ttu-id="b9c0f-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="b9c0f-122">-Name</span></span>
<span data-ttu-id="b9c0f-123">Namn på behållar gruppen.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-123">The container group name.</span></span>

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

### <span data-ttu-id="b9c0f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9c0f-124">-PassThru</span></span>
<span data-ttu-id="b9c0f-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b9c0f-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b9c0f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9c0f-126">-ResourceGroupName</span></span>
<span data-ttu-id="b9c0f-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-127">The resource group name.</span></span>

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

### <span data-ttu-id="b9c0f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9c0f-128">-ResourceId</span></span>
<span data-ttu-id="b9c0f-129">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-129">The resource id.</span></span>

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

### <span data-ttu-id="b9c0f-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b9c0f-130">-Confirm</span></span>
<span data-ttu-id="b9c0f-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9c0f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9c0f-132">-WhatIf</span></span>
<span data-ttu-id="b9c0f-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9c0f-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9c0f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c0f-135">CommonParameters</span></span>
<span data-ttu-id="b9c0f-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c0f-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9c0f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c0f-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b9c0f-138">INPUTS</span></span>

### <span data-ttu-id="b9c0f-139">Microsoft. Azure. commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="b9c0f-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="b9c0f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b9c0f-140">System.String</span></span>

## <span data-ttu-id="b9c0f-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b9c0f-141">OUTPUTS</span></span>

### <span data-ttu-id="b9c0f-142">Microsoft. Azure. commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="b9c0f-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="b9c0f-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b9c0f-143">NOTES</span></span>

## <span data-ttu-id="b9c0f-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b9c0f-144">RELATED LINKS</span></span>