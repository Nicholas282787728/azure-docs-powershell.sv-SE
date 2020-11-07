---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
ms.openlocfilehash: 1e4e1d50df44715fe433a5106619264063b2f22e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746927"
---
# <span data-ttu-id="b4254-101">Get-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="b4254-101">Get-AzServiceBusNamespace</span></span>

## <span data-ttu-id="b4254-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4254-102">SYNOPSIS</span></span>
<span data-ttu-id="b4254-103">Hämtar en beskrivning för det angivna Service Bus-namnområdet i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b4254-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="b4254-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4254-104">SYNTAX</span></span>

```
Get-AzServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4254-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4254-105">DESCRIPTION</span></span>
<span data-ttu-id="b4254-106">Cmdleten **Get-AzServiceBusNamespace** hämtar en beskrivning för det angivna tjänst bussens namnrymds namn i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b4254-106">The **Get-AzServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="b4254-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4254-107">EXAMPLES</span></span>

### <span data-ttu-id="b4254-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b4254-108">Example 1</span></span>

```
PS C:\> Get-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroup      : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 1:40:01 AM
UpdatedAt          : 1/20/2017 1:40:24 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

## <span data-ttu-id="b4254-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4254-109">PARAMETERS</span></span>

### <span data-ttu-id="b4254-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4254-110">-DefaultProfile</span></span>
<span data-ttu-id="b4254-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b4254-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4254-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="b4254-112">-Name</span></span>
<span data-ttu-id="b4254-113">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="b4254-113">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4254-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4254-114">-ResourceGroupName</span></span>
<span data-ttu-id="b4254-115">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="b4254-115">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4254-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4254-116">CommonParameters</span></span>
<span data-ttu-id="b4254-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4254-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4254-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4254-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4254-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4254-119">INPUTS</span></span>

### <span data-ttu-id="b4254-120">System. String</span><span class="sxs-lookup"><span data-stu-id="b4254-120">System.String</span></span>

## <span data-ttu-id="b4254-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4254-121">OUTPUTS</span></span>

### <span data-ttu-id="b4254-122">Microsoft. Azure. commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="b4254-122">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="b4254-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4254-123">NOTES</span></span>

## <span data-ttu-id="b4254-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4254-124">RELATED LINKS</span></span>