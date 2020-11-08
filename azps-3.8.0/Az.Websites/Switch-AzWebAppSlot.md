---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/switch-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
ms.openlocfilehash: 1f1bcd7b0eb7318746f2f5a48ce5ccd58941196c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090312"
---
# <span data-ttu-id="2a37f-101">Switch-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2a37f-101">Switch-AzWebAppSlot</span></span>

## <span data-ttu-id="2a37f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a37f-102">SYNOPSIS</span></span>
<span data-ttu-id="2a37f-103">Växla två platser med ett webb program</span><span class="sxs-lookup"><span data-stu-id="2a37f-103">Swap two slots with a Web App</span></span>

## <span data-ttu-id="2a37f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a37f-104">SYNTAX</span></span>

### <span data-ttu-id="2a37f-105">S</span><span class="sxs-lookup"><span data-stu-id="2a37f-105">S1</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a37f-106">S2</span><span class="sxs-lookup"><span data-stu-id="2a37f-106">S2</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a37f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a37f-107">DESCRIPTION</span></span>
<span data-ttu-id="2a37f-108">**Växeln AzWebAppSlot** växlar två platser associerade med en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="2a37f-108">The **Switch-AzWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="2a37f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a37f-109">EXAMPLES</span></span>

### <span data-ttu-id="2a37f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2a37f-110">Example 1</span></span>
```
PS C:\> Switch-AzWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="2a37f-111">Det här kommandot växlar plats "sourceslot"-fack med "destinationslot" webb programmet ContosoWebApp associerat med resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="2a37f-111">This command will switch slot "sourceslot" slot with "destinationslot" the Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="2a37f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a37f-112">PARAMETERS</span></span>

### <span data-ttu-id="2a37f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a37f-113">-DefaultProfile</span></span>
<span data-ttu-id="2a37f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2a37f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a37f-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="2a37f-115">-DestinationSlotName</span></span>
<span data-ttu-id="2a37f-116">Namn på mål platsen</span><span class="sxs-lookup"><span data-stu-id="2a37f-116">Destination Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a37f-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="2a37f-117">-Name</span></span>
<span data-ttu-id="2a37f-118">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="2a37f-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a37f-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="2a37f-119">-PreserveVnet</span></span>
<span data-ttu-id="2a37f-120">Bevara VNet-boolesk</span><span class="sxs-lookup"><span data-stu-id="2a37f-120">Preserve Vnet Boolean</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a37f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a37f-121">-ResourceGroupName</span></span>
<span data-ttu-id="2a37f-122">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="2a37f-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a37f-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="2a37f-123">-SourceSlotName</span></span>
<span data-ttu-id="2a37f-124">Namn på käll plats</span><span class="sxs-lookup"><span data-stu-id="2a37f-124">Source Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a37f-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="2a37f-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="2a37f-126">Byt med förhands gransknings åtgärd</span><span class="sxs-lookup"><span data-stu-id="2a37f-126">Swap With Preview Action</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.WebApps.Utilities.SwapWithPreviewAction]
Parameter Sets: (All)
Aliases:
Accepted values: ApplySlotConfig, CompleteSlotSwap, ResetSlotSwap

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a37f-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2a37f-127">-WebApp</span></span>
<span data-ttu-id="2a37f-128">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="2a37f-128">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a37f-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2a37f-129">-Confirm</span></span>
<span data-ttu-id="2a37f-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2a37f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a37f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a37f-131">-WhatIf</span></span>
<span data-ttu-id="2a37f-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2a37f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a37f-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2a37f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a37f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a37f-134">CommonParameters</span></span>
<span data-ttu-id="2a37f-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a37f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a37f-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a37f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a37f-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a37f-137">INPUTS</span></span>

### <span data-ttu-id="2a37f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2a37f-138">System.String</span></span>

### <span data-ttu-id="2a37f-139">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="2a37f-139">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="2a37f-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a37f-140">OUTPUTS</span></span>

### <span data-ttu-id="2a37f-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="2a37f-141">System.Void</span></span>

## <span data-ttu-id="2a37f-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a37f-142">NOTES</span></span>

## <span data-ttu-id="2a37f-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a37f-143">RELATED LINKS</span></span>