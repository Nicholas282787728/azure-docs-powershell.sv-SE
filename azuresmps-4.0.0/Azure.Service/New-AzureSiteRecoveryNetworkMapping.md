---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 6802F2E9-5925-4E92-AEB8-827B5A303617
online version: ''
schema: 2.0.0
ms.openlocfilehash: 153e30c03de7a0a5c404526bd06b9acb2f0678f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099447"
---
# <span data-ttu-id="6667a-101">New-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6667a-101">New-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="6667a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6667a-102">SYNOPSIS</span></span>
<span data-ttu-id="6667a-103">Skapar en mappning mellan virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="6667a-103">Creates a mapping between virtual networks.</span></span>

## <span data-ttu-id="6667a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6667a-104">SYNTAX</span></span>

### <span data-ttu-id="6667a-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="6667a-105">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork <ASRNetwork> -RecoveryNetwork <ASRNetwork>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6667a-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="6667a-106">EnterpriseToAzure</span></span>
```
New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork <ASRNetwork> -AzureSubscriptionId <String>
 -AzureVMNetworkId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6667a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6667a-107">DESCRIPTION</span></span>
<span data-ttu-id="6667a-108">Cmdleten **New-AzureSiteRecoveryNetworkMapping** skapar en mappning mellan två virtuella nätverk och returnerar ett Azure Site Recovery-jobb för att spåra det.</span><span class="sxs-lookup"><span data-stu-id="6667a-108">The **New-AzureSiteRecoveryNetworkMapping** cmdlet creates a mapping between two virtual networks and returns an Azure Site Recovery job to track it.</span></span>

## <span data-ttu-id="6667a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6667a-109">EXAMPLES</span></span>

### <span data-ttu-id="6667a-110">Exempel 1: skapa en mappning mellan ett nätverk och ett återställnings nätverk</span><span class="sxs-lookup"><span data-stu-id="6667a-110">Example 1: Create a mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Networks = Get-AzureSiteRecoveryNetwork -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork $Networks[0] -RecoveryNetwork $Networks[1]
```

<span data-ttu-id="6667a-111">Den första kommando cmdleten hämtar servrar för det aktuella Azure Site Recovery-valvet med cmdleten **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="6667a-111">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="6667a-112">Kommandot lagrar webbplats återställnings servrarna i $Servers mat ris variabel.</span><span class="sxs-lookup"><span data-stu-id="6667a-112">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="6667a-113">Det andra kommandot får webbplatsen för webbplats återställning för den första servern i $Servers-matrisen genom att använda cmdleten **Get-AzureSiteRecoveryNetwork** .</span><span class="sxs-lookup"><span data-stu-id="6667a-113">The second command gets the site recovery network for the first server in the $Servers array by using the **Get-AzureSiteRecoveryNetwork** cmdlet.</span></span>
<span data-ttu-id="6667a-114">Kommandot lagrar nätverken i $Networks variabel.</span><span class="sxs-lookup"><span data-stu-id="6667a-114">The command stores the networks in the $Networks variable.</span></span>

<span data-ttu-id="6667a-115">Med kommandot slut skapas en mappning mellan det primära nätverket och återställnings nätverket.</span><span class="sxs-lookup"><span data-stu-id="6667a-115">The final command creates a mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="6667a-116">Kommandot anger det primära nätverket som det första elementet i $Networks.</span><span class="sxs-lookup"><span data-stu-id="6667a-116">The command specifies the primary network as the first element of $Networks.</span></span>
<span data-ttu-id="6667a-117">Kommandot anger återställnings nätverket som det andra $Networks.</span><span class="sxs-lookup"><span data-stu-id="6667a-117">The command specifies the recovery network as the second element of $Networks.</span></span>

## <span data-ttu-id="6667a-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6667a-118">PARAMETERS</span></span>

### <span data-ttu-id="6667a-119">-AzureSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6667a-119">-AzureSubscriptionId</span></span>
<span data-ttu-id="6667a-120">Anger ID för din Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="6667a-120">Specifies the ID of your Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6667a-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="6667a-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="6667a-122">Anger ID för Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="6667a-122">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6667a-123">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="6667a-123">-PrimaryNetwork</span></span>
<span data-ttu-id="6667a-124">Anger det primära nätverks objekt.</span><span class="sxs-lookup"><span data-stu-id="6667a-124">Specifies the primary network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6667a-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="6667a-125">-Profile</span></span>
<span data-ttu-id="6667a-126">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="6667a-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6667a-127">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="6667a-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6667a-128">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="6667a-128">-RecoveryNetwork</span></span>
<span data-ttu-id="6667a-129">Anger återställnings nätverks objekt.</span><span class="sxs-lookup"><span data-stu-id="6667a-129">Specifies the recovery network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6667a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6667a-130">CommonParameters</span></span>
<span data-ttu-id="6667a-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6667a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6667a-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6667a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6667a-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6667a-133">INPUTS</span></span>

## <span data-ttu-id="6667a-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6667a-134">OUTPUTS</span></span>

## <span data-ttu-id="6667a-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6667a-135">NOTES</span></span>

## <span data-ttu-id="6667a-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6667a-136">RELATED LINKS</span></span>

[<span data-ttu-id="6667a-137">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6667a-137">Get-AzureSiteRecoveryNetworkMapping</span></span>](./Get-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="6667a-138">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="6667a-138">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)

[<span data-ttu-id="6667a-139">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6667a-139">Remove-AzureSiteRecoveryNetworkMapping</span></span>](./Remove-AzureSiteRecoveryNetworkMapping.md)


