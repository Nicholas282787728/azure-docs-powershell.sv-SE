---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: dc401fc74aff737b92cfe7164c19862678a3e1c6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103231"
---
# <span data-ttu-id="b3c30-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="b3c30-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="b3c30-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b3c30-102">SYNOPSIS</span></span>
<span data-ttu-id="b3c30-103">Hämtar alla eventhub-consumergroups.</span><span class="sxs-lookup"><span data-stu-id="b3c30-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="b3c30-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b3c30-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3c30-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b3c30-105">DESCRIPTION</span></span>
<span data-ttu-id="b3c30-106">Hämtar alla eventhub-consumergroups för de olika EventHubs som används av IotHub.</span><span class="sxs-lookup"><span data-stu-id="b3c30-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="b3c30-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b3c30-107">EXAMPLES</span></span>

### <span data-ttu-id="b3c30-108">Exempel 1 hämtar alla eventhub-consumergroups för eventhub-telemetri</span><span class="sxs-lookup"><span data-stu-id="b3c30-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="b3c30-109">Hämtar alla eventhub-consumergroups för funktionen telemetri för iothub med namnet myiothub</span><span class="sxs-lookup"><span data-stu-id="b3c30-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="b3c30-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b3c30-110">PARAMETERS</span></span>

### <span data-ttu-id="b3c30-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3c30-111">-DefaultProfile</span></span>
<span data-ttu-id="b3c30-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b3c30-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3c30-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="b3c30-113">-Name</span></span>
<span data-ttu-id="b3c30-114">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="b3c30-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="b3c30-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3c30-115">-ResourceGroupName</span></span>
<span data-ttu-id="b3c30-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="b3c30-116">Resource Group Name</span></span>

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

### <span data-ttu-id="b3c30-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3c30-117">CommonParameters</span></span>
<span data-ttu-id="b3c30-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3c30-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3c30-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3c30-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3c30-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b3c30-120">INPUTS</span></span>

### <span data-ttu-id="b3c30-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b3c30-121">System.String</span></span>

## <span data-ttu-id="b3c30-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b3c30-122">OUTPUTS</span></span>

### <span data-ttu-id="b3c30-123">Microsoft. Azure. commands. Management. IotHub. Models. PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="b3c30-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="b3c30-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b3c30-124">NOTES</span></span>

## <span data-ttu-id="b3c30-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b3c30-125">RELATED LINKS</span></span>