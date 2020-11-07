---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: d36e362f1782e3566bc0d2febd65aebd4c68220d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926262"
---
# <span data-ttu-id="0e676-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0e676-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="0e676-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0e676-102">SYNOPSIS</span></span>
<span data-ttu-id="0e676-103">Tar bort en behållar register.</span><span class="sxs-lookup"><span data-stu-id="0e676-103">Removes a container registry.</span></span>

## <span data-ttu-id="0e676-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0e676-104">SYNTAX</span></span>

### <span data-ttu-id="0e676-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0e676-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e676-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e676-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e676-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e676-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e676-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0e676-108">DESCRIPTION</span></span>
<span data-ttu-id="0e676-109">Remove-AzContainerRegistry cmdlet tar bort en behållar register.</span><span class="sxs-lookup"><span data-stu-id="0e676-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="0e676-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0e676-110">EXAMPLES</span></span>

### <span data-ttu-id="0e676-111">Exempel 1: ta bort ett angivet behållar register</span><span class="sxs-lookup"><span data-stu-id="0e676-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="0e676-112">Det här kommandot tar bort den angivna behållar registret.</span><span class="sxs-lookup"><span data-stu-id="0e676-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="0e676-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0e676-113">PARAMETERS</span></span>

### <span data-ttu-id="0e676-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e676-114">-DefaultProfile</span></span>
<span data-ttu-id="0e676-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0e676-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e676-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="0e676-116">-Name</span></span>
<span data-ttu-id="0e676-117">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="0e676-117">Container Registry Name.</span></span>

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

### <span data-ttu-id="0e676-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e676-118">-PassThru</span></span>
<span data-ttu-id="0e676-119">Anger att denna cmdlet returnerar sant om borttagningen lyckades.</span><span class="sxs-lookup"><span data-stu-id="0e676-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="0e676-120">-Register</span><span class="sxs-lookup"><span data-stu-id="0e676-120">-Registry</span></span>
<span data-ttu-id="0e676-121">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="0e676-121">Container Registry Object.</span></span>

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

### <span data-ttu-id="0e676-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e676-122">-ResourceGroupName</span></span>
<span data-ttu-id="0e676-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="0e676-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="0e676-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e676-124">-ResourceId</span></span>
<span data-ttu-id="0e676-125">Resurs-ID för behållar registret</span><span class="sxs-lookup"><span data-stu-id="0e676-125">The container registry resource id</span></span>

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

### <span data-ttu-id="0e676-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0e676-126">-Confirm</span></span>
<span data-ttu-id="0e676-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0e676-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e676-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e676-128">-WhatIf</span></span>
<span data-ttu-id="0e676-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0e676-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e676-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0e676-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e676-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e676-131">CommonParameters</span></span>
<span data-ttu-id="0e676-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e676-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e676-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e676-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e676-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0e676-134">INPUTS</span></span>

### <span data-ttu-id="0e676-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0e676-135">System.String</span></span>

## <span data-ttu-id="0e676-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0e676-136">OUTPUTS</span></span>

### <span data-ttu-id="0e676-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0e676-137">System.Boolean</span></span>

## <span data-ttu-id="0e676-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0e676-138">NOTES</span></span>

## <span data-ttu-id="0e676-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0e676-139">RELATED LINKS</span></span>

[<span data-ttu-id="0e676-140">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0e676-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="0e676-141">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0e676-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="0e676-142">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0e676-142">Update-AzContainerRegistry</span></span>]()

