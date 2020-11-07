---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
ms.openlocfilehash: 1c96b33fd93082c33dfb49abdf23fac8795b2b28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754407"
---
# <span data-ttu-id="d0664-101">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d0664-101">Remove-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="d0664-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0664-102">SYNOPSIS</span></span>
<span data-ttu-id="d0664-103">Tar bort en behållar registrerings-webhook.</span><span class="sxs-lookup"><span data-stu-id="d0664-103">Removes a container registry webhook.</span></span>

## <span data-ttu-id="d0664-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0664-104">SYNTAX</span></span>

### <span data-ttu-id="d0664-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d0664-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0664-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0664-106">WebhookObjectParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0664-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0664-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0664-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0664-108">DESCRIPTION</span></span>
<span data-ttu-id="d0664-109">Remove-AzContainerRegistryWebhook cmdlet tar bort en behållar registrerings-webhook.</span><span class="sxs-lookup"><span data-stu-id="d0664-109">The Remove-AzContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="d0664-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0664-110">EXAMPLES</span></span>

### <span data-ttu-id="d0664-111">Exempel 1: ta bort en behållar register-webhook.</span><span class="sxs-lookup"><span data-stu-id="d0664-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="d0664-112">Tar bort en behållar registrerings-webhook.</span><span class="sxs-lookup"><span data-stu-id="d0664-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="d0664-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0664-113">PARAMETERS</span></span>

### <span data-ttu-id="d0664-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0664-114">-DefaultProfile</span></span>
<span data-ttu-id="d0664-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d0664-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0664-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="d0664-116">-Name</span></span>
<span data-ttu-id="d0664-117">Namn på webhook.</span><span class="sxs-lookup"><span data-stu-id="d0664-117">Webhook Name.</span></span>

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

### <span data-ttu-id="d0664-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0664-118">-PassThru</span></span>
<span data-ttu-id="d0664-119">Anger att denna cmdlet returnerar sant om borttagningen lyckades.</span><span class="sxs-lookup"><span data-stu-id="d0664-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="d0664-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="d0664-120">-RegistryName</span></span>
<span data-ttu-id="d0664-121">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="d0664-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="d0664-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0664-122">-ResourceGroupName</span></span>
<span data-ttu-id="d0664-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="d0664-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="d0664-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0664-124">-ResourceId</span></span>
<span data-ttu-id="d0664-125">Resurs-ID för behållar registret webhook</span><span class="sxs-lookup"><span data-stu-id="d0664-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="d0664-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="d0664-126">-Webhook</span></span>
<span data-ttu-id="d0664-127">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="d0664-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="d0664-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d0664-128">-Confirm</span></span>
<span data-ttu-id="d0664-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d0664-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0664-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0664-130">-WhatIf</span></span>
<span data-ttu-id="d0664-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d0664-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0664-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d0664-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0664-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0664-133">CommonParameters</span></span>
<span data-ttu-id="d0664-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0664-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0664-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0664-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0664-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0664-136">INPUTS</span></span>

### <span data-ttu-id="d0664-137">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d0664-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="d0664-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d0664-138">System.String</span></span>

## <span data-ttu-id="d0664-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0664-139">OUTPUTS</span></span>

### <span data-ttu-id="d0664-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d0664-140">System.Boolean</span></span>

## <span data-ttu-id="d0664-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0664-141">NOTES</span></span>

## <span data-ttu-id="d0664-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0664-142">RELATED LINKS</span></span>

[<span data-ttu-id="d0664-143">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d0664-143">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="d0664-144">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d0664-144">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="d0664-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d0664-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="d0664-146">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d0664-146">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)