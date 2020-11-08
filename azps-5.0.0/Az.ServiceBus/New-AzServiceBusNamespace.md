---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
ms.openlocfilehash: 9ef77d9a02f2337aac2886cf033cfa752463e8d2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270063"
---
# <span data-ttu-id="535f4-101">New-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="535f4-101">New-AzServiceBusNamespace</span></span>

## <span data-ttu-id="535f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="535f4-102">SYNOPSIS</span></span>
<span data-ttu-id="535f4-103">Skapar ett nytt Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="535f4-103">Creates a new Service Bus namespace.</span></span>

## <span data-ttu-id="535f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="535f4-104">SYNTAX</span></span>

```
New-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="535f4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="535f4-105">DESCRIPTION</span></span>
<span data-ttu-id="535f4-106">Cmdleten **New-AzServiceBusNamespace** skapar ett nytt Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="535f4-106">The **New-AzServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="535f4-107">När namn rymds resursens manifest har skapats är det oföränderligt.</span><span class="sxs-lookup"><span data-stu-id="535f4-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="535f4-108">Denna åtgärd är idempotent.</span><span class="sxs-lookup"><span data-stu-id="535f4-108">This operation is idempotent.</span></span>

## <span data-ttu-id="535f4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="535f4-109">EXAMPLES</span></span>

### <span data-ttu-id="535f4-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="535f4-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/{SubscriptionId}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="535f4-111">Skapar ett nytt Service Bus-namnområde i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="535f4-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="535f4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="535f4-112">PARAMETERS</span></span>

### <span data-ttu-id="535f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="535f4-113">-DefaultProfile</span></span>
<span data-ttu-id="535f4-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="535f4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="535f4-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="535f4-115">-Location</span></span>
<span data-ttu-id="535f4-116">Plats för Service Bus-namnrymden.</span><span class="sxs-lookup"><span data-stu-id="535f4-116">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="535f4-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="535f4-117">-Name</span></span>
<span data-ttu-id="535f4-118">Namn områdes namnet ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="535f4-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="535f4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="535f4-119">-ResourceGroupName</span></span>
<span data-ttu-id="535f4-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="535f4-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="535f4-121">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="535f4-121">-SkuCapacity</span></span>
<span data-ttu-id="535f4-122">Data flödes enheterna för Service Bus Premium namespace, tillåtna värden 1 eller 4</span><span class="sxs-lookup"><span data-stu-id="535f4-122">The Service Bus premium namespace throughput units, allowed values 1 or 2 or 4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="535f4-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="535f4-123">-SkuName</span></span>
<span data-ttu-id="535f4-124">Service Bus namn områdets SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="535f4-124">The Service Bus namespace SKU name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="535f4-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="535f4-125">-Tag</span></span>
<span data-ttu-id="535f4-126">Par med nyckelord i en hash-tabell som taggar på servern.</span><span class="sxs-lookup"><span data-stu-id="535f4-126">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="535f4-127">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="535f4-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="535f4-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="535f4-128">-Confirm</span></span>
<span data-ttu-id="535f4-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="535f4-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="535f4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="535f4-130">-WhatIf</span></span>
<span data-ttu-id="535f4-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="535f4-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="535f4-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="535f4-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="535f4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="535f4-133">CommonParameters</span></span>
<span data-ttu-id="535f4-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="535f4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="535f4-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="535f4-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="535f4-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="535f4-136">INPUTS</span></span>

### <span data-ttu-id="535f4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="535f4-137">System.String</span></span>

### <span data-ttu-id="535f4-138">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="535f4-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="535f4-139">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="535f4-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="535f4-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="535f4-140">OUTPUTS</span></span>

### <span data-ttu-id="535f4-141">Microsoft. Azure. commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="535f4-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="535f4-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="535f4-142">NOTES</span></span>

## <span data-ttu-id="535f4-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="535f4-143">RELATED LINKS</span></span>
