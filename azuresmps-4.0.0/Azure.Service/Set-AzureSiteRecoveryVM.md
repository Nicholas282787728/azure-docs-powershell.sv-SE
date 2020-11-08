---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 30D56D40-2EA0-48D1-846A-AFB4A987E08F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9dac9858a251e0390fd2a11a2c01dddede1613b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093480"
---
# <span data-ttu-id="35b84-101">Set-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="35b84-101">Set-AzureSiteRecoveryVM</span></span>

## <span data-ttu-id="35b84-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="35b84-102">SYNOPSIS</span></span>
<span data-ttu-id="35b84-103">Anger återställnings sidans alternativ för en entitet för webbplats återställnings skydd.</span><span class="sxs-lookup"><span data-stu-id="35b84-103">Sets the recovery-side options for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="35b84-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="35b84-104">SYNTAX</span></span>

```
Set-AzureSiteRecoveryVM -VirtualMachine <ASRVirtualMachine> [-Name <String>] [-Size <String>]
 [-PrimaryNic <String>] [-RecoveryNetworkId <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="35b84-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="35b84-105">DESCRIPTION</span></span>
<span data-ttu-id="35b84-106">Cmdleten **set-AzureSiteRecoveryVM** anger återställnings skydds alternativen, till exempel storlek på virtuell dator och Återställ virtuellt dator nätverk, för entiteter för Azure Site Recovery-skydd.</span><span class="sxs-lookup"><span data-stu-id="35b84-106">The **Set-AzureSiteRecoveryVM** cmdlet sets the recovery-side protection options, such as the recovery virtual machine size and recovery virtual machine network, for Azure Site Recovery protection entities.</span></span>

## <span data-ttu-id="35b84-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="35b84-107">EXAMPLES</span></span>

### <span data-ttu-id="35b84-108">Exempel 1: Tillåt uppdateringen på en skyddad virtuell dator</span><span class="sxs-lookup"><span data-stu-id="35b84-108">Example 1: Allow the update on a protected virtual machine</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $VirtualMachines = Get-AzureSiteRecoveryVM -ProtectionContainer $ProtectionContainer 
PS C:\> Set-AzureSiteRecoveryVM -VirtualMachine $VirtualMachines[0] -Name "NewVirtualMachine05"
Name             : 
ID               : 8170d274-1e48-404a-b080-172ada140bc3
ClientRequestId  : 09354052-8430-4fa8-9a35-63196dd4b2b4-2015-02-03 04:19:06Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="35b84-109">Det första kommandot använder cmdleten **Get-AzureSiteRecoveryProtectionContainer** för att hämta en skyddad container och lagrar den sedan i $ProtectionContainer variabel.</span><span class="sxs-lookup"><span data-stu-id="35b84-109">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="35b84-110">Det andra kommandot får de virtuella datorerna i $ProtectionContainer genom att använda cmdleten **Get-AzureSiteRecoveryVM** och sedan lagra dem i $VitrualMachines variabel.</span><span class="sxs-lookup"><span data-stu-id="35b84-110">The second command gets the virtual machines in $ProtectionContainer, by using the **Get-AzureSiteRecoveryVM** cmdlet, and then stores them in the $VitrualMachines variable.</span></span>

<span data-ttu-id="35b84-111">Med kommandot slutgiltig kan du uppdatera den första virtuella datorn i $VitrualMachines-matrisen med namnet NewVirtualMachine05.</span><span class="sxs-lookup"><span data-stu-id="35b84-111">The final command allows updates for the first virtual machine in the $VitrualMachines array, named NewVirtualMachine05.</span></span>

## <span data-ttu-id="35b84-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="35b84-112">PARAMETERS</span></span>

### <span data-ttu-id="35b84-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="35b84-113">-Name</span></span>
<span data-ttu-id="35b84-114">Anger namnet på den virtuella mål datorn.</span><span class="sxs-lookup"><span data-stu-id="35b84-114">Specifies the name of the target virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b84-115">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="35b84-115">-PrimaryNic</span></span>
<span data-ttu-id="35b84-116">Anger det primära nätverkskortet.</span><span class="sxs-lookup"><span data-stu-id="35b84-116">Specifies the primary network adapter card.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b84-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="35b84-117">-Profile</span></span>
<span data-ttu-id="35b84-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="35b84-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="35b84-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="35b84-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="35b84-120">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="35b84-120">-RecoveryNetworkId</span></span>
<span data-ttu-id="35b84-121">Anger återställnings nätverkets ID.</span><span class="sxs-lookup"><span data-stu-id="35b84-121">Specifies the recovery network ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b84-122">-Storlek</span><span class="sxs-lookup"><span data-stu-id="35b84-122">-Size</span></span>
<span data-ttu-id="35b84-123">Anger storleken på den virtuella datorns mål.</span><span class="sxs-lookup"><span data-stu-id="35b84-123">Specifies the target virtual machine size.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b84-124">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="35b84-124">-VirtualMachine</span></span>
<span data-ttu-id="35b84-125">Anger det virtuella datorobjektet för webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="35b84-125">Specifies the Site Recovery virtual machine object.</span></span>

```yaml
Type: ASRVirtualMachine
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b84-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35b84-126">CommonParameters</span></span>
<span data-ttu-id="35b84-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35b84-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35b84-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35b84-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35b84-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="35b84-129">INPUTS</span></span>

## <span data-ttu-id="35b84-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="35b84-130">OUTPUTS</span></span>

## <span data-ttu-id="35b84-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="35b84-131">NOTES</span></span>

## <span data-ttu-id="35b84-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="35b84-132">RELATED LINKS</span></span>

[<span data-ttu-id="35b84-133">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="35b84-133">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="35b84-134">Get-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="35b84-134">Get-AzureSiteRecoveryVM</span></span>](./Get-AzureSiteRecoveryVM.md)


