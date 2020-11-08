---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 78DE0AD2-6210-4604-89A8-41915D58BD68
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3c40cb0fd38953ff46fa1138dc91f0b9e97ece75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093302"
---
# <span data-ttu-id="9d8d6-101">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="9d8d6-101">Get-AzureSiteRecoveryStorage</span></span>

## <span data-ttu-id="9d8d6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9d8d6-102">SYNOPSIS</span></span>
<span data-ttu-id="9d8d6-103">Hämtar lagrings utrymme för webbplats återställning för ett valv.</span><span class="sxs-lookup"><span data-stu-id="9d8d6-103">Gets Site Recovery Storages for a vault.</span></span>

## <span data-ttu-id="9d8d6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9d8d6-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryStorage -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9d8d6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9d8d6-105">DESCRIPTION</span></span>
<span data-ttu-id="9d8d6-106">Cmdleten **Get-AzureSiteRecoveryStorage** får Azure Site Recovery-lagring för det aktuella Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="9d8d6-106">The **Get-AzureSiteRecoveryStorage** cmdlet gets Azure Site Recovery Storages for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="9d8d6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9d8d6-107">EXAMPLES</span></span>

### <span data-ttu-id="9d8d6-108">Exempel 1: Hämta lagrings utrymme för webbplats</span><span class="sxs-lookup"><span data-stu-id="9d8d6-108">Example 1: Get site recovery storage</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryStorage -Server $Servers[0]
Name           : phase2PrimaryStorageClassification
ID             : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
FabricObjectID : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
ServerId       : 774859b0-1966-48cc-9df7-759c441b7a8c
Type           : Classification
FabricType     : VMM

Name           : phase2RecoveryStorageClassification
ID             : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
FabricObjectID : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
ServerId       : 774859b0-1966-48cc-9df7-759c441b7a8c
Type           : Classification
FabricType     : VMM
```

<span data-ttu-id="9d8d6-109">Den första kommando cmdleten hämtar servrar för det aktuella Azure Site Recovery-valvet med cmdleten **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="9d8d6-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="9d8d6-110">Kommandot lagrar webbplats återställnings servrarna i $Servers mat ris variabel.</span><span class="sxs-lookup"><span data-stu-id="9d8d6-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="9d8d6-111">Det andra kommandot får webbplatsen för webbplats återställning för den första servern i $Servers matrisen.</span><span class="sxs-lookup"><span data-stu-id="9d8d6-111">The second command gets the site recovery storage for the first server in the $Servers array.</span></span>

## <span data-ttu-id="9d8d6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9d8d6-112">PARAMETERS</span></span>

### <span data-ttu-id="9d8d6-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="9d8d6-113">-Profile</span></span>
<span data-ttu-id="9d8d6-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="9d8d6-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9d8d6-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="9d8d6-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9d8d6-116">-Server</span><span class="sxs-lookup"><span data-stu-id="9d8d6-116">-Server</span></span>
<span data-ttu-id="9d8d6-117">Anger en server för Azure Site Recovery-lagring.</span><span class="sxs-lookup"><span data-stu-id="9d8d6-117">Specifies a server for Azure Site Recovery Storage.</span></span>
<span data-ttu-id="9d8d6-118">För att få ett **ASRServer** -objekt, Använd cmdleten **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="9d8d6-118">To obtain an **ASRServer** object, use the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d8d6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d8d6-119">CommonParameters</span></span>
<span data-ttu-id="9d8d6-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d8d6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d8d6-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d8d6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d8d6-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9d8d6-122">INPUTS</span></span>

## <span data-ttu-id="9d8d6-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9d8d6-123">OUTPUTS</span></span>

## <span data-ttu-id="9d8d6-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9d8d6-124">NOTES</span></span>

## <span data-ttu-id="9d8d6-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9d8d6-125">RELATED LINKS</span></span>

[<span data-ttu-id="9d8d6-126">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="9d8d6-126">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)


