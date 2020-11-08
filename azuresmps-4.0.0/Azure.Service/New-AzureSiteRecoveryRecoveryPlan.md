---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2F749E4A-149F-44E0-8AEB-F2C416140906
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7d1162ed2c9126942cc6ae31cbe31fdc2ef130d8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099206"
---
# <span data-ttu-id="d59e7-101">New-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d59e7-101">New-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="d59e7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d59e7-102">SYNOPSIS</span></span>
<span data-ttu-id="d59e7-103">Skapar en plan för webbplats återställning i webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="d59e7-103">Creates a site recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="d59e7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d59e7-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryRecoveryPlan -File <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d59e7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d59e7-105">DESCRIPTION</span></span>
<span data-ttu-id="d59e7-106">Cmdleten **New-AzureSiteRecoveryRecoveryPlan** skapar en återställnings plan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d59e7-106">The **New-AzureSiteRecoveryRecoveryPlan** cmdlet creates a recovery plan in Azure Site Recovery.</span></span>

<span data-ttu-id="d59e7-107">En återställnings plan samlar virtuella datorer i en grupp för användning av redundans och återställning.</span><span class="sxs-lookup"><span data-stu-id="d59e7-107">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="d59e7-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d59e7-108">EXAMPLES</span></span>

### <span data-ttu-id="d59e7-109">Exempel 1: lägga till en återställnings plan i ett valv för webbplats återställning</span><span class="sxs-lookup"><span data-stu-id="d59e7-109">Example 1: Add a recovery plan to a Site Recovery vault</span></span>
```
PS C:\> New-AzureSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="d59e7-110">Det här kommandot lägger till återställnings planen RecoveryPlan.xml till Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="d59e7-110">This command adds the recovery plan named RecoveryPlan.xml to the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="d59e7-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d59e7-111">PARAMETERS</span></span>

### <span data-ttu-id="d59e7-112">-Fil</span><span class="sxs-lookup"><span data-stu-id="d59e7-112">-File</span></span>
<span data-ttu-id="d59e7-113">Anger sökvägen till återställnings plan filen.</span><span class="sxs-lookup"><span data-stu-id="d59e7-113">Specifies the path of the recovery plan file.</span></span>

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

### <span data-ttu-id="d59e7-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="d59e7-114">-Profile</span></span>
<span data-ttu-id="d59e7-115">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="d59e7-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d59e7-116">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="d59e7-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d59e7-117">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="d59e7-117">-WaitForCompletion</span></span>
<span data-ttu-id="d59e7-118">Anger att cmdleten väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.</span><span class="sxs-lookup"><span data-stu-id="d59e7-118">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="d59e7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d59e7-119">CommonParameters</span></span>
<span data-ttu-id="d59e7-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d59e7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d59e7-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d59e7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d59e7-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d59e7-122">INPUTS</span></span>

## <span data-ttu-id="d59e7-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d59e7-123">OUTPUTS</span></span>

## <span data-ttu-id="d59e7-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d59e7-124">NOTES</span></span>

## <span data-ttu-id="d59e7-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d59e7-125">RELATED LINKS</span></span>

[<span data-ttu-id="d59e7-126">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d59e7-126">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="d59e7-127">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d59e7-127">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="d59e7-128">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d59e7-128">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


