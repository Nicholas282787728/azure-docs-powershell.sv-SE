---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 17836b900e56fdfd5d90211c9bceb79fce87c66e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758019"
---
# <span data-ttu-id="57212-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="57212-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="57212-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="57212-102">SYNOPSIS</span></span>
<span data-ttu-id="57212-103">Stoppar/inaktiverar replikering för ett skyddat objekt i Azure Site Recovery-replikering.</span><span class="sxs-lookup"><span data-stu-id="57212-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57212-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="57212-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57212-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="57212-105">DESCRIPTION</span></span>
<span data-ttu-id="57212-106">Cmdleten **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** inaktiverar replikeringen av angivet skyddat objekt för Azure Site Recovery-objektet.</span><span class="sxs-lookup"><span data-stu-id="57212-106">The **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="57212-107">Den här åtgärden gör att replikering stoppas för det skyddade objektet.</span><span class="sxs-lookup"><span data-stu-id="57212-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="57212-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="57212-108">EXAMPLES</span></span>

### <span data-ttu-id="57212-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="57212-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="57212-110">Startar åtgärden inaktivera replikering för det angivna replikerade skyddade objektet och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="57212-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="57212-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="57212-111">PARAMETERS</span></span>

### <span data-ttu-id="57212-112">-Force</span><span class="sxs-lookup"><span data-stu-id="57212-112">-Force</span></span>
<span data-ttu-id="57212-113">Tvinga kommandot att köras utan ytterligare en varning.</span><span class="sxs-lookup"><span data-stu-id="57212-113">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57212-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57212-114">-InputObject</span></span>
<span data-ttu-id="57212-115">Indatavärdet till cmdleten: objektet Protected ASR-objekt som är kopplat till det replikerade objektet för replikering ska inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="57212-115">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57212-116">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="57212-116">-WaitForCompletion</span></span>
<span data-ttu-id="57212-117">Anger att cmdleten ska vänta på att åtgärden ska slutföras innan den returneras.</span><span class="sxs-lookup"><span data-stu-id="57212-117">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57212-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="57212-118">-Confirm</span></span>
<span data-ttu-id="57212-119">Ange om du vill bekräfta.</span><span class="sxs-lookup"><span data-stu-id="57212-119">Specify if confirmation is required.</span></span> <span data-ttu-id="57212-120">Ange värdet för parametern Confirm till $false för att hoppa över bekräftelsen.</span><span class="sxs-lookup"><span data-stu-id="57212-120">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="57212-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57212-121">-WhatIf</span></span>
<span data-ttu-id="57212-122">Visar vad som händer om cmdleten körs utan att köra cmdleten.</span><span class="sxs-lookup"><span data-stu-id="57212-122">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="57212-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57212-123">CommonParameters</span></span>
<span data-ttu-id="57212-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57212-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57212-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57212-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57212-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="57212-126">INPUTS</span></span>

### <span data-ttu-id="57212-127">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="57212-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="57212-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="57212-128">OUTPUTS</span></span>

### <span data-ttu-id="57212-129">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="57212-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="57212-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="57212-130">NOTES</span></span>

## <span data-ttu-id="57212-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="57212-131">RELATED LINKS</span></span>

[<span data-ttu-id="57212-132">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="57212-132">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="57212-133">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="57212-133">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="57212-134">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="57212-134">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
