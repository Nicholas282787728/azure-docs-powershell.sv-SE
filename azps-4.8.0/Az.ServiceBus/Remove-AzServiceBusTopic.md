---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
ms.openlocfilehash: 75da2231dae7ea0dc587d48ca832b7631fc24986
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261051"
---
# <span data-ttu-id="e07dd-101">Remove-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="e07dd-101">Remove-AzServiceBusTopic</span></span>

## <span data-ttu-id="e07dd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e07dd-102">SYNOPSIS</span></span>
<span data-ttu-id="e07dd-103">Tar bort avsnittet från det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="e07dd-103">Removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="e07dd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e07dd-104">SYNTAX</span></span>

### <span data-ttu-id="e07dd-105">TopicPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e07dd-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e07dd-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e07dd-106">TopicInputObjectSet</span></span>
```
Remove-AzServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e07dd-107">TopicResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e07dd-107">TopicResourceIdSet</span></span>
```
Remove-AzServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e07dd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e07dd-108">DESCRIPTION</span></span>
<span data-ttu-id="e07dd-109">Cmdleten **Remove-AzServiceBusTopic** tar bort avsnittet från det angivna tjänst buss namn området.</span><span class="sxs-lookup"><span data-stu-id="e07dd-109">The **Remove-AzServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="e07dd-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e07dd-110">EXAMPLES</span></span>

### <span data-ttu-id="e07dd-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e07dd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="e07dd-112">Tar bort avsnittet `SB-Topic_exampl1` från namn området `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="e07dd-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="e07dd-113">Exempel 2: InputObject – använder variabel:</span><span class="sxs-lookup"><span data-stu-id="e07dd-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusTopic <parmas>
PS C:\> Remove-AzServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="e07dd-114">Exempel 3: InputObject-använder rör:</span><span class="sxs-lookup"><span data-stu-id="e07dd-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusTopic <parmas> | Remove-AzServiceBusTopic
```

### <span data-ttu-id="e07dd-115">Exempel 4: ResourceId med variabel:</span><span class="sxs-lookup"><span data-stu-id="e07dd-115">Example 4: ResourceId Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusTopic <params>
PS C:\> Remove-AzServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="e07dd-116">Exempel 5: ResourceId med sträng värde</span><span class="sxs-lookup"><span data-stu-id="e07dd-116">Example 5: ResourceId Using String value</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="e07dd-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e07dd-117">PARAMETERS</span></span>

### <span data-ttu-id="e07dd-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e07dd-118">-AsJob</span></span>
<span data-ttu-id="e07dd-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e07dd-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e07dd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e07dd-120">-DefaultProfile</span></span>
<span data-ttu-id="e07dd-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e07dd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e07dd-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e07dd-122">-InputObject</span></span>
<span data-ttu-id="e07dd-123">Ämne för Service Bus-objekt</span><span class="sxs-lookup"><span data-stu-id="e07dd-123">Service Bus Topic Object</span></span>

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

### <span data-ttu-id="e07dd-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="e07dd-124">-Name</span></span>
<span data-ttu-id="e07dd-125">Namn på avsnitt</span><span class="sxs-lookup"><span data-stu-id="e07dd-125">Topic Name</span></span>

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

### <span data-ttu-id="e07dd-126">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="e07dd-126">-Namespace</span></span>
<span data-ttu-id="e07dd-127">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="e07dd-127">Namespace Name</span></span>

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

### <span data-ttu-id="e07dd-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e07dd-128">-PassThru</span></span>
<span data-ttu-id="e07dd-129">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="e07dd-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="e07dd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e07dd-130">-ResourceGroupName</span></span>
<span data-ttu-id="e07dd-131">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="e07dd-131">The name of the resource group</span></span>

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

### <span data-ttu-id="e07dd-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e07dd-132">-ResourceId</span></span>
<span data-ttu-id="e07dd-133">Service Bus ämne resurs-ID</span><span class="sxs-lookup"><span data-stu-id="e07dd-133">Service Bus Topic Resource Id</span></span>

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

### <span data-ttu-id="e07dd-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e07dd-134">-Confirm</span></span>
<span data-ttu-id="e07dd-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e07dd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e07dd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e07dd-136">-WhatIf</span></span>
<span data-ttu-id="e07dd-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e07dd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e07dd-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e07dd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e07dd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e07dd-139">CommonParameters</span></span>
<span data-ttu-id="e07dd-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e07dd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e07dd-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e07dd-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e07dd-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e07dd-142">INPUTS</span></span>

### <span data-ttu-id="e07dd-143">System. String</span><span class="sxs-lookup"><span data-stu-id="e07dd-143">System.String</span></span>

### <span data-ttu-id="e07dd-144">Microsoft. Azure. commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="e07dd-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="e07dd-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e07dd-145">OUTPUTS</span></span>

### <span data-ttu-id="e07dd-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e07dd-146">System.Boolean</span></span>

## <span data-ttu-id="e07dd-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e07dd-147">NOTES</span></span>

## <span data-ttu-id="e07dd-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e07dd-148">RELATED LINKS</span></span>
