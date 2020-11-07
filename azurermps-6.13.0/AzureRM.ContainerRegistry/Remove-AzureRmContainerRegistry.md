---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: 2235e533e999fedbb06b79548bf4e2ce8de3586a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757106"
---
# <span data-ttu-id="5048b-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5048b-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="5048b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5048b-102">SYNOPSIS</span></span>
<span data-ttu-id="5048b-103">Tar bort en behållar register.</span><span class="sxs-lookup"><span data-stu-id="5048b-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5048b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5048b-104">SYNTAX</span></span>

### <span data-ttu-id="5048b-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5048b-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5048b-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5048b-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5048b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5048b-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5048b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5048b-108">DESCRIPTION</span></span>
<span data-ttu-id="5048b-109">Remove-AzureRmContainerRegistry cmdlet tar bort en behållar register.</span><span class="sxs-lookup"><span data-stu-id="5048b-109">The Remove-AzureRmContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="5048b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5048b-110">EXAMPLES</span></span>

### <span data-ttu-id="5048b-111">Exempel 1: ta bort ett angivet behållar register</span><span class="sxs-lookup"><span data-stu-id="5048b-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="5048b-112">Det här kommandot tar bort den angivna behållar registret.</span><span class="sxs-lookup"><span data-stu-id="5048b-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="5048b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5048b-113">PARAMETERS</span></span>

### <span data-ttu-id="5048b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5048b-114">-DefaultProfile</span></span>
<span data-ttu-id="5048b-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5048b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5048b-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="5048b-116">-Name</span></span>
<span data-ttu-id="5048b-117">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="5048b-117">Container Registry Name.</span></span>

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

### <span data-ttu-id="5048b-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5048b-118">-PassThru</span></span>
<span data-ttu-id="5048b-119">Anger att denna cmdlet returnerar sant om borttagningen lyckades.</span><span class="sxs-lookup"><span data-stu-id="5048b-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="5048b-120">-Register</span><span class="sxs-lookup"><span data-stu-id="5048b-120">-Registry</span></span>
<span data-ttu-id="5048b-121">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="5048b-121">Container Registry Object.</span></span>

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

### <span data-ttu-id="5048b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5048b-122">-ResourceGroupName</span></span>
<span data-ttu-id="5048b-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="5048b-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="5048b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5048b-124">-ResourceId</span></span>
<span data-ttu-id="5048b-125">Resurs-ID för behållar registret</span><span class="sxs-lookup"><span data-stu-id="5048b-125">The container registry resource id</span></span>

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

### <span data-ttu-id="5048b-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5048b-126">-Confirm</span></span>
<span data-ttu-id="5048b-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5048b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5048b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5048b-128">-WhatIf</span></span>
<span data-ttu-id="5048b-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5048b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5048b-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5048b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5048b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5048b-131">CommonParameters</span></span>
<span data-ttu-id="5048b-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5048b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5048b-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5048b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5048b-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5048b-134">INPUTS</span></span>

### <span data-ttu-id="5048b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5048b-135">System.String</span></span>

## <span data-ttu-id="5048b-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5048b-136">OUTPUTS</span></span>

### <span data-ttu-id="5048b-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5048b-137">System.Boolean</span></span>

## <span data-ttu-id="5048b-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5048b-138">NOTES</span></span>

## <span data-ttu-id="5048b-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5048b-139">RELATED LINKS</span></span>

[<span data-ttu-id="5048b-140">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5048b-140">New-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="5048b-141">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5048b-141">Get-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="5048b-142">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5048b-142">Update-AzureRmContainerRegistry</span></span>]()

