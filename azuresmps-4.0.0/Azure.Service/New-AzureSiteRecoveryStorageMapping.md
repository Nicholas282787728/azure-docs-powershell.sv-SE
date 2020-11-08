---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2D09422F-82B1-4243-B835-8BF223A6F936
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6f02f333601172341de4fe8a0bf629037f712a5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099205"
---
# <span data-ttu-id="e0544-101">New-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="e0544-101">New-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="e0544-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0544-102">SYNOPSIS</span></span>
<span data-ttu-id="e0544-103">Skapar en mappning mellan ett Azure-lagringssystem och ett återställnings objekt.</span><span class="sxs-lookup"><span data-stu-id="e0544-103">Creates a mapping between an Azure Storage object and recovery Storage object.</span></span>

## <span data-ttu-id="e0544-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0544-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryStorageMapping -PrimaryStorage <ASRStorage> -RecoveryStorage <ASRStorage>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e0544-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0544-105">DESCRIPTION</span></span>
<span data-ttu-id="e0544-106">Cmdleten **New-AzureSiteRecoveryStorageMapping** skapar en mappning mellan ett Azure Site Recovery-hanterat primärt Azure-lagringssystem och ett återställnings objekt.</span><span class="sxs-lookup"><span data-stu-id="e0544-106">The **New-AzureSiteRecoveryStorageMapping** cmdlet creates a mapping between an Azure Site Recovery managed primary Azure Storage object and a recovery Storage object.</span></span>

## <span data-ttu-id="e0544-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0544-107">EXAMPLES</span></span>

### <span data-ttu-id="e0544-108">Exempel 1: skapa en mappning mellan ett lagrings objekt och ett återställnings objekt</span><span class="sxs-lookup"><span data-stu-id="e0544-108">Example 1: Create a mapping between a storage object and a recovery storage object</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Storages = Get-AzureSiteRecoveryStorage -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryStorageMapping -PrimaryStorage $Storages[0] -RecoveryStorage $Storages[1]
```

<span data-ttu-id="e0544-109">Den första kommando cmdleten hämtar servrar för det aktuella Azure Site Recovery-valvet med cmdleten **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="e0544-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="e0544-110">Kommandot lagrar webbplats återställnings servrarna i $Servers mat ris variabel.</span><span class="sxs-lookup"><span data-stu-id="e0544-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="e0544-111">Det andra kommandot får webbplatsen för webbplats återställning för den första servern i $Servers matris och lagrar den sedan i $Storages.</span><span class="sxs-lookup"><span data-stu-id="e0544-111">The second command gets the site recovery storage for the first server in the $Servers array, and then stores it in the $Storages.</span></span>

<span data-ttu-id="e0544-112">Med kommandot slut skapas en mappning mellan det primära nätverket och återställnings nätverket.</span><span class="sxs-lookup"><span data-stu-id="e0544-112">The final command creates a mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="e0544-113">Kommandot anger det primära lagrings objekt som det första elementet i $Storages.</span><span class="sxs-lookup"><span data-stu-id="e0544-113">The command specifies the primary Storage object as the first element of $Storages.</span></span>
<span data-ttu-id="e0544-114">Kommandot anger återställnings objekt som det andra elementet i $Storages.</span><span class="sxs-lookup"><span data-stu-id="e0544-114">The command specifies the recovery Storage object as the second element of $Storages.</span></span>

## <span data-ttu-id="e0544-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0544-115">PARAMETERS</span></span>

### <span data-ttu-id="e0544-116">-PrimaryStorage</span><span class="sxs-lookup"><span data-stu-id="e0544-116">-PrimaryStorage</span></span>
<span data-ttu-id="e0544-117">Anger primär lagrings utrymmet som ska mappas till återställnings lagringen.</span><span class="sxs-lookup"><span data-stu-id="e0544-117">Specifies the primary Storage to map to the recovery Storage.</span></span>
<span data-ttu-id="e0544-118">Använd Get-AzureSiteRecoveryStorage cmdlet för att få ett **ASRStorage** -objekt.</span><span class="sxs-lookup"><span data-stu-id="e0544-118">To obtain an **ASRStorage** object, use the Get-AzureSiteRecoveryStorage cmdlet.</span></span>

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0544-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="e0544-119">-Profile</span></span>
<span data-ttu-id="e0544-120">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e0544-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e0544-121">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e0544-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e0544-122">-RecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="e0544-122">-RecoveryStorage</span></span>
<span data-ttu-id="e0544-123">Anger återställnings objekt.</span><span class="sxs-lookup"><span data-stu-id="e0544-123">Specifies the recovery Storage object.</span></span>
<span data-ttu-id="e0544-124">Denna cmdlet mappar det primära lagrings objekt till det lagrings objekt som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e0544-124">This cmdlet maps the primary Storage object to the Storage object that this parameter specifies.</span></span>
<span data-ttu-id="e0544-125">För att få ett **ASRStorage** -objekt, Använd **Get-AzureSiteRecoveryStorage**.</span><span class="sxs-lookup"><span data-stu-id="e0544-125">To obtain an **ASRStorage** object, use **Get-AzureSiteRecoveryStorage**.</span></span>

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0544-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0544-126">CommonParameters</span></span>
<span data-ttu-id="e0544-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0544-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0544-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0544-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0544-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0544-129">INPUTS</span></span>

## <span data-ttu-id="e0544-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0544-130">OUTPUTS</span></span>

## <span data-ttu-id="e0544-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0544-131">NOTES</span></span>

## <span data-ttu-id="e0544-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0544-132">RELATED LINKS</span></span>

[<span data-ttu-id="e0544-133">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="e0544-133">Get-AzureSiteRecoveryStorage</span></span>](./Get-AzureSiteRecoveryStorage.md)

[<span data-ttu-id="e0544-134">Get-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="e0544-134">Get-AzureSiteRecoveryStorageMapping</span></span>](./Get-AzureSiteRecoveryStorageMapping.md)

[<span data-ttu-id="e0544-135">Remove-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="e0544-135">Remove-AzureSiteRecoveryStorageMapping</span></span>](./Remove-AzureSiteRecoveryStorageMapping.md)


