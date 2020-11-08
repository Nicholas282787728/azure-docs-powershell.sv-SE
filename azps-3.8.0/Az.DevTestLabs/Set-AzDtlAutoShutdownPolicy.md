---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 8AAD9309-5763-4903-AF6A-1E50310146C0
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoShutdownPolicy.md
ms.openlocfilehash: 3b8c6965034b741ddd281bb81c9748a25d7038be
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090112"
---
# <span data-ttu-id="a6bcb-101">Set-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="a6bcb-101">Set-AzDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="a6bcb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a6bcb-102">SYNOPSIS</span></span>
<span data-ttu-id="a6bcb-103">Ställer in policyn för automatisk avstängning för ett labb DevTest labb.</span><span class="sxs-lookup"><span data-stu-id="a6bcb-103">Sets the auto shutdown policy of a lab DevTest Labs.</span></span>

## <span data-ttu-id="a6bcb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a6bcb-104">SYNTAX</span></span>

### <span data-ttu-id="a6bcb-105">Aktivera (standard)</span><span class="sxs-lookup"><span data-stu-id="a6bcb-105">Enable (Default)</span></span>
```
Set-AzDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6bcb-106">Aktiverar</span><span class="sxs-lookup"><span data-stu-id="a6bcb-106">Disable</span></span>
```
Set-AzDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6bcb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a6bcb-107">DESCRIPTION</span></span>
<span data-ttu-id="a6bcb-108">Cmdleten **set-AzDtlAutoShutdownPolicy** anger den automatiska avslutnings principen för en laboratoriet som automatiskt stänger av alla virtuella datorer i laboratorium under en viss tid på dagen.</span><span class="sxs-lookup"><span data-stu-id="a6bcb-108">The **Set-AzDtlAutoShutdownPolicy** cmdlet sets the auto shutdown policy of a lab, which automatically shuts down all the virtual machines in the lab at a specified time of the day.</span></span>
<span data-ttu-id="a6bcb-109">Cmdleten använder den angivna resurs gruppen och namnet på laboratoriet för att ange principen.</span><span class="sxs-lookup"><span data-stu-id="a6bcb-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="a6bcb-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a6bcb-110">EXAMPLES</span></span>

## <span data-ttu-id="a6bcb-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a6bcb-111">PARAMETERS</span></span>

### <span data-ttu-id="a6bcb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6bcb-112">-DefaultProfile</span></span>
<span data-ttu-id="a6bcb-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a6bcb-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6bcb-114">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="a6bcb-114">-Disable</span></span>
<span data-ttu-id="a6bcb-115">Anger att cmdleten inaktiverar principen i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="a6bcb-115">Indicates that the cmdlet disables the policy in the lab.</span></span>

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

### <span data-ttu-id="a6bcb-116">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="a6bcb-116">-Enable</span></span>
<span data-ttu-id="a6bcb-117">Anger att cmdleten aktiverar policyn i labbet.</span><span class="sxs-lookup"><span data-stu-id="a6bcb-117">Indicates that the cmdlet enables the policy in the lab.</span></span>

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

### <span data-ttu-id="a6bcb-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="a6bcb-118">-LabName</span></span>
<span data-ttu-id="a6bcb-119">Anger namnet på den Lab för vilken denna cmdlet ställer in principen för automatisk avstängning.</span><span class="sxs-lookup"><span data-stu-id="a6bcb-119">Specifies the name of the lab for which this cmdlet sets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="a6bcb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6bcb-120">-ResourceGroupName</span></span>
<span data-ttu-id="a6bcb-121">Anger namnet på den resurs grupp som laboratoriet hör till.</span><span class="sxs-lookup"><span data-stu-id="a6bcb-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="a6bcb-122">-Tid</span><span class="sxs-lookup"><span data-stu-id="a6bcb-122">-Time</span></span>
<span data-ttu-id="a6bcb-123">Anger tiden, som ett **datetime** -objekt, för när de virtuella datorerna i laboratoriet måste stängas av.</span><span class="sxs-lookup"><span data-stu-id="a6bcb-123">Specifies the time, as a **DateTime** object, for when the virtual machines in the lab must shut down.</span></span>

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

### <span data-ttu-id="a6bcb-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a6bcb-124">-Confirm</span></span>
<span data-ttu-id="a6bcb-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a6bcb-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6bcb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6bcb-126">-WhatIf</span></span>
<span data-ttu-id="a6bcb-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a6bcb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6bcb-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a6bcb-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6bcb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6bcb-129">CommonParameters</span></span>
<span data-ttu-id="a6bcb-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6bcb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6bcb-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6bcb-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6bcb-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a6bcb-132">INPUTS</span></span>

### <span data-ttu-id="a6bcb-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a6bcb-133">System.String</span></span>

## <span data-ttu-id="a6bcb-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a6bcb-134">OUTPUTS</span></span>

### <span data-ttu-id="a6bcb-135">Microsoft. Azure. commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="a6bcb-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="a6bcb-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a6bcb-136">NOTES</span></span>

## <span data-ttu-id="a6bcb-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a6bcb-137">RELATED LINKS</span></span>

[<span data-ttu-id="a6bcb-138">Get-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="a6bcb-138">Get-AzDtlAutoShutdownPolicy</span></span>](./Get-AzDtlAutoShutdownPolicy.md)


