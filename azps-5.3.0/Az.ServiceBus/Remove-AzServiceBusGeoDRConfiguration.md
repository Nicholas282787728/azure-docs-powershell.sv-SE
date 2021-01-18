---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: c226f11eecc7cf046234378be7f0417da301cf40
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525501"
---
# <span data-ttu-id="ee3f9-101">Remove-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee3f9-101">Remove-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="ee3f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ee3f9-102">SYNOPSIS</span></span>
<span data-ttu-id="ee3f9-103">Tar bort ett alias (återställning efter katastrof)</span><span class="sxs-lookup"><span data-stu-id="ee3f9-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="ee3f9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ee3f9-104">SYNTAX</span></span>

### <span data-ttu-id="ee3f9-105">GeoDRPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ee3f9-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee3f9-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ee3f9-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee3f9-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee3f9-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee3f9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ee3f9-108">DESCRIPTION</span></span>
<span data-ttu-id="ee3f9-109">Cmdleten **Remove-AzServiceBusGeoDRConfiguration** tar bort ett alias (konfiguration av katastrof återställning)</span><span class="sxs-lookup"><span data-stu-id="ee3f9-109">The **Remove-AzServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="ee3f9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ee3f9-110">EXAMPLES</span></span>

### <span data-ttu-id="ee3f9-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ee3f9-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="ee3f9-112">Tar bort ett alias (återställning efter katastrof)</span><span class="sxs-lookup"><span data-stu-id="ee3f9-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="ee3f9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ee3f9-113">PARAMETERS</span></span>

### <span data-ttu-id="ee3f9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee3f9-114">-AsJob</span></span>
<span data-ttu-id="ee3f9-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ee3f9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ee3f9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee3f9-116">-DefaultProfile</span></span>
<span data-ttu-id="ee3f9-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ee3f9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee3f9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee3f9-118">-InputObject</span></span>
<span data-ttu-id="ee3f9-119">Service Bus GeoDR konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="ee3f9-119">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="ee3f9-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="ee3f9-120">-Name</span></span>
<span data-ttu-id="ee3f9-121">Alias-namn (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="ee3f9-121">Alias (GeoDR) Name</span></span>

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

### <span data-ttu-id="ee3f9-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="ee3f9-122">-Namespace</span></span>
<span data-ttu-id="ee3f9-123">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="ee3f9-123">Namespace Name</span></span>

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

### <span data-ttu-id="ee3f9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee3f9-124">-PassThru</span></span>
<span data-ttu-id="ee3f9-125">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="ee3f9-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ee3f9-126">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="ee3f9-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ee3f9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee3f9-127">-ResourceGroupName</span></span>
<span data-ttu-id="ee3f9-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="ee3f9-128">Resource Group Name</span></span>

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

### <span data-ttu-id="ee3f9-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee3f9-129">-ResourceId</span></span>
<span data-ttu-id="ee3f9-130">Resurs-ID för GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee3f9-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="ee3f9-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ee3f9-131">-Confirm</span></span>
<span data-ttu-id="ee3f9-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ee3f9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee3f9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee3f9-133">-WhatIf</span></span>
<span data-ttu-id="ee3f9-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ee3f9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee3f9-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ee3f9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee3f9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee3f9-136">CommonParameters</span></span>
<span data-ttu-id="ee3f9-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee3f9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee3f9-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee3f9-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee3f9-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ee3f9-139">INPUTS</span></span>

### <span data-ttu-id="ee3f9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ee3f9-140">System.String</span></span>

### <span data-ttu-id="ee3f9-141">Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="ee3f9-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="ee3f9-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ee3f9-142">OUTPUTS</span></span>

### <span data-ttu-id="ee3f9-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ee3f9-143">System.Boolean</span></span>

## <span data-ttu-id="ee3f9-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ee3f9-144">NOTES</span></span>

## <span data-ttu-id="ee3f9-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ee3f9-145">RELATED LINKS</span></span>
