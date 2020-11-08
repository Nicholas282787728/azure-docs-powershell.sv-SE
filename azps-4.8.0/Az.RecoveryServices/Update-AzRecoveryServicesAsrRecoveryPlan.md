---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 99c91f24bcc81ee6d6971b74779dfd116b90fdef
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101299"
---
# <span data-ttu-id="3f952-101">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3f952-101">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="3f952-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f952-102">SYNOPSIS</span></span>
<span data-ttu-id="3f952-103">Uppdaterar innehållet i en Azure Site Recovery-plan.</span><span class="sxs-lookup"><span data-stu-id="3f952-103">Updates the contents of an Azure Site recovery plan.</span></span>

## <span data-ttu-id="3f952-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f952-104">SYNTAX</span></span>

### <span data-ttu-id="3f952-105">ByRPObject (standard)</span><span class="sxs-lookup"><span data-stu-id="3f952-105">ByRPObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f952-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="3f952-106">ByRPFile</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f952-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f952-107">DESCRIPTION</span></span>
<span data-ttu-id="3f952-108">Cmdleten **Update-AzRecoveryServicesAsrRecoveryPlan** uppdaterar innehållet i en återställnings plan med hjälp av innehållet i det angivna objektet för ASR-återställning eller en JSON-fil för ASR-återställning.</span><span class="sxs-lookup"><span data-stu-id="3f952-108">The **Update-AzRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="3f952-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f952-109">EXAMPLES</span></span>

### <span data-ttu-id="3f952-110">Exempel 1: uppdatera en återställnings plan</span><span class="sxs-lookup"><span data-stu-id="3f952-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="3f952-111">Starta uppdateringen av en återställnings plan med innehållet i det angivna objektet för ASR-återställning och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="3f952-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="3f952-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f952-112">PARAMETERS</span></span>

### <span data-ttu-id="3f952-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f952-113">-DefaultProfile</span></span>
<span data-ttu-id="3f952-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3f952-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="3f952-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f952-115">-InputObject</span></span>
<span data-ttu-id="3f952-116">Indatavärdet till cmdlet: anger ett objekt för ASR-återställning, vars innehåll används för att uppdatera den återställnings plan som refereras till av objektet.</span><span class="sxs-lookup"><span data-stu-id="3f952-116">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f952-117">-Path</span><span class="sxs-lookup"><span data-stu-id="3f952-117">-Path</span></span>
<span data-ttu-id="3f952-118">Anger sökvägen till den definitions fil för återhämtnings plan som används för att uppdatera återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="3f952-118">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f952-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3f952-119">-Confirm</span></span>
<span data-ttu-id="3f952-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3f952-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f952-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f952-121">-WhatIf</span></span>
<span data-ttu-id="3f952-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3f952-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f952-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3f952-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f952-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f952-124">CommonParameters</span></span>
<span data-ttu-id="3f952-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f952-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f952-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f952-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f952-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f952-127">INPUTS</span></span>

### <span data-ttu-id="3f952-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3f952-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="3f952-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f952-129">OUTPUTS</span></span>

### <span data-ttu-id="3f952-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3f952-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3f952-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f952-131">NOTES</span></span>

## <span data-ttu-id="3f952-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f952-132">RELATED LINKS</span></span>

[<span data-ttu-id="3f952-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3f952-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="3f952-134">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3f952-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="3f952-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3f952-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)
