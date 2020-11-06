---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
ms.openlocfilehash: 2d944b629a72a8b97bf1bd639ced79d9bd1eab02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580432"
---
# <span data-ttu-id="8098b-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="8098b-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="8098b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8098b-102">SYNOPSIS</span></span>
<span data-ttu-id="8098b-103">Skapar ett namn område för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="8098b-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8098b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8098b-104">SYNTAX</span></span>

### <span data-ttu-id="8098b-105">NamespaceParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8098b-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8098b-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="8098b-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8098b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8098b-107">DESCRIPTION</span></span>
<span data-ttu-id="8098b-108">New-AzureRmEventHubNamespace-cmdleten skapar ett nytt namn område av typen Event Hub.</span><span class="sxs-lookup"><span data-stu-id="8098b-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="8098b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8098b-109">EXAMPLES</span></span>

### <span data-ttu-id="8098b-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8098b-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation
```

<span data-ttu-id="8098b-111">Skapar en namnrymd för händelse nav \` MyNamespaceName \` på min plats med geografisk plats \` \` i MyResourceGroupName för resurs \` grupp \` .</span><span class="sxs-lookup"><span data-stu-id="8098b-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="8098b-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8098b-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="8098b-113">Skapar namn områdes \` MyNamespaceName för Event Hub \` på den angivna geografiska platsen min \` plats \` , i resurs grupp \` MyResourceGroupName \` och automittre är aktiverat med MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="8098b-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

## <span data-ttu-id="8098b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8098b-114">PARAMETERS</span></span>

### <span data-ttu-id="8098b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8098b-115">-DefaultProfile</span></span>
<span data-ttu-id="8098b-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8098b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8098b-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="8098b-117">-EnableAutoInflate</span></span>
<span data-ttu-id="8098b-118">Anger om autoöka-funktionen är aktive rad</span><span class="sxs-lookup"><span data-stu-id="8098b-118">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8098b-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="8098b-119">-Location</span></span>
<span data-ttu-id="8098b-120">Plats för EventHub-namnrymd.</span><span class="sxs-lookup"><span data-stu-id="8098b-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="8098b-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="8098b-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="8098b-122">Övre gräns för flödes enheter när automittre är aktiverat ska värdet vara inom 0 till 20 data flödes enheter.</span><span class="sxs-lookup"><span data-stu-id="8098b-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8098b-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="8098b-123">-Name</span></span>
<span data-ttu-id="8098b-124">Namn område för EventHub.</span><span class="sxs-lookup"><span data-stu-id="8098b-124">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8098b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8098b-125">-ResourceGroupName</span></span>
<span data-ttu-id="8098b-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="8098b-126">Resource Group Name</span></span>

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

### <span data-ttu-id="8098b-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="8098b-127">-SkuCapacity</span></span>
<span data-ttu-id="8098b-128">Eventhub-dataflöden.</span><span class="sxs-lookup"><span data-stu-id="8098b-128">The eventhub throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8098b-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8098b-129">-SkuName</span></span>
<span data-ttu-id="8098b-130">Namn på SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="8098b-130">Namespace Sku Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8098b-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="8098b-131">-Tag</span></span>
<span data-ttu-id="8098b-132">Hashtables som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="8098b-132">Hashtables which represents resource Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8098b-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8098b-133">-Confirm</span></span>
<span data-ttu-id="8098b-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8098b-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8098b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8098b-135">-WhatIf</span></span>
<span data-ttu-id="8098b-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8098b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8098b-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8098b-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8098b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8098b-138">CommonParameters</span></span>
<span data-ttu-id="8098b-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8098b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8098b-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8098b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8098b-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8098b-141">INPUTS</span></span>

### <span data-ttu-id="8098b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="8098b-142">System.String</span></span>
<span data-ttu-id="8098b-143">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] system. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="8098b-143">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable</span></span>


## <span data-ttu-id="8098b-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8098b-144">OUTPUTS</span></span>

### <span data-ttu-id="8098b-145">Microsoft. Azure. commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="8098b-145">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="8098b-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8098b-146">NOTES</span></span>

## <span data-ttu-id="8098b-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8098b-147">RELATED LINKS</span></span>
