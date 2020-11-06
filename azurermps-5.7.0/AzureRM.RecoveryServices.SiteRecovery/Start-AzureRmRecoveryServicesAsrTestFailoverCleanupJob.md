---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrtestfailovercleanupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob.md
ms.openlocfilehash: 423ec89745b21176c714c1c2e956d4320c28b034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573352"
---
# <span data-ttu-id="4ff06-101">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="4ff06-101">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span></span>

## <span data-ttu-id="4ff06-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ff06-102">SYNOPSIS</span></span>
<span data-ttu-id="4ff06-103">Startar rensning av redundanstestning.</span><span class="sxs-lookup"><span data-stu-id="4ff06-103">Starts the test failover cleanup operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ff06-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ff06-104">SYNTAX</span></span>

### <span data-ttu-id="4ff06-105">ByRPIObject (standard)</span><span class="sxs-lookup"><span data-stu-id="4ff06-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Comment <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ff06-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4ff06-106">ByResourceId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ResourceId <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ff06-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="4ff06-107">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan <ASRRecoveryPlan> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ff06-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ff06-108">DESCRIPTION</span></span>
<span data-ttu-id="4ff06-109">Cmdleten **Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob** startar rensning av redundanstest för ett replikerat objekt eller en återställnings plan där en redundanstestning har utförts.</span><span class="sxs-lookup"><span data-stu-id="4ff06-109">The **Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob** cmdlet starts the test failover cleanup operation on a replication protected item or recovery plan on which a test failover has been performed.</span></span>

## <span data-ttu-id="4ff06-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ff06-110">EXAMPLES</span></span>

### <span data-ttu-id="4ff06-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4ff06-111">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $rpi -Comments "testing done"
```

<span data-ttu-id="4ff06-112">Jobb för att spåra rensning av redundanstestning av ett skyddat objekt i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4ff06-112">Job to track test failover Cleanup of an Azure Site Recovery replication protected item.</span></span>

### <span data-ttu-id="4ff06-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4ff06-113">Example 2</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $recoveryPlan -Comments "testing done"
```

<span data-ttu-id="4ff06-114">Jobb för att spåra rensning av redundanstestning av en Azure Site Recovery-recoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="4ff06-114">Job to track test failover Cleanup of an Azure Site Recovery recoveryPlan.</span></span>

## <span data-ttu-id="4ff06-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ff06-115">PARAMETERS</span></span>

### <span data-ttu-id="4ff06-116">-Kommentera</span><span class="sxs-lookup"><span data-stu-id="4ff06-116">-Comment</span></span>
<span data-ttu-id="4ff06-117">Användar kommentar för testning av redundans.</span><span class="sxs-lookup"><span data-stu-id="4ff06-117">User Comment for Test Failover.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ff06-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4ff06-118">-Confirm</span></span>
<span data-ttu-id="4ff06-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4ff06-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ff06-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ff06-120">-DefaultProfile</span></span>
<span data-ttu-id="4ff06-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4ff06-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ff06-122">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4ff06-122">-RecoveryPlan</span></span>
<span data-ttu-id="4ff06-123">Återställnings plan för rensning av redundanstestning på.</span><span class="sxs-lookup"><span data-stu-id="4ff06-123">Recovery Plan to perform the test failover cleanup on.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ff06-124">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4ff06-124">-ReplicationProtectedItem</span></span>
<span data-ttu-id="4ff06-125">Replikerat objekt som ska användas för testning av redundans.</span><span class="sxs-lookup"><span data-stu-id="4ff06-125">Replication Protected Item to perform the test failover cleanup on.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ff06-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ff06-126">-ResourceId</span></span>
<span data-ttu-id="4ff06-127">Resurs-ID för ett replikerat objekt/återställnings plan för cleaningup.</span><span class="sxs-lookup"><span data-stu-id="4ff06-127">Resource Id of replication protected item / recovery plan for cleaningup test failover.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ff06-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ff06-128">-WhatIf</span></span>
<span data-ttu-id="4ff06-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4ff06-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ff06-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4ff06-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ff06-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ff06-131">CommonParameters</span></span>
<span data-ttu-id="4ff06-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ff06-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ff06-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ff06-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ff06-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ff06-134">INPUTS</span></span>

### <span data-ttu-id="4ff06-135">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4ff06-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="4ff06-136">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4ff06-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="4ff06-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ff06-137">OUTPUTS</span></span>

### <span data-ttu-id="4ff06-138">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4ff06-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4ff06-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ff06-139">NOTES</span></span>

## <span data-ttu-id="4ff06-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ff06-140">RELATED LINKS</span></span>
