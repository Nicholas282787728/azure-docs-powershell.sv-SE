---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 5625ED47-BD85-4BF5-9044-2012E5A67BA4
online version: ''
schema: 2.0.0
ms.openlocfilehash: d1c680adf1d9d850f89cb81e1525a0e0e06eb6c9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099244"
---
# <span data-ttu-id="f6269-101">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f6269-101">Update-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="f6269-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6269-102">SYNOPSIS</span></span>
<span data-ttu-id="f6269-103">Uppdaterar en återställnings plan i webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="f6269-103">Updates a recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="f6269-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6269-104">SYNTAX</span></span>

```
Update-AzureSiteRecoveryRecoveryPlan -File <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6269-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6269-105">DESCRIPTION</span></span>
<span data-ttu-id="f6269-106">Cmdleten **Update-AzureSiteRecoveryRecoveryPlan** uppdaterar en återställnings plan i Azure Site Recovery och publicerar den sedan.</span><span class="sxs-lookup"><span data-stu-id="f6269-106">The **Update-AzureSiteRecoveryRecoveryPlan** cmdlet updates a recovery plan in Azure Site Recovery and then publishes it.</span></span>

## <span data-ttu-id="f6269-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6269-107">EXAMPLES</span></span>

### <span data-ttu-id="f6269-108">Exempel 1: uppdatera en återställnings plan</span><span class="sxs-lookup"><span data-stu-id="f6269-108">Example 1: Update a recovery plan</span></span>
```
PS C:\> Update-AzureSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="f6269-109">Det här kommandot uppdaterar den angivna återställnings planen och publicerar den sedan.</span><span class="sxs-lookup"><span data-stu-id="f6269-109">This command updates the specified recovery plan, and then publishes it.</span></span>

## <span data-ttu-id="f6269-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6269-110">PARAMETERS</span></span>

### <span data-ttu-id="f6269-111">-Fil</span><span class="sxs-lookup"><span data-stu-id="f6269-111">-File</span></span>
<span data-ttu-id="f6269-112">Anger återställnings plan filen för återställnings planen som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="f6269-112">Specifies the recovery plan file of the recovery plan that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6269-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="f6269-113">-Profile</span></span>
<span data-ttu-id="f6269-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="f6269-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f6269-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="f6269-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f6269-116">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="f6269-116">-WaitForCompletion</span></span>
<span data-ttu-id="f6269-117">Anger att cmdleten väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.</span><span class="sxs-lookup"><span data-stu-id="f6269-117">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="f6269-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6269-118">CommonParameters</span></span>
<span data-ttu-id="f6269-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6269-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6269-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6269-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6269-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6269-121">INPUTS</span></span>

## <span data-ttu-id="f6269-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6269-122">OUTPUTS</span></span>

## <span data-ttu-id="f6269-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6269-123">NOTES</span></span>

## <span data-ttu-id="f6269-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6269-124">RELATED LINKS</span></span>

[<span data-ttu-id="f6269-125">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f6269-125">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="f6269-126">New-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f6269-126">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="f6269-127">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f6269-127">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)


