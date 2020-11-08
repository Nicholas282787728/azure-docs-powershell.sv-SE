---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/switch-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
ms.openlocfilehash: 1f1bcd7b0eb7318746f2f5a48ce5ccd58941196c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260162"
---
# <span data-ttu-id="a7389-101">Switch-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a7389-101">Switch-AzWebAppSlot</span></span>

## <span data-ttu-id="a7389-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a7389-102">SYNOPSIS</span></span>
<span data-ttu-id="a7389-103">Växla två platser med ett webb program</span><span class="sxs-lookup"><span data-stu-id="a7389-103">Swap two slots with a Web App</span></span>

## <span data-ttu-id="a7389-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a7389-104">SYNTAX</span></span>

### <span data-ttu-id="a7389-105">S</span><span class="sxs-lookup"><span data-stu-id="a7389-105">S1</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7389-106">S2</span><span class="sxs-lookup"><span data-stu-id="a7389-106">S2</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7389-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a7389-107">DESCRIPTION</span></span>
<span data-ttu-id="a7389-108">**Växeln AzWebAppSlot** växlar två platser associerade med en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a7389-108">The **Switch-AzWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="a7389-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a7389-109">EXAMPLES</span></span>

### <span data-ttu-id="a7389-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a7389-110">Example 1</span></span>
```
PS C:\> Switch-AzWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="a7389-111">Det här kommandot växlar plats "sourceslot"-fack med "destinationslot" webb programmet ContosoWebApp associerat med resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="a7389-111">This command will switch slot "sourceslot" slot with "destinationslot" the Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="a7389-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a7389-112">PARAMETERS</span></span>

### <span data-ttu-id="a7389-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7389-113">-DefaultProfile</span></span>
<span data-ttu-id="a7389-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a7389-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7389-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="a7389-115">-DestinationSlotName</span></span>
<span data-ttu-id="a7389-116">Namn på mål platsen</span><span class="sxs-lookup"><span data-stu-id="a7389-116">Destination Slot Name</span></span>

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

### <span data-ttu-id="a7389-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="a7389-117">-Name</span></span>
<span data-ttu-id="a7389-118">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="a7389-118">WebApp Name</span></span>

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

### <span data-ttu-id="a7389-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="a7389-119">-PreserveVnet</span></span>
<span data-ttu-id="a7389-120">Bevara VNet-boolesk</span><span class="sxs-lookup"><span data-stu-id="a7389-120">Preserve Vnet Boolean</span></span>

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

### <span data-ttu-id="a7389-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7389-121">-ResourceGroupName</span></span>
<span data-ttu-id="a7389-122">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a7389-122">Resource Group Name</span></span>

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

### <span data-ttu-id="a7389-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="a7389-123">-SourceSlotName</span></span>
<span data-ttu-id="a7389-124">Namn på käll plats</span><span class="sxs-lookup"><span data-stu-id="a7389-124">Source Slot Name</span></span>

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

### <span data-ttu-id="a7389-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="a7389-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="a7389-126">Byt med förhands gransknings åtgärd</span><span class="sxs-lookup"><span data-stu-id="a7389-126">Swap With Preview Action</span></span>

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

### <span data-ttu-id="a7389-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a7389-127">-WebApp</span></span>
<span data-ttu-id="a7389-128">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="a7389-128">WebApp Object</span></span>

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

### <span data-ttu-id="a7389-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a7389-129">-Confirm</span></span>
<span data-ttu-id="a7389-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a7389-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7389-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7389-131">-WhatIf</span></span>
<span data-ttu-id="a7389-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a7389-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7389-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a7389-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7389-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7389-134">CommonParameters</span></span>
<span data-ttu-id="a7389-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7389-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7389-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7389-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7389-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a7389-137">INPUTS</span></span>

### <span data-ttu-id="a7389-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a7389-138">System.String</span></span>

### <span data-ttu-id="a7389-139">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="a7389-139">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a7389-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a7389-140">OUTPUTS</span></span>

### <span data-ttu-id="a7389-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="a7389-141">System.Void</span></span>

## <span data-ttu-id="a7389-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a7389-142">NOTES</span></span>

## <span data-ttu-id="a7389-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a7389-143">RELATED LINKS</span></span>
