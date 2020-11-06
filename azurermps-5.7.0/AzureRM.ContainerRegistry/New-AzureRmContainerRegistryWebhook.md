---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 0a23cfb79c341fb4fcee5b5688b0780ba178e978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578255"
---
# <span data-ttu-id="44789-101">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="44789-101">New-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="44789-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="44789-102">SYNOPSIS</span></span>
<span data-ttu-id="44789-103">Skapar en container-webhook.</span><span class="sxs-lookup"><span data-stu-id="44789-103">Creates a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44789-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="44789-104">SYNTAX</span></span>

### <span data-ttu-id="44789-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="44789-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44789-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44789-106">RegistryObjectParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44789-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="44789-107">ResourceIdParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44789-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="44789-108">DESCRIPTION</span></span>
<span data-ttu-id="44789-109">New-AzureRmContainerRegistryWebhook cmdlet skapar en behållar registrerings-webhook.</span><span class="sxs-lookup"><span data-stu-id="44789-109">The New-AzureRmContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="44789-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="44789-110">EXAMPLES</span></span>

### <span data-ttu-id="44789-111">Exempel 1: skapa en container-webhook.</span><span class="sxs-lookup"><span data-stu-id="44789-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="44789-112">Skapa en container-webhook.</span><span class="sxs-lookup"><span data-stu-id="44789-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="44789-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="44789-113">PARAMETERS</span></span>

### <span data-ttu-id="44789-114">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="44789-114">-Action</span></span>
<span data-ttu-id="44789-115">Blankstegsavgränsad lista med åtgärder som utlöser webhooken för att publicera meddelanden.</span><span class="sxs-lookup"><span data-stu-id="44789-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44789-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="44789-116">-Confirm</span></span>
<span data-ttu-id="44789-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="44789-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44789-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44789-118">-DefaultProfile</span></span>
<span data-ttu-id="44789-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="44789-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44789-120">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="44789-120">-Header</span></span>
<span data-ttu-id="44789-121">Anpassade rubriker som läggs till i webhook-aviseringarna.</span><span class="sxs-lookup"><span data-stu-id="44789-121">Custom headers that will be added to the webhook notifications.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: WebhookHeaders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44789-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="44789-122">-Location</span></span>
<span data-ttu-id="44789-123">Webhook-plats.</span><span class="sxs-lookup"><span data-stu-id="44789-123">Webhook Location.</span></span>
<span data-ttu-id="44789-124">Standard platsen för registret.</span><span class="sxs-lookup"><span data-stu-id="44789-124">Default to the location of the registry.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44789-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="44789-125">-Name</span></span>
<span data-ttu-id="44789-126">Namn på webhook.</span><span class="sxs-lookup"><span data-stu-id="44789-126">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44789-127">-Register</span><span class="sxs-lookup"><span data-stu-id="44789-127">-Registry</span></span>
<span data-ttu-id="44789-128">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="44789-128">Container Registry Object.</span></span>

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

### <span data-ttu-id="44789-129">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="44789-129">-RegistryName</span></span>
<span data-ttu-id="44789-130">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="44789-130">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44789-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44789-131">-ResourceGroupName</span></span>
<span data-ttu-id="44789-132">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="44789-132">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44789-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44789-133">-ResourceId</span></span>
<span data-ttu-id="44789-134">Resurs-ID för behållar registret</span><span class="sxs-lookup"><span data-stu-id="44789-134">The container registry resource id</span></span>

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

### <span data-ttu-id="44789-135">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="44789-135">-Scope</span></span>
<span data-ttu-id="44789-136">Webhook-scope.</span><span class="sxs-lookup"><span data-stu-id="44789-136">Webhook scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookScope

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44789-137">-Status</span><span class="sxs-lookup"><span data-stu-id="44789-137">-Status</span></span>
<span data-ttu-id="44789-138">Webhook-status, standardvärde är aktiverat</span><span class="sxs-lookup"><span data-stu-id="44789-138">Webhook status, default value is enabled</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookStatus
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44789-139">-Tagg</span><span class="sxs-lookup"><span data-stu-id="44789-139">-Tag</span></span>
<span data-ttu-id="44789-140">Webhook-taggar.</span><span class="sxs-lookup"><span data-stu-id="44789-140">Webhook tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44789-141">-URI</span><span class="sxs-lookup"><span data-stu-id="44789-141">-Uri</span></span>
<span data-ttu-id="44789-142">Tjänste-URI för webhooken för att publicera meddelanden.</span><span class="sxs-lookup"><span data-stu-id="44789-142">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44789-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44789-143">-WhatIf</span></span>
<span data-ttu-id="44789-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="44789-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44789-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="44789-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44789-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44789-146">CommonParameters</span></span>
<span data-ttu-id="44789-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44789-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44789-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44789-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44789-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="44789-149">INPUTS</span></span>

### <span data-ttu-id="44789-150">System. String</span><span class="sxs-lookup"><span data-stu-id="44789-150">System.String</span></span>

## <span data-ttu-id="44789-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="44789-151">OUTPUTS</span></span>

### <span data-ttu-id="44789-152">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="44789-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="44789-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="44789-153">NOTES</span></span>

## <span data-ttu-id="44789-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="44789-154">RELATED LINKS</span></span>

[<span data-ttu-id="44789-155">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="44789-155">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="44789-156">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="44789-156">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="44789-157">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="44789-157">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="44789-158">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="44789-158">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
