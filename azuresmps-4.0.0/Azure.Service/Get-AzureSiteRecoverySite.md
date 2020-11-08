---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 6DD09F28-BFAE-4F9B-BF9C-F09767F9BFEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9151cb5a64b5873ab1c63420a97eb2e7bcffc0ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093303"
---
# <span data-ttu-id="4e6e2-101">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="4e6e2-101">Get-AzureSiteRecoverySite</span></span>

## <span data-ttu-id="4e6e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4e6e2-102">SYNOPSIS</span></span>
<span data-ttu-id="4e6e2-103">Hämtar Hyper-V-webbplatser från ett återställnings valv för webbplatser.</span><span class="sxs-lookup"><span data-stu-id="4e6e2-103">Gets the Hyper-V sites from a Site Recovery vault.</span></span>

## <span data-ttu-id="4e6e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4e6e2-104">SYNTAX</span></span>

```
Get-AzureSiteRecoverySite [-Vault <ASRVault>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4e6e2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4e6e2-105">DESCRIPTION</span></span>
<span data-ttu-id="4e6e2-106">Cmdleten **Get-AzureSiteRecoverySite** hämtar Hyper-V-webbplatserna i ett Azure Site Recovery-valv.</span><span class="sxs-lookup"><span data-stu-id="4e6e2-106">The **Get-AzureSiteRecoverySite** cmdlet gets the Hyper-V sites in an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="4e6e2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4e6e2-107">EXAMPLES</span></span>

### <span data-ttu-id="4e6e2-108">Exempel 1: skaffa återställnings webbplatser</span><span class="sxs-lookup"><span data-stu-id="4e6e2-108">Example 1: Get recovery sites</span></span>
```
PS C:\> Get-AzureSiteRecoverySite
Type                                    Name                                    ID
----                                    ----                                    --
HyperVSite                              RecoverySite07                          f16829b4-5b01-4209-a6cf-8e0aff1fe328
```

<span data-ttu-id="4e6e2-109">Det här kommandot får återställnings webbplatserna för det aktuella valvet.</span><span class="sxs-lookup"><span data-stu-id="4e6e2-109">This command gets the recovery sites for the current vault.</span></span>

## <span data-ttu-id="4e6e2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4e6e2-110">PARAMETERS</span></span>

### <span data-ttu-id="4e6e2-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="4e6e2-111">-Profile</span></span>
<span data-ttu-id="4e6e2-112">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="4e6e2-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4e6e2-113">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="4e6e2-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4e6e2-114">-Valv</span><span class="sxs-lookup"><span data-stu-id="4e6e2-114">-Vault</span></span>
<span data-ttu-id="4e6e2-115">Anger ett valv som du ska hämta webbplatser för.</span><span class="sxs-lookup"><span data-stu-id="4e6e2-115">Specifies a vault for which to get sites.</span></span>
<span data-ttu-id="4e6e2-116">För att få ett **ASRVault** -objekt, Använd cmdleten **Get-AzureSiteRecoveryVault** .</span><span class="sxs-lookup"><span data-stu-id="4e6e2-116">To obtain an **ASRVault** object, use the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>

```yaml
Type: ASRVault
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e6e2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e6e2-117">CommonParameters</span></span>
<span data-ttu-id="4e6e2-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e6e2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e6e2-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e6e2-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e6e2-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4e6e2-120">INPUTS</span></span>

## <span data-ttu-id="4e6e2-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4e6e2-121">OUTPUTS</span></span>

## <span data-ttu-id="4e6e2-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4e6e2-122">NOTES</span></span>

## <span data-ttu-id="4e6e2-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4e6e2-123">RELATED LINKS</span></span>

[<span data-ttu-id="4e6e2-124">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="4e6e2-124">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="4e6e2-125">New-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="4e6e2-125">New-AzureSiteRecoverySite</span></span>](./New-AzureSiteRecoverySite.md)


