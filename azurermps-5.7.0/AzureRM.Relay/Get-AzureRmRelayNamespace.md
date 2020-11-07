---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
ms.openlocfilehash: fe0991296ad5f2dc8be89c92117e74c4231b495c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757241"
---
# <span data-ttu-id="58053-101">Get-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="58053-101">Get-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="58053-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="58053-102">SYNOPSIS</span></span>
<span data-ttu-id="58053-103">Hämtar en beskrivning för det angivna relä namn området i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="58053-103">Gets a description for the specified Relay namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58053-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="58053-104">SYNTAX</span></span>

```
Get-AzureRmRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58053-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="58053-105">DESCRIPTION</span></span>
<span data-ttu-id="58053-106">Cmdleten **Get-AzureRmRelayNamespace** hämtar en beskrivning för det angivna relä namn området i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="58053-106">The **Get-AzureRmRelayNamespace** cmdlet gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="58053-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="58053-107">EXAMPLES</span></span>

### <span data-ttu-id="58053-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="58053-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="58053-109">Returnerar en beskrivning av det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="58053-109">Returns a description of the specified Relay namespace.</span></span>

## <span data-ttu-id="58053-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="58053-110">PARAMETERS</span></span>

### <span data-ttu-id="58053-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58053-111">-DefaultProfile</span></span>
<span data-ttu-id="58053-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="58053-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58053-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="58053-113">-Name</span></span>
<span data-ttu-id="58053-114">Namn på relä området.</span><span class="sxs-lookup"><span data-stu-id="58053-114">Relay Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58053-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58053-115">-ResourceGroupName</span></span>
<span data-ttu-id="58053-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="58053-116">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58053-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58053-117">CommonParameters</span></span>
<span data-ttu-id="58053-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58053-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58053-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58053-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58053-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="58053-120">INPUTS</span></span>

### <span data-ttu-id="58053-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58053-121">-ResourceGroupName</span></span>
<span data-ttu-id="58053-122">System. String</span><span class="sxs-lookup"><span data-stu-id="58053-122">System.String</span></span>

### <span data-ttu-id="58053-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="58053-123">-Name</span></span>
 <span data-ttu-id="58053-124">System. String</span><span class="sxs-lookup"><span data-stu-id="58053-124">System.String</span></span>

## <span data-ttu-id="58053-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="58053-125">OUTPUTS</span></span>

### <span data-ttu-id="58053-126">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Relay. Models. RelayNamespaceAttributes, Microsoft. Azure. commands. Relay, version = 0.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="58053-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="58053-127">ProvisioningState: lyckades CreatedAt: 4/12/2017 12:38:47 AM UpdatedAt: 4/12/2017 12:39:10 AM ServiceBusEndpoint: https://TestNameSpace-Relay1.servicebus.windows.net:443/ MetricId: 854d368f-1828-428F-8f3c-f2affa9b2f7d: testnamespace-Relay1 plats: väst amerikanska Taggar: {[tag1, Tag1Value]} ID:/Subscriptions/854d368f-1828-428F-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1 namn: TestNameSpace-Relay1 typ: Microsoft. Relay/Namespaces</span><span class="sxs-lookup"><span data-stu-id="58053-127">ProvisioningState  : Succeeded CreatedAt          : 4/12/2017 12:38:47 AM UpdatedAt          : 4/12/2017 12:39:10 AM ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/ MetricId           : 854d368f-1828-428f-8f3c-f2affa9b2f7d:testnamespace-relay1 Location           : West US Tags               : {[tag1, Tag1Value]} Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1 Name               : TestNameSpace-Relay1 Type               : Microsoft.Relay/namespaces</span></span>

## <span data-ttu-id="58053-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="58053-128">NOTES</span></span>

## <span data-ttu-id="58053-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="58053-129">RELATED LINKS</span></span>

