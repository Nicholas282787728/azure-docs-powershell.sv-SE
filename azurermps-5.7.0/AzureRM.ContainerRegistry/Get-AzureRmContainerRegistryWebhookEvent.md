---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhookEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhookEvent.md
ms.openlocfilehash: 68a0bd0c2e076cbd2e96fdbe06def979937ed714
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755612"
---
# <span data-ttu-id="4e423-101">Get-AzureRmContainerRegistryWebhookEvent</span><span class="sxs-lookup"><span data-stu-id="4e423-101">Get-AzureRmContainerRegistryWebhookEvent</span></span>

## <span data-ttu-id="4e423-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4e423-102">SYNOPSIS</span></span>
<span data-ttu-id="4e423-103">Hämtar händelser för en behållar registrerings-webhook.</span><span class="sxs-lookup"><span data-stu-id="4e423-103">Gets events of a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e423-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4e423-104">SYNTAX</span></span>

### <span data-ttu-id="4e423-105">ListWebhookEventsByNameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4e423-105">ListWebhookEventsByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryWebhookEvent -WebhookName <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e423-106">ListWebhookEventsByWebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e423-106">ListWebhookEventsByWebhookObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhookEvent -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e423-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e423-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhookEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e423-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4e423-108">DESCRIPTION</span></span>
<span data-ttu-id="4e423-109">I Get-AzureRmContainerRegistryWebhookEvent cmdlet visas alla händelser för en webhook.</span><span class="sxs-lookup"><span data-stu-id="4e423-109">The Get-AzureRmContainerRegistryWebhookEvent cmdlet lists all the events of a webhook.</span></span>

## <span data-ttu-id="4e423-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4e423-110">EXAMPLES</span></span>

### <span data-ttu-id="4e423-111">Exempel 1: hämtar alla händelser för en webhook.</span><span class="sxs-lookup"><span data-stu-id="4e423-111">Example 1: Gets all the events of a webhook.</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhookEvent -ResourceGroupName mattacrtest001 -RegistryName premium001 -Name webhook001

   Webhook service Uri: http://www.bing.com/

ID                                       Action   Timestamp                      Response
                                                                                 StatusCode
--                                       ------   ---------                      ----------
3c6281b6-47cd-4129-948b-4036780236f0     ping     11/17/2017 5:10:09 PM          200
70f1d41d-15fe-4251-87b6-43c32a91eae7     ping     11/17/2017 6:56:23 AM          200
5d25556b-32d0-4377-8031-d8ba7a263d6a     ping     11/17/2017 6:27:41 AM          200
c1e7d8aa-9f1b-447c-9583-2a58b7f81026     ping     11/17/2017 12:09:41 AM         200
eb4aa503-0d14-4f25-8ae5-33cce9a8fd50     ping     11/16/2017 11:35:03 PM         200
85a93d7f-3923-4ec5-bb8e-9ded5b6549c1     ping     11/17/2017 5:10:09 PM          200
9e3c8b5f-e0ee-47cf-9727-df1c8d45a497     ping     11/17/2017 6:56:23 AM          200
2d0ce294-9b59-4f5c-953a-47f2b270526f     ping     11/17/2017 6:27:41 AM          200
```

<span data-ttu-id="4e423-112">Hämtar alla händelser för en webhook.</span><span class="sxs-lookup"><span data-stu-id="4e423-112">Gets all the events of a webhook.</span></span>

## <span data-ttu-id="4e423-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4e423-113">PARAMETERS</span></span>

### <span data-ttu-id="4e423-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e423-114">-DefaultProfile</span></span>
<span data-ttu-id="4e423-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4e423-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e423-116">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="4e423-116">-RegistryName</span></span>
<span data-ttu-id="4e423-117">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="4e423-117">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: ListWebhookEventsByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e423-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e423-118">-ResourceGroupName</span></span>
<span data-ttu-id="4e423-119">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="4e423-119">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListWebhookEventsByNameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e423-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e423-120">-ResourceId</span></span>
<span data-ttu-id="4e423-121">Resurs-ID för behållar registret webhook</span><span class="sxs-lookup"><span data-stu-id="4e423-121">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="4e423-122">-Webhook</span><span class="sxs-lookup"><span data-stu-id="4e423-122">-Webhook</span></span>
<span data-ttu-id="4e423-123">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="4e423-123">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistryWebhook
Parameter Sets: ListWebhookEventsByWebhookObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e423-124">-WebhookName</span><span class="sxs-lookup"><span data-stu-id="4e423-124">-WebhookName</span></span>
<span data-ttu-id="4e423-125">Namn på webhook.</span><span class="sxs-lookup"><span data-stu-id="4e423-125">Webhook Name.</span></span>
```yaml
Type: String
Parameter Sets: ListWebhookEventsByNameResourceGroupParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e423-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e423-126">CommonParameters</span></span>
<span data-ttu-id="4e423-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e423-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e423-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e423-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e423-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4e423-129">INPUTS</span></span>

### <span data-ttu-id="4e423-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4e423-130">System.String</span></span>

## <span data-ttu-id="4e423-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4e423-131">OUTPUTS</span></span>

### <span data-ttu-id="4e423-132">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryWebhookEvent, Microsoft. Azure. commands. ContainerRegistry, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4e423-132">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhookEvent, Microsoft.Azure.Commands.ContainerRegistry, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4e423-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4e423-133">NOTES</span></span>

## <span data-ttu-id="4e423-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4e423-134">RELATED LINKS</span></span>

[<span data-ttu-id="4e423-135">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4e423-135">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="4e423-136">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4e423-136">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="4e423-137">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4e423-137">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="4e423-138">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4e423-138">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="4e423-139">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4e423-139">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)

