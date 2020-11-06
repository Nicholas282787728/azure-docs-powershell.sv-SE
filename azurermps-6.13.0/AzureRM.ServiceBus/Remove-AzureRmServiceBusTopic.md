---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
ms.openlocfilehash: 8434893dd3661bbfb1f78a4973dc206f44e9f400
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573894"
---
# <span data-ttu-id="12e7c-101">Remove-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="12e7c-101">Remove-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="12e7c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="12e7c-103">Tar bort avsnittet från det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="12e7c-103">Removes the topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12e7c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12e7c-104">SYNTAX</span></span>

### <span data-ttu-id="12e7c-105">TopicPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="12e7c-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12e7c-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="12e7c-106">TopicInputObjectSet</span></span>
```
Remove-AzureRmServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12e7c-107">TopicResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="12e7c-107">TopicResourceIdSet</span></span>
```
Remove-AzureRmServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12e7c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12e7c-108">DESCRIPTION</span></span>
<span data-ttu-id="12e7c-109">Cmdleten **Remove-AzureRmServiceBusTopic** tar bort avsnittet från det angivna tjänst buss namn området.</span><span class="sxs-lookup"><span data-stu-id="12e7c-109">The **Remove-AzureRmServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="12e7c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12e7c-110">EXAMPLES</span></span>

### <span data-ttu-id="12e7c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="12e7c-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="12e7c-112">Tar bort avsnittet `SB-Topic_exampl1` från namn området `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="12e7c-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="12e7c-113">Exempel 2,1 – InputObject – använder variabel:</span><span class="sxs-lookup"><span data-stu-id="12e7c-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusTopic <parmas>
PS C:\> Remove-AzureRmServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="12e7c-114">Exempel 2,2 – InputObject-med rör dragning:</span><span class="sxs-lookup"><span data-stu-id="12e7c-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic <parmas> | Remove-AzureRmServiceBusTopic
```

### <span data-ttu-id="12e7c-115">Exempel 3,1-ResourceId med variabel:</span><span class="sxs-lookup"><span data-stu-id="12e7c-115">Example 3.1 - ResourceId Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzureRmServiceBusTopic <params>
PS C:\> Remove-AzureRmServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="12e7c-116">Exempel 3,2-ResourceId med sträng värde</span><span class="sxs-lookup"><span data-stu-id="12e7c-116">Example 3.2 - ResourceId Using String value</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="12e7c-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12e7c-117">PARAMETERS</span></span>

### <span data-ttu-id="12e7c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12e7c-118">-AsJob</span></span>
<span data-ttu-id="12e7c-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="12e7c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12e7c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e7c-120">-DefaultProfile</span></span>
<span data-ttu-id="12e7c-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="12e7c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12e7c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12e7c-122">-InputObject</span></span>
<span data-ttu-id="12e7c-123">Ämne för Service Bus-objekt</span><span class="sxs-lookup"><span data-stu-id="12e7c-123">Service Bus Topic Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: TopicInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12e7c-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="12e7c-124">-Name</span></span>
<span data-ttu-id="12e7c-125">Namn på avsnitt</span><span class="sxs-lookup"><span data-stu-id="12e7c-125">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12e7c-126">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="12e7c-126">-Namespace</span></span>
<span data-ttu-id="12e7c-127">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="12e7c-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12e7c-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12e7c-128">-PassThru</span></span>
<span data-ttu-id="12e7c-129">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="12e7c-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="12e7c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12e7c-130">-ResourceGroupName</span></span>
<span data-ttu-id="12e7c-131">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="12e7c-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12e7c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12e7c-132">-ResourceId</span></span>
<span data-ttu-id="12e7c-133">Service Bus ämne resurs-ID</span><span class="sxs-lookup"><span data-stu-id="12e7c-133">Service Bus Topic Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: TopicResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12e7c-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="12e7c-134">-Confirm</span></span>
<span data-ttu-id="12e7c-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="12e7c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12e7c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12e7c-136">-WhatIf</span></span>
<span data-ttu-id="12e7c-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="12e7c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12e7c-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="12e7c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12e7c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e7c-139">CommonParameters</span></span>
<span data-ttu-id="12e7c-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12e7c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e7c-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12e7c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e7c-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12e7c-142">INPUTS</span></span>

### <span data-ttu-id="12e7c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="12e7c-143">System.String</span></span>

### <span data-ttu-id="12e7c-144">Microsoft. Azure. commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="12e7c-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>
<span data-ttu-id="12e7c-145">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="12e7c-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="12e7c-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12e7c-146">OUTPUTS</span></span>

### <span data-ttu-id="12e7c-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="12e7c-147">System.Boolean</span></span>

## <span data-ttu-id="12e7c-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12e7c-148">NOTES</span></span>

## <span data-ttu-id="12e7c-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12e7c-149">RELATED LINKS</span></span>
