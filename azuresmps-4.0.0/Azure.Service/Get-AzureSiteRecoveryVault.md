---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2A6DDF5F-2906-4DB5-B791-B6BF590261A0
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffdf63e9e4d1d8e34dc63cb90c1fa0de15369fbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099795"
---
# <span data-ttu-id="c103f-101">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="c103f-101">Get-AzureSiteRecoveryVault</span></span>

## <span data-ttu-id="c103f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c103f-102">SYNOPSIS</span></span>
<span data-ttu-id="c103f-103">Hämtar Site Recovery-valv från det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c103f-103">Gets Site Recovery vaults from the current subscription.</span></span>

## <span data-ttu-id="c103f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c103f-104">SYNTAX</span></span>

### <span data-ttu-id="c103f-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="c103f-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryVault [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c103f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c103f-106">ByName</span></span>
```
Get-AzureSiteRecoveryVault -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c103f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c103f-107">DESCRIPTION</span></span>
<span data-ttu-id="c103f-108">Cmdleten **Get-AzureSiteRecoveryVault** hämtar en lista med Azure Site Recovery-valv eller ett specifikt webbplats återställnings valv från det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c103f-108">The **Get-AzureSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="c103f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c103f-109">EXAMPLES</span></span>

### <span data-ttu-id="c103f-110">Exempel 1: Skaffa det aktiva valvet</span><span class="sxs-lookup"><span data-stu-id="c103f-110">Example 1: Get the active vault</span></span>
```
PS C:\> Get-AzureSiteRecoveryVault
Name             : ContosoVault
ID               : 6467459117394545458
CloudServiceName : CS-West-US-RecoveryServices
SubscriptionId   : a5aa5997-33e5-46cc-8ab8-b8d89b76b7ba
StatusReason     : 
Status           : Active
Location         : West US
```

<span data-ttu-id="c103f-111">Det här kommandot får det aktiva Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="c103f-111">This command gets the active Azure Site Recovery vault.</span></span>

## <span data-ttu-id="c103f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c103f-112">PARAMETERS</span></span>

### <span data-ttu-id="c103f-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="c103f-113">-Name</span></span>
<span data-ttu-id="c103f-114">Anger namnet på valvet som ska visas.</span><span class="sxs-lookup"><span data-stu-id="c103f-114">Specifies the name of the vault to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c103f-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="c103f-115">-Profile</span></span>
<span data-ttu-id="c103f-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="c103f-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c103f-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="c103f-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c103f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c103f-118">CommonParameters</span></span>
<span data-ttu-id="c103f-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c103f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c103f-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c103f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c103f-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c103f-121">INPUTS</span></span>

## <span data-ttu-id="c103f-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c103f-122">OUTPUTS</span></span>

## <span data-ttu-id="c103f-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c103f-123">NOTES</span></span>

## <span data-ttu-id="c103f-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c103f-124">RELATED LINKS</span></span>

[<span data-ttu-id="c103f-125">New-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="c103f-125">New-AzureSiteRecoveryVault</span></span>](./New-AzureSiteRecoveryVault.md)


