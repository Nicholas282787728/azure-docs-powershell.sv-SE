---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 1df32bfcf049346b3f434b252a413eef020d0b77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576471"
---
# <span data-ttu-id="9457f-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9457f-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="9457f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9457f-102">SYNOPSIS</span></span>
<span data-ttu-id="9457f-103">Stoppar/inaktiverar replikering för ett skyddat objekt i Azure Site Recovery-replikering.</span><span class="sxs-lookup"><span data-stu-id="9457f-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9457f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9457f-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9457f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9457f-105">DESCRIPTION</span></span>
<span data-ttu-id="9457f-106">Cmdleten **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** inaktiverar replikeringen av angivet skyddat objekt för Azure Site Recovery-objektet.</span><span class="sxs-lookup"><span data-stu-id="9457f-106">The **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="9457f-107">Den här åtgärden gör att replikering stoppas för det skyddade objektet.</span><span class="sxs-lookup"><span data-stu-id="9457f-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="9457f-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9457f-108">EXAMPLES</span></span>

### <span data-ttu-id="9457f-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9457f-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="9457f-110">Startar åtgärden inaktivera replikering för det angivna replikerade skyddade objektet och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="9457f-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="9457f-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9457f-111">PARAMETERS</span></span>

### <span data-ttu-id="9457f-112">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9457f-112">-Confirm</span></span>
<span data-ttu-id="9457f-113">Ange om du vill bekräfta.</span><span class="sxs-lookup"><span data-stu-id="9457f-113">Specify if confirmation is required.</span></span> <span data-ttu-id="9457f-114">Ange värdet för parametern Confirm till $false för att hoppa över bekräftelsen.</span><span class="sxs-lookup"><span data-stu-id="9457f-114">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="9457f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9457f-115">-DefaultProfile</span></span>
<span data-ttu-id="9457f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9457f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9457f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9457f-117">-Force</span></span>
<span data-ttu-id="9457f-118">Tvinga kommandot att köras utan ytterligare en varning.</span><span class="sxs-lookup"><span data-stu-id="9457f-118">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="9457f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9457f-119">-InputObject</span></span>
<span data-ttu-id="9457f-120">Indatavärdet till cmdleten: objektet Protected ASR-objekt som är kopplat till det replikerade objektet för replikering ska inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="9457f-120">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

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

### <span data-ttu-id="9457f-121">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="9457f-121">-WaitForCompletion</span></span>
<span data-ttu-id="9457f-122">Anger att cmdleten ska vänta på att åtgärden ska slutföras innan den returneras.</span><span class="sxs-lookup"><span data-stu-id="9457f-122">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

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

### <span data-ttu-id="9457f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9457f-123">-WhatIf</span></span>
<span data-ttu-id="9457f-124">Visar vad som händer om cmdleten körs utan att köra cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9457f-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="9457f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9457f-125">CommonParameters</span></span>
<span data-ttu-id="9457f-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9457f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9457f-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9457f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9457f-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9457f-128">INPUTS</span></span>

### <span data-ttu-id="9457f-129">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9457f-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="9457f-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9457f-130">OUTPUTS</span></span>

### <span data-ttu-id="9457f-131">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9457f-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9457f-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9457f-132">NOTES</span></span>

## <span data-ttu-id="9457f-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9457f-133">RELATED LINKS</span></span>

[<span data-ttu-id="9457f-134">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9457f-134">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="9457f-135">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9457f-135">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="9457f-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9457f-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
