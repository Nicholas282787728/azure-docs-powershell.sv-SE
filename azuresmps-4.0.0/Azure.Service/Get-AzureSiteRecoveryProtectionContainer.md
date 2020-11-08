---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 02396628-5E3E-49A6-8377-3F6DC488FEF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75a083c2f892b7b4f07c37ef978d1babb1dd0cb0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093319"
---
# <span data-ttu-id="d9480-101">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d9480-101">Get-AzureSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="d9480-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9480-102">SYNOPSIS</span></span>
<span data-ttu-id="d9480-103">Hämtar skydds behållare för ett återställnings valv för webbplatser.</span><span class="sxs-lookup"><span data-stu-id="d9480-103">Gets protection containers for a Site Recovery vault.</span></span>

## <span data-ttu-id="d9480-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9480-104">SYNTAX</span></span>

### <span data-ttu-id="d9480-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="d9480-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryProtectionContainer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d9480-106">ById</span><span class="sxs-lookup"><span data-stu-id="d9480-106">ById</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d9480-107">ByName</span><span class="sxs-lookup"><span data-stu-id="d9480-107">ByName</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d9480-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9480-108">DESCRIPTION</span></span>
<span data-ttu-id="d9480-109">Cmdleten **Get-AzureSiteRecoveryProtectionContainer** får skydds behållare för det aktuella Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="d9480-109">The **Get-AzureSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="d9480-110">En skydds behållare är en logisk behållare för skyddade objekt, till exempel virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="d9480-110">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="d9480-111">Skydds principer definierar replikeringsinställningar för skyddade objekt och kan associeras med en skydds behållare och tillämpas på en skyddad entitet.</span><span class="sxs-lookup"><span data-stu-id="d9480-111">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="d9480-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9480-112">EXAMPLES</span></span>

### <span data-ttu-id="d9480-113">Exempel 1: skaffa skyddade behållare</span><span class="sxs-lookup"><span data-stu-id="d9480-113">Example 1: Get protected containers</span></span>
```
PS C:\> Get-AzureSiteRecoveryProtectionContainer
Name                        : PrimaryCloud
ID                          : fd00d920-79e4-4f2d-a282-a779c0cecb7f_ce995917-c962-45d0-b7f3-9f408a4e1429
FabricObjectId              : fd00d920-79e4-4f2d-a282-a779c0cecb7f
FabricType                  : VMM
Type                        : VMM
ServerId                    : fd00d920-79e4-4f2d-a282-a779c0cecb7f
Role                        : Primary
AvailableProtectionProfiles : {ab01dcbe-9da0-4c31-9564-d6904cfadfde, ad388147-83de-4d2f-a09d-fa46c626747e}
```

<span data-ttu-id="d9480-114">Det här kommandot hämtar de skyddade behållarna för det aktuella valvet.</span><span class="sxs-lookup"><span data-stu-id="d9480-114">This command gets the protected containers for the current vault.</span></span>

## <span data-ttu-id="d9480-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9480-115">PARAMETERS</span></span>

### <span data-ttu-id="d9480-116">-ID</span><span class="sxs-lookup"><span data-stu-id="d9480-116">-Id</span></span>
<span data-ttu-id="d9480-117">Anger ID för en skyddad behållare som ska visas.</span><span class="sxs-lookup"><span data-stu-id="d9480-117">Specifies the ID of a protected container to get.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9480-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="d9480-118">-Name</span></span>
<span data-ttu-id="d9480-119">Anger namnet på en skydds behållare att hämta.</span><span class="sxs-lookup"><span data-stu-id="d9480-119">Specifies the name of a protection container to get.</span></span>

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

### <span data-ttu-id="d9480-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="d9480-120">-Profile</span></span>
<span data-ttu-id="d9480-121">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="d9480-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d9480-122">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="d9480-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d9480-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9480-123">CommonParameters</span></span>
<span data-ttu-id="d9480-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9480-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9480-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9480-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9480-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9480-126">INPUTS</span></span>

## <span data-ttu-id="d9480-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9480-127">OUTPUTS</span></span>

## <span data-ttu-id="d9480-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9480-128">NOTES</span></span>

## <span data-ttu-id="d9480-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9480-129">RELATED LINKS</span></span>

[<span data-ttu-id="d9480-130">Azure Site Recovery Services-cmdletar</span><span class="sxs-lookup"><span data-stu-id="d9480-130">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


