---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/switch-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Switch-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Switch-AzWebAppSlot.md
ms.openlocfilehash: e30179ce2e9198729771d406d1963ff0048e05b1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923225"
---
# <span data-ttu-id="86c28-101">Switch-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86c28-101">Switch-AzWebAppSlot</span></span>

## <span data-ttu-id="86c28-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="86c28-102">SYNOPSIS</span></span>
<span data-ttu-id="86c28-103">Växla två platser med ett webb program</span><span class="sxs-lookup"><span data-stu-id="86c28-103">Swap two slots with a Web App</span></span>

## <span data-ttu-id="86c28-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="86c28-104">SYNTAX</span></span>

### <span data-ttu-id="86c28-105">S</span><span class="sxs-lookup"><span data-stu-id="86c28-105">S1</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86c28-106">S2</span><span class="sxs-lookup"><span data-stu-id="86c28-106">S2</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86c28-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="86c28-107">DESCRIPTION</span></span>
<span data-ttu-id="86c28-108">**Växeln AzWebAppSlot** växlar två platser associerade med en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="86c28-108">The **Switch-AzWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="86c28-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="86c28-109">EXAMPLES</span></span>

### <span data-ttu-id="86c28-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="86c28-110">Example 1</span></span>
```
PS C:\> Switch-AzWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="86c28-111">Det här kommandot växlar plats "sourceslot"-fack med "destinationslot" för webb programmet ContosoWebApp associerat med resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="86c28-111">This command will switch slot "sourceslot" slot with "destinationslot" for for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="86c28-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="86c28-112">PARAMETERS</span></span>

### <span data-ttu-id="86c28-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86c28-113">-DefaultProfile</span></span>
<span data-ttu-id="86c28-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="86c28-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86c28-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="86c28-115">-DestinationSlotName</span></span>
<span data-ttu-id="86c28-116">Namn på mål platsen</span><span class="sxs-lookup"><span data-stu-id="86c28-116">Destination Slot Name</span></span>

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

### <span data-ttu-id="86c28-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="86c28-117">-Name</span></span>
<span data-ttu-id="86c28-118">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="86c28-118">WebApp Name</span></span>

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

### <span data-ttu-id="86c28-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="86c28-119">-PreserveVnet</span></span>
<span data-ttu-id="86c28-120">Bevara VNet-boolesk</span><span class="sxs-lookup"><span data-stu-id="86c28-120">Preserve Vnet Boolean</span></span>

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

### <span data-ttu-id="86c28-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86c28-121">-ResourceGroupName</span></span>
<span data-ttu-id="86c28-122">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="86c28-122">Resource Group Name</span></span>

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

### <span data-ttu-id="86c28-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="86c28-123">-SourceSlotName</span></span>
<span data-ttu-id="86c28-124">Namn på käll plats</span><span class="sxs-lookup"><span data-stu-id="86c28-124">Source Slot Name</span></span>

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

### <span data-ttu-id="86c28-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="86c28-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="86c28-126">Byt med förhands gransknings åtgärd</span><span class="sxs-lookup"><span data-stu-id="86c28-126">Swap With Preview Action</span></span>

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

### <span data-ttu-id="86c28-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="86c28-127">-WebApp</span></span>
<span data-ttu-id="86c28-128">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="86c28-128">WebApp Object</span></span>

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

### <span data-ttu-id="86c28-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="86c28-129">-Confirm</span></span>
<span data-ttu-id="86c28-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="86c28-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86c28-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86c28-131">-WhatIf</span></span>
<span data-ttu-id="86c28-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="86c28-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86c28-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="86c28-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86c28-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86c28-134">CommonParameters</span></span>
<span data-ttu-id="86c28-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86c28-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86c28-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86c28-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86c28-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="86c28-137">INPUTS</span></span>

### <span data-ttu-id="86c28-138">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="86c28-138">Site</span></span>
<span data-ttu-id="86c28-139">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="86c28-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="86c28-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="86c28-140">OUTPUTS</span></span>

## <span data-ttu-id="86c28-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="86c28-141">NOTES</span></span>

## <span data-ttu-id="86c28-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="86c28-142">RELATED LINKS</span></span>

