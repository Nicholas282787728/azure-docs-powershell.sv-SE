---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 3905111a0855eef6421a587bc7151b411106d13a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744008"
---
# <span data-ttu-id="92a61-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="92a61-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="92a61-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92a61-102">SYNOPSIS</span></span>
<span data-ttu-id="92a61-103">Hämtar alla eventhub-consumergroups.</span><span class="sxs-lookup"><span data-stu-id="92a61-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="92a61-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92a61-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92a61-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92a61-105">DESCRIPTION</span></span>
<span data-ttu-id="92a61-106">Hämtar alla eventhub-consumergroups för de olika EventHubs som används av IotHub.</span><span class="sxs-lookup"><span data-stu-id="92a61-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="92a61-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92a61-107">EXAMPLES</span></span>

### <span data-ttu-id="92a61-108">Exempel 1 hämtar alla eventhub-consumergroups för eventhub-telemetri</span><span class="sxs-lookup"><span data-stu-id="92a61-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="92a61-109">Hämtar alla eventhub-consumergroups för funktionen telemetri för iothub med namnet myiothub</span><span class="sxs-lookup"><span data-stu-id="92a61-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="92a61-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92a61-110">PARAMETERS</span></span>

### <span data-ttu-id="92a61-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92a61-111">-DefaultProfile</span></span>
<span data-ttu-id="92a61-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="92a61-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92a61-113">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="92a61-113">-EventHubEndpointName</span></span>
<span data-ttu-id="92a61-114">Namn på händelse grenens slut punkt.</span><span class="sxs-lookup"><span data-stu-id="92a61-114">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="92a61-115">Möjliga värden, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="92a61-115">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="92a61-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="92a61-116">-Name</span></span>
<span data-ttu-id="92a61-117">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="92a61-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="92a61-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92a61-118">-ResourceGroupName</span></span>
<span data-ttu-id="92a61-119">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="92a61-119">Resource Group Name</span></span>

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

### <span data-ttu-id="92a61-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92a61-120">CommonParameters</span></span>
<span data-ttu-id="92a61-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92a61-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92a61-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92a61-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92a61-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92a61-123">INPUTS</span></span>

### <span data-ttu-id="92a61-124">System. String</span><span class="sxs-lookup"><span data-stu-id="92a61-124">System.String</span></span>

## <span data-ttu-id="92a61-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92a61-125">OUTPUTS</span></span>

### <span data-ttu-id="92a61-126">Microsoft. Azure. commands. Management. IotHub. Models. PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="92a61-126">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="92a61-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92a61-127">NOTES</span></span>

## <span data-ttu-id="92a61-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92a61-128">RELATED LINKS</span></span>
