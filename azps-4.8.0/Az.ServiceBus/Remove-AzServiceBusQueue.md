---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
ms.openlocfilehash: c93f0d8a44a67195d2c901dd581505276b7ae2f0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100842"
---
# <span data-ttu-id="3e751-101">Remove-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="3e751-101">Remove-AzServiceBusQueue</span></span>

## <span data-ttu-id="3e751-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e751-102">SYNOPSIS</span></span>
<span data-ttu-id="3e751-103">Tar bort kön från det angivna tjänst buss utrymmet.</span><span class="sxs-lookup"><span data-stu-id="3e751-103">Removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="3e751-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e751-104">SYNTAX</span></span>

### <span data-ttu-id="3e751-105">QueuePropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3e751-105">QueuePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e751-106">QueueInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3e751-106">QueueInputObjectSet</span></span>
```
Remove-AzServiceBusQueue [-InputObject] <PSQueueAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e751-107">QueueResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3e751-107">QueueResourceIdSet</span></span>
```
Remove-AzServiceBusQueue [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e751-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e751-108">DESCRIPTION</span></span>
<span data-ttu-id="3e751-109">Cmdleten **Remove-AzServiceBusQueue** tar bort kön från det angivna tjänst buss utrymmet.</span><span class="sxs-lookup"><span data-stu-id="3e751-109">The **Remove-AzServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="3e751-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e751-110">EXAMPLES</span></span>

### <span data-ttu-id="3e751-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3e751-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="3e751-112">Tar bort Service Bus-kön `SB-Queue_exampl1` från namn området `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="3e751-112">Removes the Service Bus queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="3e751-113">Exempel 2: InputObject – använder variabel:</span><span class="sxs-lookup"><span data-stu-id="3e751-113">Example 2: InputObject - Using variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -InputObject $inputobject
```

<span data-ttu-id="3e751-114">Tar bort Service Bus-kön som finns i parametern $inputobject för InputObject</span><span class="sxs-lookup"><span data-stu-id="3e751-114">Removes the Service Bus queue provided in the $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="3e751-115">Exempel 3: InputObject-använder rör:</span><span class="sxs-lookup"><span data-stu-id="3e751-115">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\>  Get-AzServiceBusQueue <params> | Remove-AzServiceBusQueue
```

### <span data-ttu-id="3e751-116">Exempel 4: ResourceId-använder variabel:</span><span class="sxs-lookup"><span data-stu-id="3e751-116">Example 4: ResourceId - Using variable:</span></span>
```powershell
PS c:\> $resourceid = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -ResourceId $resourceid.Id
```

<span data-ttu-id="3e751-117">Tar bort Service Bus-kön som tillhandahålls i ARM-ID: t $resourceid/String för parametern-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e751-117">Removes the Service Bus queue provided in the ARM id in $resourceid/string for -ResourceId parameter</span></span>

### <span data-ttu-id="3e751-118">Exempel 5: ResourceId-skicka som sträng:</span><span class="sxs-lookup"><span data-stu-id="3e751-118">Example 5: ResourceId - passing as string:</span></span>
```powershell
PS C:\> Remove-AzServiceBusQueue -ResourceId "/subscriptions/xxxx-xxxxx-xxxxx-xxxxxx-xxxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/queues/QueueName"
```

## <span data-ttu-id="3e751-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e751-119">PARAMETERS</span></span>

### <span data-ttu-id="3e751-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e751-120">-AsJob</span></span>
<span data-ttu-id="3e751-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3e751-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e751-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e751-122">-DefaultProfile</span></span>
<span data-ttu-id="3e751-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3e751-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e751-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e751-124">-InputObject</span></span>
<span data-ttu-id="3e751-125">Service Bus-köobjekt</span><span class="sxs-lookup"><span data-stu-id="3e751-125">Service Bus Queue Object</span></span>

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

### <span data-ttu-id="3e751-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="3e751-126">-Name</span></span>
<span data-ttu-id="3e751-127">Könamn</span><span class="sxs-lookup"><span data-stu-id="3e751-127">Queue Name</span></span>

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

### <span data-ttu-id="3e751-128">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="3e751-128">-Namespace</span></span>
<span data-ttu-id="3e751-129">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="3e751-129">Namespace Name</span></span>

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

### <span data-ttu-id="3e751-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e751-130">-PassThru</span></span>
<span data-ttu-id="3e751-131">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="3e751-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="3e751-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e751-132">-ResourceGroupName</span></span>
<span data-ttu-id="3e751-133">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="3e751-133">The name of the resource group</span></span>

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

### <span data-ttu-id="3e751-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e751-134">-ResourceId</span></span>
<span data-ttu-id="3e751-135">Resurs-ID för Service Bus-kö</span><span class="sxs-lookup"><span data-stu-id="3e751-135">Service Bus Queue Resource Id</span></span>

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

### <span data-ttu-id="3e751-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3e751-136">-Confirm</span></span>
<span data-ttu-id="3e751-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3e751-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e751-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e751-138">-WhatIf</span></span>
<span data-ttu-id="3e751-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3e751-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e751-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3e751-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e751-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e751-141">CommonParameters</span></span>
<span data-ttu-id="3e751-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e751-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e751-143">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e751-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e751-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e751-144">INPUTS</span></span>

### <span data-ttu-id="3e751-145">System. String</span><span class="sxs-lookup"><span data-stu-id="3e751-145">System.String</span></span>

### <span data-ttu-id="3e751-146">Microsoft. Azure. commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="3e751-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="3e751-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e751-147">OUTPUTS</span></span>

### <span data-ttu-id="3e751-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3e751-148">System.Boolean</span></span>

## <span data-ttu-id="3e751-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e751-149">NOTES</span></span>

## <span data-ttu-id="3e751-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e751-150">RELATED LINKS</span></span>