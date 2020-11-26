---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayNamespace.md
ms.openlocfilehash: ddbc0631b6ba6a3cb55d6e91ab951d44d644e85d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324455"
---
# <span data-ttu-id="7f0ff-101">Get-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="7f0ff-101">Get-AzRelayNamespace</span></span>

## <span data-ttu-id="7f0ff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7f0ff-102">SYNOPSIS</span></span>
<span data-ttu-id="7f0ff-103">Hämtar en beskrivning för det angivna relä namn området i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7f0ff-103">Gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="7f0ff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7f0ff-104">SYNTAX</span></span>

```
Get-AzRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f0ff-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7f0ff-105">DESCRIPTION</span></span>
<span data-ttu-id="7f0ff-106">Cmdleten **Get-AzRelayNamespace** hämtar en beskrivning för det angivna relä namn området i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7f0ff-106">The **Get-AzRelayNamespace** cmdlet gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="7f0ff-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7f0ff-107">EXAMPLES</span></span>

### <span data-ttu-id="7f0ff-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7f0ff-108">Example 1</span></span>
```
PS C:\> Get-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1

ProvisioningState  : Succeeded
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           : 854d368f-1828-428f-8f3c-f2affa9b2f7d:testnamespace-relay1
Location           : West US
Tags               : {[tag1, Tag1Value]}
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1
Name               : TestNameSpace-Relay1
Type               : Microsoft.Relay/namespaces
```

<span data-ttu-id="7f0ff-109">Returnerar en beskrivning av det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="7f0ff-109">Returns a description of the specified Relay namespace.</span></span>

## <span data-ttu-id="7f0ff-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7f0ff-110">PARAMETERS</span></span>

### <span data-ttu-id="7f0ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f0ff-111">-DefaultProfile</span></span>
<span data-ttu-id="7f0ff-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7f0ff-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f0ff-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="7f0ff-113">-Name</span></span>
<span data-ttu-id="7f0ff-114">Namn på relä området.</span><span class="sxs-lookup"><span data-stu-id="7f0ff-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="7f0ff-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f0ff-115">-ResourceGroupName</span></span>
<span data-ttu-id="7f0ff-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="7f0ff-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="7f0ff-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f0ff-117">CommonParameters</span></span>
<span data-ttu-id="7f0ff-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f0ff-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f0ff-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f0ff-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f0ff-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7f0ff-120">INPUTS</span></span>

### <span data-ttu-id="7f0ff-121">System. String</span><span class="sxs-lookup"><span data-stu-id="7f0ff-121">System.String</span></span>

## <span data-ttu-id="7f0ff-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7f0ff-122">OUTPUTS</span></span>

### <span data-ttu-id="7f0ff-123">Microsoft. Azure. commands. Relay. Models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="7f0ff-123">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="7f0ff-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7f0ff-124">NOTES</span></span>

## <span data-ttu-id="7f0ff-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7f0ff-125">RELATED LINKS</span></span>