---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 8AAD9309-5763-4903-AF6A-1E50310146C0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoShutdownPolicy.md
ms.openlocfilehash: 65fee8d72217c4f30a8e05477217938240067b7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576287"
---
# <span data-ttu-id="59a11-101">Set-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="59a11-101">Set-AzureRmDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="59a11-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59a11-102">SYNOPSIS</span></span>
<span data-ttu-id="59a11-103">Ställer in policyn för automatisk avstängning för ett labb DevTest labb.</span><span class="sxs-lookup"><span data-stu-id="59a11-103">Sets the auto shutdown policy of a lab DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59a11-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59a11-104">SYNTAX</span></span>

### <span data-ttu-id="59a11-105">Aktivera (standard)</span><span class="sxs-lookup"><span data-stu-id="59a11-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59a11-106">Aktiverar</span><span class="sxs-lookup"><span data-stu-id="59a11-106">Disable</span></span>
```
Set-AzureRmDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59a11-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59a11-107">DESCRIPTION</span></span>
<span data-ttu-id="59a11-108">Cmdleten **set-AzureRmDtlAutoShutdownPolicy** anger den automatiska avslutnings principen för en laboratoriet som automatiskt stänger av alla virtuella datorer i laboratorium under en viss tid på dagen.</span><span class="sxs-lookup"><span data-stu-id="59a11-108">The **Set-AzureRmDtlAutoShutdownPolicy** cmdlet sets the auto shutdown policy of a lab, which automatically shuts down all the virtual machines in the lab at a specified time of the day.</span></span>
<span data-ttu-id="59a11-109">Cmdleten använder den angivna resurs gruppen och namnet på laboratoriet för att ange principen.</span><span class="sxs-lookup"><span data-stu-id="59a11-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="59a11-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59a11-110">EXAMPLES</span></span>

## <span data-ttu-id="59a11-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59a11-111">PARAMETERS</span></span>

### <span data-ttu-id="59a11-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59a11-112">-DefaultProfile</span></span>
<span data-ttu-id="59a11-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="59a11-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59a11-114">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="59a11-114">-Disable</span></span>
<span data-ttu-id="59a11-115">Anger att cmdleten inaktiverar principen i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="59a11-115">Indicates that the cmdlet disables the policy in the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a11-116">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="59a11-116">-Enable</span></span>
<span data-ttu-id="59a11-117">Anger att cmdleten aktiverar policyn i labbet.</span><span class="sxs-lookup"><span data-stu-id="59a11-117">Indicates that the cmdlet enables the policy in the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a11-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="59a11-118">-LabName</span></span>
<span data-ttu-id="59a11-119">Anger namnet på den Lab för vilken denna cmdlet ställer in principen för automatisk avstängning.</span><span class="sxs-lookup"><span data-stu-id="59a11-119">Specifies the name of the lab for which this cmdlet sets the auto shutdown policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59a11-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59a11-120">-ResourceGroupName</span></span>
<span data-ttu-id="59a11-121">Anger namnet på den resurs grupp som laboratoriet hör till.</span><span class="sxs-lookup"><span data-stu-id="59a11-121">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59a11-122">-Tid</span><span class="sxs-lookup"><span data-stu-id="59a11-122">-Time</span></span>
<span data-ttu-id="59a11-123">Anger tiden, som ett **datetime** -objekt, för när de virtuella datorerna i laboratoriet måste stängas av.</span><span class="sxs-lookup"><span data-stu-id="59a11-123">Specifies the time, as a **DateTime** object, for when the virtual machines in the lab must shut down.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a11-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="59a11-124">-Confirm</span></span>
<span data-ttu-id="59a11-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="59a11-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a11-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59a11-126">-WhatIf</span></span>
<span data-ttu-id="59a11-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="59a11-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59a11-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="59a11-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a11-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59a11-129">CommonParameters</span></span>
<span data-ttu-id="59a11-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59a11-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59a11-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59a11-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59a11-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59a11-132">INPUTS</span></span>

### <span data-ttu-id="59a11-133">System. String</span><span class="sxs-lookup"><span data-stu-id="59a11-133">System.String</span></span>

## <span data-ttu-id="59a11-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59a11-134">OUTPUTS</span></span>

### <span data-ttu-id="59a11-135">Microsoft. Azure. commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="59a11-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="59a11-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59a11-136">NOTES</span></span>

## <span data-ttu-id="59a11-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59a11-137">RELATED LINKS</span></span>

[<span data-ttu-id="59a11-138">Get-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="59a11-138">Get-AzureRmDtlAutoShutdownPolicy</span></span>](./Get-AzureRmDtlAutoShutdownPolicy.md)

