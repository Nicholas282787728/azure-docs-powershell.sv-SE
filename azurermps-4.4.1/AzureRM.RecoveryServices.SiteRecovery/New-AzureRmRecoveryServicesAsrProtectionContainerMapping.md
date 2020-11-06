---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: aa2cd93d21ba22405fff0f3c5fcf336d00f2f6b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575901"
---
# <span data-ttu-id="83b6e-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="83b6e-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="83b6e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="83b6e-102">SYNOPSIS</span></span>
<span data-ttu-id="83b6e-103">Skapar en mappning av en behållare för Azure Site Recovery-skydd genom att associera den angivna replikeringsprincipen till den angivna tjänsten för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="83b6e-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83b6e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="83b6e-104">SYNTAX</span></span>

### <span data-ttu-id="83b6e-105">EnterpriseToAzure (standard)</span><span class="sxs-lookup"><span data-stu-id="83b6e-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83b6e-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="83b6e-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83b6e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="83b6e-107">DESCRIPTION</span></span>
<span data-ttu-id="83b6e-108">Cmdleten **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** skapar en mappning för Azure Site Recovery-skydd genom att associera den angivna replikeringsprincipen till den angivna skydds behållaren.</span><span class="sxs-lookup"><span data-stu-id="83b6e-108">The **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="83b6e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="83b6e-109">EXAMPLES</span></span>

### <span data-ttu-id="83b6e-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="83b6e-110">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer
```

<span data-ttu-id="83b6e-111">Startar skapandet av mappning av skydds behållare med angivna parametrar och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="83b6e-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="83b6e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="83b6e-112">PARAMETERS</span></span>

### <span data-ttu-id="83b6e-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="83b6e-113">-Name</span></span>
<span data-ttu-id="83b6e-114">Anger namnet på skydds behållar mappningen.</span><span class="sxs-lookup"><span data-stu-id="83b6e-114">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="83b6e-115">-Princip</span><span class="sxs-lookup"><span data-stu-id="83b6e-115">-Policy</span></span>
<span data-ttu-id="83b6e-116">Anger ASR-principobjektet för den replikeringsprincip som ska användas i mappningen.</span><span class="sxs-lookup"><span data-stu-id="83b6e-116">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83b6e-117">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="83b6e-117">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="83b6e-118">Anger att objektet ASR Protection container för den primära skydds behållaren ska användas i mappningen.</span><span class="sxs-lookup"><span data-stu-id="83b6e-118">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b6e-119">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="83b6e-119">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="83b6e-120">Anger att objektet ASR Protection container för den återställnings skydds behållare som ska användas i mappningen (används om du replikerar till en återställnings plats som inte är Azure.)</span><span class="sxs-lookup"><span data-stu-id="83b6e-120">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b6e-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="83b6e-121">-Confirm</span></span>
<span data-ttu-id="83b6e-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="83b6e-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b6e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83b6e-123">-WhatIf</span></span>
<span data-ttu-id="83b6e-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="83b6e-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83b6e-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="83b6e-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b6e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83b6e-126">CommonParameters</span></span>
<span data-ttu-id="83b6e-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83b6e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83b6e-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83b6e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83b6e-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="83b6e-129">INPUTS</span></span>

### <span data-ttu-id="83b6e-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="83b6e-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="83b6e-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="83b6e-131">OUTPUTS</span></span>

### <span data-ttu-id="83b6e-132">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="83b6e-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="83b6e-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="83b6e-133">NOTES</span></span>

## <span data-ttu-id="83b6e-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="83b6e-134">RELATED LINKS</span></span>

[<span data-ttu-id="83b6e-135">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="83b6e-135">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="83b6e-136">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="83b6e-136">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
