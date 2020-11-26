---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: adaf7485b0af16821a1f4adec7919422bef07f90
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322752"
---
# <span data-ttu-id="a4adc-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="a4adc-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="a4adc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4adc-102">SYNOPSIS</span></span>
<span data-ttu-id="a4adc-103">Kontrollerar tillgängligheten för den angivna kön eller det här namnet</span><span class="sxs-lookup"><span data-stu-id="a4adc-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="a4adc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4adc-104">SYNTAX</span></span>

### <span data-ttu-id="a4adc-105">QueueCheckNameAvailabilitySet (standard)</span><span class="sxs-lookup"><span data-stu-id="a4adc-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4adc-106">TopicCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a4adc-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4adc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4adc-107">DESCRIPTION</span></span>
<span data-ttu-id="a4adc-108">**Test-AzServiceBusNameAvailability** cmdlet kontrollerar tillgängligheten för det tillhandahållna namnet på kön eller ämnet</span><span class="sxs-lookup"><span data-stu-id="a4adc-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="a4adc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4adc-109">EXAMPLES</span></span>

### <span data-ttu-id="a4adc-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a4adc-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="a4adc-111">Returnerar sant om det tillhandahållna $nameQueue-namnet är Availabile eller returnerar falskt om angivet $nameQueue namn inte är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="a4adc-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="a4adc-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a4adc-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="a4adc-113">Returnerar sant om det tillhandahållna $nameTopic-namnet är Availabile eller returnerar falskt om angivet $nameTopic namn inte är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="a4adc-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="a4adc-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4adc-114">PARAMETERS</span></span>

### <span data-ttu-id="a4adc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4adc-115">-DefaultProfile</span></span>
<span data-ttu-id="a4adc-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a4adc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4adc-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="a4adc-117">-Name</span></span>
<span data-ttu-id="a4adc-118">Könamn för att kontrol lera namn tillgänglighet</span><span class="sxs-lookup"><span data-stu-id="a4adc-118">Queue Name to check the Name Availability</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4adc-119">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="a4adc-119">-Namespace</span></span>
<span data-ttu-id="a4adc-120">Namn namn för ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a4adc-120">Servicebus Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4adc-121">-Kö</span><span class="sxs-lookup"><span data-stu-id="a4adc-121">-Queue</span></span>
<span data-ttu-id="a4adc-122">Så här kontrollerar du namn tillgänglighet för könamn</span><span class="sxs-lookup"><span data-stu-id="a4adc-122">To Check Name Availability for Queue Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: QueueCheckNameAvailabilitySet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4adc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4adc-123">-ResourceGroupName</span></span>
<span data-ttu-id="a4adc-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a4adc-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4adc-125">-Ämne</span><span class="sxs-lookup"><span data-stu-id="a4adc-125">-Topic</span></span>
<span data-ttu-id="a4adc-126">Så här kontrollerar du namns tillgänglighet för namn på ämnet</span><span class="sxs-lookup"><span data-stu-id="a4adc-126">To Check Name Availability for Topic Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TopicCheckNameAvailabilitySet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4adc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4adc-127">CommonParameters</span></span>
<span data-ttu-id="a4adc-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4adc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a4adc-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4adc-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4adc-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4adc-130">INPUTS</span></span>

### <span data-ttu-id="a4adc-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a4adc-131">System.String</span></span>

## <span data-ttu-id="a4adc-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4adc-132">OUTPUTS</span></span>

### <span data-ttu-id="a4adc-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a4adc-133">System.Boolean</span></span>

## <span data-ttu-id="a4adc-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4adc-134">NOTES</span></span>

## <span data-ttu-id="a4adc-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4adc-135">RELATED LINKS</span></span>