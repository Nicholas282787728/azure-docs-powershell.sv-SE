---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: c389f62f6f9b76f0ebdab30ddf600d333263a87c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744847"
---
# <span data-ttu-id="fb3ba-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fb3ba-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="fb3ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb3ba-102">SYNOPSIS</span></span>
<span data-ttu-id="fb3ba-103">Tar bort en behållar register.</span><span class="sxs-lookup"><span data-stu-id="fb3ba-103">Removes a container registry.</span></span>

## <span data-ttu-id="fb3ba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb3ba-104">SYNTAX</span></span>

### <span data-ttu-id="fb3ba-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fb3ba-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb3ba-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb3ba-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb3ba-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb3ba-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb3ba-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb3ba-108">DESCRIPTION</span></span>
<span data-ttu-id="fb3ba-109">Remove-AzContainerRegistry cmdlet tar bort en behållar register.</span><span class="sxs-lookup"><span data-stu-id="fb3ba-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="fb3ba-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb3ba-110">EXAMPLES</span></span>

### <span data-ttu-id="fb3ba-111">Exempel 1: ta bort ett angivet behållar register</span><span class="sxs-lookup"><span data-stu-id="fb3ba-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="fb3ba-112">Det här kommandot tar bort den angivna behållar registret.</span><span class="sxs-lookup"><span data-stu-id="fb3ba-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="fb3ba-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb3ba-113">PARAMETERS</span></span>

### <span data-ttu-id="fb3ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb3ba-114">-DefaultProfile</span></span>
<span data-ttu-id="fb3ba-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fb3ba-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb3ba-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="fb3ba-116">-Name</span></span>
<span data-ttu-id="fb3ba-117">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="fb3ba-117">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3ba-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb3ba-118">-PassThru</span></span>
<span data-ttu-id="fb3ba-119">Anger att denna cmdlet returnerar sant om borttagningen lyckades.</span><span class="sxs-lookup"><span data-stu-id="fb3ba-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="fb3ba-120">-Register</span><span class="sxs-lookup"><span data-stu-id="fb3ba-120">-Registry</span></span>
<span data-ttu-id="fb3ba-121">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="fb3ba-121">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3ba-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb3ba-122">-ResourceGroupName</span></span>
<span data-ttu-id="fb3ba-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="fb3ba-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3ba-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb3ba-124">-ResourceId</span></span>
<span data-ttu-id="fb3ba-125">Resurs-ID för behållar registret</span><span class="sxs-lookup"><span data-stu-id="fb3ba-125">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb3ba-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fb3ba-126">-Confirm</span></span>
<span data-ttu-id="fb3ba-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fb3ba-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3ba-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb3ba-128">-WhatIf</span></span>
<span data-ttu-id="fb3ba-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fb3ba-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb3ba-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fb3ba-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3ba-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb3ba-131">CommonParameters</span></span>
<span data-ttu-id="fb3ba-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb3ba-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb3ba-133">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb3ba-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb3ba-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb3ba-134">INPUTS</span></span>

### <span data-ttu-id="fb3ba-135">System. String</span><span class="sxs-lookup"><span data-stu-id="fb3ba-135">System.String</span></span>

## <span data-ttu-id="fb3ba-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb3ba-136">OUTPUTS</span></span>

### <span data-ttu-id="fb3ba-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fb3ba-137">System.Boolean</span></span>

## <span data-ttu-id="fb3ba-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb3ba-138">NOTES</span></span>

## <span data-ttu-id="fb3ba-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb3ba-139">RELATED LINKS</span></span>

[<span data-ttu-id="fb3ba-140">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fb3ba-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="fb3ba-141">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fb3ba-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="fb3ba-142">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fb3ba-142">Update-AzContainerRegistry</span></span>]()

