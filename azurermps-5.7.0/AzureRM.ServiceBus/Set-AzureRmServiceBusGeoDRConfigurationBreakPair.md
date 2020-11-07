---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationBreakPair.md
ms.openlocfilehash: da4df1206035e5ecae1a21d70e67091e852b1c51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756066"
---
# <span data-ttu-id="2ea62-101">Set-AzureRmServiceBusGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="2ea62-101">Set-AzureRmServiceBusGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="2ea62-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2ea62-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea62-103">Den här åtgärden inaktiverar katastrof återställning och upphör att replikera ändringar från primära till sekundära namn områden</span><span class="sxs-lookup"><span data-stu-id="2ea62-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ea62-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2ea62-104">SYNTAX</span></span>

### <span data-ttu-id="2ea62-105">GeoDRBreakPairFailOverPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2ea62-105">GeoDRBreakPairFailOverPropertiesSet (Default)</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ea62-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2ea62-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-InputObject] <PSServiceBusDRConfigurationAttributes>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ea62-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ea62-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ea62-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2ea62-108">DESCRIPTION</span></span>
<span data-ttu-id="2ea62-109">Cmdleten **set-AzureRmServiceBusGeoDRConfigurationBreakPair** inaktiverar katastrof återställning och slutar replikera ändringar från primära till sekundära namn områden</span><span class="sxs-lookup"><span data-stu-id="2ea62-109">The **Set-AzureRmServiceBusGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="2ea62-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2ea62-110">EXAMPLES</span></span>

### <span data-ttu-id="2ea62-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2ea62-111">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"
```

<span data-ttu-id="2ea62-112">Den här åtgärden inaktiverar katastrof återställning och upphör att replikera ändringar från primära till sekundära namn områden</span><span class="sxs-lookup"><span data-stu-id="2ea62-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="2ea62-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2ea62-113">PARAMETERS</span></span>

### <span data-ttu-id="2ea62-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ea62-114">-DefaultProfile</span></span>
<span data-ttu-id="2ea62-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2ea62-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ea62-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ea62-116">-InputObject</span></span>
<span data-ttu-id="2ea62-117">Service Bus GeoDR konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="2ea62-117">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea62-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="2ea62-118">-Name</span></span>
<span data-ttu-id="2ea62-119">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="2ea62-119">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea62-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="2ea62-120">-Namespace</span></span>
<span data-ttu-id="2ea62-121">Namn områdes namn – primär namnrymd</span><span class="sxs-lookup"><span data-stu-id="2ea62-121">Namespace Name - Primary Namespace</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea62-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ea62-122">-PassThru</span></span>
<span data-ttu-id="2ea62-123">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="2ea62-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2ea62-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="2ea62-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea62-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ea62-125">-ResourceGroupName</span></span>
<span data-ttu-id="2ea62-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="2ea62-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea62-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ea62-127">-ResourceId</span></span>
<span data-ttu-id="2ea62-128">Resurs-ID för GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ea62-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea62-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2ea62-129">-Confirm</span></span>
<span data-ttu-id="2ea62-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2ea62-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ea62-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ea62-131">-WhatIf</span></span>
<span data-ttu-id="2ea62-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2ea62-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ea62-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2ea62-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ea62-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea62-134">CommonParameters</span></span>
<span data-ttu-id="2ea62-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ea62-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2ea62-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ea62-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea62-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2ea62-137">INPUTS</span></span>

### <span data-ttu-id="2ea62-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2ea62-138">System.String</span></span>
<span data-ttu-id="2ea62-139">Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="2ea62-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>


## <span data-ttu-id="2ea62-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2ea62-140">OUTPUTS</span></span>

### <span data-ttu-id="2ea62-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2ea62-141">System.Boolean</span></span>


## <span data-ttu-id="2ea62-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2ea62-142">NOTES</span></span>

## <span data-ttu-id="2ea62-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2ea62-143">RELATED LINKS</span></span>
