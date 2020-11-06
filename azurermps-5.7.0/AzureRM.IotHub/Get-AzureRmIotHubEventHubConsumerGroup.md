---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 62704390e28f6f6a256b2202a61d1e400de7f7e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577199"
---
# <span data-ttu-id="bbf65-101">Get-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="bbf65-101">Get-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="bbf65-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bbf65-102">SYNOPSIS</span></span>
<span data-ttu-id="bbf65-103">Hämtar alla eventhub-consumergroups.</span><span class="sxs-lookup"><span data-stu-id="bbf65-103">Gets all the eventhub consumergroups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbf65-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bbf65-104">SYNTAX</span></span>

```
Get-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbf65-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bbf65-105">DESCRIPTION</span></span>
<span data-ttu-id="bbf65-106">Hämtar alla eventhub-consumergroups för de olika EventHubs som används av IotHub.</span><span class="sxs-lookup"><span data-stu-id="bbf65-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="bbf65-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bbf65-107">EXAMPLES</span></span>

### <span data-ttu-id="bbf65-108">Exempel 1 hämtar alla eventhub-consumergroups för eventhub-telemetri</span><span class="sxs-lookup"><span data-stu-id="bbf65-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="bbf65-109">Hämtar alla eventhub-consumergroups för funktionen telemetri för iothub med namnet myiothub</span><span class="sxs-lookup"><span data-stu-id="bbf65-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

### <span data-ttu-id="bbf65-110">Exempel 2 får alla eventhub-consumergroups för operationsmonitoring-eventhub</span><span class="sxs-lookup"><span data-stu-id="bbf65-110">Example 2 Gets all the eventhub consumergroups for the operationsmonitoring eventhub</span></span>
```
PS C:\> Get-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents"
```

<span data-ttu-id="bbf65-111">Hämtar alla eventhub-consumergroups för operationsMonitoringEvents-eventhub för iothub som heter myiothub</span><span class="sxs-lookup"><span data-stu-id="bbf65-111">Gets all the eventhub consumergroups for the operationsMonitoringEvents eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="bbf65-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bbf65-112">PARAMETERS</span></span>

### <span data-ttu-id="bbf65-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbf65-113">-DefaultProfile</span></span>
<span data-ttu-id="bbf65-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bbf65-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bbf65-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="bbf65-115">-EventHubEndpointName</span></span>
<span data-ttu-id="bbf65-116">Namn på händelse grenens slut punkt.</span><span class="sxs-lookup"><span data-stu-id="bbf65-116">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="bbf65-117">Möjliga värden, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="bbf65-117">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf65-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="bbf65-118">-Name</span></span>
<span data-ttu-id="bbf65-119">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="bbf65-119">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf65-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbf65-120">-ResourceGroupName</span></span>
<span data-ttu-id="bbf65-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="bbf65-121">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf65-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbf65-122">CommonParameters</span></span>
<span data-ttu-id="bbf65-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbf65-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbf65-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbf65-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbf65-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bbf65-125">INPUTS</span></span>

### <span data-ttu-id="bbf65-126">System. String</span><span class="sxs-lookup"><span data-stu-id="bbf65-126">System.String</span></span>

## <span data-ttu-id="bbf65-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bbf65-127">OUTPUTS</span></span>

### <span data-ttu-id="bbf65-128">System. Collections. Generic. IEnumerable ' 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="bbf65-128">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="bbf65-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bbf65-129">NOTES</span></span>

## <span data-ttu-id="bbf65-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bbf65-130">RELATED LINKS</span></span>

