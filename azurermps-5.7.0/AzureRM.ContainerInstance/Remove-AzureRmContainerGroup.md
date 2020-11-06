---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/remove-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
ms.openlocfilehash: 80343713c9bf7a0e34a1d9a3b3b75825cbb97a12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584395"
---
# <span data-ttu-id="c4d59-101">Remove-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="c4d59-101">Remove-AzureRmContainerGroup</span></span>

## <span data-ttu-id="c4d59-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4d59-102">SYNOPSIS</span></span>
<span data-ttu-id="c4d59-103">Tar bort en behållar grupp.</span><span class="sxs-lookup"><span data-stu-id="c4d59-103">Removes a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4d59-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4d59-104">SYNTAX</span></span>

### <span data-ttu-id="c4d59-105">RemoveContainerGroupByResourceGroupAndNameParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c4d59-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4d59-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="c4d59-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzureRmContainerGroup -InputObject <PSContainerGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4d59-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="c4d59-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzureRmContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4d59-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4d59-108">DESCRIPTION</span></span>
<span data-ttu-id="c4d59-109">Cmdleten **Remove-AzureRmContainerGroup** tar bort en behållar grupp.</span><span class="sxs-lookup"><span data-stu-id="c4d59-109">The **Remove-AzureRmContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="c4d59-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4d59-110">EXAMPLES</span></span>

### <span data-ttu-id="c4d59-111">Exempel 1: tar bort en behållar grupp</span><span class="sxs-lookup"><span data-stu-id="c4d59-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="c4d59-112">Det här kommandot tar bort den angivna behållar gruppen.</span><span class="sxs-lookup"><span data-stu-id="c4d59-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="c4d59-113">Exempel 2: tar bort en behållar grupp efter ledning</span><span class="sxs-lookup"><span data-stu-id="c4d59-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="c4d59-114">Det här kommandot tar bort en behållar grupp efter dragning.</span><span class="sxs-lookup"><span data-stu-id="c4d59-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="c4d59-115">Exempel 3: tar bort en behållar grupp efter resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="c4d59-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="c4d59-116">Det här kommandot tar bort en behållar grupp efter resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="c4d59-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="c4d59-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4d59-117">PARAMETERS</span></span>

### <span data-ttu-id="c4d59-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4d59-118">-DefaultProfile</span></span>
<span data-ttu-id="c4d59-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c4d59-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4d59-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4d59-120">-InputObject</span></span>
<span data-ttu-id="c4d59-121">Behållar gruppen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c4d59-121">The container group to remove.</span></span>

```yaml
Type: PSContainerGroup
Parameter Sets: RemoveContainerGroupByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4d59-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="c4d59-122">-Name</span></span>
<span data-ttu-id="c4d59-123">Namn på behållar gruppen.</span><span class="sxs-lookup"><span data-stu-id="c4d59-123">The container group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4d59-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4d59-124">-PassThru</span></span>
<span data-ttu-id="c4d59-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c4d59-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4d59-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4d59-126">-ResourceGroupName</span></span>
<span data-ttu-id="c4d59-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="c4d59-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4d59-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4d59-128">-ResourceId</span></span>
<span data-ttu-id="c4d59-129">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="c4d59-129">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: RemoveContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4d59-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c4d59-130">-Confirm</span></span>
<span data-ttu-id="c4d59-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c4d59-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4d59-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4d59-132">-WhatIf</span></span>
<span data-ttu-id="c4d59-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c4d59-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4d59-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c4d59-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4d59-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4d59-135">CommonParameters</span></span>
<span data-ttu-id="c4d59-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4d59-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4d59-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4d59-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4d59-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4d59-138">INPUTS</span></span>

### <span data-ttu-id="c4d59-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c4d59-139">System.String</span></span>
<span data-ttu-id="c4d59-140">Microsoft. Azure. commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="c4d59-140">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="c4d59-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4d59-141">OUTPUTS</span></span>

### <span data-ttu-id="c4d59-142">Microsoft. Azure. commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="c4d59-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="c4d59-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4d59-143">NOTES</span></span>

## <span data-ttu-id="c4d59-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4d59-144">RELATED LINKS</span></span>
