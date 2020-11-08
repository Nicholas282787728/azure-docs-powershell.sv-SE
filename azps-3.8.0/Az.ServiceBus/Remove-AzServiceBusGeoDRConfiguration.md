---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: c226f11eecc7cf046234378be7f0417da301cf40
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089024"
---
# <span data-ttu-id="35536-101">Remove-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="35536-101">Remove-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="35536-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="35536-102">SYNOPSIS</span></span>
<span data-ttu-id="35536-103">Tar bort ett alias (återställning efter katastrof)</span><span class="sxs-lookup"><span data-stu-id="35536-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="35536-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="35536-104">SYNTAX</span></span>

### <span data-ttu-id="35536-105">GeoDRPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="35536-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35536-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="35536-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35536-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="35536-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35536-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="35536-108">DESCRIPTION</span></span>
<span data-ttu-id="35536-109">Cmdleten **Remove-AzServiceBusGeoDRConfiguration** tar bort ett alias (konfiguration av katastrof återställning)</span><span class="sxs-lookup"><span data-stu-id="35536-109">The **Remove-AzServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="35536-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="35536-110">EXAMPLES</span></span>

### <span data-ttu-id="35536-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="35536-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="35536-112">Tar bort ett alias (återställning efter katastrof)</span><span class="sxs-lookup"><span data-stu-id="35536-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="35536-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="35536-113">PARAMETERS</span></span>

### <span data-ttu-id="35536-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35536-114">-AsJob</span></span>
<span data-ttu-id="35536-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="35536-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35536-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35536-116">-DefaultProfile</span></span>
<span data-ttu-id="35536-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="35536-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35536-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35536-118">-InputObject</span></span>
<span data-ttu-id="35536-119">Service Bus GeoDR konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="35536-119">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="35536-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="35536-120">-Name</span></span>
<span data-ttu-id="35536-121">Alias-namn (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="35536-121">Alias (GeoDR) Name</span></span>

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

### <span data-ttu-id="35536-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="35536-122">-Namespace</span></span>
<span data-ttu-id="35536-123">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="35536-123">Namespace Name</span></span>

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

### <span data-ttu-id="35536-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35536-124">-PassThru</span></span>
<span data-ttu-id="35536-125">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="35536-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="35536-126">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="35536-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="35536-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35536-127">-ResourceGroupName</span></span>
<span data-ttu-id="35536-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="35536-128">Resource Group Name</span></span>

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

### <span data-ttu-id="35536-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35536-129">-ResourceId</span></span>
<span data-ttu-id="35536-130">Resurs-ID för GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="35536-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="35536-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="35536-131">-Confirm</span></span>
<span data-ttu-id="35536-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="35536-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35536-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35536-133">-WhatIf</span></span>
<span data-ttu-id="35536-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="35536-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35536-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="35536-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35536-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35536-136">CommonParameters</span></span>
<span data-ttu-id="35536-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35536-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35536-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35536-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35536-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="35536-139">INPUTS</span></span>

### <span data-ttu-id="35536-140">System. String</span><span class="sxs-lookup"><span data-stu-id="35536-140">System.String</span></span>

### <span data-ttu-id="35536-141">Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="35536-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="35536-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="35536-142">OUTPUTS</span></span>

### <span data-ttu-id="35536-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="35536-143">System.Boolean</span></span>

## <span data-ttu-id="35536-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="35536-144">NOTES</span></span>

## <span data-ttu-id="35536-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="35536-145">RELATED LINKS</span></span>
