---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8557B04E-DE35-473E-8F5D-B72B70300AA6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1949d30d6bbea16e1626954bf241df36d81533e1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093311"
---
# <span data-ttu-id="747c9-101">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="747c9-101">Get-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="747c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="747c9-102">SYNOPSIS</span></span>
<span data-ttu-id="747c9-103">Hämtar en återställnings plan i webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="747c9-103">Gets a recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="747c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="747c9-104">SYNTAX</span></span>

### <span data-ttu-id="747c9-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="747c9-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="747c9-106">ById</span><span class="sxs-lookup"><span data-stu-id="747c9-106">ById</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="747c9-107">ByName</span><span class="sxs-lookup"><span data-stu-id="747c9-107">ByName</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="747c9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="747c9-108">DESCRIPTION</span></span>
<span data-ttu-id="747c9-109">Cmdleten **Get-AzureSiteRecoveryRecoveryPlan** hämtar en återställnings plan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="747c9-109">The **Get-AzureSiteRecoveryRecoveryPlan** cmdlet gets a recovery plan in Azure Site Recovery.</span></span>

## <span data-ttu-id="747c9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="747c9-110">EXAMPLES</span></span>

### <span data-ttu-id="747c9-111">Exempel 1: skaffa en återställnings plan</span><span class="sxs-lookup"><span data-stu-id="747c9-111">Example 1: Get a recovery plan</span></span>
```
PS C:\> Get-AzureSiteRecoveryRecoveryPlan
ID                            Name                          ServerId                      TargetServerId
--                            ----                          --------                      --------------
71de8ebc-1e9a-4242-aec3-ee... ContosoPlan                   4a94c4a9-c856-4577-afbd-36... 78facf56-b273-4941-82fd-cc...
```

<span data-ttu-id="747c9-112">Det här kommandot får information om återställnings planen för det aktuella Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="747c9-112">This command gets information about the recovery plan for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="747c9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="747c9-113">PARAMETERS</span></span>

### <span data-ttu-id="747c9-114">-ID</span><span class="sxs-lookup"><span data-stu-id="747c9-114">-Id</span></span>
<span data-ttu-id="747c9-115">Anger ID för den återställnings plan som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="747c9-115">Specifies the ID of the recovery plan to get.</span></span>

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

### <span data-ttu-id="747c9-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="747c9-116">-Name</span></span>
<span data-ttu-id="747c9-117">Anger namnet på den återställnings plan som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="747c9-117">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="747c9-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="747c9-118">-Profile</span></span>
<span data-ttu-id="747c9-119">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="747c9-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="747c9-120">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="747c9-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="747c9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="747c9-121">CommonParameters</span></span>
<span data-ttu-id="747c9-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="747c9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="747c9-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="747c9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="747c9-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="747c9-124">INPUTS</span></span>

## <span data-ttu-id="747c9-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="747c9-125">OUTPUTS</span></span>

## <span data-ttu-id="747c9-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="747c9-126">NOTES</span></span>

## <span data-ttu-id="747c9-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="747c9-127">RELATED LINKS</span></span>

[<span data-ttu-id="747c9-128">New-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="747c9-128">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="747c9-129">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="747c9-129">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="747c9-130">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="747c9-130">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


