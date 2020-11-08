---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
ms.openlocfilehash: e9f228b284b690681b2a4d55eb436e4062d7c861
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092034"
---
# <span data-ttu-id="3b916-101">Set-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="3b916-101">Set-AzServiceBusNamespace</span></span>

## <span data-ttu-id="3b916-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3b916-102">SYNOPSIS</span></span>
<span data-ttu-id="3b916-103">Uppdaterar beskrivningen av ett befintligt Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="3b916-103">Updates the description of an existing Service Bus namespace.</span></span>

## <span data-ttu-id="3b916-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3b916-104">SYNTAX</span></span>

```
Set-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b916-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3b916-105">DESCRIPTION</span></span>
<span data-ttu-id="3b916-106">Cmdleten **set-AzServiceBusNamespace** uppdaterar beskrivningen av angivet Service Bus-namnrymd i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3b916-106">The **Set-AzServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="3b916-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3b916-107">EXAMPLES</span></span>

### <span data-ttu-id="3b916-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3b916-108">Example 1</span></span>
```
PS C:\> Set-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 1 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {Tag2, Tag2Value}
Sku                : Name : Premium , Tier : Premium, Capacity : 1
ProvisioningState  : Succeeded
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
```

<span data-ttu-id="3b916-109">Uppdaterar Service Bus namn området med en ny beskrivning.</span><span class="sxs-lookup"><span data-stu-id="3b916-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="3b916-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3b916-110">PARAMETERS</span></span>

### <span data-ttu-id="3b916-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b916-111">-DefaultProfile</span></span>
<span data-ttu-id="3b916-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3b916-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b916-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="3b916-113">-Location</span></span>
<span data-ttu-id="3b916-114">Plats för Service Bus-namnrymden.</span><span class="sxs-lookup"><span data-stu-id="3b916-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="3b916-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="3b916-115">-Name</span></span>
<span data-ttu-id="3b916-116">Namn områdes namnet ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="3b916-116">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="3b916-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b916-117">-ResourceGroupName</span></span>
<span data-ttu-id="3b916-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="3b916-118">The resource group name.</span></span>

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

### <span data-ttu-id="3b916-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="3b916-119">-SkuCapacity</span></span>
<span data-ttu-id="3b916-120">Namn på SKU-kapacitet.</span><span class="sxs-lookup"><span data-stu-id="3b916-120">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="3b916-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3b916-121">-SkuName</span></span>
<span data-ttu-id="3b916-122">Namn på SKU-namnet.</span><span class="sxs-lookup"><span data-stu-id="3b916-122">The namespace SKU name.</span></span>

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

### <span data-ttu-id="3b916-123">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3b916-123">-Tag</span></span>
<span data-ttu-id="3b916-124">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="3b916-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3b916-125">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="3b916-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3b916-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3b916-126">-Confirm</span></span>
<span data-ttu-id="3b916-127">Uppdaterar Service Bus-namnområdet med angiven information.</span><span class="sxs-lookup"><span data-stu-id="3b916-127">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="3b916-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b916-128">-WhatIf</span></span>
<span data-ttu-id="3b916-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3b916-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b916-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3b916-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b916-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b916-131">CommonParameters</span></span>
<span data-ttu-id="3b916-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b916-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b916-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b916-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b916-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3b916-134">INPUTS</span></span>

### <span data-ttu-id="3b916-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3b916-135">System.String</span></span>

### <span data-ttu-id="3b916-136">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3b916-136">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3b916-137">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="3b916-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3b916-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3b916-138">OUTPUTS</span></span>

### <span data-ttu-id="3b916-139">Microsoft. Azure. commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="3b916-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="3b916-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3b916-140">NOTES</span></span>

## <span data-ttu-id="3b916-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3b916-141">RELATED LINKS</span></span>
