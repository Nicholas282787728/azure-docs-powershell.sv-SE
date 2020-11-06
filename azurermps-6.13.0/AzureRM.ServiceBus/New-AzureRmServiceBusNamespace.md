---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 532135578418a90e9ce6887602723c2165f28aa3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579983"
---
# <span data-ttu-id="a463f-101">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="a463f-101">New-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="a463f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a463f-102">SYNOPSIS</span></span>
<span data-ttu-id="a463f-103">Skapar ett nytt Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="a463f-103">Creates a new Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a463f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a463f-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a463f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a463f-105">DESCRIPTION</span></span>
<span data-ttu-id="a463f-106">Cmdleten **New-AzureRmServiceBusNamespace** skapar ett nytt Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="a463f-106">The **New-AzureRmServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="a463f-107">När namn rymds resursens manifest har skapats är det oföränderligt.</span><span class="sxs-lookup"><span data-stu-id="a463f-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="a463f-108">Denna åtgärd är idempotent.</span><span class="sxs-lookup"><span data-stu-id="a463f-108">This operation is idempotent.</span></span>

## <span data-ttu-id="a463f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a463f-109">EXAMPLES</span></span>

### <span data-ttu-id="a463f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a463f-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/{SubscriptionId}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroup      : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="a463f-111">Skapar ett nytt Service Bus-namnområde i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a463f-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="a463f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a463f-112">PARAMETERS</span></span>

### <span data-ttu-id="a463f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a463f-113">-DefaultProfile</span></span>
<span data-ttu-id="a463f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a463f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a463f-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="a463f-115">-Location</span></span>
<span data-ttu-id="a463f-116">Plats för Service Bus-namnrymden.</span><span class="sxs-lookup"><span data-stu-id="a463f-116">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="a463f-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="a463f-117">-Name</span></span>
<span data-ttu-id="a463f-118">Namn områdes namnet ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="a463f-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="a463f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a463f-119">-ResourceGroupName</span></span>
<span data-ttu-id="a463f-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="a463f-120">The resource group name.</span></span>

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

### <span data-ttu-id="a463f-121">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="a463f-121">-SkuCapacity</span></span>
<span data-ttu-id="a463f-122">Data flödes enheterna för Service Bus Premium namespace, tillåtna värden 1 eller 4</span><span class="sxs-lookup"><span data-stu-id="a463f-122">The Service Bus premium namespace throughput units, allowed values 1 or 2 or 4</span></span>

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

### <span data-ttu-id="a463f-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a463f-123">-SkuName</span></span>
<span data-ttu-id="a463f-124">Service Bus namn områdets SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="a463f-124">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="a463f-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a463f-125">-Tag</span></span>
<span data-ttu-id="a463f-126">Par med nyckelord i en hash-tabell som taggar på servern.</span><span class="sxs-lookup"><span data-stu-id="a463f-126">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="a463f-127">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="a463f-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a463f-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a463f-128">-Confirm</span></span>
<span data-ttu-id="a463f-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a463f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a463f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a463f-130">-WhatIf</span></span>
<span data-ttu-id="a463f-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a463f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a463f-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a463f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a463f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a463f-133">CommonParameters</span></span>
<span data-ttu-id="a463f-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a463f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a463f-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a463f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a463f-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a463f-136">INPUTS</span></span>

### <span data-ttu-id="a463f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a463f-137">System.String</span></span>

### <span data-ttu-id="a463f-138">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a463f-138">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="a463f-139">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="a463f-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a463f-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a463f-140">OUTPUTS</span></span>

### <span data-ttu-id="a463f-141">Microsoft. Azure. commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a463f-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="a463f-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a463f-142">NOTES</span></span>

## <span data-ttu-id="a463f-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a463f-143">RELATED LINKS</span></span>
