---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 00B8AB6D-02E0-45B5-AB69-49FC69246A34
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb66f34cea13ac95cac47738e7cec214a6a10103
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093309"
---
# <span data-ttu-id="e3063-101">Get-AzureSiteRecoveryRecoveryPlanFile</span><span class="sxs-lookup"><span data-stu-id="e3063-101">Get-AzureSiteRecoveryRecoveryPlanFile</span></span>

## <span data-ttu-id="e3063-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3063-102">SYNOPSIS</span></span>
<span data-ttu-id="e3063-103">Laddar ned en Azure Site Recovery-plan i XML-format.</span><span class="sxs-lookup"><span data-stu-id="e3063-103">Downloads an Azure Site Recovery plan in XML format.</span></span>

## <span data-ttu-id="e3063-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3063-104">SYNTAX</span></span>

### <span data-ttu-id="e3063-105">ByRPObject (standard)</span><span class="sxs-lookup"><span data-stu-id="e3063-105">ByRPObject (Default)</span></span>
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -RecoveryPlan <ASRRecoveryPlan>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e3063-106">ById</span><span class="sxs-lookup"><span data-stu-id="e3063-106">ById</span></span>
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -Id <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3063-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3063-107">DESCRIPTION</span></span>
<span data-ttu-id="e3063-108">Cmdleten **Get-AzureSiteRecoveryRecoveryPlanFile** laddar ned en Azure Site Recovery-plan i XML-format.</span><span class="sxs-lookup"><span data-stu-id="e3063-108">The **Get-AzureSiteRecoveryRecoveryPlanFile** cmdlet downloads an Azure Site Recovery plan in XML format.</span></span>
<span data-ttu-id="e3063-109">Du kan använda den här filen för att uppdatera återställnings planen och sedan överföra den till Site Recovery Server.</span><span class="sxs-lookup"><span data-stu-id="e3063-109">You can use this file to update the recovery plan and then upload it to the Site Recovery server.</span></span>

<span data-ttu-id="e3063-110">En återställnings plan samlar virtuella datorer i en grupp för användning av redundans och återställning.</span><span class="sxs-lookup"><span data-stu-id="e3063-110">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="e3063-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3063-111">EXAMPLES</span></span>

### <span data-ttu-id="e3063-112">Exempel 1: skaffa en återställnings plan fil</span><span class="sxs-lookup"><span data-stu-id="e3063-112">Example 1: Get a recovery plan file</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Get-AzureSiteRecoveryRecoveryPlanFile -RecoveryPlan $RecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="e3063-113">Det här kommandot använder cmdleten **Get-AzureSiteRecoveryRecoveryPlan** för att få återställnings planen och lagrar den sedan i $RecoveryPlan variabel.</span><span class="sxs-lookup"><span data-stu-id="e3063-113">This command uses the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet to get the recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="e3063-114">Det andra kommandot använder cmdleten **GetAzureSiteRecoveryRecoveryPlanFile** för att hämta en XML-fil för återställnings plan i $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="e3063-114">The second command uses the **GetAzureSiteRecoveryRecoveryPlanFile** cmdlet to get the site recovery plan XML file in $RecoveryPlan.</span></span>
<span data-ttu-id="e3063-115">Kommandot lagrar XML-filen på den angivna sökvägen.</span><span class="sxs-lookup"><span data-stu-id="e3063-115">The command stores the XML file at the specified path.</span></span>

## <span data-ttu-id="e3063-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3063-116">PARAMETERS</span></span>

### <span data-ttu-id="e3063-117">-ID</span><span class="sxs-lookup"><span data-stu-id="e3063-117">-Id</span></span>
<span data-ttu-id="e3063-118">Anger ID för den återställnings plan som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="e3063-118">Specifies the ID of the recovery plan to get.</span></span>

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

### <span data-ttu-id="e3063-119">-Path</span><span class="sxs-lookup"><span data-stu-id="e3063-119">-Path</span></span>
<span data-ttu-id="e3063-120">Anger den fullständiga sökvägen för att lagra en återställnings plan XML-fil.</span><span class="sxs-lookup"><span data-stu-id="e3063-120">Specifies the full path to store the recovery plan XML file.</span></span>

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

### <span data-ttu-id="e3063-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="e3063-121">-Profile</span></span>
<span data-ttu-id="e3063-122">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e3063-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e3063-123">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e3063-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e3063-124">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e3063-124">-RecoveryPlan</span></span>
<span data-ttu-id="e3063-125">Anger ett **ASRRecoveryPlan** -objekt som du vill hämta återställnings planen från.</span><span class="sxs-lookup"><span data-stu-id="e3063-125">Specifies an **ASRRecoveryPlan** object from which to get the recovery plan.</span></span>
<span data-ttu-id="e3063-126">För att få ett **ASRRecoveryPlan** -objekt, Använd cmdleten **Get-AzureSiteRecoveryRecoveryPlan** .</span><span class="sxs-lookup"><span data-stu-id="e3063-126">To obtain an **ASRRecoveryPlan** object, use the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>

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

### <span data-ttu-id="e3063-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3063-127">CommonParameters</span></span>
<span data-ttu-id="e3063-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3063-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3063-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3063-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3063-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3063-130">INPUTS</span></span>

## <span data-ttu-id="e3063-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3063-131">OUTPUTS</span></span>

## <span data-ttu-id="e3063-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3063-132">NOTES</span></span>

## <span data-ttu-id="e3063-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3063-133">RELATED LINKS</span></span>

[<span data-ttu-id="e3063-134">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e3063-134">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)


