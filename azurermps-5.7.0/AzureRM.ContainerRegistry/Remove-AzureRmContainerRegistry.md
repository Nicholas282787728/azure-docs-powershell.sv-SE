---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: df0c938db8f44ebffedc9760e4a3d33ee175ae01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578244"
---
# <span data-ttu-id="12915-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="12915-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="12915-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12915-102">SYNOPSIS</span></span>
<span data-ttu-id="12915-103">Tar bort en behållar register.</span><span class="sxs-lookup"><span data-stu-id="12915-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12915-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12915-104">SYNTAX</span></span>

### <span data-ttu-id="12915-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="12915-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12915-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12915-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12915-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="12915-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12915-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12915-108">DESCRIPTION</span></span>
<span data-ttu-id="12915-109">Remove-AzureRmContainerRegistry cmdlet tar bort en behållar register.</span><span class="sxs-lookup"><span data-stu-id="12915-109">The Remove-AzureRmContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="12915-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12915-110">EXAMPLES</span></span>

### <span data-ttu-id="12915-111">Exempel 1: ta bort ett angivet behållar register</span><span class="sxs-lookup"><span data-stu-id="12915-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="12915-112">Det här kommandot tar bort den angivna behållar registret.</span><span class="sxs-lookup"><span data-stu-id="12915-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="12915-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12915-113">PARAMETERS</span></span>

### <span data-ttu-id="12915-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="12915-114">-Name</span></span>
<span data-ttu-id="12915-115">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="12915-115">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12915-116">-Register</span><span class="sxs-lookup"><span data-stu-id="12915-116">-Registry</span></span>
<span data-ttu-id="12915-117">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="12915-117">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12915-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12915-118">-ResourceGroupName</span></span>
<span data-ttu-id="12915-119">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="12915-119">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12915-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="12915-120">-Confirm</span></span>
<span data-ttu-id="12915-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="12915-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12915-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12915-122">-WhatIf</span></span>
<span data-ttu-id="12915-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="12915-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12915-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="12915-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12915-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12915-125">-DefaultProfile</span></span>
<span data-ttu-id="12915-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="12915-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12915-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12915-127">-ResourceId</span></span>
<span data-ttu-id="12915-128">Resurs-ID för behållar registret</span><span class="sxs-lookup"><span data-stu-id="12915-128">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12915-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12915-129">-PassThru</span></span>
<span data-ttu-id="12915-130">Anger att denna cmdlet returnerar sant om borttagningen lyckades.</span><span class="sxs-lookup"><span data-stu-id="12915-130">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="12915-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12915-131">CommonParameters</span></span>
<span data-ttu-id="12915-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12915-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12915-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12915-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12915-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12915-134">INPUTS</span></span>

### <span data-ttu-id="12915-135">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="12915-135">PSContainerRegistry</span></span>
<span data-ttu-id="12915-136">Parametern ' Registry ' godkänner värdet av typen ' PSContainerRegistry ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="12915-136">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="12915-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12915-137">OUTPUTS</span></span>

### <span data-ttu-id="12915-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="12915-138">None</span></span>

## <span data-ttu-id="12915-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12915-139">NOTES</span></span>

## <span data-ttu-id="12915-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12915-140">RELATED LINKS</span></span>

[<span data-ttu-id="12915-141">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="12915-141">New-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="12915-142">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="12915-142">Get-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="12915-143">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="12915-143">Update-AzureRmContainerRegistry</span></span>]()

