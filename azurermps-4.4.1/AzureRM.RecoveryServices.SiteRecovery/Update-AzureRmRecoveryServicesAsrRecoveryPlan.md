---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 21a46346c681a6f184033d4f50d65e6c9a019844
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756873"
---
# <span data-ttu-id="2ef32-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2ef32-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="2ef32-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2ef32-102">SYNOPSIS</span></span>
<span data-ttu-id="2ef32-103">Uppdaterar innehållet i en Azure Site Recovery-plan.</span><span class="sxs-lookup"><span data-stu-id="2ef32-103">Updates the contents of an Azure Site recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ef32-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2ef32-104">SYNTAX</span></span>

### <span data-ttu-id="2ef32-105">ByRPObject (standard)</span><span class="sxs-lookup"><span data-stu-id="2ef32-105">ByRPObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ef32-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="2ef32-106">ByRPFile</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ef32-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2ef32-107">DESCRIPTION</span></span>
<span data-ttu-id="2ef32-108">Cmdleten **Update-AzureRmRecoveryServicesAsrRecoveryPlan** uppdaterar innehållet i en återställnings plan med hjälp av innehållet i det angivna objektet för ASR-återställning eller en JSON-fil för ASR-återställning.</span><span class="sxs-lookup"><span data-stu-id="2ef32-108">The **Update-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="2ef32-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2ef32-109">EXAMPLES</span></span>

### <span data-ttu-id="2ef32-110">Exempel 1: uppdatera en återställnings plan</span><span class="sxs-lookup"><span data-stu-id="2ef32-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="2ef32-111">Starta uppdateringen av en återställnings plan med innehållet i det angivna objektet för ASR-återställning och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="2ef32-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="2ef32-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2ef32-112">PARAMETERS</span></span>

### <span data-ttu-id="2ef32-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ef32-113">-InputObject</span></span>
<span data-ttu-id="2ef32-114">Indatavärdet till cmdlet: anger ett objekt för ASR-återställning, vars innehåll används för att uppdatera den återställnings plan som refereras till av objektet.</span><span class="sxs-lookup"><span data-stu-id="2ef32-114">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ef32-115">-Path</span><span class="sxs-lookup"><span data-stu-id="2ef32-115">-Path</span></span>
<span data-ttu-id="2ef32-116">Anger sökvägen till den definitions fil för återhämtnings plan som används för att uppdatera återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="2ef32-116">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ef32-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2ef32-117">-Confirm</span></span>
<span data-ttu-id="2ef32-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2ef32-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ef32-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ef32-119">-WhatIf</span></span>
<span data-ttu-id="2ef32-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2ef32-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ef32-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2ef32-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ef32-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ef32-122">CommonParameters</span></span>
<span data-ttu-id="2ef32-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ef32-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ef32-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ef32-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ef32-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2ef32-125">INPUTS</span></span>

### <span data-ttu-id="2ef32-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2ef32-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="2ef32-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2ef32-127">OUTPUTS</span></span>

### <span data-ttu-id="2ef32-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="2ef32-128">System.Object</span></span>

## <span data-ttu-id="2ef32-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2ef32-129">NOTES</span></span>

## <span data-ttu-id="2ef32-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2ef32-130">RELATED LINKS</span></span>

[<span data-ttu-id="2ef32-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2ef32-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2ef32-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2ef32-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2ef32-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2ef32-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)


