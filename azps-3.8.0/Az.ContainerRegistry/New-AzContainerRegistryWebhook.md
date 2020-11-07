---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
ms.openlocfilehash: 8ea10f2acbe69e31bf80e35f0a8ea1577ffac6f5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926270"
---
# <span data-ttu-id="b00cd-101">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b00cd-101">New-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="b00cd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b00cd-102">SYNOPSIS</span></span>
<span data-ttu-id="b00cd-103">Skapar en container-webhook.</span><span class="sxs-lookup"><span data-stu-id="b00cd-103">Creates a container registry webhook.</span></span>

## <span data-ttu-id="b00cd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b00cd-104">SYNTAX</span></span>

### <span data-ttu-id="b00cd-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b00cd-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b00cd-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b00cd-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b00cd-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b00cd-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b00cd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b00cd-108">DESCRIPTION</span></span>
<span data-ttu-id="b00cd-109">New-AzContainerRegistryWebhook cmdlet skapar en behållar registrerings-webhook.</span><span class="sxs-lookup"><span data-stu-id="b00cd-109">The New-AzContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="b00cd-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b00cd-110">EXAMPLES</span></span>

### <span data-ttu-id="b00cd-111">Exempel 1: skapa en container-webhook.</span><span class="sxs-lookup"><span data-stu-id="b00cd-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="b00cd-112">Skapa en container-webhook.</span><span class="sxs-lookup"><span data-stu-id="b00cd-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="b00cd-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b00cd-113">PARAMETERS</span></span>

### <span data-ttu-id="b00cd-114">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="b00cd-114">-Action</span></span>
<span data-ttu-id="b00cd-115">Blankstegsavgränsad lista med åtgärder som utlöser webhooken för att publicera meddelanden.</span><span class="sxs-lookup"><span data-stu-id="b00cd-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00cd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b00cd-116">-DefaultProfile</span></span>
<span data-ttu-id="b00cd-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b00cd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b00cd-118">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="b00cd-118">-Header</span></span>
<span data-ttu-id="b00cd-119">Anpassade rubriker som läggs till i webhook-aviseringarna.</span><span class="sxs-lookup"><span data-stu-id="b00cd-119">Custom headers that will be added to the webhook notifications.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: WebhookHeaders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00cd-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="b00cd-120">-Location</span></span>
<span data-ttu-id="b00cd-121">Webhook-plats.</span><span class="sxs-lookup"><span data-stu-id="b00cd-121">Webhook Location.</span></span>
<span data-ttu-id="b00cd-122">Standard platsen för registret.</span><span class="sxs-lookup"><span data-stu-id="b00cd-122">Default to the location of the registry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00cd-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="b00cd-123">-Name</span></span>
<span data-ttu-id="b00cd-124">Namn på webhook.</span><span class="sxs-lookup"><span data-stu-id="b00cd-124">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00cd-125">-Register</span><span class="sxs-lookup"><span data-stu-id="b00cd-125">-Registry</span></span>
<span data-ttu-id="b00cd-126">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="b00cd-126">Container Registry Object.</span></span>

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

### <span data-ttu-id="b00cd-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="b00cd-127">-RegistryName</span></span>
<span data-ttu-id="b00cd-128">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="b00cd-128">Container Registry Name.</span></span>

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

### <span data-ttu-id="b00cd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b00cd-129">-ResourceGroupName</span></span>
<span data-ttu-id="b00cd-130">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b00cd-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="b00cd-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b00cd-131">-ResourceId</span></span>
<span data-ttu-id="b00cd-132">Resurs-ID för behållar registret</span><span class="sxs-lookup"><span data-stu-id="b00cd-132">The container registry resource id</span></span>

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

### <span data-ttu-id="b00cd-133">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="b00cd-133">-Scope</span></span>
<span data-ttu-id="b00cd-134">Webhook-scope.</span><span class="sxs-lookup"><span data-stu-id="b00cd-134">Webhook scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookScope

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00cd-135">-Status</span><span class="sxs-lookup"><span data-stu-id="b00cd-135">-Status</span></span>
<span data-ttu-id="b00cd-136">Webhook-status, standardvärde är aktiverat</span><span class="sxs-lookup"><span data-stu-id="b00cd-136">Webhook status, default value is enabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookStatus
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00cd-137">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b00cd-137">-Tag</span></span>
<span data-ttu-id="b00cd-138">Webhook-taggar.</span><span class="sxs-lookup"><span data-stu-id="b00cd-138">Webhook tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00cd-139">-URI</span><span class="sxs-lookup"><span data-stu-id="b00cd-139">-Uri</span></span>
<span data-ttu-id="b00cd-140">Tjänste-URI för webhooken för att publicera meddelanden.</span><span class="sxs-lookup"><span data-stu-id="b00cd-140">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00cd-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b00cd-141">-Confirm</span></span>
<span data-ttu-id="b00cd-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b00cd-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b00cd-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b00cd-143">-WhatIf</span></span>
<span data-ttu-id="b00cd-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b00cd-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b00cd-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b00cd-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b00cd-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b00cd-146">CommonParameters</span></span>
<span data-ttu-id="b00cd-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b00cd-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b00cd-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b00cd-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b00cd-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b00cd-149">INPUTS</span></span>

### <span data-ttu-id="b00cd-150">System. String</span><span class="sxs-lookup"><span data-stu-id="b00cd-150">System.String</span></span>

## <span data-ttu-id="b00cd-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b00cd-151">OUTPUTS</span></span>

### <span data-ttu-id="b00cd-152">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b00cd-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="b00cd-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b00cd-153">NOTES</span></span>

## <span data-ttu-id="b00cd-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b00cd-154">RELATED LINKS</span></span>

[<span data-ttu-id="b00cd-155">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b00cd-155">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="b00cd-156">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b00cd-156">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="b00cd-157">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b00cd-157">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="b00cd-158">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b00cd-158">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)