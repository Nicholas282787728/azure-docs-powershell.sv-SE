---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
ms.openlocfilehash: 2343b58891109d829a37131dff084b2b51e7f8ad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321740"
---
# <span data-ttu-id="94ca8-101">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="94ca8-101">Update-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="94ca8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="94ca8-102">SYNOPSIS</span></span>
<span data-ttu-id="94ca8-103">Uppdaterar en behållar registrerings-webhook.</span><span class="sxs-lookup"><span data-stu-id="94ca8-103">Updates a container registry webhook.</span></span>

## <span data-ttu-id="94ca8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="94ca8-104">SYNTAX</span></span>

### <span data-ttu-id="94ca8-105">ResourceIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="94ca8-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>]
 [-Status <String>] [-Scope <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94ca8-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="94ca8-106">NameResourceGroupParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94ca8-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94ca8-107">WebhookObjectParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94ca8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="94ca8-108">DESCRIPTION</span></span>
<span data-ttu-id="94ca8-109">Update-AzContainerRegistryWebhook cmdlet uppdaterar en behållar registrerings-webhook.</span><span class="sxs-lookup"><span data-stu-id="94ca8-109">The Update-AzContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="94ca8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="94ca8-110">EXAMPLES</span></span>

### <span data-ttu-id="94ca8-111">Exempel 1: uppdatera en befintlig webhook för behållar registret.</span><span class="sxs-lookup"><span data-stu-id="94ca8-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="94ca8-112">Uppdatera en befintlig webhook för behållar registret.</span><span class="sxs-lookup"><span data-stu-id="94ca8-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="94ca8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="94ca8-113">PARAMETERS</span></span>

### <span data-ttu-id="94ca8-114">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="94ca8-114">-Action</span></span>
<span data-ttu-id="94ca8-115">Blankstegsavgränsad lista med åtgärder som utlöser webhooken för att publicera meddelanden.</span><span class="sxs-lookup"><span data-stu-id="94ca8-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ca8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94ca8-116">-DefaultProfile</span></span>
<span data-ttu-id="94ca8-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="94ca8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94ca8-118">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="94ca8-118">-Header</span></span>
<span data-ttu-id="94ca8-119">Separerade blankstegsavgränsad anpassade rubriker i ' Key \[ = Value \] '-format som läggs till i webhook-aviseringarna.</span><span class="sxs-lookup"><span data-stu-id="94ca8-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="94ca8-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="94ca8-120">-Name</span></span>
<span data-ttu-id="94ca8-121">Namn på webhook.</span><span class="sxs-lookup"><span data-stu-id="94ca8-121">Webhook Name.</span></span>

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

### <span data-ttu-id="94ca8-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="94ca8-122">-RegistryName</span></span>
<span data-ttu-id="94ca8-123">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="94ca8-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="94ca8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94ca8-124">-ResourceGroupName</span></span>
<span data-ttu-id="94ca8-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="94ca8-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="94ca8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94ca8-126">-ResourceId</span></span>
<span data-ttu-id="94ca8-127">Resurs-ID för behållar registret webhook</span><span class="sxs-lookup"><span data-stu-id="94ca8-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="94ca8-128">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="94ca8-128">-Scope</span></span>
<span data-ttu-id="94ca8-129">Webhook-scope.</span><span class="sxs-lookup"><span data-stu-id="94ca8-129">Webhook scope.</span></span>

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

### <span data-ttu-id="94ca8-130">-Status</span><span class="sxs-lookup"><span data-stu-id="94ca8-130">-Status</span></span>
<span data-ttu-id="94ca8-131">Webhook-status</span><span class="sxs-lookup"><span data-stu-id="94ca8-131">Webhook status</span></span>

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

### <span data-ttu-id="94ca8-132">-Tagg</span><span class="sxs-lookup"><span data-stu-id="94ca8-132">-Tag</span></span>
<span data-ttu-id="94ca8-133">Blank steg avgränsade med "Key \[ = Value \] "-format.</span><span class="sxs-lookup"><span data-stu-id="94ca8-133">Space separated tags in 'key\[=value\]' format.</span></span>

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

### <span data-ttu-id="94ca8-134">-URI</span><span class="sxs-lookup"><span data-stu-id="94ca8-134">-Uri</span></span>
<span data-ttu-id="94ca8-135">Tjänste-URI för webhooken för att publicera meddelanden.</span><span class="sxs-lookup"><span data-stu-id="94ca8-135">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ca8-136">-Webhook</span><span class="sxs-lookup"><span data-stu-id="94ca8-136">-Webhook</span></span>
<span data-ttu-id="94ca8-137">Webhook-objekt för container-registret.</span><span class="sxs-lookup"><span data-stu-id="94ca8-137">Container Registry Webhook Object.</span></span>

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

### <span data-ttu-id="94ca8-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="94ca8-138">-Confirm</span></span>
<span data-ttu-id="94ca8-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="94ca8-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94ca8-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94ca8-140">-WhatIf</span></span>
<span data-ttu-id="94ca8-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="94ca8-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94ca8-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="94ca8-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94ca8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94ca8-143">CommonParameters</span></span>
<span data-ttu-id="94ca8-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94ca8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94ca8-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94ca8-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94ca8-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="94ca8-146">INPUTS</span></span>

### <span data-ttu-id="94ca8-147">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="94ca8-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="94ca8-148">System. String</span><span class="sxs-lookup"><span data-stu-id="94ca8-148">System.String</span></span>

## <span data-ttu-id="94ca8-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="94ca8-149">OUTPUTS</span></span>

### <span data-ttu-id="94ca8-150">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="94ca8-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="94ca8-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="94ca8-151">NOTES</span></span>

## <span data-ttu-id="94ca8-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="94ca8-152">RELATED LINKS</span></span>

[<span data-ttu-id="94ca8-153">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="94ca8-153">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="94ca8-154">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="94ca8-154">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="94ca8-155">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="94ca8-155">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)

[<span data-ttu-id="94ca8-156">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="94ca8-156">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)