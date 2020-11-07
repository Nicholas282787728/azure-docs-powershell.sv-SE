---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
ms.openlocfilehash: be9a289e7d3aca0bc0a4cc4e2ae8e23dbe5b1ae7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757006"
---
# <span data-ttu-id="698fe-101">Remove-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="698fe-101">Remove-AzureRmContainerGroup</span></span>

## <span data-ttu-id="698fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="698fe-102">SYNOPSIS</span></span>
<span data-ttu-id="698fe-103">Tar bort en behållar grupp.</span><span class="sxs-lookup"><span data-stu-id="698fe-103">Removes a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="698fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="698fe-104">SYNTAX</span></span>

### <span data-ttu-id="698fe-105">RemoveContainerGroupByResourceGroupAndNameParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="698fe-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="698fe-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="698fe-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzureRmContainerGroup -InputObject <PSContainerGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="698fe-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="698fe-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzureRmContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="698fe-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="698fe-108">DESCRIPTION</span></span>
<span data-ttu-id="698fe-109">Cmdleten **Remove-AzureRmContainerGroup** tar bort en behållar grupp.</span><span class="sxs-lookup"><span data-stu-id="698fe-109">The **Remove-AzureRmContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="698fe-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="698fe-110">EXAMPLES</span></span>

### <span data-ttu-id="698fe-111">Exempel 1: tar bort en behållar grupp</span><span class="sxs-lookup"><span data-stu-id="698fe-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="698fe-112">Det här kommandot tar bort den angivna behållar gruppen.</span><span class="sxs-lookup"><span data-stu-id="698fe-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="698fe-113">Exempel 2: tar bort en behållar grupp efter ledning</span><span class="sxs-lookup"><span data-stu-id="698fe-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="698fe-114">Det här kommandot tar bort en behållar grupp efter dragning.</span><span class="sxs-lookup"><span data-stu-id="698fe-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="698fe-115">Exempel 3: tar bort en behållar grupp efter resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="698fe-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="698fe-116">Det här kommandot tar bort en behållar grupp efter resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="698fe-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="698fe-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="698fe-117">PARAMETERS</span></span>

### <span data-ttu-id="698fe-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="698fe-118">-Confirm</span></span>
<span data-ttu-id="698fe-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="698fe-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="698fe-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="698fe-120">-InputObject</span></span>
<span data-ttu-id="698fe-121">Behållar gruppen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="698fe-121">The container group to remove.</span></span>

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

### <span data-ttu-id="698fe-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="698fe-122">-Name</span></span>
<span data-ttu-id="698fe-123">Namn på behållar gruppen.</span><span class="sxs-lookup"><span data-stu-id="698fe-123">The container group name.</span></span>

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

### <span data-ttu-id="698fe-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="698fe-124">-PassThru</span></span>
<span data-ttu-id="698fe-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="698fe-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="698fe-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="698fe-126">-ResourceGroupName</span></span>
<span data-ttu-id="698fe-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="698fe-127">The resource group name.</span></span>

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

### <span data-ttu-id="698fe-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="698fe-128">-ResourceId</span></span>
<span data-ttu-id="698fe-129">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="698fe-129">The resource id.</span></span>

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

### <span data-ttu-id="698fe-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="698fe-130">-WhatIf</span></span>
<span data-ttu-id="698fe-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="698fe-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="698fe-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="698fe-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="698fe-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="698fe-133">-DefaultProfile</span></span>
<span data-ttu-id="698fe-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="698fe-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="698fe-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="698fe-135">CommonParameters</span></span>
<span data-ttu-id="698fe-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="698fe-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="698fe-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="698fe-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="698fe-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="698fe-138">INPUTS</span></span>

### <span data-ttu-id="698fe-139">System. String</span><span class="sxs-lookup"><span data-stu-id="698fe-139">System.String</span></span>
<span data-ttu-id="698fe-140">Microsoft. Azure. commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="698fe-140">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="698fe-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="698fe-141">OUTPUTS</span></span>

### <span data-ttu-id="698fe-142">Microsoft. Azure. commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="698fe-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="698fe-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="698fe-143">NOTES</span></span>

## <span data-ttu-id="698fe-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="698fe-144">RELATED LINKS</span></span>

