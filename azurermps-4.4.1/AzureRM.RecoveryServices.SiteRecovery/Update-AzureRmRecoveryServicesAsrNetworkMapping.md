---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: dd17eef73ab07d662a10177ffb68776aa4ec6016
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582248"
---
# <span data-ttu-id="7b950-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7b950-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="7b950-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7b950-102">SYNOPSIS</span></span>
<span data-ttu-id="7b950-103">Uppdaterar den angivna nätverks mappningen för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="7b950-103">Updates the specified ASR network mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b950-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7b950-104">SYNTAX</span></span>

### <span data-ttu-id="7b950-105">ByNetworkObject (standard)</span><span class="sxs-lookup"><span data-stu-id="7b950-105">ByNetworkObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b950-106">ById</span><span class="sxs-lookup"><span data-stu-id="7b950-106">ById</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 -RecoveryAzureNetworkId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b950-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7b950-107">DESCRIPTION</span></span>
<span data-ttu-id="7b950-108">Cmdleten **Update-AzureRmRecoveryServicesAsrNetworkMapping** uppdaterar den angivna nätverks mappningen för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7b950-108">The **Update-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="7b950-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7b950-109">EXAMPLES</span></span>

### <span data-ttu-id="7b950-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7b950-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="7b950-111">Startar uppdateringen av nätverks mappningen med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="7b950-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7b950-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7b950-112">PARAMETERS</span></span>

### <span data-ttu-id="7b950-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b950-113">-InputObject</span></span>
<span data-ttu-id="7b950-114">Input-objekt: anger det nätverks mappnings objekt för ASR som motsvarar nätverks mappningen för automatisk system återställning</span><span class="sxs-lookup"><span data-stu-id="7b950-114">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated</span></span> 

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b950-115">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="7b950-115">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="7b950-116">Anger återställnings-nätverks-ID för nätverks mappningen.</span><span class="sxs-lookup"><span data-stu-id="7b950-116">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="7b950-117">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="7b950-117">-RecoveryNetwork</span></span>
<span data-ttu-id="7b950-118">Anger återställnings nätverks objekt för nätverks mappningen.</span><span class="sxs-lookup"><span data-stu-id="7b950-118">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByNetworkObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b950-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7b950-119">-Confirm</span></span>
<span data-ttu-id="7b950-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7b950-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b950-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b950-121">-WhatIf</span></span>
<span data-ttu-id="7b950-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7b950-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b950-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7b950-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b950-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b950-124">CommonParameters</span></span>
<span data-ttu-id="7b950-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b950-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b950-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b950-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b950-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7b950-127">INPUTS</span></span>

### <span data-ttu-id="7b950-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="7b950-128">None</span></span>

## <span data-ttu-id="7b950-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7b950-129">OUTPUTS</span></span>

### <span data-ttu-id="7b950-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7b950-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7b950-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7b950-131">NOTES</span></span>

## <span data-ttu-id="7b950-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7b950-132">RELATED LINKS</span></span>

