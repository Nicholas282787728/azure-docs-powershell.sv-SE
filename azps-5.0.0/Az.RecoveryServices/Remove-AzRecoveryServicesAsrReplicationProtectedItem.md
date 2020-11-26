---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 71731c0a6f4f0bb917cb7490c1647add71b9a893
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271267"
---
# <span data-ttu-id="a056b-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a056b-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="a056b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a056b-102">SYNOPSIS</span></span>
<span data-ttu-id="a056b-103">Stoppar/inaktiverar replikering för ett skyddat objekt i Azure Site Recovery-replikering.</span><span class="sxs-lookup"><span data-stu-id="a056b-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

## <span data-ttu-id="a056b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a056b-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a056b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a056b-105">DESCRIPTION</span></span>
<span data-ttu-id="a056b-106">Cmdleten **Remove-AzRecoveryServicesAsrReplicationProtectedItem** inaktiverar replikeringen av angivet skyddat objekt för Azure Site Recovery-objektet.</span><span class="sxs-lookup"><span data-stu-id="a056b-106">The **Remove-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="a056b-107">Den här åtgärden gör att replikering stoppas för det skyddade objektet.</span><span class="sxs-lookup"><span data-stu-id="a056b-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="a056b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a056b-108">EXAMPLES</span></span>

### <span data-ttu-id="a056b-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a056b-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="a056b-110">Startar åtgärden inaktivera replikering för det angivna replikerade skyddade objektet och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="a056b-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a056b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a056b-111">PARAMETERS</span></span>

### <span data-ttu-id="a056b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a056b-112">-DefaultProfile</span></span>
<span data-ttu-id="a056b-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a056b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a056b-114">-Force</span><span class="sxs-lookup"><span data-stu-id="a056b-114">-Force</span></span>
<span data-ttu-id="a056b-115">Tvinga kommandot att köras utan ytterligare en varning.</span><span class="sxs-lookup"><span data-stu-id="a056b-115">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a056b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a056b-116">-InputObject</span></span>
<span data-ttu-id="a056b-117">Indatavärdet till cmdleten: objektet Protected ASR-objekt som är kopplat till det replikerade objektet för replikering ska inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="a056b-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a056b-118">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="a056b-118">-WaitForCompletion</span></span>
<span data-ttu-id="a056b-119">Anger att cmdleten ska vänta på att åtgärden ska slutföras innan den returneras.</span><span class="sxs-lookup"><span data-stu-id="a056b-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a056b-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a056b-120">-Confirm</span></span>
<span data-ttu-id="a056b-121">Ange om du vill bekräfta.</span><span class="sxs-lookup"><span data-stu-id="a056b-121">Specify if confirmation is required.</span></span> <span data-ttu-id="a056b-122">Ange värdet för parametern Confirm till $false för att hoppa över bekräftelsen.</span><span class="sxs-lookup"><span data-stu-id="a056b-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a056b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a056b-123">-WhatIf</span></span>
<span data-ttu-id="a056b-124">Visar vad som händer om cmdleten körs utan att köra cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a056b-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a056b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a056b-125">CommonParameters</span></span>
<span data-ttu-id="a056b-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a056b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a056b-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a056b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a056b-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a056b-128">INPUTS</span></span>

### <span data-ttu-id="a056b-129">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a056b-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="a056b-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a056b-130">OUTPUTS</span></span>

### <span data-ttu-id="a056b-131">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a056b-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a056b-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a056b-132">NOTES</span></span>

## <span data-ttu-id="a056b-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a056b-133">RELATED LINKS</span></span>

[<span data-ttu-id="a056b-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a056b-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="a056b-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a056b-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="a056b-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a056b-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)