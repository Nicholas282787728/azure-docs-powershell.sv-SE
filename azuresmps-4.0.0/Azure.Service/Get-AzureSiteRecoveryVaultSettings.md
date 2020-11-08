---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 305511DC-477F-4A33-8B16-063B39B19ED3
online version: ''
schema: 2.0.0
ms.openlocfilehash: cd96d7dd63791c5ef2e4a8a036949823d5c73313
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099796"
---
# <span data-ttu-id="2d15f-101">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="2d15f-101">Get-AzureSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="2d15f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2d15f-102">SYNOPSIS</span></span>
<span data-ttu-id="2d15f-103">Hämtar inställningar för ett återställnings valv för webbplatser.</span><span class="sxs-lookup"><span data-stu-id="2d15f-103">Gets settings for a Site Recovery vault.</span></span>

## <span data-ttu-id="2d15f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2d15f-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryVaultSettings [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2d15f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2d15f-105">DESCRIPTION</span></span>
<span data-ttu-id="2d15f-106">Cmdleten **Get-AzureSiteRecoveryVaultSettings** hämtar inställningar relaterade till det aktuella Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="2d15f-106">The **Get-AzureSiteRecoveryVaultSettings** cmdlet gets settings related to the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="2d15f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2d15f-107">EXAMPLES</span></span>

### <span data-ttu-id="2d15f-108">Exempel 1: Hämta information om inställningar</span><span class="sxs-lookup"><span data-stu-id="2d15f-108">Example 1: Get settings information</span></span>
```
PS C:\> Get-AzureSiteRecoveryVaultSettings
ResourceName                                                CloudServiceName
------------                                                ----------------
ContosoVault                                                RecoveryServices-6JP23WE3SKKOM5AFQG2YQAI22MNOWK52QDKWMUP...
```

<span data-ttu-id="2d15f-109">Det här kommandot hämtar inställningar för det aktuella Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="2d15f-109">This command gets settings information for the current  Azure Site Recovery vault.</span></span>

## <span data-ttu-id="2d15f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2d15f-110">PARAMETERS</span></span>

### <span data-ttu-id="2d15f-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="2d15f-111">-Profile</span></span>
<span data-ttu-id="2d15f-112">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="2d15f-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2d15f-113">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="2d15f-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2d15f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d15f-114">CommonParameters</span></span>
<span data-ttu-id="2d15f-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d15f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d15f-116">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d15f-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d15f-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2d15f-117">INPUTS</span></span>

## <span data-ttu-id="2d15f-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2d15f-118">OUTPUTS</span></span>

## <span data-ttu-id="2d15f-119">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2d15f-119">NOTES</span></span>

## <span data-ttu-id="2d15f-120">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2d15f-120">RELATED LINKS</span></span>

[<span data-ttu-id="2d15f-121">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="2d15f-121">Get-AzureSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureSiteRecoveryVaultSettingsFile.md)

[<span data-ttu-id="2d15f-122">Import-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="2d15f-122">Import-AzureSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureSiteRecoveryVaultSettingsFile.md)


