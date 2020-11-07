---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 065c2e185be1a9cdc0f495b61104f659076b54b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916477"
---
# <span data-ttu-id="82deb-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="82deb-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="82deb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82deb-102">SYNOPSIS</span></span>
<span data-ttu-id="82deb-103">Hämtar alla eventhub-consumergroups.</span><span class="sxs-lookup"><span data-stu-id="82deb-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="82deb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82deb-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82deb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82deb-105">DESCRIPTION</span></span>
<span data-ttu-id="82deb-106">Hämtar alla eventhub-consumergroups för de olika EventHubs som används av IotHub.</span><span class="sxs-lookup"><span data-stu-id="82deb-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="82deb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82deb-107">EXAMPLES</span></span>

### <span data-ttu-id="82deb-108">Exempel 1 hämtar alla eventhub-consumergroups för eventhub-telemetri</span><span class="sxs-lookup"><span data-stu-id="82deb-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="82deb-109">Hämtar alla eventhub-consumergroups för funktionen telemetri för iothub med namnet myiothub</span><span class="sxs-lookup"><span data-stu-id="82deb-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

### <span data-ttu-id="82deb-110">Exempel 2 får alla eventhub-consumergroups för operationsmonitoring-eventhub</span><span class="sxs-lookup"><span data-stu-id="82deb-110">Example 2 Gets all the eventhub consumergroups for the operationsmonitoring eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents"
```

<span data-ttu-id="82deb-111">Hämtar alla eventhub-consumergroups för operationsMonitoringEvents-eventhub för iothub som heter myiothub</span><span class="sxs-lookup"><span data-stu-id="82deb-111">Gets all the eventhub consumergroups for the operationsMonitoringEvents eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="82deb-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82deb-112">PARAMETERS</span></span>

### <span data-ttu-id="82deb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82deb-113">-DefaultProfile</span></span>
<span data-ttu-id="82deb-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="82deb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82deb-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="82deb-115">-EventHubEndpointName</span></span>
<span data-ttu-id="82deb-116">Namn på händelse grenens slut punkt.</span><span class="sxs-lookup"><span data-stu-id="82deb-116">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="82deb-117">Möjliga värden, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="82deb-117">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82deb-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="82deb-118">-Name</span></span>
<span data-ttu-id="82deb-119">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="82deb-119">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82deb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82deb-120">-ResourceGroupName</span></span>
<span data-ttu-id="82deb-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="82deb-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82deb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82deb-122">CommonParameters</span></span>
<span data-ttu-id="82deb-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82deb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82deb-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82deb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82deb-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82deb-125">INPUTS</span></span>

### <span data-ttu-id="82deb-126">System. String</span><span class="sxs-lookup"><span data-stu-id="82deb-126">System.String</span></span>

## <span data-ttu-id="82deb-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82deb-127">OUTPUTS</span></span>

### <span data-ttu-id="82deb-128">Microsoft. Azure. commands. Management. IotHub. Models. PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="82deb-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="82deb-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82deb-129">NOTES</span></span>

## <span data-ttu-id="82deb-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82deb-130">RELATED LINKS</span></span>
