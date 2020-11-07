---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 07b5de12e042c81bb5f27c844d1fc8962453310a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758084"
---
# <span data-ttu-id="faee8-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="faee8-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="faee8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="faee8-102">SYNOPSIS</span></span>
<span data-ttu-id="faee8-103">Skapar ett namn område för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="faee8-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="faee8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="faee8-104">SYNTAX</span></span>

### <span data-ttu-id="faee8-105">NamespaceParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="faee8-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="faee8-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="faee8-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-EnableAutoInflate]
 [-MaximumThroughputUnits] <Int32> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="faee8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="faee8-107">DESCRIPTION</span></span>
<span data-ttu-id="faee8-108">New-AzureRmEventHubNamespace-cmdleten skapar ett nytt namn område av typen Event Hub.</span><span class="sxs-lookup"><span data-stu-id="faee8-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="faee8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="faee8-109">EXAMPLES</span></span>

### <span data-ttu-id="faee8-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="faee8-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation 
```

<span data-ttu-id="faee8-111">Skapar en namnrymd för händelse nav \` MyNamespaceName \` på min plats med geografisk plats \` \` i MyResourceGroupName för resurs \` grupp \` .</span><span class="sxs-lookup"><span data-stu-id="faee8-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="faee8-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="faee8-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="faee8-113">Skapar namn områdes \` MyNamespaceName för Event Hub \` på den angivna geografiska platsen min \` plats \` , i resurs grupp \` MyResourceGroupName \` och automittre är aktiverat med MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="faee8-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

## <span data-ttu-id="faee8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="faee8-114">PARAMETERS</span></span>

### <span data-ttu-id="faee8-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="faee8-115">-Location</span></span>
<span data-ttu-id="faee8-116">Namn område för händelse nav Geo-Location.</span><span class="sxs-lookup"><span data-stu-id="faee8-116">Event Hubs namespace geo-location.</span></span>

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

### <span data-ttu-id="faee8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faee8-117">-ResourceGroupName</span></span>
<span data-ttu-id="faee8-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="faee8-118">Resource group name.</span></span>

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

### <span data-ttu-id="faee8-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="faee8-119">-SkuCapacity</span></span>
<span data-ttu-id="faee8-120">Data flödes enheter för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="faee8-120">The Event Hub throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="faee8-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="faee8-121">-SkuName</span></span>
<span data-ttu-id="faee8-122">Namn på SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="faee8-122">Namespace Sku name.</span></span>

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

### <span data-ttu-id="faee8-123">-Tagg</span><span class="sxs-lookup"><span data-stu-id="faee8-123">-Tag</span></span>
<span data-ttu-id="faee8-124">Hashtables som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="faee8-124">Hashtables that represent resource tags.</span></span>

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

### <span data-ttu-id="faee8-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="faee8-125">-Confirm</span></span>
<span data-ttu-id="faee8-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="faee8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faee8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faee8-127">-WhatIf</span></span>
<span data-ttu-id="faee8-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="faee8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faee8-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="faee8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faee8-130">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="faee8-130">-EnableAutoInflate</span></span>
<span data-ttu-id="faee8-131">Anger om autoöka-funktionen är aktive rad</span><span class="sxs-lookup"><span data-stu-id="faee8-131">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: NamespaceParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faee8-132">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="faee8-132">-MaximumThroughputUnits</span></span>
<span data-ttu-id="faee8-133">Övre gräns för flödes enheter när automittre är aktiverat ska Vaule vara inom 0 till 20 data flödes enheter.</span><span class="sxs-lookup"><span data-stu-id="faee8-133">Upper limit of throughput units when AutoInflate is enabled, vaule should be within 0 to 20 throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="faee8-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="faee8-134">-Name</span></span>
<span data-ttu-id="faee8-135">Namn område för EventHub.</span><span class="sxs-lookup"><span data-stu-id="faee8-135">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="faee8-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="faee8-136">INPUTS</span></span>

### <span data-ttu-id="faee8-137">System. String</span><span class="sxs-lookup"><span data-stu-id="faee8-137">System.String</span></span>
<span data-ttu-id="faee8-138">System. Nullable \` 1 \[ \[ system. Int32, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = B77a5c561934e089 \] \] system. Nullable \` 1 \[ \[ system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089 \] \] system. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="faee8-138">System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Collections.Hashtable</span></span>

## <span data-ttu-id="faee8-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="faee8-139">OUTPUTS</span></span>

### <span data-ttu-id="faee8-140">Microsoft. Azure. commands. EventHub. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="faee8-140">Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="faee8-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="faee8-141">NOTES</span></span>

## <span data-ttu-id="faee8-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="faee8-142">RELATED LINKS</span></span>

