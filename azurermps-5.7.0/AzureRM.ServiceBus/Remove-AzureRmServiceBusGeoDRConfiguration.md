---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 9c5fe091e5e218c4e70ef1486f1211bc0be7894b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579395"
---
# <span data-ttu-id="933a2-101">Remove-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="933a2-101">Remove-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="933a2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="933a2-102">SYNOPSIS</span></span>
<span data-ttu-id="933a2-103">Tar bort ett alias (återställning efter katastrof)</span><span class="sxs-lookup"><span data-stu-id="933a2-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="933a2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="933a2-104">SYNTAX</span></span>

### <span data-ttu-id="933a2-105">GeoDRBreakPairFailOverPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="933a2-105">GeoDRBreakPairFailOverPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="933a2-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="933a2-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="933a2-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="933a2-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="933a2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="933a2-108">DESCRIPTION</span></span>
<span data-ttu-id="933a2-109">Cmdleten **Remove-AzureRmServiceBusGeoDRConfiguration** tar bort ett alias (konfiguration av katastrof återställning)</span><span class="sxs-lookup"><span data-stu-id="933a2-109">The **Remove-AzureRmServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="933a2-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="933a2-110">EXAMPLES</span></span>

### <span data-ttu-id="933a2-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="933a2-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="933a2-112">Tar bort ett alias (återställning efter katastrof)</span><span class="sxs-lookup"><span data-stu-id="933a2-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="933a2-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="933a2-113">PARAMETERS</span></span>

### <span data-ttu-id="933a2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="933a2-114">-AsJob</span></span>
<span data-ttu-id="933a2-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="933a2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="933a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="933a2-116">-DefaultProfile</span></span>
<span data-ttu-id="933a2-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="933a2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="933a2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="933a2-118">-InputObject</span></span>
<span data-ttu-id="933a2-119">Service Bus GeoDR konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="933a2-119">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="933a2-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="933a2-120">-Name</span></span>
<span data-ttu-id="933a2-121">Alias-namn (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="933a2-121">Alias (GeoDR) Name</span></span>

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

### <span data-ttu-id="933a2-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="933a2-122">-Namespace</span></span>
<span data-ttu-id="933a2-123">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="933a2-123">Namespace Name</span></span>

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

### <span data-ttu-id="933a2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="933a2-124">-PassThru</span></span>
<span data-ttu-id="933a2-125">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="933a2-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="933a2-126">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="933a2-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="933a2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="933a2-127">-ResourceGroupName</span></span>
<span data-ttu-id="933a2-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="933a2-128">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="933a2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="933a2-129">-ResourceId</span></span>
<span data-ttu-id="933a2-130">Resurs-ID för GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="933a2-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="933a2-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="933a2-131">-Confirm</span></span>
<span data-ttu-id="933a2-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="933a2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="933a2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="933a2-133">-WhatIf</span></span>
<span data-ttu-id="933a2-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="933a2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="933a2-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="933a2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="933a2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="933a2-136">CommonParameters</span></span>
<span data-ttu-id="933a2-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="933a2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="933a2-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="933a2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="933a2-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="933a2-139">INPUTS</span></span>

### <span data-ttu-id="933a2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="933a2-140">System.String</span></span>
<span data-ttu-id="933a2-141">Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="933a2-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>


## <span data-ttu-id="933a2-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="933a2-142">OUTPUTS</span></span>

### <span data-ttu-id="933a2-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="933a2-143">System.Boolean</span></span>


## <span data-ttu-id="933a2-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="933a2-144">NOTES</span></span>

## <span data-ttu-id="933a2-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="933a2-145">RELATED LINKS</span></span>
