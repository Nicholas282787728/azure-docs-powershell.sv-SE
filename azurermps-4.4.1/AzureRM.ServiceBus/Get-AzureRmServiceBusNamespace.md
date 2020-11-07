---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 2e6e044d888386b56d04ad48b7fbdaedadbd7497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755424"
---
# <span data-ttu-id="26934-101">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="26934-101">Get-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="26934-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="26934-102">SYNOPSIS</span></span>
<span data-ttu-id="26934-103">Hämtar en beskrivning för det angivna Service Bus-namnområdet i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="26934-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26934-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="26934-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26934-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="26934-105">DESCRIPTION</span></span>
<span data-ttu-id="26934-106">Cmdleten **Get-AzureRmServiceBusNamespace** hämtar en beskrivning för det angivna tjänst bussens namnrymds namn i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="26934-106">The **Get-AzureRmServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="26934-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="26934-107">EXAMPLES</span></span>

### <span data-ttu-id="26934-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="26934-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="26934-109">Returnerar en beskrivning av det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="26934-109">Returns a description of the specified Service Bus namespace.</span></span>

## <span data-ttu-id="26934-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="26934-110">PARAMETERS</span></span>

### <span data-ttu-id="26934-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26934-111">-DefaultProfile</span></span>
<span data-ttu-id="26934-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="26934-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26934-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="26934-113">-Name</span></span>
<span data-ttu-id="26934-114">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="26934-114">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26934-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26934-115">-ResourceGroupName</span></span>
<span data-ttu-id="26934-116">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="26934-116">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26934-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26934-117">CommonParameters</span></span>
<span data-ttu-id="26934-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26934-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26934-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26934-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26934-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="26934-120">INPUTS</span></span>

### <span data-ttu-id="26934-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="26934-121">-ResourceGroup</span></span>
<span data-ttu-id="26934-122">System. String</span><span class="sxs-lookup"><span data-stu-id="26934-122">System.String</span></span>

### <span data-ttu-id="26934-123">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="26934-123">-NamespaceName</span></span>
 <span data-ttu-id="26934-124">System. String</span><span class="sxs-lookup"><span data-stu-id="26934-124">System.String</span></span>

## <span data-ttu-id="26934-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="26934-125">OUTPUTS</span></span>

### <span data-ttu-id="26934-126">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. ServiceBus. Models. NamespaceAttributes, Microsoft. Azure. commands. ServiceBus, version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="26934-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="26934-127">Namn: SB-Example1-ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1 plats: väst amerikansk SKU: namn: standard, kapacitet: 1, nivå: standard ProvisioningState: lyckades: Active CreatedAt: 1/20/2017 1:40:01 AM UpdatedAt: 1/20/2017 1:40:24 AM ServiceBusEndpoint: https://SB-Example1.servicebus.windows.net:443/ Enabled: true</span><span class="sxs-lookup"><span data-stu-id="26934-127">Name               : SB-Example1 Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1 Location           : West US Sku                : Name : Standard , Capacity : 1 , Tier : Standard ProvisioningState  : Succeeded Status             : Active CreatedAt          : 1/20/2017 1:40:01 AM UpdatedAt          : 1/20/2017 1:40:24 AM ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/ Enabled            : True</span></span>

## <span data-ttu-id="26934-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="26934-128">NOTES</span></span>
## <span data-ttu-id="26934-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26934-129">RELATED LINKS</span></span>

## <span data-ttu-id="26934-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26934-130">RELATED LINKS</span></span>

