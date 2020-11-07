---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
ms.openlocfilehash: 785685981c38248fba944cc9e3809a2de1f32e71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576413"
---
# <span data-ttu-id="b7748-101">Set-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="b7748-101">Set-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="b7748-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b7748-102">SYNOPSIS</span></span>
<span data-ttu-id="b7748-103">Uppdaterar beskrivningen av en Service Bus-kö i angivet Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="b7748-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7748-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b7748-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <QueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7748-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b7748-105">DESCRIPTION</span></span>
<span data-ttu-id="b7748-106">Cmdleten **set-AzureRmServiceBusQueue** uppdaterar beskrivningen för Service Bus-kön i angivet Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="b7748-106">The **Set-AzureRmServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="b7748-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b7748-107">EXAMPLES</span></span>

### <span data-ttu-id="b7748-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b7748-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -QueueObj $QueueObj

Name                                : SB-Queue_exampl1
LockDuration                        : 
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 2:51:34 AM
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : True
MaxDeliveryCount                    : 
MaxSizeInMegabytes                  : 16384
MessageCount                        : 
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 
Status                              : Active
UpdatedAt                           : 1/20/2017 6:16:18 PM
```

<span data-ttu-id="b7748-109">Uppdaterar den angivna kön med en ny beskrivning i det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="b7748-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="b7748-110">Det här exemplet uppdaterar egenskapen **DeadLetteringOnMessageExpiration** till **True** och **SupportOrdering** till **True**.</span><span class="sxs-lookup"><span data-stu-id="b7748-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="b7748-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b7748-111">PARAMETERS</span></span>

### <span data-ttu-id="b7748-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7748-112">-DefaultProfile</span></span>
<span data-ttu-id="b7748-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b7748-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7748-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7748-114">-InputObject</span></span>
<span data-ttu-id="b7748-115">ServiceBus-definitionen.</span><span class="sxs-lookup"><span data-stu-id="b7748-115">ServiceBus definition.</span></span>

```yaml
Type: PSQueueAttributes
Parameter Sets: (All)
Aliases: QueueObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7748-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="b7748-116">-Name</span></span>
<span data-ttu-id="b7748-117">Könamn.</span><span class="sxs-lookup"><span data-stu-id="b7748-117">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7748-118">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="b7748-118">-Namespace</span></span>
<span data-ttu-id="b7748-119">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="b7748-119">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7748-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7748-120">-ResourceGroupName</span></span>
<span data-ttu-id="b7748-121">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="b7748-121">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7748-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b7748-122">-Confirm</span></span>
<span data-ttu-id="b7748-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b7748-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7748-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7748-124">-WhatIf</span></span>
<span data-ttu-id="b7748-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b7748-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7748-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b7748-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7748-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7748-127">CommonParameters</span></span>
<span data-ttu-id="b7748-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7748-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7748-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7748-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7748-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b7748-130">INPUTS</span></span>

### <span data-ttu-id="b7748-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b7748-131">-ResourceGroup</span></span>
 <span data-ttu-id="b7748-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b7748-132">System.String</span></span>

### <span data-ttu-id="b7748-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b7748-133">-NamespaceName</span></span>
 <span data-ttu-id="b7748-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b7748-134">System.String</span></span>

### <span data-ttu-id="b7748-135">-QueueName</span><span class="sxs-lookup"><span data-stu-id="b7748-135">-QueueName</span></span>
 <span data-ttu-id="b7748-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b7748-136">System.String</span></span>

### <span data-ttu-id="b7748-137">-QueueObj</span><span class="sxs-lookup"><span data-stu-id="b7748-137">-QueueObj</span></span>
 <span data-ttu-id="b7748-138">Microsoft. Azure. commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="b7748-138">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="b7748-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b7748-139">OUTPUTS</span></span>

### <span data-ttu-id="b7748-140">Microsoft. Azure. commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="b7748-140">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="b7748-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b7748-141">NOTES</span></span>

## <span data-ttu-id="b7748-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b7748-142">RELATED LINKS</span></span>
