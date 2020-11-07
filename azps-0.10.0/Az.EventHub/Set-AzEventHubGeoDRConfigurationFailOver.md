---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: 6569c5081ec92e20682edf63c09f1b4319d4c038
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922837"
---
# <span data-ttu-id="20b4e-101">Set-AzEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="20b4e-101">Set-AzEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="20b4e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20b4e-102">SYNOPSIS</span></span>
<span data-ttu-id="20b4e-103">Anropar GEO-failover och konfigurerar om aliaset så att det pekar på det sekundära namn området</span><span class="sxs-lookup"><span data-stu-id="20b4e-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="20b4e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20b4e-104">SYNTAX</span></span>

### <span data-ttu-id="20b4e-105">GeoDRParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="20b4e-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20b4e-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="20b4e-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20b4e-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20b4e-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20b4e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20b4e-108">DESCRIPTION</span></span>
<span data-ttu-id="20b4e-109">Cmdleten **set-AzEventHubGeoDRConfigurationFailOver** anropar geo Dr och konfigurerar om aliaset så att det pekar på det sekundära namn området</span><span class="sxs-lookup"><span data-stu-id="20b4e-109">The **Set-AzEventHubGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="20b4e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20b4e-110">EXAMPLES</span></span>

### <span data-ttu-id="20b4e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="20b4e-111">Example 1</span></span>
```
PS C:\>Set-AzEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="20b4e-112">Anropar redundans över alias "SampleDRConfigName", konfigurerar om och pekar på sekundär namn område "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="20b4e-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="20b4e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20b4e-113">PARAMETERS</span></span>

### <span data-ttu-id="20b4e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20b4e-114">-DefaultProfile</span></span>
<span data-ttu-id="20b4e-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="20b4e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20b4e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20b4e-116">-InputObject</span></span>
<span data-ttu-id="20b4e-117">Eventhub-GeoDR</span><span class="sxs-lookup"><span data-stu-id="20b4e-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="20b4e-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="20b4e-118">-Name</span></span>
<span data-ttu-id="20b4e-119">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="20b4e-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="20b4e-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="20b4e-120">-Namespace</span></span>
<span data-ttu-id="20b4e-121">Namn områdes namn-sekundärt namn område</span><span class="sxs-lookup"><span data-stu-id="20b4e-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="20b4e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20b4e-122">-PassThru</span></span>
<span data-ttu-id="20b4e-123">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="20b4e-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="20b4e-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="20b4e-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="20b4e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20b4e-125">-ResourceGroupName</span></span>
<span data-ttu-id="20b4e-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="20b4e-126">Resource Group Name</span></span>

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

### <span data-ttu-id="20b4e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20b4e-127">-ResourceId</span></span>
<span data-ttu-id="20b4e-128">Resurs-ID för GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="20b4e-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="20b4e-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="20b4e-129">-Confirm</span></span>
<span data-ttu-id="20b4e-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="20b4e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20b4e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20b4e-131">-WhatIf</span></span>
<span data-ttu-id="20b4e-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="20b4e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20b4e-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="20b4e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20b4e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20b4e-134">CommonParameters</span></span>
<span data-ttu-id="20b4e-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20b4e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20b4e-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20b4e-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20b4e-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20b4e-137">INPUTS</span></span>

### <span data-ttu-id="20b4e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="20b4e-138">System.String</span></span>

### <span data-ttu-id="20b4e-139">Microsoft. Azure. commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="20b4e-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="20b4e-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20b4e-140">OUTPUTS</span></span>

### <span data-ttu-id="20b4e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="20b4e-141">System.Boolean</span></span>

## <span data-ttu-id="20b4e-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20b4e-142">NOTES</span></span>

## <span data-ttu-id="20b4e-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20b4e-143">RELATED LINKS</span></span>
