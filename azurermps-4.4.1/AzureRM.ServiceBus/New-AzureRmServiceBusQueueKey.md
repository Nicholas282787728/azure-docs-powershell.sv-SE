---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueKey.md
ms.openlocfilehash: 0a2bfe70e986b3ed92cef215cc23245216c0e961
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758002"
---
# <span data-ttu-id="f2a91-101">New-AzureRmServiceBusQueueKey</span><span class="sxs-lookup"><span data-stu-id="f2a91-101">New-AzureRmServiceBusQueueKey</span></span>

## <span data-ttu-id="f2a91-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f2a91-102">SYNOPSIS</span></span>
<span data-ttu-id="f2a91-103">Återskapar primära eller sekundära anslutnings strängar för Service Bus-kön.</span><span class="sxs-lookup"><span data-stu-id="f2a91-103">Regenerates the primary or secondary connection strings for the Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2a91-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f2a91-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueueKey [-ResourceGroup] <String> [-NamespaceName] <String> [-QueueName] <String>
 [-AuthorizationRuleName] <String> [-RegenerateKeys] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2a91-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f2a91-105">DESCRIPTION</span></span>
<span data-ttu-id="f2a91-106">**New-AzureRmServiceBusQueueKey** cmdlet återskapar primära eller sekundära anslutnings strängar för den angivna tjänst buss kön och auktoriseringsregeln.</span><span class="sxs-lookup"><span data-stu-id="f2a91-106">The **New-AzureRmServiceBusQueueKey** cmdlet regenerates the primary or secondary connection strings for the specified Service Bus queue and authorization rule.</span></span>

## <span data-ttu-id="f2a91-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f2a91-107">EXAMPLES</span></span>

### <span data-ttu-id="f2a91-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f2a91-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="f2a91-109">Återskapar den primära anslutnings strängen för namn området.</span><span class="sxs-lookup"><span data-stu-id="f2a91-109">Regenerates the primary connection string for the namespace.</span></span>

### <span data-ttu-id="f2a91-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f2a91-110">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -RegenerateKeys SecondaryKey
```

<span data-ttu-id="f2a91-111">Återskapar sekundär anslutnings strängen för namn området.</span><span class="sxs-lookup"><span data-stu-id="f2a91-111">Regenerates the secondary connection string for the namespace.</span></span>

## <span data-ttu-id="f2a91-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f2a91-112">PARAMETERS</span></span>

### <span data-ttu-id="f2a91-113">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="f2a91-113">-AuthorizationRuleName</span></span>
<span data-ttu-id="f2a91-114">Namn på auktoriseringsregeln.</span><span class="sxs-lookup"><span data-stu-id="f2a91-114">The authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2a91-115">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f2a91-115">-NamespaceName</span></span>
<span data-ttu-id="f2a91-116">Namn på Service Bus-namnrymden.</span><span class="sxs-lookup"><span data-stu-id="f2a91-116">The Service Bus namespace name.</span></span>

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

### <span data-ttu-id="f2a91-117">-QueueName</span><span class="sxs-lookup"><span data-stu-id="f2a91-117">-QueueName</span></span>
<span data-ttu-id="f2a91-118">Namn på Service Bus-kön.</span><span class="sxs-lookup"><span data-stu-id="f2a91-118">The Service Bus queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2a91-119">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="f2a91-119">-RegenerateKeys</span></span>
<span data-ttu-id="f2a91-120">Anger om primära eller sekundära nycklar ska återskapas.</span><span class="sxs-lookup"><span data-stu-id="f2a91-120">Specifies whether to regenerate the primary or secondary keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2a91-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f2a91-121">-ResourceGroup</span></span>
<span data-ttu-id="f2a91-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f2a91-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="f2a91-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f2a91-123">-Confirm</span></span>
<span data-ttu-id="f2a91-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f2a91-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2a91-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2a91-125">-WhatIf</span></span>
<span data-ttu-id="f2a91-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f2a91-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2a91-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f2a91-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2a91-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2a91-128">CommonParameters</span></span>
<span data-ttu-id="f2a91-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2a91-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2a91-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2a91-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2a91-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f2a91-131">INPUTS</span></span>

### <span data-ttu-id="f2a91-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f2a91-132">-ResourceGroup</span></span>
 <span data-ttu-id="f2a91-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f2a91-133">System.String</span></span>
 

### <span data-ttu-id="f2a91-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f2a91-134">-NamespaceName</span></span>
 <span data-ttu-id="f2a91-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f2a91-135">System.String</span></span>
 

### <span data-ttu-id="f2a91-136">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="f2a91-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="f2a91-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f2a91-137">System.String</span></span>
 

### <span data-ttu-id="f2a91-138">-QueueName</span><span class="sxs-lookup"><span data-stu-id="f2a91-138">-QueueName</span></span>
 <span data-ttu-id="f2a91-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f2a91-139">System.String</span></span>
 

### <span data-ttu-id="f2a91-140">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="f2a91-140">-RegenerateKeys</span></span>
 <span data-ttu-id="f2a91-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f2a91-141">System.String</span></span>

## <span data-ttu-id="f2a91-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f2a91-142">OUTPUTS</span></span>

### <span data-ttu-id="f2a91-143">Microsoft. Azure. Management. ServiceBus. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="f2a91-143">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="f2a91-144">PrimaryConnectionString: slut punkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Queue_exa mpl1 SecondaryConnectionString: slut punkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Queue_exa mpl1 PrimaryKey: {PrimaryKey Value} SecondaryKey: {SecondaryKey värde} nyckel namn: SBAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="f2a91-144">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_exa mpl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_exa mpl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBAuthoRule1</span></span>

## <span data-ttu-id="f2a91-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f2a91-145">NOTES</span></span>

## <span data-ttu-id="f2a91-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f2a91-146">RELATED LINKS</span></span>

