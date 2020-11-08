---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: d669e450e096e4d9c0c61a3e1d485e3caaaa9ae3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920187"
---
# <span data-ttu-id="da7b3-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="da7b3-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="da7b3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="da7b3-102">SYNOPSIS</span></span>
<span data-ttu-id="da7b3-103">Ändrar en återställnings punkt för ett misslyckat överskyddat objekt innan redundans utförs.</span><span class="sxs-lookup"><span data-stu-id="da7b3-103">Changes a recovery point for a failed over protected item before committing the failover operation.</span></span>

## <span data-ttu-id="da7b3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="da7b3-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da7b3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="da7b3-105">DESCRIPTION</span></span>
<span data-ttu-id="da7b3-106">**Start-AzRecoveryServicesAsrApplyRecoveryPoint** ändrar återställnings punkten för ett misslyckat överskyddat objekt innan redundansväxlingen genomförs.</span><span class="sxs-lookup"><span data-stu-id="da7b3-106">The **Start-AzRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="da7b3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="da7b3-107">EXAMPLES</span></span>

### <span data-ttu-id="da7b3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="da7b3-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="da7b3-109">Börjar tillämpa den angivna återställnings punkten på det replikerade objektet och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="da7b3-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="da7b3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="da7b3-110">PARAMETERS</span></span>

### <span data-ttu-id="da7b3-111">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="da7b3-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="da7b3-112">Anger den primära certifikat filen om data kryptering används.</span><span class="sxs-lookup"><span data-stu-id="da7b3-112">Specifies the primary certificate file if data encryption is being used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7b3-113">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="da7b3-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="da7b3-114">Anger den sekundära certifikat filen om data kryptering används.</span><span class="sxs-lookup"><span data-stu-id="da7b3-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da7b3-115">-DefaultProfile</span></span>
<span data-ttu-id="da7b3-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="da7b3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="da7b3-117">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="da7b3-117">-RecoveryPoint</span></span>
<span data-ttu-id="da7b3-118">Anger det återställnings punkt objekt som motsvarar återställnings punkten som ska användas.</span><span class="sxs-lookup"><span data-stu-id="da7b3-118">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7b3-119">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="da7b3-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="da7b3-120">Anger objekt för skyddat objekt för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="da7b3-120">Specifies the ASR replication protected item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da7b3-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="da7b3-121">-Confirm</span></span>
<span data-ttu-id="da7b3-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="da7b3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da7b3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da7b3-123">-WhatIf</span></span>
<span data-ttu-id="da7b3-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="da7b3-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da7b3-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="da7b3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da7b3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da7b3-126">CommonParameters</span></span>
<span data-ttu-id="da7b3-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da7b3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da7b3-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da7b3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da7b3-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="da7b3-129">INPUTS</span></span>

### <span data-ttu-id="da7b3-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="da7b3-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="da7b3-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="da7b3-131">OUTPUTS</span></span>

### <span data-ttu-id="da7b3-132">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="da7b3-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="da7b3-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="da7b3-133">NOTES</span></span>

## <span data-ttu-id="da7b3-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="da7b3-134">RELATED LINKS</span></span>

[<span data-ttu-id="da7b3-135">Azure Site Recovery-cmdletar</span><span class="sxs-lookup"><span data-stu-id="da7b3-135">Azure Site Recovery Cmdlets</span></span>](./Az.SiteRecovery.md)