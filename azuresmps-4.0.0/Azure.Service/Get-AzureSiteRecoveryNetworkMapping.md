---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: F6C01C25-655C-4798-9826-F7CB168181C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc8b7dc7e23a98111e75c2b2c9c079f010e3c5dc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093316"
---
# <span data-ttu-id="7f657-101">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7f657-101">Get-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="7f657-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7f657-102">SYNOPSIS</span></span>
<span data-ttu-id="7f657-103">Hämtar nätverks mappningar för ett återställnings valv för webbplatser.</span><span class="sxs-lookup"><span data-stu-id="7f657-103">Gets network mappings for a Site Recovery vault.</span></span>

## <span data-ttu-id="7f657-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7f657-104">SYNTAX</span></span>

### <span data-ttu-id="7f657-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="7f657-105">EnterpriseToEnterprise</span></span>
```
Get-AzureSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7f657-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="7f657-106">EnterpriseToAzure</span></span>
```
Get-AzureSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> [-Azure] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f657-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7f657-107">DESCRIPTION</span></span>
<span data-ttu-id="7f657-108">Cmdleten **Get-AzureSiteRecoveryNetworkMapping** hämtar information om nätverks mappningar för Azure Site Recovery för det aktuella Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="7f657-108">The **Get-AzureSiteRecoveryNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the current Site Recovery vault.</span></span>

## <span data-ttu-id="7f657-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7f657-109">EXAMPLES</span></span>

### <span data-ttu-id="7f657-110">Exempel 1: Hämta mappningen mellan ett nätverk och ett återställnings nätverk</span><span class="sxs-lookup"><span data-stu-id="7f657-110">Example 1: Get the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryNetworkId    : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
PrimaryNetworkName  : phase2RecoveryVMNetwork
RecoveryServerId    : 774859b0-1966-48cc-9df7-759c441b7a8c
RecoveryNetworkId   : d903e2c6-3141-4cef-bfe1-04616cd43cbb
RecoveryNetworkName : phase2PrimaryVMNetwork
PairingStatus       : OK
```

<span data-ttu-id="7f657-111">Den första kommando cmdleten hämtar servrar för det aktuella Azure Site Recovery-valvet med cmdleten **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="7f657-111">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="7f657-112">Kommandot lagrar webbplats återställnings servrarna i $Servers mat ris variabel.</span><span class="sxs-lookup"><span data-stu-id="7f657-112">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="7f657-113">Det andra kommandot får mappningen mellan det primära nätverket och återställnings nätverket.</span><span class="sxs-lookup"><span data-stu-id="7f657-113">The second command gets the mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="7f657-114">Kommandot anger den primära servern för nätverks mappningen som det första elementet i $Servers.</span><span class="sxs-lookup"><span data-stu-id="7f657-114">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="7f657-115">Kommandot anger Server för återställnings nätverket som det andra $Servers.</span><span class="sxs-lookup"><span data-stu-id="7f657-115">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

### <span data-ttu-id="7f657-116">Exempel 2: Hämta mappningen mellan ett nätverk och ett nätverk med Azure Virtual Machine</span><span class="sxs-lookup"><span data-stu-id="7f657-116">Example 2: Get the mapping between a network and an Azure virtual machine network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetworkMapping -Azure -PrimaryServer $Servers[0] 
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryNetworkId    : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
PrimaryNetworkName  : phase2RecoveryVMNetwork
RecoveryServerId    : 21a9403c-6ec1-44f2-b744-b4e50b792387
RecoveryNetworkId   : ecb3a462-664f-4f57-873e-d09b5925e1a1
RecoveryNetworkName : AzureVMNetwork
PairingStatus       : OK
```

<span data-ttu-id="7f657-117">Den första kommando cmdleten hämtar servrar för det aktuella Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="7f657-117">The first command cmdlet gets servers for the current Site Recovery vault.</span></span>
<span data-ttu-id="7f657-118">Kommandot lagrar servrarna i $Servers mat ris variabel.</span><span class="sxs-lookup"><span data-stu-id="7f657-118">The command stores the servers in the $Servers array variable.</span></span>

<span data-ttu-id="7f657-119">Det andra kommandot får en mappning mellan det primära nätverket och ett virtuellt Azure-nätverk.</span><span class="sxs-lookup"><span data-stu-id="7f657-119">The second command gets a mapping between the primary network and an Azure virtual machine network.</span></span>
<span data-ttu-id="7f657-120">Kommandot anger det primära servern för nätverket som det första elementet i $Servers.</span><span class="sxs-lookup"><span data-stu-id="7f657-120">The command specifies the primary server for the network as the first element of $Servers.</span></span>
<span data-ttu-id="7f657-121">Kommandot anger *Azure* -parametern.</span><span class="sxs-lookup"><span data-stu-id="7f657-121">The command specifies the *Azure* parameter.</span></span>
<span data-ttu-id="7f657-122">Därför hämtas kommandot till en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="7f657-122">Therefore, the command gets the mapping to an Azure virtual machine network.</span></span>

## <span data-ttu-id="7f657-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7f657-123">PARAMETERS</span></span>

### <span data-ttu-id="7f657-124">-Azure</span><span class="sxs-lookup"><span data-stu-id="7f657-124">-Azure</span></span>
<span data-ttu-id="7f657-125">Anger att denna cmdlet hämtar nätverks mappningar för nätverk på den primära servern som mappats till virtuella Azure-nätverk.</span><span class="sxs-lookup"><span data-stu-id="7f657-125">Indicates that this cmdlet gets network mappings for networks on the primary server mapped to Azure virtual networks.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f657-126">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="7f657-126">-PrimaryServer</span></span>
<span data-ttu-id="7f657-127">Anger en primär server för att hämta mappningar.</span><span class="sxs-lookup"><span data-stu-id="7f657-127">Specifies a primary server for which to get mappings.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f657-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="7f657-128">-Profile</span></span>
<span data-ttu-id="7f657-129">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="7f657-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7f657-130">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="7f657-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7f657-131">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="7f657-131">-RecoveryServer</span></span>
<span data-ttu-id="7f657-132">Anger en återställnings Server för att hämta mappningar.</span><span class="sxs-lookup"><span data-stu-id="7f657-132">Specifies a recovery server for which to get mappings.</span></span>

```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f657-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f657-133">CommonParameters</span></span>
<span data-ttu-id="7f657-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f657-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f657-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f657-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f657-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7f657-136">INPUTS</span></span>

## <span data-ttu-id="7f657-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7f657-137">OUTPUTS</span></span>

## <span data-ttu-id="7f657-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7f657-138">NOTES</span></span>

## <span data-ttu-id="7f657-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7f657-139">RELATED LINKS</span></span>

[<span data-ttu-id="7f657-140">New-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7f657-140">New-AzureSiteRecoveryNetworkMapping</span></span>](./New-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="7f657-141">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7f657-141">Remove-AzureSiteRecoveryNetworkMapping</span></span>](./Remove-AzureSiteRecoveryNetworkMapping.md)


