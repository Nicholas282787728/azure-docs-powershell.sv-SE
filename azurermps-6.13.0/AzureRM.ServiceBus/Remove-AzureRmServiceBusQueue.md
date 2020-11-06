---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
ms.openlocfilehash: ba59f19183cf49802240d7631b99b3e69a9bc6f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577908"
---
# <span data-ttu-id="6f9a5-101">Remove-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="6f9a5-101">Remove-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="6f9a5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f9a5-102">SYNOPSIS</span></span>
<span data-ttu-id="6f9a5-103">Tar bort kön från det angivna tjänst buss utrymmet.</span><span class="sxs-lookup"><span data-stu-id="6f9a5-103">Removes the queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f9a5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f9a5-104">SYNTAX</span></span>

### <span data-ttu-id="6f9a5-105">QueuePropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6f9a5-105">QueuePropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f9a5-106">QueueInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6f9a5-106">QueueInputObjectSet</span></span>
```
Remove-AzureRmServiceBusQueue [-InputObject] <PSQueueAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f9a5-107">QueueResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6f9a5-107">QueueResourceIdSet</span></span>
```
Remove-AzureRmServiceBusQueue [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f9a5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f9a5-108">DESCRIPTION</span></span>
<span data-ttu-id="6f9a5-109">Cmdleten **Remove-AzureRmServiceBusQueue** tar bort kön från det angivna tjänst buss utrymmet.</span><span class="sxs-lookup"><span data-stu-id="6f9a5-109">The **Remove-AzureRmServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="6f9a5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f9a5-110">EXAMPLES</span></span>

### <span data-ttu-id="6f9a5-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6f9a5-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="6f9a5-112">Tar bort Service Bus-kön `SB-Queue_exampl1` från namn området `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="6f9a5-112">Removes the Service Bus queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="6f9a5-113">Exempel 2,1 – InputObject – använder variabel:</span><span class="sxs-lookup"><span data-stu-id="6f9a5-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusQueue <params>
PS C:\> Remove-AzureRmServiceBusQueue -InputObject $inputobject
```

<span data-ttu-id="6f9a5-114">Tar bort Service Bus-kön som finns i parametern $inputobject för InputObject</span><span class="sxs-lookup"><span data-stu-id="6f9a5-114">Removes the Service Bus queue provided in the $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="6f9a5-115">Exempel 2,1 – InputObject-med rör dragning:</span><span class="sxs-lookup"><span data-stu-id="6f9a5-115">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\>  Get-AzureRmServiceBusQueue <params> | Remove-AzureRmServiceBusQueue
```

### <span data-ttu-id="6f9a5-116">Exempel 3,1-ResourceId-använder variabel:</span><span class="sxs-lookup"><span data-stu-id="6f9a5-116">Example 3.1 - ResourceId - Using variable:</span></span>
```
PS c:\> $resourceid = Get-AzureRmServiceBusQueue <params>
PS C:\> Remove-AzureRmServiceBusQueue -ResourceId $resourceid.Id
```

<span data-ttu-id="6f9a5-117">Tar bort Service Bus-kön som tillhandahålls i ARM-ID: t $resourceid/String för parametern-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f9a5-117">Removes the Service Bus queue provided in the ARM id in $resourceid/string for -ResourceId parameter</span></span>

### <span data-ttu-id="6f9a5-118">Exempel 3,2-ResourceId-passign som sträng:</span><span class="sxs-lookup"><span data-stu-id="6f9a5-118">Example 3.2 - ResourceId - passign as string:</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceId "/subscriptions/xxxx-xxxxx-xxxxx-xxxxxx-xxxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/queues/QueueName"
```

## <span data-ttu-id="6f9a5-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f9a5-119">PARAMETERS</span></span>

### <span data-ttu-id="6f9a5-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f9a5-120">-AsJob</span></span>
<span data-ttu-id="6f9a5-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6f9a5-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9a5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f9a5-122">-DefaultProfile</span></span>
<span data-ttu-id="6f9a5-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6f9a5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9a5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f9a5-124">-InputObject</span></span>
<span data-ttu-id="6f9a5-125">Service Bus-köobjekt</span><span class="sxs-lookup"><span data-stu-id="6f9a5-125">Service Bus Queue Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes
Parameter Sets: QueueInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f9a5-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="6f9a5-126">-Name</span></span>
<span data-ttu-id="6f9a5-127">Könamn</span><span class="sxs-lookup"><span data-stu-id="6f9a5-127">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f9a5-128">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="6f9a5-128">-Namespace</span></span>
<span data-ttu-id="6f9a5-129">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="6f9a5-129">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f9a5-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f9a5-130">-PassThru</span></span>
<span data-ttu-id="6f9a5-131">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="6f9a5-131">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9a5-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f9a5-132">-ResourceGroupName</span></span>
<span data-ttu-id="6f9a5-133">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="6f9a5-133">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f9a5-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f9a5-134">-ResourceId</span></span>
<span data-ttu-id="6f9a5-135">Resurs-ID för Service Bus-kö</span><span class="sxs-lookup"><span data-stu-id="6f9a5-135">Service Bus Queue Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: QueueResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f9a5-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6f9a5-136">-Confirm</span></span>
<span data-ttu-id="6f9a5-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6f9a5-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9a5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f9a5-138">-WhatIf</span></span>
<span data-ttu-id="6f9a5-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6f9a5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f9a5-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6f9a5-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9a5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f9a5-141">CommonParameters</span></span>
<span data-ttu-id="6f9a5-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f9a5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f9a5-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f9a5-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f9a5-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f9a5-144">INPUTS</span></span>

### <span data-ttu-id="6f9a5-145">System. String</span><span class="sxs-lookup"><span data-stu-id="6f9a5-145">System.String</span></span>

### <span data-ttu-id="6f9a5-146">Microsoft. Azure. commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="6f9a5-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>
<span data-ttu-id="6f9a5-147">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6f9a5-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="6f9a5-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f9a5-148">OUTPUTS</span></span>

### <span data-ttu-id="6f9a5-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6f9a5-149">System.Boolean</span></span>

## <span data-ttu-id="6f9a5-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f9a5-150">NOTES</span></span>

## <span data-ttu-id="6f9a5-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f9a5-151">RELATED LINKS</span></span>
