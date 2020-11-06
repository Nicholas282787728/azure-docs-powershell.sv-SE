---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/switch-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Switch-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Switch-AzureRmWebAppSlot.md
ms.openlocfilehash: e1cfb3e70ab8176cfd686dc404b13dbbfb23e4e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574112"
---
# <span data-ttu-id="41fd5-101">Switch-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="41fd5-101">Switch-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="41fd5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="41fd5-102">SYNOPSIS</span></span>
<span data-ttu-id="41fd5-103">Växla två platser med ett webb program</span><span class="sxs-lookup"><span data-stu-id="41fd5-103">Swap two slots with a Web App</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41fd5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="41fd5-104">SYNTAX</span></span>

### <span data-ttu-id="41fd5-105">S</span><span class="sxs-lookup"><span data-stu-id="41fd5-105">S1</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41fd5-106">S2</span><span class="sxs-lookup"><span data-stu-id="41fd5-106">S2</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41fd5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="41fd5-107">DESCRIPTION</span></span>
<span data-ttu-id="41fd5-108">**Växeln AzureRmWebAppSlot** växlar två platser associerade med en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="41fd5-108">The **Switch-AzureRmWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="41fd5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="41fd5-109">EXAMPLES</span></span>

### <span data-ttu-id="41fd5-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="41fd5-110">Example 1</span></span>
```
PS C:\> Switch-AzureRmWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="41fd5-111">Det här kommandot växlar plats "sourceslot"-fack med "destinationslot" för webb programmet ContosoWebApp associerat med resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="41fd5-111">This command will switch slot "sourceslot" slot with "destinationslot" for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="41fd5-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="41fd5-112">PARAMETERS</span></span>

### <span data-ttu-id="41fd5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41fd5-113">-DefaultProfile</span></span>
<span data-ttu-id="41fd5-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="41fd5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41fd5-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="41fd5-115">-DestinationSlotName</span></span>
<span data-ttu-id="41fd5-116">Namn på mål platsen</span><span class="sxs-lookup"><span data-stu-id="41fd5-116">Destination Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41fd5-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="41fd5-117">-Name</span></span>
<span data-ttu-id="41fd5-118">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="41fd5-118">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41fd5-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="41fd5-119">-PreserveVnet</span></span>
<span data-ttu-id="41fd5-120">Bevara VNet-boolesk</span><span class="sxs-lookup"><span data-stu-id="41fd5-120">Preserve Vnet Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41fd5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41fd5-121">-ResourceGroupName</span></span>
<span data-ttu-id="41fd5-122">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="41fd5-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41fd5-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="41fd5-123">-SourceSlotName</span></span>
<span data-ttu-id="41fd5-124">Namn på käll plats</span><span class="sxs-lookup"><span data-stu-id="41fd5-124">Source Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41fd5-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="41fd5-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="41fd5-126">Byt med förhands gransknings åtgärd</span><span class="sxs-lookup"><span data-stu-id="41fd5-126">Swap With Preview Action</span></span>

```yaml
Type: SwapWithPreviewAction
Parameter Sets: (All)
Aliases: 
Accepted values: ApplySlotConfig, CompleteSlotSwap, ResetSlotSwap

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41fd5-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="41fd5-127">-WebApp</span></span>
<span data-ttu-id="41fd5-128">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="41fd5-128">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41fd5-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="41fd5-129">-Confirm</span></span>
<span data-ttu-id="41fd5-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="41fd5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41fd5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41fd5-131">-WhatIf</span></span>
<span data-ttu-id="41fd5-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="41fd5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41fd5-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="41fd5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41fd5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41fd5-134">CommonParameters</span></span>
<span data-ttu-id="41fd5-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41fd5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41fd5-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41fd5-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41fd5-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="41fd5-137">INPUTS</span></span>

### <span data-ttu-id="41fd5-138">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="41fd5-138">Site</span></span>
<span data-ttu-id="41fd5-139">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="41fd5-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="41fd5-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="41fd5-140">OUTPUTS</span></span>

## <span data-ttu-id="41fd5-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="41fd5-141">NOTES</span></span>

## <span data-ttu-id="41fd5-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="41fd5-142">RELATED LINKS</span></span>

