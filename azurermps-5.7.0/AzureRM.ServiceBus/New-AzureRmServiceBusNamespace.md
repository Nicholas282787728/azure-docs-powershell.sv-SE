---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 1834adfdb275bc5454e16e72732b649c82704a34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579407"
---
# <span data-ttu-id="81b2c-101">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="81b2c-101">New-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="81b2c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="81b2c-102">SYNOPSIS</span></span>
<span data-ttu-id="81b2c-103">Skapar ett nytt Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="81b2c-103">Creates a new Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81b2c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="81b2c-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81b2c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="81b2c-105">DESCRIPTION</span></span>
<span data-ttu-id="81b2c-106">Cmdleten **New-AzureRmServiceBusNamespace** skapar ett nytt Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="81b2c-106">The **New-AzureRmServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="81b2c-107">När namn rymds resursens manifest har skapats är det oföränderligt.</span><span class="sxs-lookup"><span data-stu-id="81b2c-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="81b2c-108">Denna åtgärd är idempotent.</span><span class="sxs-lookup"><span data-stu-id="81b2c-108">This operation is idempotent.</span></span>

## <span data-ttu-id="81b2c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="81b2c-109">EXAMPLES</span></span>

### <span data-ttu-id="81b2c-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="81b2c-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 1 , Tier : Standard
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="81b2c-111">Skapar ett nytt Service Bus-namnområde i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="81b2c-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="81b2c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="81b2c-112">PARAMETERS</span></span>

### <span data-ttu-id="81b2c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81b2c-113">-DefaultProfile</span></span>
<span data-ttu-id="81b2c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="81b2c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81b2c-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="81b2c-115">-Location</span></span>
<span data-ttu-id="81b2c-116">Plats för Service Bus-namnrymden.</span><span class="sxs-lookup"><span data-stu-id="81b2c-116">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="81b2c-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="81b2c-117">-Name</span></span>
<span data-ttu-id="81b2c-118">Namn områdes namnet ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="81b2c-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81b2c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81b2c-119">-ResourceGroupName</span></span>
<span data-ttu-id="81b2c-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="81b2c-120">The resource group name.</span></span>

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

### <span data-ttu-id="81b2c-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="81b2c-121">-SkuName</span></span>
<span data-ttu-id="81b2c-122">Service Bus namn områdets SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="81b2c-122">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="81b2c-123">-Tagg</span><span class="sxs-lookup"><span data-stu-id="81b2c-123">-Tag</span></span>
<span data-ttu-id="81b2c-124">Par med nyckelord i en hash-tabell som taggar på servern.</span><span class="sxs-lookup"><span data-stu-id="81b2c-124">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="81b2c-125">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="81b2c-125">For example:</span></span>

<span data-ttu-id="81b2c-126">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="81b2c-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="81b2c-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="81b2c-127">-Confirm</span></span>
<span data-ttu-id="81b2c-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="81b2c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81b2c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81b2c-129">-WhatIf</span></span>
<span data-ttu-id="81b2c-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="81b2c-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81b2c-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="81b2c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81b2c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81b2c-132">CommonParameters</span></span>
<span data-ttu-id="81b2c-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81b2c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81b2c-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81b2c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81b2c-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="81b2c-135">INPUTS</span></span>

### <span data-ttu-id="81b2c-136">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="81b2c-136">-ResourceGroup</span></span>
 <span data-ttu-id="81b2c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="81b2c-137">System.String</span></span>

### <span data-ttu-id="81b2c-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="81b2c-138">-NamespaceName</span></span>
 <span data-ttu-id="81b2c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="81b2c-139">System.String</span></span>

### <span data-ttu-id="81b2c-140">-Plats</span><span class="sxs-lookup"><span data-stu-id="81b2c-140">-Location</span></span>
 <span data-ttu-id="81b2c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="81b2c-141">System.String</span></span>

### <span data-ttu-id="81b2c-142">-SkuName</span><span class="sxs-lookup"><span data-stu-id="81b2c-142">-SkuName</span></span>
 <span data-ttu-id="81b2c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="81b2c-143">System.String</span></span>

### <span data-ttu-id="81b2c-144">-Tagg</span><span class="sxs-lookup"><span data-stu-id="81b2c-144">-Tag</span></span>
 <span data-ttu-id="81b2c-145">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="81b2c-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="81b2c-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="81b2c-146">OUTPUTS</span></span>

### <span data-ttu-id="81b2c-147">Microsoft. Azure. commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="81b2c-147">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="81b2c-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="81b2c-148">NOTES</span></span>

## <span data-ttu-id="81b2c-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="81b2c-149">RELATED LINKS</span></span>

