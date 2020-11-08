---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 3FADEC2E-4A2B-46EB-8A94-CF48D717C7FC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoStartPolicy.md
ms.openlocfilehash: 7031aaa5a0e5655f933beadbb51569aba0adbef1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090113"
---
# <span data-ttu-id="94790-101">Set-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="94790-101">Set-AzDtlAutoStartPolicy</span></span>

## <span data-ttu-id="94790-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="94790-102">SYNOPSIS</span></span>
<span data-ttu-id="94790-103">Ställer in en policy för automatisk start för ett labb i DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="94790-103">Sets the auto start policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="94790-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="94790-104">SYNTAX</span></span>

### <span data-ttu-id="94790-105">Aktivera (standard)</span><span class="sxs-lookup"><span data-stu-id="94790-105">Enable (Default)</span></span>
```
Set-AzDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94790-106">Aktiverar</span><span class="sxs-lookup"><span data-stu-id="94790-106">Disable</span></span>
```
Set-AzDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94790-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="94790-107">DESCRIPTION</span></span>
<span data-ttu-id="94790-108">Cmdleten **set-AzDtlAutoStartPolicy** anger den automatiska start principen för ett labb som tillåter att virtuella laboratorie datorer schemaläggs för automatisk start.</span><span class="sxs-lookup"><span data-stu-id="94790-108">The **Set-AzDtlAutoStartPolicy** cmdlet sets the auto start policy of a lab, which allows lab virtual machines to be scheduled for automatic start.</span></span>
<span data-ttu-id="94790-109">Cmdleten använder den angivna resurs gruppen och namnet på laboratoriet för att ange principen.</span><span class="sxs-lookup"><span data-stu-id="94790-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="94790-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="94790-110">EXAMPLES</span></span>

## <span data-ttu-id="94790-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="94790-111">PARAMETERS</span></span>

### <span data-ttu-id="94790-112">-Dagar</span><span class="sxs-lookup"><span data-stu-id="94790-112">-Days</span></span>
<span data-ttu-id="94790-113">Anger, i en matris, veckans vecko dagar när de virtuella datorerna i Lab måste startas.</span><span class="sxs-lookup"><span data-stu-id="94790-113">Specifies, as an array, the days of the week for when the virtual machines of the lab must be started.</span></span>

```yaml
Type: System.DayOfWeek[]
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94790-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94790-114">-DefaultProfile</span></span>
<span data-ttu-id="94790-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="94790-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94790-116">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="94790-116">-Disable</span></span>
<span data-ttu-id="94790-117">Anger att denna cmdlet inaktiverar principen för de virtuella datorerna i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="94790-117">Indicates that this cmdlet disables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="94790-118">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="94790-118">-Enable</span></span>
<span data-ttu-id="94790-119">Anger att denna cmdlet aktiverar principen för de virtuella datorerna i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="94790-119">Indicates that this cmdlet enables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="94790-120">-LabName</span><span class="sxs-lookup"><span data-stu-id="94790-120">-LabName</span></span>
<span data-ttu-id="94790-121">Anger namnet på den Lab för vilken den här cmdleten ställer in principen för automatisk start.</span><span class="sxs-lookup"><span data-stu-id="94790-121">Specifies the name of the lab for which this cmdlet sets the automatic start policy.</span></span>

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

### <span data-ttu-id="94790-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94790-122">-ResourceGroupName</span></span>
<span data-ttu-id="94790-123">Anger namnet på den resurs grupp som laboratoriet hör till.</span><span class="sxs-lookup"><span data-stu-id="94790-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="94790-124">-Tid</span><span class="sxs-lookup"><span data-stu-id="94790-124">-Time</span></span>
<span data-ttu-id="94790-125">Anger den tid då de virtuella datorerna i laboratoriet måste startas.</span><span class="sxs-lookup"><span data-stu-id="94790-125">Specifies the time when the virtual machines of the lab must be started.</span></span>

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

### <span data-ttu-id="94790-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="94790-126">-Confirm</span></span>
<span data-ttu-id="94790-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="94790-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94790-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94790-128">-WhatIf</span></span>
<span data-ttu-id="94790-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="94790-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94790-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="94790-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94790-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94790-131">CommonParameters</span></span>
<span data-ttu-id="94790-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94790-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94790-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94790-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94790-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="94790-134">INPUTS</span></span>

### <span data-ttu-id="94790-135">System. String</span><span class="sxs-lookup"><span data-stu-id="94790-135">System.String</span></span>

## <span data-ttu-id="94790-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="94790-136">OUTPUTS</span></span>

### <span data-ttu-id="94790-137">Microsoft. Azure. commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="94790-137">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="94790-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="94790-138">NOTES</span></span>

## <span data-ttu-id="94790-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="94790-139">RELATED LINKS</span></span>

[<span data-ttu-id="94790-140">Get-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="94790-140">Get-AzDtlAutoStartPolicy</span></span>](./Get-AzDtlAutoStartPolicy.md)


