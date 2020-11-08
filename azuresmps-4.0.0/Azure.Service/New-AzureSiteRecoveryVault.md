---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: FD43AFDA-E37D-4B5E-8EB5-CC2CF1E36AFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea09f45de760de7ff02a768094c6f98c3f2a0643
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099204"
---
# <span data-ttu-id="514a4-101">New-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="514a4-101">New-AzureSiteRecoveryVault</span></span>

## <span data-ttu-id="514a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="514a4-102">SYNOPSIS</span></span>
<span data-ttu-id="514a4-103">Skapar ett valv för webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="514a4-103">Creates a Site Recovery services vault.</span></span>

## <span data-ttu-id="514a4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="514a4-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryVault -Name <String> -Location <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="514a4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="514a4-105">DESCRIPTION</span></span>
<span data-ttu-id="514a4-106">Cmdleten **New-AzureSiteRecoveryVault** skapar ett valv för Azure Site Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="514a4-106">The **New-AzureSiteRecoveryVault** cmdlet creates an Azure Site Recovery services vault.</span></span>

## <span data-ttu-id="514a4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="514a4-107">EXAMPLES</span></span>

### <span data-ttu-id="514a4-108">Exempel 1: skapa ett valv</span><span class="sxs-lookup"><span data-stu-id="514a4-108">Example 1: Create a vault</span></span>
```
PS C:\> New-AzureSiteRecoveryVault -Location "West US" -Name "ContosoVault" 
Response
--------
Vault has been created
```

<span data-ttu-id="514a4-109">Det här kommandot skapar ett valv med namnet ContosoVault i den plats där du står för USA.</span><span class="sxs-lookup"><span data-stu-id="514a4-109">This command creates a vault named ContosoVault in the West US location.</span></span>

## <span data-ttu-id="514a4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="514a4-110">PARAMETERS</span></span>

### <span data-ttu-id="514a4-111">-Plats</span><span class="sxs-lookup"><span data-stu-id="514a4-111">-Location</span></span>
<span data-ttu-id="514a4-112">Anger den geografiska platsen.</span><span class="sxs-lookup"><span data-stu-id="514a4-112">Specifies the geographical location.</span></span>

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

### <span data-ttu-id="514a4-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="514a4-113">-Name</span></span>
<span data-ttu-id="514a4-114">Anger namnet på valvet.</span><span class="sxs-lookup"><span data-stu-id="514a4-114">Specifies the name of the vault.</span></span>

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

### <span data-ttu-id="514a4-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="514a4-115">-Profile</span></span>
<span data-ttu-id="514a4-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="514a4-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="514a4-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="514a4-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="514a4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="514a4-118">CommonParameters</span></span>
<span data-ttu-id="514a4-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="514a4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="514a4-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="514a4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="514a4-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="514a4-121">INPUTS</span></span>

## <span data-ttu-id="514a4-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="514a4-122">OUTPUTS</span></span>

## <span data-ttu-id="514a4-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="514a4-123">NOTES</span></span>

## <span data-ttu-id="514a4-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="514a4-124">RELATED LINKS</span></span>

[<span data-ttu-id="514a4-125">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="514a4-125">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)


