---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 02d16be7c41a95c32d4aa7b6f3231b68c0ba7244
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578235"
---
# <span data-ttu-id="9ad10-101">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9ad10-101">Test-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="9ad10-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9ad10-102">SYNOPSIS</span></span>
<span data-ttu-id="9ad10-103">Startar en webhook-ping-händelse.</span><span class="sxs-lookup"><span data-stu-id="9ad10-103">Triggers a webhook ping event.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ad10-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9ad10-104">SYNTAX</span></span>

### <span data-ttu-id="9ad10-105">ResourceIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9ad10-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzureRmContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ad10-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ad10-106">NameResourceGroupParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ad10-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ad10-107">WebhookObjectParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ad10-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9ad10-108">DESCRIPTION</span></span>
<span data-ttu-id="9ad10-109">Test-AzureRmContainerRegistryWebhook cmdleten utlöser en webhook-ping-händelse.</span><span class="sxs-lookup"><span data-stu-id="9ad10-109">The Test-AzureRmContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="9ad10-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9ad10-110">EXAMPLES</span></span>

### <span data-ttu-id="9ad10-111">Exempel 1: utlöser ett webhook-ping-händelse.</span><span class="sxs-lookup"><span data-stu-id="9ad10-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="9ad10-112">Startar en webhook-ping-händelse.</span><span class="sxs-lookup"><span data-stu-id="9ad10-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="9ad10-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9ad10-113">PARAMETERS</span></span>

### <span data-ttu-id="9ad10-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ad10-114">-DefaultProfile</span></span>
<span data-ttu-id="9ad10-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9ad10-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ad10-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="9ad10-116">-Name</span></span>
<span data-ttu-id="9ad10-117">Namn på webhook.</span><span class="sxs-lookup"><span data-stu-id="9ad10-117">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ad10-118">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="9ad10-118">-RegistryName</span></span>
<span data-ttu-id="9ad10-119">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="9ad10-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="9ad10-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ad10-120">-ResourceGroupName</span></span>
<span data-ttu-id="9ad10-121">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="9ad10-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="9ad10-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ad10-122">-ResourceId</span></span>
<span data-ttu-id="9ad10-123">Resurs-ID för behållar registret webhook</span><span class="sxs-lookup"><span data-stu-id="9ad10-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="9ad10-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="9ad10-124">-Webhook</span></span>
<span data-ttu-id="9ad10-125">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="9ad10-125">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistryWebhook
Parameter Sets: WebhookObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ad10-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ad10-126">CommonParameters</span></span>
<span data-ttu-id="9ad10-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ad10-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ad10-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ad10-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ad10-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9ad10-129">INPUTS</span></span>

### <span data-ttu-id="9ad10-130">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9ad10-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="9ad10-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9ad10-131">System.String</span></span>

## <span data-ttu-id="9ad10-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9ad10-132">OUTPUTS</span></span>

### <span data-ttu-id="9ad10-133">Microsoft. Azure. Management. ContainerRegistry. Models. EventInfo</span><span class="sxs-lookup"><span data-stu-id="9ad10-133">Microsoft.Azure.Management.ContainerRegistry.Models.EventInfo</span></span>

## <span data-ttu-id="9ad10-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9ad10-134">NOTES</span></span>

## <span data-ttu-id="9ad10-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9ad10-135">RELATED LINKS</span></span>

[<span data-ttu-id="9ad10-136">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9ad10-136">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="9ad10-137">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9ad10-137">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="9ad10-138">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9ad10-138">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="9ad10-139">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9ad10-139">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)
