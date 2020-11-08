---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 4F083EBC-7D7E-4836-8AAB-6BF2B08162DF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a69d54b315319e3dacc150edc2a8737be9b96e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093301"
---
# <span data-ttu-id="b0949-101">Get-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="b0949-101">Get-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="b0949-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0949-102">SYNOPSIS</span></span>
<span data-ttu-id="b0949-103">Hämtar mappningar av plats objekt för webbplats återställning för ett valv.</span><span class="sxs-lookup"><span data-stu-id="b0949-103">Gets mappings of Site Recovery Storage objects for a vault.</span></span>

## <span data-ttu-id="b0949-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0949-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryStorageMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b0949-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0949-105">DESCRIPTION</span></span>
<span data-ttu-id="b0949-106">Cmdleten **Get-AzureSiteRecoveryStorageMapping** hämtar mappningar av objekt för Azure Site Recovery-objekten för det aktuella Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="b0949-106">The **Get-AzureSiteRecoveryStorageMapping** cmdlet gets mappings of Azure Site Recovery Storage objects for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="b0949-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0949-107">EXAMPLES</span></span>

### <span data-ttu-id="b0949-108">Exempel 1: Hämta mappningen mellan ett lagrings objekt och ett återställnings objekt</span><span class="sxs-lookup"><span data-stu-id="b0949-108">Example 1: Get the mapping between a Storage object and a recovery Storage object</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryStorageMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[1]
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryStorageId    : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
PrimaryStorageName  : phase2PrimaryStorageClassification
RecoveryServerId    : 774859b0-1966-48cc-9df7-759c441b7a8c
RecoveryStorageId   : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
RecoveryStorageName : phase2RecoveryStorageClassification
```

<span data-ttu-id="b0949-109">Den första kommando cmdleten hämtar servrar för det aktuella Azure Site Recovery-valvet med cmdleten **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="b0949-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="b0949-110">Kommandot lagrar webbplats återställnings servrarna i $Servers mat ris variabel.</span><span class="sxs-lookup"><span data-stu-id="b0949-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="b0949-111">Det andra kommandot hämtar mappningen mellan två Azure Storage-objekt.</span><span class="sxs-lookup"><span data-stu-id="b0949-111">The second command gets the mapping between two Azure Storage objects.</span></span>
<span data-ttu-id="b0949-112">Kommandot anger den primära servern för mappning av lagrings objekt som det första elementet i $Servers.</span><span class="sxs-lookup"><span data-stu-id="b0949-112">The command specifies the primary server for the Storage object mapping as the first element of $Servers.</span></span>
<span data-ttu-id="b0949-113">Kommandot anger Server för återställnings objekt som det andra elementet i $Servers.</span><span class="sxs-lookup"><span data-stu-id="b0949-113">The command specifies the server for the recovery Storage object as the second element of $Servers.</span></span>

## <span data-ttu-id="b0949-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0949-114">PARAMETERS</span></span>

### <span data-ttu-id="b0949-115">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="b0949-115">-PrimaryServer</span></span>
<span data-ttu-id="b0949-116">Anger den primära servern.</span><span class="sxs-lookup"><span data-stu-id="b0949-116">Specifies the primary server.</span></span>
<span data-ttu-id="b0949-117">Använd cmdleten **Get-AzureSiteRecoveryServer** för att få en server.</span><span class="sxs-lookup"><span data-stu-id="b0949-117">To obtain a server, use the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>

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

### <span data-ttu-id="b0949-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="b0949-118">-Profile</span></span>
<span data-ttu-id="b0949-119">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="b0949-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b0949-120">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="b0949-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b0949-121">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="b0949-121">-RecoveryServer</span></span>
<span data-ttu-id="b0949-122">Anger återställnings Server.</span><span class="sxs-lookup"><span data-stu-id="b0949-122">Specifies the recovery server.</span></span>
<span data-ttu-id="b0949-123">För att få en server, Använd **Get-AzureSiteRecoveryServer**.</span><span class="sxs-lookup"><span data-stu-id="b0949-123">To obtain a server, use **Get-AzureSiteRecoveryServer**.</span></span>

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

### <span data-ttu-id="b0949-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0949-124">CommonParameters</span></span>
<span data-ttu-id="b0949-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0949-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0949-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0949-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0949-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0949-127">INPUTS</span></span>

## <span data-ttu-id="b0949-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0949-128">OUTPUTS</span></span>

## <span data-ttu-id="b0949-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0949-129">NOTES</span></span>

## <span data-ttu-id="b0949-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0949-130">RELATED LINKS</span></span>

[<span data-ttu-id="b0949-131">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="b0949-131">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)

[<span data-ttu-id="b0949-132">New-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="b0949-132">New-AzureSiteRecoveryStorageMapping</span></span>](./New-AzureSiteRecoveryStorageMapping.md)

[<span data-ttu-id="b0949-133">Remove-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="b0949-133">Remove-AzureSiteRecoveryStorageMapping</span></span>](./Remove-AzureSiteRecoveryStorageMapping.md)


