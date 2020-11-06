---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/switch-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Switch-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Switch-AzureRmWebAppSlot.md
ms.openlocfilehash: ada4e30b69d4dcb6193db94e3f770966c15c5f70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576718"
---
# <span data-ttu-id="7cea9-101">Switch-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7cea9-101">Switch-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="7cea9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7cea9-102">SYNOPSIS</span></span>
<span data-ttu-id="7cea9-103">Växla två platser med ett webb program</span><span class="sxs-lookup"><span data-stu-id="7cea9-103">Swap two slots with a Web App</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cea9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7cea9-104">SYNTAX</span></span>

### <span data-ttu-id="7cea9-105">S</span><span class="sxs-lookup"><span data-stu-id="7cea9-105">S1</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cea9-106">S2</span><span class="sxs-lookup"><span data-stu-id="7cea9-106">S2</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cea9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7cea9-107">DESCRIPTION</span></span>
<span data-ttu-id="7cea9-108">**Växeln AzureRmWebAppSlot** växlar två platser associerade med en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="7cea9-108">The **Switch-AzureRmWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="7cea9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7cea9-109">EXAMPLES</span></span>

### <span data-ttu-id="7cea9-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7cea9-110">Example 1</span></span>
```
PS C:\> Switch-AzureRmWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="7cea9-111">Det här kommandot växlar plats "sourceslot"-fack med "destinationslot" för webb programmet ContosoWebApp associerat med resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="7cea9-111">This command will switch slot "sourceslot" slot with "destinationslot" for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="7cea9-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7cea9-112">PARAMETERS</span></span>

### <span data-ttu-id="7cea9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cea9-113">-DefaultProfile</span></span>
<span data-ttu-id="7cea9-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7cea9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cea9-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="7cea9-115">-DestinationSlotName</span></span>
<span data-ttu-id="7cea9-116">Namn på mål platsen</span><span class="sxs-lookup"><span data-stu-id="7cea9-116">Destination Slot Name</span></span>

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

### <span data-ttu-id="7cea9-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="7cea9-117">-Name</span></span>
<span data-ttu-id="7cea9-118">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="7cea9-118">WebApp Name</span></span>

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

### <span data-ttu-id="7cea9-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="7cea9-119">-PreserveVnet</span></span>
<span data-ttu-id="7cea9-120">Bevara VNet-boolesk</span><span class="sxs-lookup"><span data-stu-id="7cea9-120">Preserve Vnet Boolean</span></span>

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

### <span data-ttu-id="7cea9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cea9-121">-ResourceGroupName</span></span>
<span data-ttu-id="7cea9-122">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="7cea9-122">Resource Group Name</span></span>

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

### <span data-ttu-id="7cea9-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="7cea9-123">-SourceSlotName</span></span>
<span data-ttu-id="7cea9-124">Namn på käll plats</span><span class="sxs-lookup"><span data-stu-id="7cea9-124">Source Slot Name</span></span>

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

### <span data-ttu-id="7cea9-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="7cea9-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="7cea9-126">Byt med förhands gransknings åtgärd</span><span class="sxs-lookup"><span data-stu-id="7cea9-126">Swap With Preview Action</span></span>

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

### <span data-ttu-id="7cea9-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="7cea9-127">-WebApp</span></span>
<span data-ttu-id="7cea9-128">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="7cea9-128">WebApp Object</span></span>

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

### <span data-ttu-id="7cea9-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7cea9-129">-Confirm</span></span>
<span data-ttu-id="7cea9-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7cea9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cea9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cea9-131">-WhatIf</span></span>
<span data-ttu-id="7cea9-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7cea9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cea9-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7cea9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cea9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cea9-134">CommonParameters</span></span>
<span data-ttu-id="7cea9-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cea9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cea9-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cea9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cea9-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7cea9-137">INPUTS</span></span>

### <span data-ttu-id="7cea9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7cea9-138">System.String</span></span>

### <span data-ttu-id="7cea9-139">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="7cea9-139">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="7cea9-140">Parametrar: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7cea9-140">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="7cea9-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7cea9-141">OUTPUTS</span></span>

### <span data-ttu-id="7cea9-142">System. Void</span><span class="sxs-lookup"><span data-stu-id="7cea9-142">System.Void</span></span>

## <span data-ttu-id="7cea9-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7cea9-143">NOTES</span></span>

## <span data-ttu-id="7cea9-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7cea9-144">RELATED LINKS</span></span>
