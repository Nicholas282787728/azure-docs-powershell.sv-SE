---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 16146A0D-4605-489A-8259-A37BEAC98306
online version: ''
schema: 2.0.0
ms.openlocfilehash: 664c9af9373120f293153a1bbdc65d1a82637631
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099245"
---
# <span data-ttu-id="130af-101">Update-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="130af-101">Update-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="130af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="130af-102">SYNOPSIS</span></span>
<span data-ttu-id="130af-103">Uppdaterar egenskaperna för en skydds enhet i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="130af-103">Updates the properties of a protection entity in Azure Site Recovery.</span></span>

## <span data-ttu-id="130af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="130af-104">SYNTAX</span></span>

```
Update-AzureSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="130af-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="130af-105">DESCRIPTION</span></span>
<span data-ttu-id="130af-106">Cmdleten **Update-AzureSiteRecoveryProtectionEntity** uppdaterar egenskaperna för en skydds enhet i Azure Site Recovery, till exempel ägare till virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="130af-106">The **Update-AzureSiteRecoveryProtectionEntity** cmdlet updates the properties of a protection entity in Azure Site Recovery, such as virtual machine owner information.</span></span>
<span data-ttu-id="130af-107">Denna cmdlet stöds endast för bildskärm (VMM) för virtuella datorer för entiteter som skyddas av VMM.</span><span class="sxs-lookup"><span data-stu-id="130af-107">This cmdlet is supported only for Virtual Machine Monitor (VMM) to VMM protected protection entities.</span></span>

## <span data-ttu-id="130af-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="130af-108">EXAMPLES</span></span>

### <span data-ttu-id="130af-109">Exempel 1: uppdatera en skydds enhet</span><span class="sxs-lookup"><span data-stu-id="130af-109">Example 1: Update a protection entity</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container
PS C:\> Update-AzureSiteRecoveryProtectionEntity -ProtectionEntity $ProtectionEntity
           Name             : 
           ID               : 680ffe0f-6236-465e-8c94-81242fa67e6d
           ClientRequestId  : 2c47e6ce-1460-4187-8a0f-b9073735fa38-2014-12-30 06:44:40Z-P
           State            : NotStarted
           StateDescription : NotStarted
           StartTime        : 
           EndTime          : 
           AllowedActions   : {}
           Tasks            : {}
           Errors           : {}
```

<span data-ttu-id="130af-110">Det första kommandot får en skyddad container med cmdleten **Get-AzureSiteRecoveryProtectionContainer** och lagrar sedan objektet i variabeln $container.</span><span class="sxs-lookup"><span data-stu-id="130af-110">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that object in the $Container variable.</span></span>

<span data-ttu-id="130af-111">Med det andra kommandot hämtas den skyddade virtuella datorn som tillhör behållaren som är lagrad i $Container med hjälp av cmdleten **Get-AzureSiteRecoveryProtectionEntity** och sparas sedan i $ProtectionEntity variabel.</span><span class="sxs-lookup"><span data-stu-id="130af-111">The second command gets the protected virtual machine that belongs to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet, and then stores it in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="130af-112">Kommandot uppdaterar skydds enheten i $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="130af-112">The final command updates the protection entity in $ProtectionEntity.</span></span>

## <span data-ttu-id="130af-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="130af-113">PARAMETERS</span></span>

### <span data-ttu-id="130af-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="130af-114">-Profile</span></span>
<span data-ttu-id="130af-115">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="130af-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="130af-116">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="130af-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="130af-117">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="130af-117">-ProtectionEntity</span></span>
<span data-ttu-id="130af-118">Anger en skydds enhet att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="130af-118">Specifies a protection entity to update.</span></span>
<span data-ttu-id="130af-119">För att få ett **ASRProtectionEntity** -objekt, Använd cmdleten **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="130af-119">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="130af-120">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="130af-120">-WaitForCompletion</span></span>
<span data-ttu-id="130af-121">Anger att denna cmdlet väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.</span><span class="sxs-lookup"><span data-stu-id="130af-121">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="130af-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="130af-122">CommonParameters</span></span>
<span data-ttu-id="130af-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="130af-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="130af-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="130af-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="130af-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="130af-125">INPUTS</span></span>

## <span data-ttu-id="130af-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="130af-126">OUTPUTS</span></span>

## <span data-ttu-id="130af-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="130af-127">NOTES</span></span>

## <span data-ttu-id="130af-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="130af-128">RELATED LINKS</span></span>

[<span data-ttu-id="130af-129">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="130af-129">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="130af-130">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="130af-130">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="130af-131">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="130af-131">Set-AzureSiteRecoveryProtectionEntity</span></span>](./Set-AzureSiteRecoveryProtectionEntity.md)


