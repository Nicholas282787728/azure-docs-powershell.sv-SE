---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: c1ba245f83db386e39f9fecf22f95d3681452d7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757385"
---
# <span data-ttu-id="46523-101">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="46523-101">Remove-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="46523-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="46523-102">SYNOPSIS</span></span>
<span data-ttu-id="46523-103">Tar bort en behållar registrerings-webhook.</span><span class="sxs-lookup"><span data-stu-id="46523-103">Removes a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46523-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="46523-104">SYNTAX</span></span>

### <span data-ttu-id="46523-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="46523-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46523-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46523-106">WebhookObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46523-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="46523-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46523-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="46523-108">DESCRIPTION</span></span>
<span data-ttu-id="46523-109">Remove-AzureRmContainerRegistryWebhook cmdlet tar bort en behållar registrerings-webhook.</span><span class="sxs-lookup"><span data-stu-id="46523-109">The Remove-AzureRmContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="46523-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="46523-110">EXAMPLES</span></span>

### <span data-ttu-id="46523-111">Exempel 1: ta bort en behållar register-webhook.</span><span class="sxs-lookup"><span data-stu-id="46523-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="46523-112">Tar bort en behållar registrerings-webhook.</span><span class="sxs-lookup"><span data-stu-id="46523-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="46523-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="46523-113">PARAMETERS</span></span>

### <span data-ttu-id="46523-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46523-114">-DefaultProfile</span></span>
<span data-ttu-id="46523-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="46523-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46523-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="46523-116">-Name</span></span>
<span data-ttu-id="46523-117">Namn på webhook.</span><span class="sxs-lookup"><span data-stu-id="46523-117">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46523-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46523-118">-PassThru</span></span>
<span data-ttu-id="46523-119">Anger att denna cmdlet returnerar sant om borttagningen lyckades.</span><span class="sxs-lookup"><span data-stu-id="46523-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="46523-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="46523-120">-RegistryName</span></span>
<span data-ttu-id="46523-121">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="46523-121">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46523-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46523-122">-ResourceGroupName</span></span>
<span data-ttu-id="46523-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="46523-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46523-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46523-124">-ResourceId</span></span>
<span data-ttu-id="46523-125">Resurs-ID för behållar registret webhook</span><span class="sxs-lookup"><span data-stu-id="46523-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="46523-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="46523-126">-Webhook</span></span>
<span data-ttu-id="46523-127">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="46523-127">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook
Parameter Sets: WebhookObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46523-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="46523-128">-Confirm</span></span>
<span data-ttu-id="46523-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="46523-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46523-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46523-130">-WhatIf</span></span>
<span data-ttu-id="46523-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="46523-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46523-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="46523-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46523-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46523-133">CommonParameters</span></span>
<span data-ttu-id="46523-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46523-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46523-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46523-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46523-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="46523-136">INPUTS</span></span>

### <span data-ttu-id="46523-137">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="46523-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="46523-138">Parametrar: webhook (ByValue)</span><span class="sxs-lookup"><span data-stu-id="46523-138">Parameters: Webhook (ByValue)</span></span>

### <span data-ttu-id="46523-139">System. String</span><span class="sxs-lookup"><span data-stu-id="46523-139">System.String</span></span>

## <span data-ttu-id="46523-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="46523-140">OUTPUTS</span></span>

### <span data-ttu-id="46523-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="46523-141">System.Boolean</span></span>

## <span data-ttu-id="46523-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="46523-142">NOTES</span></span>

## <span data-ttu-id="46523-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="46523-143">RELATED LINKS</span></span>

[<span data-ttu-id="46523-144">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="46523-144">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="46523-145">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="46523-145">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="46523-146">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="46523-146">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="46523-147">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="46523-147">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
