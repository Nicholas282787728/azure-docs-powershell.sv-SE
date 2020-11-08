---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 43E5EC54-5DF4-4D32-8657-D7039DD04513
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68152b80711544a76abc17f697fe9730d1a6f1bc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099122"
---
# <span data-ttu-id="dff5a-101">New-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="dff5a-101">New-AzureSiteRecoverySite</span></span>

## <span data-ttu-id="dff5a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dff5a-102">SYNOPSIS</span></span>
<span data-ttu-id="dff5a-103">Skapar en webbplats återställnings webbplats.</span><span class="sxs-lookup"><span data-stu-id="dff5a-103">Creates a Site Recovery site.</span></span>

## <span data-ttu-id="dff5a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dff5a-104">SYNTAX</span></span>

```
New-AzureSiteRecoverySite -Name <String> [-Vault <ASRVault>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dff5a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dff5a-105">DESCRIPTION</span></span>
<span data-ttu-id="dff5a-106">Cmdleten **New-AzureSiteRecoverySite** skapar en Azure Site Recovery-webbplats i det aktuella valvet.</span><span class="sxs-lookup"><span data-stu-id="dff5a-106">The **New-AzureSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="dff5a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dff5a-107">EXAMPLES</span></span>

### <span data-ttu-id="dff5a-108">Exempel 1: skapa en webbplats återställnings webbplats</span><span class="sxs-lookup"><span data-stu-id="dff5a-108">Example 1: Create a Site Recovery site</span></span>
```
PS C:\> New-AzureSiteRecoverySite -Name "RecoverySite07"
```

<span data-ttu-id="dff5a-109">Det här kommandot skapar en webbplats återställnings webbplats med namnet RecoverySite07.</span><span class="sxs-lookup"><span data-stu-id="dff5a-109">This command creates a site recovery site named RecoverySite07.</span></span>

## <span data-ttu-id="dff5a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dff5a-110">PARAMETERS</span></span>

### <span data-ttu-id="dff5a-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="dff5a-111">-Name</span></span>
<span data-ttu-id="dff5a-112">Anger namnet på webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="dff5a-112">Specifies the name of the site.</span></span>

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

### <span data-ttu-id="dff5a-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="dff5a-113">-Profile</span></span>
<span data-ttu-id="dff5a-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="dff5a-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dff5a-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="dff5a-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dff5a-116">-Valv</span><span class="sxs-lookup"><span data-stu-id="dff5a-116">-Vault</span></span>
<span data-ttu-id="dff5a-117">Anger ett valv som webbplatsen ska skapas för.</span><span class="sxs-lookup"><span data-stu-id="dff5a-117">Specifies a vault for which to create the site.</span></span>
<span data-ttu-id="dff5a-118">För att få ett **ASRVault** -objekt, Använd cmdleten **Get-AzureSiteRecoveryVault** .</span><span class="sxs-lookup"><span data-stu-id="dff5a-118">To obtain an **ASRVault** object, use the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>

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

### <span data-ttu-id="dff5a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dff5a-119">CommonParameters</span></span>
<span data-ttu-id="dff5a-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dff5a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dff5a-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dff5a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dff5a-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dff5a-122">INPUTS</span></span>

## <span data-ttu-id="dff5a-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dff5a-123">OUTPUTS</span></span>

## <span data-ttu-id="dff5a-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dff5a-124">NOTES</span></span>

## <span data-ttu-id="dff5a-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dff5a-125">RELATED LINKS</span></span>

[<span data-ttu-id="dff5a-126">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="dff5a-126">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="dff5a-127">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="dff5a-127">Get-AzureSiteRecoverySite</span></span>](./Get-AzureSiteRecoverySite.md)


