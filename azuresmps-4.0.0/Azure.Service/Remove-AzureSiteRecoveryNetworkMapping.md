---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: BB36A434-6BE3-46BF-B10A-FCD6C766CB84
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87414a56778123053615bb36a06113e2b0b0633f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099340"
---
# <span data-ttu-id="9faf4-101">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9faf4-101">Remove-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="9faf4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9faf4-102">SYNOPSIS</span></span>
<span data-ttu-id="9faf4-103">Tar bort en nätverks mappning från ett återställnings valv för webbplatser.</span><span class="sxs-lookup"><span data-stu-id="9faf4-103">Removes a network mapping from a Site Recovery vault.</span></span>

## <span data-ttu-id="9faf4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9faf4-104">SYNTAX</span></span>

```
Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9faf4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9faf4-105">DESCRIPTION</span></span>
<span data-ttu-id="9faf4-106">Cmdleten **Remove-AzureSiteRecoveryNetworkMapping** tar bort en nätverks mappning från det aktuella Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="9faf4-106">The **Remove-AzureSiteRecoveryNetworkMapping** cmdlet removes a network mapping from the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="9faf4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9faf4-107">EXAMPLES</span></span>

### <span data-ttu-id="9faf4-108">Exempel 1: ta bort mappningen mellan ett nätverk och ett återställnings nätverk</span><span class="sxs-lookup"><span data-stu-id="9faf4-108">Example 1: Remove the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

<span data-ttu-id="9faf4-109">Den första kommando cmdleten hämtar servrar för det aktuella Azure Site Recovery-valvet med cmdleten **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="9faf4-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="9faf4-110">Kommandot lagrar webbplats återställnings servrarna i $Servers mat ris variabel.</span><span class="sxs-lookup"><span data-stu-id="9faf4-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="9faf4-111">Det andra kommandot får mappningen mellan det primära nätverket och återställnings nätverket och lagrar det i $NetworkMapping variabeln.</span><span class="sxs-lookup"><span data-stu-id="9faf4-111">The second command gets the mapping between the primary network and the recovery network, and then stores it in the $NetworkMapping variable.</span></span>
<span data-ttu-id="9faf4-112">Kommandot anger den primära servern för nätverks mappningen som det första elementet i $Servers.</span><span class="sxs-lookup"><span data-stu-id="9faf4-112">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="9faf4-113">Kommandot anger Server för återställnings nätverket som det andra $Servers.</span><span class="sxs-lookup"><span data-stu-id="9faf4-113">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

<span data-ttu-id="9faf4-114">Kommandot tar bort nätverks mappningen i $NetworkMapping.</span><span class="sxs-lookup"><span data-stu-id="9faf4-114">The final command removes the network mapping in $NetworkMapping.</span></span>

### <span data-ttu-id="9faf4-115">Exempel 2: ta bort mappningen mellan ett nätverk och ett virtuellt Azure-nätverk</span><span class="sxs-lookup"><span data-stu-id="9faf4-115">Example 2: Remove the mapping between a network and an Azure virtual machine network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -Azure
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

<span data-ttu-id="9faf4-116">Den första kommando cmdleten hämtar servrar för det aktuella Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="9faf4-116">The first command cmdlet gets servers for the current Site Recovery vault.</span></span>
<span data-ttu-id="9faf4-117">Kommandot lagrar webbplats återställnings servrarna i $Servers mat ris variabel.</span><span class="sxs-lookup"><span data-stu-id="9faf4-117">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="9faf4-118">Det andra kommandot får en mappning mellan det primära nätverket och ett nätverk med Azure Virtual Machine och lagrar det sedan i $NetworkMapping variabel.</span><span class="sxs-lookup"><span data-stu-id="9faf4-118">The second command gets a mapping between the primary network and an Azure virtual machine network, and then stores it in the $NetworkMapping variable.</span></span>
<span data-ttu-id="9faf4-119">Kommandot anger det primära servern för nätverket som det första elementet i $Servers.</span><span class="sxs-lookup"><span data-stu-id="9faf4-119">The command specifies the primary server for the network as the first element of $Servers.</span></span>
<span data-ttu-id="9faf4-120">Kommandot anger *Azure* -parametern.</span><span class="sxs-lookup"><span data-stu-id="9faf4-120">The command specifies the *Azure* parameter.</span></span>
<span data-ttu-id="9faf4-121">Därför hämtas kommandot till en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="9faf4-121">Therefore, the command gets the mapping to an Azure virtual machine network.</span></span>

<span data-ttu-id="9faf4-122">Kommandot tar bort nätverks mappningen i $NetworkMapping.</span><span class="sxs-lookup"><span data-stu-id="9faf4-122">The final command removes the network mapping in $NetworkMapping.</span></span>

## <span data-ttu-id="9faf4-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9faf4-123">PARAMETERS</span></span>

### <span data-ttu-id="9faf4-124">-NetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9faf4-124">-NetworkMapping</span></span>
<span data-ttu-id="9faf4-125">Anger den nätverks mappning som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="9faf4-125">Specifies the network mapping to remove.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9faf4-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="9faf4-126">-Profile</span></span>
<span data-ttu-id="9faf4-127">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="9faf4-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9faf4-128">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="9faf4-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9faf4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9faf4-129">CommonParameters</span></span>
<span data-ttu-id="9faf4-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9faf4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9faf4-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9faf4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9faf4-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9faf4-132">INPUTS</span></span>

## <span data-ttu-id="9faf4-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9faf4-133">OUTPUTS</span></span>

## <span data-ttu-id="9faf4-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9faf4-134">NOTES</span></span>

## <span data-ttu-id="9faf4-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9faf4-135">RELATED LINKS</span></span>

[<span data-ttu-id="9faf4-136">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9faf4-136">Get-AzureSiteRecoveryNetworkMapping</span></span>](./Get-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="9faf4-137">New-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9faf4-137">New-AzureSiteRecoveryNetworkMapping</span></span>](./New-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="9faf4-138">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="9faf4-138">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)


