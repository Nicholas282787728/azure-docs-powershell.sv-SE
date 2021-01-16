---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
ms.openlocfilehash: 231ff710e2c8c2945947ecf2d09845e635ee6244
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409480"
---
# <span data-ttu-id="eb851-101">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="eb851-101">Get-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="eb851-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb851-102">SYNOPSIS</span></span>
<span data-ttu-id="eb851-103">Hämtar en container-webhook.</span><span class="sxs-lookup"><span data-stu-id="eb851-103">Gets a container registry webhook.</span></span>

## <span data-ttu-id="eb851-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb851-104">SYNTAX</span></span>

### <span data-ttu-id="eb851-105">ListWebhookByNameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="eb851-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb851-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb851-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb851-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb851-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb851-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb851-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb851-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb851-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb851-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb851-110">DESCRIPTION</span></span>
<span data-ttu-id="eb851-111">Med den Get-AzContainerRegistryWebhook cmdleten hämtas en angiven webhook med behållar-registret eller alla webhookar i ett behållar register.</span><span class="sxs-lookup"><span data-stu-id="eb851-111">The Get-AzContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="eb851-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb851-112">EXAMPLES</span></span>

### <span data-ttu-id="eb851-113">Exempel 1: skaffa en angiven webhook för en behållar registrering</span><span class="sxs-lookup"><span data-stu-id="eb851-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="eb851-114">Skaffa en angiven webhook för en behållar registrering</span><span class="sxs-lookup"><span data-stu-id="eb851-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="eb851-115">Exempel 2: skaffa alla webhookar för en behållar registrering</span><span class="sxs-lookup"><span data-stu-id="eb851-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="eb851-116">Skaffa alla webhookar för en behållar registrering</span><span class="sxs-lookup"><span data-stu-id="eb851-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="eb851-117">Exempel 3: skaffa en angiven webhook för en behållar register med konfigurations information</span><span class="sxs-lookup"><span data-stu-id="eb851-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="eb851-118">Skaffa en angiven webhook för en behållar register med konfigurations information</span><span class="sxs-lookup"><span data-stu-id="eb851-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="eb851-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb851-119">PARAMETERS</span></span>

### <span data-ttu-id="eb851-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb851-120">-DefaultProfile</span></span>
<span data-ttu-id="eb851-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eb851-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb851-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb851-122">-IncludeConfiguration</span></span>
<span data-ttu-id="eb851-123">Hämta konfigurations information för en webhook.</span><span class="sxs-lookup"><span data-stu-id="eb851-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="eb851-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="eb851-124">-Name</span></span>
<span data-ttu-id="eb851-125">Namn på webhook.</span><span class="sxs-lookup"><span data-stu-id="eb851-125">Webhook Name.</span></span>

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

### <span data-ttu-id="eb851-126">-Register</span><span class="sxs-lookup"><span data-stu-id="eb851-126">-Registry</span></span>
<span data-ttu-id="eb851-127">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="eb851-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="eb851-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="eb851-128">-RegistryName</span></span>
<span data-ttu-id="eb851-129">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="eb851-129">Container Registry Name.</span></span>

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

### <span data-ttu-id="eb851-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb851-130">-ResourceGroupName</span></span>
<span data-ttu-id="eb851-131">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="eb851-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="eb851-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb851-132">-ResourceId</span></span>
<span data-ttu-id="eb851-133">Resurs-ID för behållar registret webhook</span><span class="sxs-lookup"><span data-stu-id="eb851-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="eb851-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb851-134">CommonParameters</span></span>
<span data-ttu-id="eb851-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb851-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb851-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb851-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb851-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb851-137">INPUTS</span></span>

### <span data-ttu-id="eb851-138">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="eb851-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="eb851-139">System. String</span><span class="sxs-lookup"><span data-stu-id="eb851-139">System.String</span></span>

## <span data-ttu-id="eb851-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb851-140">OUTPUTS</span></span>

### <span data-ttu-id="eb851-141">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="eb851-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="eb851-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb851-142">NOTES</span></span>

## <span data-ttu-id="eb851-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb851-143">RELATED LINKS</span></span>

[<span data-ttu-id="eb851-144">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="eb851-144">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="eb851-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="eb851-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="eb851-146">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="eb851-146">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="eb851-147">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="eb851-147">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)