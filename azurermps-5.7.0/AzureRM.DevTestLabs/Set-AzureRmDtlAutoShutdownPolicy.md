---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 8AAD9309-5763-4903-AF6A-1E50310146C0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoShutdownPolicy.md
ms.openlocfilehash: edded91551b87e180b17ff8f97d84d16bef0b0ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584348"
---
# <span data-ttu-id="21ad6-101">Set-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="21ad6-101">Set-AzureRmDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="21ad6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="21ad6-102">SYNOPSIS</span></span>
<span data-ttu-id="21ad6-103">Ställer in policyn för automatisk avstängning för ett labb DevTest labb.</span><span class="sxs-lookup"><span data-stu-id="21ad6-103">Sets the auto shutdown policy of a lab DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21ad6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="21ad6-104">SYNTAX</span></span>

### <span data-ttu-id="21ad6-105">Aktivera (standard)</span><span class="sxs-lookup"><span data-stu-id="21ad6-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21ad6-106">Aktiverar</span><span class="sxs-lookup"><span data-stu-id="21ad6-106">Disable</span></span>
```
Set-AzureRmDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="21ad6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="21ad6-107">DESCRIPTION</span></span>
<span data-ttu-id="21ad6-108">Cmdleten **set-AzureRmDtlAutoShutdownPolicy** anger den automatiska avslutnings principen för en laboratoriet som automatiskt stänger av alla virtuella datorer i laboratorium under en viss tid på dagen.</span><span class="sxs-lookup"><span data-stu-id="21ad6-108">The **Set-AzureRmDtlAutoShutdownPolicy** cmdlet sets the auto shutdown policy of a lab, which automatically shuts down all the virtual machines in the lab at a specified time of the day.</span></span>
<span data-ttu-id="21ad6-109">Cmdleten använder den angivna resurs gruppen och namnet på laboratoriet för att ange principen.</span><span class="sxs-lookup"><span data-stu-id="21ad6-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="21ad6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="21ad6-110">EXAMPLES</span></span>

## <span data-ttu-id="21ad6-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="21ad6-111">PARAMETERS</span></span>

### <span data-ttu-id="21ad6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21ad6-112">-DefaultProfile</span></span>
<span data-ttu-id="21ad6-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="21ad6-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21ad6-114">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="21ad6-114">-Disable</span></span>
<span data-ttu-id="21ad6-115">Anger att cmdleten inaktiverar principen i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="21ad6-115">Indicates that the cmdlet disables the policy in the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disable
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ad6-116">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="21ad6-116">-Enable</span></span>
<span data-ttu-id="21ad6-117">Anger att cmdleten aktiverar policyn i labbet.</span><span class="sxs-lookup"><span data-stu-id="21ad6-117">Indicates that the cmdlet enables the policy in the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Enable
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ad6-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="21ad6-118">-LabName</span></span>
<span data-ttu-id="21ad6-119">Anger namnet på den Lab för vilken denna cmdlet ställer in principen för automatisk avstängning.</span><span class="sxs-lookup"><span data-stu-id="21ad6-119">Specifies the name of the lab for which this cmdlet sets the auto shutdown policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ad6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21ad6-120">-ResourceGroupName</span></span>
<span data-ttu-id="21ad6-121">Anger namnet på den resurs grupp som laboratoriet hör till.</span><span class="sxs-lookup"><span data-stu-id="21ad6-121">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ad6-122">-Tid</span><span class="sxs-lookup"><span data-stu-id="21ad6-122">-Time</span></span>
<span data-ttu-id="21ad6-123">Anger tiden, som ett **datetime** -objekt, för när de virtuella datorerna i laboratoriet måste stängas av.</span><span class="sxs-lookup"><span data-stu-id="21ad6-123">Specifies the time, as a **DateTime** object, for when the virtual machines in the lab must shut down.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ad6-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="21ad6-124">-Confirm</span></span>
<span data-ttu-id="21ad6-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="21ad6-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ad6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21ad6-126">-WhatIf</span></span>
<span data-ttu-id="21ad6-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="21ad6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21ad6-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="21ad6-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ad6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21ad6-129">CommonParameters</span></span>
<span data-ttu-id="21ad6-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21ad6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21ad6-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21ad6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21ad6-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="21ad6-132">INPUTS</span></span>

### <span data-ttu-id="21ad6-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="21ad6-133">None</span></span>
<span data-ttu-id="21ad6-134">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="21ad6-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="21ad6-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="21ad6-135">OUTPUTS</span></span>

### <span data-ttu-id="21ad6-136">Microsoft. Azure. commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="21ad6-136">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="21ad6-137">Denna cmdlet returnerar schemat som anger när de virtuella datorerna i laboratoriet måste stängas av.</span><span class="sxs-lookup"><span data-stu-id="21ad6-137">This cmdlet returns the schedule which specifies when the virtual machines in the lab must shut down.</span></span>

## <span data-ttu-id="21ad6-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="21ad6-138">NOTES</span></span>

## <span data-ttu-id="21ad6-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="21ad6-139">RELATED LINKS</span></span>

[<span data-ttu-id="21ad6-140">Get-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="21ad6-140">Get-AzureRmDtlAutoShutdownPolicy</span></span>](./Get-AzureRmDtlAutoShutdownPolicy.md)


