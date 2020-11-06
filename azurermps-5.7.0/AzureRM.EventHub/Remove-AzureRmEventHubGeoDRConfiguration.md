---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: 929ebdfb9cc38d5233027da75752f4c82c484536
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577229"
---
# <span data-ttu-id="9e39f-101">Remove-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e39f-101">Remove-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="9e39f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e39f-102">SYNOPSIS</span></span>
<span data-ttu-id="9e39f-103">Tar bort ett alias (återställning efter katastrof)</span><span class="sxs-lookup"><span data-stu-id="9e39f-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e39f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e39f-104">SYNTAX</span></span>

### <span data-ttu-id="9e39f-105">GeoDRParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9e39f-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e39f-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9e39f-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e39f-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e39f-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e39f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e39f-108">DESCRIPTION</span></span>
<span data-ttu-id="9e39f-109">Cmdleten **Remove-AzureRmEventHubGeoDRConfiguration** tar bort ett alias (konfiguration av katastrof återställning)</span><span class="sxs-lookup"><span data-stu-id="9e39f-109">The **Remove-AzureRmEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="9e39f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e39f-110">EXAMPLES</span></span>

### <span data-ttu-id="9e39f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9e39f-111">Example 1</span></span>
```
PS C:\>Remove-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="9e39f-112">Tar bort ett alias (återställning efter katastrof)</span><span class="sxs-lookup"><span data-stu-id="9e39f-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="9e39f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e39f-113">PARAMETERS</span></span>

### <span data-ttu-id="9e39f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e39f-114">-AsJob</span></span>
<span data-ttu-id="9e39f-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9e39f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e39f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e39f-116">-DefaultProfile</span></span>
<span data-ttu-id="9e39f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9e39f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e39f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e39f-118">-InputObject</span></span>
<span data-ttu-id="9e39f-119">Eventhub-GeoDR</span><span class="sxs-lookup"><span data-stu-id="9e39f-119">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e39f-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="9e39f-120">-Name</span></span>
<span data-ttu-id="9e39f-121">Alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="9e39f-121">Alias (GeoDR)</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e39f-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="9e39f-122">-Namespace</span></span>
<span data-ttu-id="9e39f-123">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="9e39f-123">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e39f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e39f-124">-PassThru</span></span>
<span data-ttu-id="9e39f-125">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="9e39f-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9e39f-126">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="9e39f-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9e39f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e39f-127">-ResourceGroupName</span></span>
<span data-ttu-id="9e39f-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="9e39f-128">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e39f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e39f-129">-ResourceId</span></span>
<span data-ttu-id="9e39f-130">Resurs-ID för GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e39f-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="9e39f-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9e39f-131">-Confirm</span></span>
<span data-ttu-id="9e39f-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9e39f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e39f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e39f-133">-WhatIf</span></span>
<span data-ttu-id="9e39f-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9e39f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e39f-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9e39f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e39f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e39f-136">CommonParameters</span></span>
<span data-ttu-id="9e39f-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e39f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9e39f-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e39f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e39f-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e39f-139">INPUTS</span></span>

### <span data-ttu-id="9e39f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9e39f-140">System.String</span></span>
<span data-ttu-id="9e39f-141">Microsoft. Azure. commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="9e39f-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>


## <span data-ttu-id="9e39f-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e39f-142">OUTPUTS</span></span>

### <span data-ttu-id="9e39f-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9e39f-143">System.Boolean</span></span>


## <span data-ttu-id="9e39f-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e39f-144">NOTES</span></span>

## <span data-ttu-id="9e39f-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e39f-145">RELATED LINKS</span></span>
