---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
ms.openlocfilehash: 1eed6f722487e3c37d9d12785b07e90516406f8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579455"
---
# <span data-ttu-id="1ff6b-101">New-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="1ff6b-101">New-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="1ff6b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1ff6b-102">SYNOPSIS</span></span>
<span data-ttu-id="1ff6b-103">Skapar ett nytt relä namn.</span><span class="sxs-lookup"><span data-stu-id="1ff6b-103">Creates a new Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ff6b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1ff6b-104">SYNTAX</span></span>

```
New-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ff6b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1ff6b-105">DESCRIPTION</span></span>
<span data-ttu-id="1ff6b-106">Cmdleten **New-AzureRmRelayNamespace** skapar ett nytt relä namn.</span><span class="sxs-lookup"><span data-stu-id="1ff6b-106">The **New-AzureRmRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="1ff6b-107">När namn rymds resursens manifest har skapats är det oföränderligt.</span><span class="sxs-lookup"><span data-stu-id="1ff6b-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="1ff6b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1ff6b-108">EXAMPLES</span></span>

### <span data-ttu-id="1ff6b-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1ff6b-109">Example 1</span></span>
```
PS C:\> New-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Location "West US" -Tag @{Tag1="Tag1Value"}

ProvisioningState  : Succeeded
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX:testnamespace-relay1
Location           : West US
Tags               : {[tag1, Tag1Value]}
Id                 : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1
Name               : TestNameSpace-Relay1
Type               : Microsoft.Relay/namespaces
```

<span data-ttu-id="1ff6b-110">Skapar ett nytt relä namn område i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1ff6b-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="1ff6b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1ff6b-111">PARAMETERS</span></span>

### <span data-ttu-id="1ff6b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ff6b-112">-DefaultProfile</span></span>
<span data-ttu-id="1ff6b-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1ff6b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ff6b-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="1ff6b-114">-Location</span></span>
<span data-ttu-id="1ff6b-115">Plats för relä namn.</span><span class="sxs-lookup"><span data-stu-id="1ff6b-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="1ff6b-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="1ff6b-116">-Name</span></span>
<span data-ttu-id="1ff6b-117">Namn område för relä</span><span class="sxs-lookup"><span data-stu-id="1ff6b-117">Relay Namespace Name</span></span>

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

### <span data-ttu-id="1ff6b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ff6b-118">-ResourceGroupName</span></span>
<span data-ttu-id="1ff6b-119">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="1ff6b-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="1ff6b-120">-Tagg</span><span class="sxs-lookup"><span data-stu-id="1ff6b-120">-Tag</span></span>
<span data-ttu-id="1ff6b-121">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="1ff6b-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1ff6b-122">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="1ff6b-122">For example:</span></span>

<span data-ttu-id="1ff6b-123">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="1ff6b-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1ff6b-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1ff6b-124">-Confirm</span></span>
<span data-ttu-id="1ff6b-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1ff6b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ff6b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ff6b-126">-WhatIf</span></span>
<span data-ttu-id="1ff6b-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1ff6b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ff6b-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1ff6b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ff6b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ff6b-129">CommonParameters</span></span>
<span data-ttu-id="1ff6b-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ff6b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ff6b-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ff6b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ff6b-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1ff6b-132">INPUTS</span></span>

### <span data-ttu-id="1ff6b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ff6b-133">-ResourceGroupName</span></span>
 <span data-ttu-id="1ff6b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1ff6b-134">System.String</span></span>

### <span data-ttu-id="1ff6b-135">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="1ff6b-135">-NamespaceName</span></span>
 <span data-ttu-id="1ff6b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1ff6b-136">System.String</span></span>

### <span data-ttu-id="1ff6b-137">-Plats</span><span class="sxs-lookup"><span data-stu-id="1ff6b-137">-Location</span></span>
 <span data-ttu-id="1ff6b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1ff6b-138">System.String</span></span>

### <span data-ttu-id="1ff6b-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1ff6b-139">-SkuName</span></span>
 <span data-ttu-id="1ff6b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1ff6b-140">System.String</span></span>

### <span data-ttu-id="1ff6b-141">-Tagg</span><span class="sxs-lookup"><span data-stu-id="1ff6b-141">-Tag</span></span>
 <span data-ttu-id="1ff6b-142">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="1ff6b-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1ff6b-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1ff6b-143">OUTPUTS</span></span>

### <span data-ttu-id="1ff6b-144">Microsoft. Azure. commands. Relay. Models. RelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="1ff6b-144">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="1ff6b-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1ff6b-145">NOTES</span></span>

## <span data-ttu-id="1ff6b-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1ff6b-146">RELATED LINKS</span></span>

