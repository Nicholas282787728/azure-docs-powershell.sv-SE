---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 615D2C5D-AB31-45DB-9535-9B9C8E957322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 96b51b49d76093be96eeab26417f4a70f70c4627
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093318"
---
# <span data-ttu-id="13a2f-101">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="13a2f-101">Get-AzureSiteRecoveryNetwork</span></span>

## <span data-ttu-id="13a2f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13a2f-102">SYNOPSIS</span></span>
<span data-ttu-id="13a2f-103">Hämtar information om nätverken som hanteras av webbplats återställning för det aktuella valvet.</span><span class="sxs-lookup"><span data-stu-id="13a2f-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="13a2f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13a2f-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryNetwork -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="13a2f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13a2f-105">DESCRIPTION</span></span>
<span data-ttu-id="13a2f-106">Cmdleten **Get-AzureSiteRecoveryNetwork** hämtar information om Azure Site Recovery-nätverk för det aktuella Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="13a2f-106">The **Get-AzureSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Site Recovery vault.</span></span>

## <span data-ttu-id="13a2f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13a2f-107">EXAMPLES</span></span>

### <span data-ttu-id="13a2f-108">Exempel 1: skaffa webbplats återställnings nätverk</span><span class="sxs-lookup"><span data-stu-id="13a2f-108">Example 1: Get site recovery networks</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetwork -Server $Servers[0]
Name                : phase2RecoveryVMNetwork
ID                  : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
FabricObjectID      : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}

Name                : phase2PrimaryVMNetwork
ID                  : d903e2c6-3141-4cef-bfe1-04616cd43cbb
FabricObjectID      : d903e2c6-3141-4cef-bfe1-04616cd43cbb
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}
```

<span data-ttu-id="13a2f-109">Den första kommando cmdleten hämtar servrar för det aktuella Azure Site Recovery-valvet med cmdleten **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="13a2f-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="13a2f-110">Kommandot lagrar webbplats återställnings servrarna i $Servers mat ris variabel.</span><span class="sxs-lookup"><span data-stu-id="13a2f-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="13a2f-111">Det andra kommandot får webbplatsen för webbplats återställning för den första servern i $Servers matris.</span><span class="sxs-lookup"><span data-stu-id="13a2f-111">The second command gets the site recovery network for the first server in the $Servers array.</span></span>

## <span data-ttu-id="13a2f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13a2f-112">PARAMETERS</span></span>

### <span data-ttu-id="13a2f-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="13a2f-113">-Profile</span></span>
<span data-ttu-id="13a2f-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="13a2f-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="13a2f-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="13a2f-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="13a2f-116">-Server</span><span class="sxs-lookup"><span data-stu-id="13a2f-116">-Server</span></span>
<span data-ttu-id="13a2f-117">Anger en återställnings Server för webbplatser.</span><span class="sxs-lookup"><span data-stu-id="13a2f-117">Specifies a Site Recovery server.</span></span>

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

### <span data-ttu-id="13a2f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13a2f-118">CommonParameters</span></span>
<span data-ttu-id="13a2f-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13a2f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13a2f-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13a2f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13a2f-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13a2f-121">INPUTS</span></span>

## <span data-ttu-id="13a2f-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13a2f-122">OUTPUTS</span></span>

## <span data-ttu-id="13a2f-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13a2f-123">NOTES</span></span>

## <span data-ttu-id="13a2f-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13a2f-124">RELATED LINKS</span></span>

[<span data-ttu-id="13a2f-125">Azure Site Recovery Services-cmdletar</span><span class="sxs-lookup"><span data-stu-id="13a2f-125">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


