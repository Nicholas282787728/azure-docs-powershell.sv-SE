---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 4f20f177b172ab9b5372de6b95d821202e991000
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575700"
---
# <span data-ttu-id="f3fb1-101">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f3fb1-101">Get-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="f3fb1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f3fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="f3fb1-103">Hämtar en container-webhook.</span><span class="sxs-lookup"><span data-stu-id="f3fb1-103">Gets a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3fb1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f3fb1-104">SYNTAX</span></span>

### <span data-ttu-id="f3fb1-105">ListWebhookByNameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f3fb1-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3fb1-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3fb1-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3fb1-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3fb1-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3fb1-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3fb1-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3fb1-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3fb1-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3fb1-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f3fb1-110">DESCRIPTION</span></span>
<span data-ttu-id="f3fb1-111">Med den Get-AzureRmContainerRegistryWebhook cmdleten hämtas en angiven webhook med behållar-registret eller alla webhookar i ett behållar register.</span><span class="sxs-lookup"><span data-stu-id="f3fb1-111">The Get-AzureRmContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="f3fb1-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f3fb1-112">EXAMPLES</span></span>

### <span data-ttu-id="f3fb1-113">Exempel 1: skaffa en angiven webhook för en behållar registrering</span><span class="sxs-lookup"><span data-stu-id="f3fb1-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="f3fb1-114">Skaffa en angiven webhook för en behållar registrering</span><span class="sxs-lookup"><span data-stu-id="f3fb1-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="f3fb1-115">Exempel 2: skaffa alla webhookar för en behållar registrering</span><span class="sxs-lookup"><span data-stu-id="f3fb1-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="f3fb1-116">Skaffa alla webhookar för en behållar registrering</span><span class="sxs-lookup"><span data-stu-id="f3fb1-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="f3fb1-117">Exempel 3: skaffa en angiven webhook för en behållar register med konfigurations information</span><span class="sxs-lookup"><span data-stu-id="f3fb1-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="f3fb1-118">Skaffa en angiven webhook för en behållar register med konfigurations information</span><span class="sxs-lookup"><span data-stu-id="f3fb1-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="f3fb1-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f3fb1-119">PARAMETERS</span></span>

### <span data-ttu-id="f3fb1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3fb1-120">-DefaultProfile</span></span>
<span data-ttu-id="f3fb1-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f3fb1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3fb1-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3fb1-122">-IncludeConfiguration</span></span>
<span data-ttu-id="f3fb1-123">Hämta konfigurations information för en webhook.</span><span class="sxs-lookup"><span data-stu-id="f3fb1-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="f3fb1-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="f3fb1-124">-Name</span></span>
<span data-ttu-id="f3fb1-125">Namn på webhook.</span><span class="sxs-lookup"><span data-stu-id="f3fb1-125">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: ShowWebhookByNameResourceGroupParameterSet, ShowWebhookByRegistryObjectParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3fb1-126">-Register</span><span class="sxs-lookup"><span data-stu-id="f3fb1-126">-Registry</span></span>
<span data-ttu-id="f3fb1-127">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="f3fb1-127">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: ShowWebhookByRegistryObjectParameterSet, ListWebhookByRegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3fb1-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="f3fb1-128">-RegistryName</span></span>
<span data-ttu-id="f3fb1-129">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="f3fb1-129">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3fb1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3fb1-130">-ResourceGroupName</span></span>
<span data-ttu-id="f3fb1-131">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="f3fb1-131">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3fb1-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3fb1-132">-ResourceId</span></span>
<span data-ttu-id="f3fb1-133">Resurs-ID för behållar registret webhook</span><span class="sxs-lookup"><span data-stu-id="f3fb1-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="f3fb1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3fb1-134">CommonParameters</span></span>
<span data-ttu-id="f3fb1-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3fb1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3fb1-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3fb1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3fb1-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f3fb1-137">INPUTS</span></span>

### <span data-ttu-id="f3fb1-138">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f3fb1-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="f3fb1-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f3fb1-139">System.String</span></span>

## <span data-ttu-id="f3fb1-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f3fb1-140">OUTPUTS</span></span>

### <span data-ttu-id="f3fb1-141">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f3fb1-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="f3fb1-142">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryWebhook, Microsoft. Azure. commands. ContainerRegistry, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f3fb1-142">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook, Microsoft.Azure.Commands.ContainerRegistry, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f3fb1-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f3fb1-143">NOTES</span></span>

## <span data-ttu-id="f3fb1-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f3fb1-144">RELATED LINKS</span></span>

[<span data-ttu-id="f3fb1-145">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f3fb1-145">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="f3fb1-146">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f3fb1-146">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="f3fb1-147">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f3fb1-147">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="f3fb1-148">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f3fb1-148">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
