---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: 5a5ea87044c18e82f4c17294356a35adb254eee4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574732"
---
# <span data-ttu-id="a85b8-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a85b8-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="a85b8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a85b8-102">SYNOPSIS</span></span>
<span data-ttu-id="a85b8-103">Tar bort en behållar register.</span><span class="sxs-lookup"><span data-stu-id="a85b8-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a85b8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a85b8-104">SYNTAX</span></span>

### <span data-ttu-id="a85b8-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a85b8-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a85b8-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a85b8-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a85b8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a85b8-107">DESCRIPTION</span></span>
<span data-ttu-id="a85b8-108">Cmdleten **Remove-AzureRmContainerRegistry** tar bort en behållare.</span><span class="sxs-lookup"><span data-stu-id="a85b8-108">The **Remove-AzureRmContainerRegistry** cmdlet removes a container registry.</span></span>

## <span data-ttu-id="a85b8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a85b8-109">EXAMPLES</span></span>

### <span data-ttu-id="a85b8-110">Exempel 1: ta bort ett angivet behållar register</span><span class="sxs-lookup"><span data-stu-id="a85b8-110">Example 1: Remove a specified container registry</span></span>
```
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="a85b8-111">Det här kommandot tar bort den angivna behållar registret.</span><span class="sxs-lookup"><span data-stu-id="a85b8-111">This command removes the specified container registry.</span></span>

## <span data-ttu-id="a85b8-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a85b8-112">PARAMETERS</span></span>

### <span data-ttu-id="a85b8-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="a85b8-113">-Name</span></span>
<span data-ttu-id="a85b8-114">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="a85b8-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="a85b8-115">-Register</span><span class="sxs-lookup"><span data-stu-id="a85b8-115">-Registry</span></span>
<span data-ttu-id="a85b8-116">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="a85b8-116">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a85b8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a85b8-117">-ResourceGroupName</span></span>
<span data-ttu-id="a85b8-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="a85b8-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="a85b8-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a85b8-119">-Confirm</span></span>
<span data-ttu-id="a85b8-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a85b8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a85b8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a85b8-121">-WhatIf</span></span>
<span data-ttu-id="a85b8-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a85b8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a85b8-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a85b8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a85b8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a85b8-124">-DefaultProfile</span></span>
<span data-ttu-id="a85b8-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a85b8-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a85b8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a85b8-126">CommonParameters</span></span>
<span data-ttu-id="a85b8-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a85b8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a85b8-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a85b8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a85b8-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a85b8-129">INPUTS</span></span>

### <span data-ttu-id="a85b8-130">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a85b8-130">PSContainerRegistry</span></span>
<span data-ttu-id="a85b8-131">Parametern ' Registry ' godkänner värdet av typen ' PSContainerRegistry ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a85b8-131">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="a85b8-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a85b8-132">OUTPUTS</span></span>

### <span data-ttu-id="a85b8-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="a85b8-133">None</span></span>

## <span data-ttu-id="a85b8-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a85b8-134">NOTES</span></span>

## <span data-ttu-id="a85b8-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a85b8-135">RELATED LINKS</span></span>

[<span data-ttu-id="a85b8-136">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a85b8-136">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="a85b8-137">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a85b8-137">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="a85b8-138">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a85b8-138">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

