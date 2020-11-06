---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 581f3c24c8c195b1cafc4962d1c6319418cc07f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576072"
---
# <span data-ttu-id="116fc-101">Remove-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="116fc-101">Remove-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="116fc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="116fc-102">SYNOPSIS</span></span>
<span data-ttu-id="116fc-103">Tar bort ett alias (återställning efter katastrof)</span><span class="sxs-lookup"><span data-stu-id="116fc-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="116fc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="116fc-104">SYNTAX</span></span>

### <span data-ttu-id="116fc-105">GeoDRPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="116fc-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="116fc-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="116fc-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="116fc-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="116fc-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="116fc-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="116fc-108">DESCRIPTION</span></span>
<span data-ttu-id="116fc-109">Cmdleten **Remove-AzureRmServiceBusGeoDRConfiguration** tar bort ett alias (konfiguration av katastrof återställning)</span><span class="sxs-lookup"><span data-stu-id="116fc-109">The **Remove-AzureRmServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="116fc-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="116fc-110">EXAMPLES</span></span>

### <span data-ttu-id="116fc-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="116fc-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="116fc-112">Tar bort ett alias (återställning efter katastrof)</span><span class="sxs-lookup"><span data-stu-id="116fc-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="116fc-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="116fc-113">PARAMETERS</span></span>

### <span data-ttu-id="116fc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="116fc-114">-AsJob</span></span>
<span data-ttu-id="116fc-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="116fc-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="116fc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="116fc-116">-DefaultProfile</span></span>
<span data-ttu-id="116fc-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="116fc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="116fc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="116fc-118">-InputObject</span></span>
<span data-ttu-id="116fc-119">Service Bus GeoDR konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="116fc-119">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="116fc-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="116fc-120">-Name</span></span>
<span data-ttu-id="116fc-121">Alias-namn (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="116fc-121">Alias (GeoDR) Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="116fc-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="116fc-122">-Namespace</span></span>
<span data-ttu-id="116fc-123">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="116fc-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="116fc-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="116fc-124">-PassThru</span></span>
<span data-ttu-id="116fc-125">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="116fc-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="116fc-126">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="116fc-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="116fc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="116fc-127">-ResourceGroupName</span></span>
<span data-ttu-id="116fc-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="116fc-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="116fc-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="116fc-129">-ResourceId</span></span>
<span data-ttu-id="116fc-130">Resurs-ID för GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="116fc-130">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="116fc-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="116fc-131">-Confirm</span></span>
<span data-ttu-id="116fc-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="116fc-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="116fc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="116fc-133">-WhatIf</span></span>
<span data-ttu-id="116fc-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="116fc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="116fc-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="116fc-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="116fc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="116fc-136">CommonParameters</span></span>
<span data-ttu-id="116fc-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="116fc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="116fc-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="116fc-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="116fc-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="116fc-139">INPUTS</span></span>

### <span data-ttu-id="116fc-140">System. String</span><span class="sxs-lookup"><span data-stu-id="116fc-140">System.String</span></span>

### <span data-ttu-id="116fc-141">Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="116fc-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="116fc-142">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="116fc-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="116fc-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="116fc-143">OUTPUTS</span></span>

### <span data-ttu-id="116fc-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="116fc-144">System.Boolean</span></span>

## <span data-ttu-id="116fc-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="116fc-145">NOTES</span></span>

## <span data-ttu-id="116fc-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="116fc-146">RELATED LINKS</span></span>
