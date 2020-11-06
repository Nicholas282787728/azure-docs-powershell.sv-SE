---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 5f4298c2a4bfdc081447e6a8b15bac565b20b2db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576473"
---
# <span data-ttu-id="f32e1-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f32e1-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="f32e1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f32e1-102">SYNOPSIS</span></span>
<span data-ttu-id="f32e1-103">Tar bort den angivna planen för ASR-återställning från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="f32e1-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f32e1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f32e1-104">SYNTAX</span></span>

### <span data-ttu-id="f32e1-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="f32e1-105">ByObject (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f32e1-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f32e1-106">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f32e1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f32e1-107">DESCRIPTION</span></span>
<span data-ttu-id="f32e1-108">Cmdleten **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** tar bort den angivna återställnings planen från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="f32e1-108">The **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="f32e1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f32e1-109">EXAMPLES</span></span>

### <span data-ttu-id="f32e1-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f32e1-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="f32e1-111">Tar bort den angivna återställnings planen och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="f32e1-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f32e1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f32e1-112">PARAMETERS</span></span>

### <span data-ttu-id="f32e1-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f32e1-113">-Confirm</span></span>
<span data-ttu-id="f32e1-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f32e1-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f32e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f32e1-115">-DefaultProfile</span></span>
<span data-ttu-id="f32e1-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f32e1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="f32e1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f32e1-117">-InputObject</span></span>
<span data-ttu-id="f32e1-118">Indatavärdet till cmdleten: det objekt för ASR-återställning som motsvarar återställnings planen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f32e1-118">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f32e1-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="f32e1-119">-Name</span></span>
<span data-ttu-id="f32e1-120">Anger namnet på den återställnings plan som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f32e1-120">Specifies the name of the recovery plan to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f32e1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f32e1-121">-WhatIf</span></span>
<span data-ttu-id="f32e1-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f32e1-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f32e1-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f32e1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f32e1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f32e1-124">CommonParameters</span></span>
<span data-ttu-id="f32e1-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f32e1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f32e1-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f32e1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f32e1-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f32e1-127">INPUTS</span></span>

### <span data-ttu-id="f32e1-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f32e1-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="f32e1-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f32e1-129">OUTPUTS</span></span>

### <span data-ttu-id="f32e1-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="f32e1-130">System.Object</span></span>

## <span data-ttu-id="f32e1-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f32e1-131">NOTES</span></span>

## <span data-ttu-id="f32e1-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f32e1-132">RELATED LINKS</span></span>

[<span data-ttu-id="f32e1-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f32e1-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="f32e1-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f32e1-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="f32e1-135">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f32e1-135">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


