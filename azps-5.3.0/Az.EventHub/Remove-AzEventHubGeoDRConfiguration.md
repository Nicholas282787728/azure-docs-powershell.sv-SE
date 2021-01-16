---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 57a4ee870e10b04e4c5e58e34122376a790ce6d4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426163"
---
# <span data-ttu-id="f2d53-101">Remove-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="f2d53-101">Remove-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="f2d53-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f2d53-102">SYNOPSIS</span></span>
<span data-ttu-id="f2d53-103">Tar bort ett alias (återställning efter katastrof)</span><span class="sxs-lookup"><span data-stu-id="f2d53-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f2d53-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f2d53-104">SYNTAX</span></span>

### <span data-ttu-id="f2d53-105">GeoDRParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f2d53-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2d53-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f2d53-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2d53-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2d53-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2d53-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f2d53-108">DESCRIPTION</span></span>
<span data-ttu-id="f2d53-109">Cmdleten **Remove-AzEventHubGeoDRConfiguration** tar bort ett alias (konfiguration av katastrof återställning)</span><span class="sxs-lookup"><span data-stu-id="f2d53-109">The **Remove-AzEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f2d53-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f2d53-110">EXAMPLES</span></span>

### <span data-ttu-id="f2d53-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f2d53-111">Example 1</span></span>
```
PS C:\>Remove-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="f2d53-112">Tar bort ett alias (återställning efter katastrof)</span><span class="sxs-lookup"><span data-stu-id="f2d53-112">Deletes an Alias (Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f2d53-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f2d53-113">PARAMETERS</span></span>

### <span data-ttu-id="f2d53-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2d53-114">-AsJob</span></span>
<span data-ttu-id="f2d53-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f2d53-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2d53-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2d53-116">-DefaultProfile</span></span>
<span data-ttu-id="f2d53-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f2d53-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2d53-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2d53-118">-InputObject</span></span>
<span data-ttu-id="f2d53-119">Eventhub-GeoDR</span><span class="sxs-lookup"><span data-stu-id="f2d53-119">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2d53-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="f2d53-120">-Name</span></span>
<span data-ttu-id="f2d53-121">Alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="f2d53-121">Alias (GeoDR)</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2d53-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="f2d53-122">-Namespace</span></span>
<span data-ttu-id="f2d53-123">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="f2d53-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2d53-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2d53-124">-PassThru</span></span>
<span data-ttu-id="f2d53-125">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="f2d53-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f2d53-126">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="f2d53-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f2d53-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2d53-127">-ResourceGroupName</span></span>
<span data-ttu-id="f2d53-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="f2d53-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2d53-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2d53-129">-ResourceId</span></span>
<span data-ttu-id="f2d53-130">Resurs-ID för GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="f2d53-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="f2d53-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f2d53-131">-Confirm</span></span>
<span data-ttu-id="f2d53-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f2d53-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2d53-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2d53-133">-WhatIf</span></span>
<span data-ttu-id="f2d53-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f2d53-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2d53-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f2d53-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2d53-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2d53-136">CommonParameters</span></span>
<span data-ttu-id="f2d53-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2d53-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2d53-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2d53-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2d53-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f2d53-139">INPUTS</span></span>

### <span data-ttu-id="f2d53-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f2d53-140">System.String</span></span>

### <span data-ttu-id="f2d53-141">Microsoft. Azure. commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="f2d53-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="f2d53-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f2d53-142">OUTPUTS</span></span>

### <span data-ttu-id="f2d53-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f2d53-143">System.Boolean</span></span>

## <span data-ttu-id="f2d53-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f2d53-144">NOTES</span></span>

## <span data-ttu-id="f2d53-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f2d53-145">RELATED LINKS</span></span>
