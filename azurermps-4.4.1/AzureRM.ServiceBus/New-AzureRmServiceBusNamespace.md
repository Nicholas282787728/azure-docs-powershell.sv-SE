---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 79b55b62c3f4add24e52a36756f83bd16466edbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583779"
---
# <span data-ttu-id="c4b9f-101">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="c4b9f-101">New-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="c4b9f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4b9f-102">SYNOPSIS</span></span>
<span data-ttu-id="c4b9f-103">Skapar ett nytt Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="c4b9f-103">Creates a new Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4b9f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4b9f-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-NamespaceName] <String>
 [-SkuName <String>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4b9f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4b9f-105">DESCRIPTION</span></span>
<span data-ttu-id="c4b9f-106">Cmdleten **New-AzureRmServiceBusNamespace** skapar ett nytt Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="c4b9f-106">The **New-AzureRmServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="c4b9f-107">När namn rymds resursens manifest har skapats är det oföränderligt.</span><span class="sxs-lookup"><span data-stu-id="c4b9f-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="c4b9f-108">Denna åtgärd är idempotent.</span><span class="sxs-lookup"><span data-stu-id="c4b9f-108">This operation is idempotent.</span></span>

## <span data-ttu-id="c4b9f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4b9f-109">EXAMPLES</span></span>

### <span data-ttu-id="c4b9f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c4b9f-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 1 , Tier : Standard
ProvisioningState  : Succeeded
Status             : Active
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
Enabled            : True
```

<span data-ttu-id="c4b9f-111">Skapar ett nytt Service Bus-namnområde i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c4b9f-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="c4b9f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4b9f-112">PARAMETERS</span></span>

### <span data-ttu-id="c4b9f-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="c4b9f-113">-Location</span></span>
<span data-ttu-id="c4b9f-114">Plats för Service Bus-namnrymden.</span><span class="sxs-lookup"><span data-stu-id="c4b9f-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="c4b9f-115">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="c4b9f-115">-NamespaceName</span></span>
<span data-ttu-id="c4b9f-116">Namn på Service Bus-namnrymden.</span><span class="sxs-lookup"><span data-stu-id="c4b9f-116">The Service Bus namespace name.</span></span>

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

### <span data-ttu-id="c4b9f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4b9f-117">-ResourceGroupName</span></span>
<span data-ttu-id="c4b9f-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="c4b9f-118">The resource group name.</span></span>

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

### <span data-ttu-id="c4b9f-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c4b9f-119">-SkuName</span></span>
<span data-ttu-id="c4b9f-120">Service Bus namn områdets SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="c4b9f-120">The Service Bus namespace SKU name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4b9f-121">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c4b9f-121">-Tag</span></span>
<span data-ttu-id="c4b9f-122">Par med nyckelord i en hash-tabell som taggar på servern.</span><span class="sxs-lookup"><span data-stu-id="c4b9f-122">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="c4b9f-123">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="c4b9f-123">For example:</span></span>

<span data-ttu-id="c4b9f-124">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="c4b9f-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4b9f-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c4b9f-125">-Confirm</span></span>
<span data-ttu-id="c4b9f-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c4b9f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4b9f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4b9f-127">-WhatIf</span></span>
<span data-ttu-id="c4b9f-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c4b9f-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4b9f-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c4b9f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4b9f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4b9f-130">CommonParameters</span></span>
<span data-ttu-id="c4b9f-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4b9f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4b9f-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4b9f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4b9f-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4b9f-133">INPUTS</span></span>

### <span data-ttu-id="c4b9f-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c4b9f-134">-ResourceGroup</span></span>
 <span data-ttu-id="c4b9f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c4b9f-135">System.String</span></span>

### <span data-ttu-id="c4b9f-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="c4b9f-136">-NamespaceName</span></span>
 <span data-ttu-id="c4b9f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c4b9f-137">System.String</span></span>

### <span data-ttu-id="c4b9f-138">-Plats</span><span class="sxs-lookup"><span data-stu-id="c4b9f-138">-Location</span></span>
 <span data-ttu-id="c4b9f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c4b9f-139">System.String</span></span>

### <span data-ttu-id="c4b9f-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c4b9f-140">-SkuName</span></span>
 <span data-ttu-id="c4b9f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c4b9f-141">System.String</span></span>

### <span data-ttu-id="c4b9f-142">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c4b9f-142">-Tag</span></span>
 <span data-ttu-id="c4b9f-143">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="c4b9f-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c4b9f-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4b9f-144">OUTPUTS</span></span>

### <span data-ttu-id="c4b9f-145">Microsoft. Azure. commands. ServiceBus. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="c4b9f-145">Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="c4b9f-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4b9f-146">NOTES</span></span>

## <span data-ttu-id="c4b9f-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4b9f-147">RELATED LINKS</span></span>
