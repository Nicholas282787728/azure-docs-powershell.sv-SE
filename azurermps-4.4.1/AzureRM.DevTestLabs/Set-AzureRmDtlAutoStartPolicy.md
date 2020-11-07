---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 3FADEC2E-4A2B-46EB-8A94-CF48D717C7FC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: a1efa9159bbe318a1de0360a3f70f197660db535
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756965"
---
# <span data-ttu-id="fecd0-101">Set-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="fecd0-101">Set-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="fecd0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fecd0-102">SYNOPSIS</span></span>
<span data-ttu-id="fecd0-103">Ställer in en policy för automatisk start för ett labb i DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="fecd0-103">Sets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fecd0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fecd0-104">SYNTAX</span></span>

### <span data-ttu-id="fecd0-105">Aktivera (standard)</span><span class="sxs-lookup"><span data-stu-id="fecd0-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fecd0-106">Aktiverar</span><span class="sxs-lookup"><span data-stu-id="fecd0-106">Disable</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fecd0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fecd0-107">DESCRIPTION</span></span>
<span data-ttu-id="fecd0-108">Cmdleten **set-AzureRmDtlAutoStartPolicy** anger den automatiska start principen för ett labb som tillåter att virtuella laboratorie datorer schemaläggs för automatisk start.</span><span class="sxs-lookup"><span data-stu-id="fecd0-108">The **Set-AzureRmDtlAutoStartPolicy** cmdlet sets the auto start policy of a lab, which allows lab virtual machines to be scheduled for automatic start.</span></span>
<span data-ttu-id="fecd0-109">Cmdleten använder den angivna resurs gruppen och namnet på laboratoriet för att ange principen.</span><span class="sxs-lookup"><span data-stu-id="fecd0-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="fecd0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fecd0-110">EXAMPLES</span></span>

## <span data-ttu-id="fecd0-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fecd0-111">PARAMETERS</span></span>

### <span data-ttu-id="fecd0-112">-Dagar</span><span class="sxs-lookup"><span data-stu-id="fecd0-112">-Days</span></span>
<span data-ttu-id="fecd0-113">Anger, i en matris, veckans vecko dagar när de virtuella datorerna i Lab måste startas.</span><span class="sxs-lookup"><span data-stu-id="fecd0-113">Specifies, as an array, the days of the week for when the virtual machines of the lab must be started.</span></span>

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

### <span data-ttu-id="fecd0-114">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="fecd0-114">-Disable</span></span>
<span data-ttu-id="fecd0-115">Anger att denna cmdlet inaktiverar principen för de virtuella datorerna i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="fecd0-115">Indicates that this cmdlet disables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="fecd0-116">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="fecd0-116">-Enable</span></span>
<span data-ttu-id="fecd0-117">Anger att denna cmdlet aktiverar principen för de virtuella datorerna i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="fecd0-117">Indicates that this cmdlet enables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="fecd0-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="fecd0-118">-LabName</span></span>
<span data-ttu-id="fecd0-119">Anger namnet på den Lab för vilken den här cmdleten ställer in principen för automatisk start.</span><span class="sxs-lookup"><span data-stu-id="fecd0-119">Specifies the name of the lab for which this cmdlet sets the automatic start policy.</span></span>

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

### <span data-ttu-id="fecd0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fecd0-120">-ResourceGroupName</span></span>
<span data-ttu-id="fecd0-121">Anger namnet på den resurs grupp som laboratoriet hör till.</span><span class="sxs-lookup"><span data-stu-id="fecd0-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="fecd0-122">-Tid</span><span class="sxs-lookup"><span data-stu-id="fecd0-122">-Time</span></span>
<span data-ttu-id="fecd0-123">Anger den tid då de virtuella datorerna i laboratoriet måste startas.</span><span class="sxs-lookup"><span data-stu-id="fecd0-123">Specifies the time when the virtual machines of the lab must be started.</span></span>

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

### <span data-ttu-id="fecd0-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fecd0-124">-Confirm</span></span>
<span data-ttu-id="fecd0-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fecd0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fecd0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fecd0-126">-WhatIf</span></span>
<span data-ttu-id="fecd0-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fecd0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fecd0-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fecd0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fecd0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fecd0-129">-DefaultProfile</span></span>
<span data-ttu-id="fecd0-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fecd0-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fecd0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fecd0-131">CommonParameters</span></span>
<span data-ttu-id="fecd0-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fecd0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fecd0-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fecd0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fecd0-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fecd0-134">INPUTS</span></span>

## <span data-ttu-id="fecd0-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fecd0-135">OUTPUTS</span></span>

### <span data-ttu-id="fecd0-136">Microsoft. Azure. commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="fecd0-136">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="fecd0-137">Denna cmdlet returnerar schemat som anger när den virtuella datorerna i Lab måste vara igång.</span><span class="sxs-lookup"><span data-stu-id="fecd0-137">This cmdlet returns the schedule that specifies when the virtual machines of the lab must be started.</span></span>

## <span data-ttu-id="fecd0-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fecd0-138">NOTES</span></span>

## <span data-ttu-id="fecd0-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fecd0-139">RELATED LINKS</span></span>

[<span data-ttu-id="fecd0-140">Get-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="fecd0-140">Get-AzureRmDtlAutoStartPolicy</span></span>](./Get-AzureRmDtlAutoStartPolicy.md)


