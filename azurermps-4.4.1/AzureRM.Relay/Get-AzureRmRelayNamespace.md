---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
ms.openlocfilehash: 5f1e8037e4a9faef508c2ffd62ff00aca4387cb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575876"
---
# <span data-ttu-id="5ed56-101">Get-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="5ed56-101">Get-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="5ed56-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ed56-102">SYNOPSIS</span></span>
<span data-ttu-id="5ed56-103">Hämtar en beskrivning för det angivna relä namn området i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5ed56-103">Gets a description for the specified Relay namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ed56-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ed56-104">SYNTAX</span></span>

```
Get-AzureRmRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ed56-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ed56-105">DESCRIPTION</span></span>
<span data-ttu-id="5ed56-106">Cmdleten **Get-AzureRmRelayNamespace** hämtar en beskrivning för det angivna relä namn området i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5ed56-106">The **Get-AzureRmRelayNamespace** cmdlet gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="5ed56-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ed56-107">EXAMPLES</span></span>

### <span data-ttu-id="5ed56-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5ed56-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="5ed56-109">Returnerar en beskrivning av det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="5ed56-109">Returns a description of the specified Relay namespace.</span></span>

## <span data-ttu-id="5ed56-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ed56-110">PARAMETERS</span></span>

### <span data-ttu-id="5ed56-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="5ed56-111">-Name</span></span>
<span data-ttu-id="5ed56-112">Namn på relä området.</span><span class="sxs-lookup"><span data-stu-id="5ed56-112">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ed56-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ed56-113">-ResourceGroupName</span></span>
<span data-ttu-id="5ed56-114">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="5ed56-114">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ed56-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ed56-115">-DefaultProfile</span></span>
<span data-ttu-id="5ed56-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5ed56-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ed56-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ed56-117">CommonParameters</span></span>
<span data-ttu-id="5ed56-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ed56-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ed56-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ed56-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ed56-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ed56-120">INPUTS</span></span>

### <span data-ttu-id="5ed56-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ed56-121">-ResourceGroupName</span></span>
<span data-ttu-id="5ed56-122">System. String</span><span class="sxs-lookup"><span data-stu-id="5ed56-122">System.String</span></span>

### <span data-ttu-id="5ed56-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="5ed56-123">-Name</span></span>
 <span data-ttu-id="5ed56-124">System. String</span><span class="sxs-lookup"><span data-stu-id="5ed56-124">System.String</span></span>

## <span data-ttu-id="5ed56-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ed56-125">OUTPUTS</span></span>

### <span data-ttu-id="5ed56-126">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Relay. Models. RelayNamespaceAttributes, Microsoft. Azure. commands. Relay, version = 0.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5ed56-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="5ed56-127">ProvisioningState: lyckades CreatedAt: 4/12/2017 12:38:47 AM UpdatedAt: 4/12/2017 12:39:10 AM ServiceBusEndpoint: https://TestNameSpace-Relay1.servicebus.windows.net:443/ MetricId: 854d368f-1828-428F-8f3c-f2affa9b2f7d: testnamespace-Relay1 plats: väst amerikanska Taggar: {[tag1, Tag1Value]} ID:/Subscriptions/854d368f-1828-428F-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1 namn: TestNameSpace-Relay1 typ: Microsoft. Relay/Namespaces</span><span class="sxs-lookup"><span data-stu-id="5ed56-127">ProvisioningState  : Succeeded CreatedAt          : 4/12/2017 12:38:47 AM UpdatedAt          : 4/12/2017 12:39:10 AM ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/ MetricId           : 854d368f-1828-428f-8f3c-f2affa9b2f7d:testnamespace-relay1 Location           : West US Tags               : {[tag1, Tag1Value]} Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1 Name               : TestNameSpace-Relay1 Type               : Microsoft.Relay/namespaces</span></span>

## <span data-ttu-id="5ed56-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ed56-128">NOTES</span></span>

## <span data-ttu-id="5ed56-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ed56-129">RELATED LINKS</span></span>

