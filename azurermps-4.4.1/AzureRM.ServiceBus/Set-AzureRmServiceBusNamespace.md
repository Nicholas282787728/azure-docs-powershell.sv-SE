---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 134e0d20566a8310a381a38297984202b7509250
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757748"
---
# <span data-ttu-id="abf3a-101">Set-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="abf3a-101">Set-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="abf3a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="abf3a-102">SYNOPSIS</span></span>
<span data-ttu-id="abf3a-103">Uppdaterar beskrivningen av ett befintligt Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="abf3a-103">Updates the description of an existing Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abf3a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="abf3a-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> -Name <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abf3a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="abf3a-105">DESCRIPTION</span></span>
<span data-ttu-id="abf3a-106">Cmdleten **set-AzureRmServiceBusNamespace** uppdaterar beskrivningen av angivet Service Bus-namnrymd i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="abf3a-106">The **Set-AzureRmServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="abf3a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="abf3a-107">EXAMPLES</span></span>

### <span data-ttu-id="abf3a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="abf3a-108">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 10 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 10 , Tier : Standard
ProvisioningState  : Succeeded
Status             :
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
Enabled            : False
```

<span data-ttu-id="abf3a-109">Uppdaterar Service Bus namn området med en ny beskrivning.</span><span class="sxs-lookup"><span data-stu-id="abf3a-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="abf3a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="abf3a-110">PARAMETERS</span></span>

### <span data-ttu-id="abf3a-111">-Plats</span><span class="sxs-lookup"><span data-stu-id="abf3a-111">-Location</span></span>
<span data-ttu-id="abf3a-112">Plats för Service Bus-namnrymden.</span><span class="sxs-lookup"><span data-stu-id="abf3a-112">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="abf3a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abf3a-113">-ResourceGroupName</span></span>
<span data-ttu-id="abf3a-114">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="abf3a-114">The resource group name.</span></span>

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

### <span data-ttu-id="abf3a-115">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="abf3a-115">-SkuCapacity</span></span>
<span data-ttu-id="abf3a-116">Namn på SKU-kapacitet.</span><span class="sxs-lookup"><span data-stu-id="abf3a-116">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="abf3a-117">-SkuName</span><span class="sxs-lookup"><span data-stu-id="abf3a-117">-SkuName</span></span>
<span data-ttu-id="abf3a-118">Namn på SKU-namnet.</span><span class="sxs-lookup"><span data-stu-id="abf3a-118">The namespace SKU name.</span></span>

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

### <span data-ttu-id="abf3a-119">-Tagg</span><span class="sxs-lookup"><span data-stu-id="abf3a-119">-Tag</span></span>
<span data-ttu-id="abf3a-120">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="abf3a-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="abf3a-121">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="abf3a-121">For example:</span></span>

<span data-ttu-id="abf3a-122">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="abf3a-122">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="abf3a-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="abf3a-123">-Confirm</span></span>
<span data-ttu-id="abf3a-124">Uppdaterar Service Bus-namnområdet med angiven information.</span><span class="sxs-lookup"><span data-stu-id="abf3a-124">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="abf3a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abf3a-125">-WhatIf</span></span>
<span data-ttu-id="abf3a-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="abf3a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abf3a-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="abf3a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abf3a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abf3a-128">-DefaultProfile</span></span>
<span data-ttu-id="abf3a-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="abf3a-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abf3a-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="abf3a-130">-Name</span></span>
<span data-ttu-id="abf3a-131">Namn områdes namnet ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="abf3a-131">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abf3a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abf3a-132">CommonParameters</span></span>
<span data-ttu-id="abf3a-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abf3a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abf3a-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abf3a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abf3a-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="abf3a-135">INPUTS</span></span>

### <span data-ttu-id="abf3a-136">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="abf3a-136">-ResourceGroup</span></span>
 <span data-ttu-id="abf3a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="abf3a-137">System.String</span></span>

### <span data-ttu-id="abf3a-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="abf3a-138">-NamespaceName</span></span>
 <span data-ttu-id="abf3a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="abf3a-139">System.String</span></span>

### <span data-ttu-id="abf3a-140">-Plats</span><span class="sxs-lookup"><span data-stu-id="abf3a-140">-Location</span></span>
 <span data-ttu-id="abf3a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="abf3a-141">System.String</span></span>

### <span data-ttu-id="abf3a-142">-SkuName</span><span class="sxs-lookup"><span data-stu-id="abf3a-142">-SkuName</span></span>
 <span data-ttu-id="abf3a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="abf3a-143">System.String</span></span>

### <span data-ttu-id="abf3a-144">-Tagg</span><span class="sxs-lookup"><span data-stu-id="abf3a-144">-Tag</span></span>
 <span data-ttu-id="abf3a-145">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="abf3a-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="abf3a-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="abf3a-146">OUTPUTS</span></span>

### <span data-ttu-id="abf3a-147">Microsoft. Azure. commands. ServiceBus. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="abf3a-147">Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="abf3a-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="abf3a-148">NOTES</span></span>
## <span data-ttu-id="abf3a-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="abf3a-149">RELATED LINKS</span></span>

## <span data-ttu-id="abf3a-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="abf3a-150">RELATED LINKS</span></span>

