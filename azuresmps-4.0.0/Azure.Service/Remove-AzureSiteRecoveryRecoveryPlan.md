---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: A62D8097-FC26-40E4-803C-09F7979A2A2B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91f96e5004446a4490a1d9b78a2dc0c7f3a25cd6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099341"
---
# <span data-ttu-id="4148e-101">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4148e-101">Remove-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="4148e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4148e-102">SYNOPSIS</span></span>
<span data-ttu-id="4148e-103">Tar bort en plan för webbplats återställning från webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="4148e-103">Removes a site recovery plan from Site Recovery.</span></span>

## <span data-ttu-id="4148e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4148e-104">SYNTAX</span></span>

### <span data-ttu-id="4148e-105">ByRPObject (standard)</span><span class="sxs-lookup"><span data-stu-id="4148e-105">ByRPObject (Default)</span></span>
```
Remove-AzureSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-WaitForCompletion] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4148e-106">ById</span><span class="sxs-lookup"><span data-stu-id="4148e-106">ById</span></span>
```
Remove-AzureSiteRecoveryRecoveryPlan -Id <String> [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4148e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4148e-107">DESCRIPTION</span></span>
<span data-ttu-id="4148e-108">Cmdleten **Remove-AzureSiteRecoveryRecoveryPlan** tar bort en plan för webbplats återställning från den aktuella Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4148e-108">The **Remove-AzureSiteRecoveryRecoveryPlan** cmdlet removes a site recovery plan from the current Azure Site Recovery.</span></span>

## <span data-ttu-id="4148e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4148e-109">EXAMPLES</span></span>

### <span data-ttu-id="4148e-110">Exempel 1: ta bort en återställnings plan</span><span class="sxs-lookup"><span data-stu-id="4148e-110">Example 1: Remove a recovery plan</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Remove-AzureSiteRecoveryRecoveryPlan -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="4148e-111">I det första kommandot används cmdleten **Get-AzureSiteRecoveryRecoveryPlan** för att hämta webbplatsen för webbplats återställning och sedan lagras den i $RecoveryPlan variabel.</span><span class="sxs-lookup"><span data-stu-id="4148e-111">The first command uses the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet to get the Site Recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="4148e-112">Det andra kommandot tar bort återställnings planen i $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="4148e-112">The second command removes the recovery plan in $RecoveryPlan.</span></span>

## <span data-ttu-id="4148e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4148e-113">PARAMETERS</span></span>

### <span data-ttu-id="4148e-114">-Force</span><span class="sxs-lookup"><span data-stu-id="4148e-114">-Force</span></span>
<span data-ttu-id="4148e-115">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4148e-115">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4148e-116">-ID</span><span class="sxs-lookup"><span data-stu-id="4148e-116">-Id</span></span>
<span data-ttu-id="4148e-117">Anger ID för återställnings planen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="4148e-117">Specifies the ID of the recovery plan to remove.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4148e-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="4148e-118">-Profile</span></span>
<span data-ttu-id="4148e-119">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="4148e-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4148e-120">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="4148e-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4148e-121">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4148e-121">-RecoveryPlan</span></span>
<span data-ttu-id="4148e-122">Anger vilken återställnings plan som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="4148e-122">Specifies the recovery plan to remove.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4148e-123">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="4148e-123">-WaitForCompletion</span></span>
<span data-ttu-id="4148e-124">Anger att cmdleten väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.</span><span class="sxs-lookup"><span data-stu-id="4148e-124">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4148e-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4148e-125">-Confirm</span></span>
<span data-ttu-id="4148e-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4148e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4148e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4148e-127">-WhatIf</span></span>
<span data-ttu-id="4148e-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4148e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4148e-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4148e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4148e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4148e-130">CommonParameters</span></span>
<span data-ttu-id="4148e-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4148e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4148e-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4148e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4148e-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4148e-133">INPUTS</span></span>

## <span data-ttu-id="4148e-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4148e-134">OUTPUTS</span></span>

## <span data-ttu-id="4148e-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4148e-135">NOTES</span></span>

## <span data-ttu-id="4148e-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4148e-136">RELATED LINKS</span></span>

[<span data-ttu-id="4148e-137">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4148e-137">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="4148e-138">New-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4148e-138">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="4148e-139">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4148e-139">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


