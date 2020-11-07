---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: 0da9ecf9fabaa1cbb21a5fe8f82bb172b84850e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755762"
---
# <span data-ttu-id="c2f65-101">Set-AzureRmEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="c2f65-101">Set-AzureRmEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="c2f65-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2f65-102">SYNOPSIS</span></span>
<span data-ttu-id="c2f65-103">Anropar GEO-failover och konfigurerar om aliaset så att det pekar på det sekundära namn området</span><span class="sxs-lookup"><span data-stu-id="c2f65-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2f65-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2f65-104">SYNTAX</span></span>

### <span data-ttu-id="c2f65-105">GeoDRParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c2f65-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2f65-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c2f65-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2f65-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2f65-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2f65-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2f65-108">DESCRIPTION</span></span>
<span data-ttu-id="c2f65-109">Cmdleten **set-AzureRmEventHubGeoDRConfigurationFailOver** -ENVOKES geo Dr och konfigurera om aliaset så att det pekar på det sekundära namn området</span><span class="sxs-lookup"><span data-stu-id="c2f65-109">The **Set-AzureRmEventHubGeoDRConfigurationFailOver** cmdlet envokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="c2f65-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2f65-110">EXAMPLES</span></span>

### <span data-ttu-id="c2f65-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c2f65-111">Example 1</span></span>
```
PS C:\>Set-AzureRmEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="c2f65-112">Anropar redundans över alias "SampleDRCongifName", konfigurerar om och pekar på sekundär namn område "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="c2f65-112">Invokes the Failover over alias "SampleDRCongifName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="c2f65-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2f65-113">PARAMETERS</span></span>

### <span data-ttu-id="c2f65-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2f65-114">-DefaultProfile</span></span>
<span data-ttu-id="c2f65-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c2f65-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2f65-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2f65-116">-InputObject</span></span>
<span data-ttu-id="c2f65-117">Eventhub-GeoDR</span><span class="sxs-lookup"><span data-stu-id="c2f65-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="c2f65-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="c2f65-118">-Name</span></span>
<span data-ttu-id="c2f65-119">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="c2f65-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="c2f65-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="c2f65-120">-Namespace</span></span>
<span data-ttu-id="c2f65-121">Namn områdes namn-sekundärt namn område</span><span class="sxs-lookup"><span data-stu-id="c2f65-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="c2f65-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2f65-122">-PassThru</span></span>
<span data-ttu-id="c2f65-123">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="c2f65-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c2f65-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="c2f65-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c2f65-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2f65-125">-ResourceGroupName</span></span>
<span data-ttu-id="c2f65-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="c2f65-126">Resource Group Name</span></span>

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

### <span data-ttu-id="c2f65-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2f65-127">-ResourceId</span></span>
<span data-ttu-id="c2f65-128">Resurs-ID för GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2f65-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="c2f65-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c2f65-129">-Confirm</span></span>
<span data-ttu-id="c2f65-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c2f65-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2f65-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2f65-131">-WhatIf</span></span>
<span data-ttu-id="c2f65-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c2f65-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2f65-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c2f65-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2f65-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2f65-134">CommonParameters</span></span>
<span data-ttu-id="c2f65-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2f65-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c2f65-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2f65-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2f65-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2f65-137">INPUTS</span></span>

### <span data-ttu-id="c2f65-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c2f65-138">System.String</span></span>
<span data-ttu-id="c2f65-139">Microsoft. Azure. commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="c2f65-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>


## <span data-ttu-id="c2f65-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2f65-140">OUTPUTS</span></span>

### <span data-ttu-id="c2f65-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2f65-141">System.Boolean</span></span>


## <span data-ttu-id="c2f65-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2f65-142">NOTES</span></span>

## <span data-ttu-id="c2f65-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2f65-143">RELATED LINKS</span></span>
