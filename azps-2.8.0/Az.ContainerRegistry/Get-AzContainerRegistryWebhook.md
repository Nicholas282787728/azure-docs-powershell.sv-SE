---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
ms.openlocfilehash: b01b2e8152d74fda5faff36221ffa9b6e75ffcbb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744857"
---
# <span data-ttu-id="849b4-101">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="849b4-101">Get-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="849b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="849b4-102">SYNOPSIS</span></span>
<span data-ttu-id="849b4-103">Hämtar en container-webhook.</span><span class="sxs-lookup"><span data-stu-id="849b4-103">Gets a container registry webhook.</span></span>

## <span data-ttu-id="849b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="849b4-104">SYNTAX</span></span>

### <span data-ttu-id="849b4-105">ListWebhookByNameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="849b4-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="849b4-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="849b4-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="849b4-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="849b4-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="849b4-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="849b4-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="849b4-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="849b4-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="849b4-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="849b4-110">DESCRIPTION</span></span>
<span data-ttu-id="849b4-111">Med den Get-AzContainerRegistryWebhook cmdleten hämtas en angiven webhook med behållar-registret eller alla webhookar i ett behållar register.</span><span class="sxs-lookup"><span data-stu-id="849b4-111">The Get-AzContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="849b4-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="849b4-112">EXAMPLES</span></span>

### <span data-ttu-id="849b4-113">Exempel 1: skaffa en angiven webhook för en behållar registrering</span><span class="sxs-lookup"><span data-stu-id="849b4-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="849b4-114">Skaffa en angiven webhook för en behållar registrering</span><span class="sxs-lookup"><span data-stu-id="849b4-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="849b4-115">Exempel 2: skaffa alla webhookar för en behållar registrering</span><span class="sxs-lookup"><span data-stu-id="849b4-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="849b4-116">Skaffa alla webhookar för en behållar registrering</span><span class="sxs-lookup"><span data-stu-id="849b4-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="849b4-117">Exempel 3: skaffa en angiven webhook för en behållar register med konfigurations information</span><span class="sxs-lookup"><span data-stu-id="849b4-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="849b4-118">Skaffa en angiven webhook för en behållar register med konfigurations information</span><span class="sxs-lookup"><span data-stu-id="849b4-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="849b4-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="849b4-119">PARAMETERS</span></span>

### <span data-ttu-id="849b4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="849b4-120">-DefaultProfile</span></span>
<span data-ttu-id="849b4-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="849b4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="849b4-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="849b4-122">-IncludeConfiguration</span></span>
<span data-ttu-id="849b4-123">Hämta konfigurations information för en webhook.</span><span class="sxs-lookup"><span data-stu-id="849b4-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="849b4-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="849b4-124">-Name</span></span>
<span data-ttu-id="849b4-125">Namn på webhook.</span><span class="sxs-lookup"><span data-stu-id="849b4-125">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShowWebhookByNameResourceGroupParameterSet, ShowWebhookByRegistryObjectParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="849b4-126">-Register</span><span class="sxs-lookup"><span data-stu-id="849b4-126">-Registry</span></span>
<span data-ttu-id="849b4-127">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="849b4-127">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: ShowWebhookByRegistryObjectParameterSet, ListWebhookByRegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="849b4-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="849b4-128">-RegistryName</span></span>
<span data-ttu-id="849b4-129">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="849b4-129">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="849b4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="849b4-130">-ResourceGroupName</span></span>
<span data-ttu-id="849b4-131">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="849b4-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="849b4-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="849b4-132">-ResourceId</span></span>
<span data-ttu-id="849b4-133">Resurs-ID för behållar registret webhook</span><span class="sxs-lookup"><span data-stu-id="849b4-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="849b4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="849b4-134">CommonParameters</span></span>
<span data-ttu-id="849b4-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="849b4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="849b4-136">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="849b4-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="849b4-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="849b4-137">INPUTS</span></span>

### <span data-ttu-id="849b4-138">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="849b4-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="849b4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="849b4-139">System.String</span></span>

## <span data-ttu-id="849b4-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="849b4-140">OUTPUTS</span></span>

### <span data-ttu-id="849b4-141">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="849b4-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="849b4-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="849b4-142">NOTES</span></span>

## <span data-ttu-id="849b4-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="849b4-143">RELATED LINKS</span></span>

[<span data-ttu-id="849b4-144">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="849b4-144">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="849b4-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="849b4-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="849b4-146">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="849b4-146">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="849b4-147">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="849b4-147">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)