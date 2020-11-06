---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 2584630c8c1d0981f354ffc920af4f8ed9ff979f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575500"
---
# <span data-ttu-id="485fd-101">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="485fd-101">Get-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="485fd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="485fd-102">SYNOPSIS</span></span>
<span data-ttu-id="485fd-103">Hämtar en beskrivning för det angivna Service Bus-namnområdet i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="485fd-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="485fd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="485fd-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="485fd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="485fd-105">DESCRIPTION</span></span>
<span data-ttu-id="485fd-106">Cmdleten **Get-AzureRmServiceBusNamespace** hämtar en beskrivning för det angivna tjänst bussens namnrymds namn i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="485fd-106">The **Get-AzureRmServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="485fd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="485fd-107">EXAMPLES</span></span>

### <span data-ttu-id="485fd-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="485fd-108">Example 1</span></span>

```
PS C:\> Get-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 1 , Tier : Standard
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 1:40:01 AM
UpdatedAt          : 1/20/2017 1:40:24 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/

```

## <span data-ttu-id="485fd-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="485fd-109">PARAMETERS</span></span>

### <span data-ttu-id="485fd-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="485fd-110">-DefaultProfile</span></span>
<span data-ttu-id="485fd-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="485fd-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="485fd-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="485fd-112">-Name</span></span>
<span data-ttu-id="485fd-113">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="485fd-113">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="485fd-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="485fd-114">-ResourceGroupName</span></span>
<span data-ttu-id="485fd-115">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="485fd-115">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="485fd-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="485fd-116">CommonParameters</span></span>
<span data-ttu-id="485fd-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="485fd-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="485fd-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="485fd-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="485fd-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="485fd-119">INPUTS</span></span>

### <span data-ttu-id="485fd-120">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="485fd-120">-ResourceGroup</span></span>
<span data-ttu-id="485fd-121">System. String</span><span class="sxs-lookup"><span data-stu-id="485fd-121">System.String</span></span>

### <span data-ttu-id="485fd-122">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="485fd-122">-NamespaceName</span></span>
 <span data-ttu-id="485fd-123">System. String</span><span class="sxs-lookup"><span data-stu-id="485fd-123">System.String</span></span>

## <span data-ttu-id="485fd-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="485fd-124">OUTPUTS</span></span>

### <span data-ttu-id="485fd-125">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. ServiceBus. Models. PSNamespaceAttributes, Microsoft. Azure. commands. ServiceBus, version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="485fd-125">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="485fd-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="485fd-126">NOTES</span></span>

## <span data-ttu-id="485fd-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="485fd-127">RELATED LINKS</span></span>

