---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 8a99625cc19eb9ac5f3d842b7c5c99979cdee69d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573944"
---
# <span data-ttu-id="1aae8-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="1aae8-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="1aae8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1aae8-102">SYNOPSIS</span></span>
<span data-ttu-id="1aae8-103">Ändrar en återställnings punkt för ett misslyckat överskyddat objekt innan redundansväxling genomförs.</span><span class="sxs-lookup"><span data-stu-id="1aae8-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1aae8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1aae8-104">SYNTAX</span></span>

```
Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1aae8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1aae8-105">DESCRIPTION</span></span>
<span data-ttu-id="1aae8-106">**Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint** ändrar återställnings punkten för ett misslyckat överskyddat objekt innan redundansväxlingen genomförs.</span><span class="sxs-lookup"><span data-stu-id="1aae8-106">The **Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="1aae8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1aae8-107">EXAMPLES</span></span>

### <span data-ttu-id="1aae8-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1aae8-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="1aae8-109">Börjar tillämpa den angivna återställnings punkten på det replikerade objektet och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="1aae8-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="1aae8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1aae8-110">PARAMETERS</span></span>

### <span data-ttu-id="1aae8-111">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="1aae8-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="1aae8-112">Anger den primära certifikat filen om data kryptering används.</span><span class="sxs-lookup"><span data-stu-id="1aae8-112">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="1aae8-113">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="1aae8-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="1aae8-114">Anger den sekundära certifikat filen om data kryptering används.</span><span class="sxs-lookup"><span data-stu-id="1aae8-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="1aae8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aae8-115">-DefaultProfile</span></span>
<span data-ttu-id="1aae8-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1aae8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aae8-117">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="1aae8-117">-RecoveryPoint</span></span>
<span data-ttu-id="1aae8-118">Anger det återställnings punkt objekt som motsvarar återställnings punkten som ska användas.</span><span class="sxs-lookup"><span data-stu-id="1aae8-118">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

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

### <span data-ttu-id="1aae8-119">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1aae8-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="1aae8-120">Anger objekt för skyddat objekt för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="1aae8-120">Specifies the ASR replication protected item object.</span></span>

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

### <span data-ttu-id="1aae8-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1aae8-121">-Confirm</span></span>
<span data-ttu-id="1aae8-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1aae8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1aae8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1aae8-123">-WhatIf</span></span>
<span data-ttu-id="1aae8-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1aae8-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1aae8-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1aae8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1aae8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aae8-126">CommonParameters</span></span>
<span data-ttu-id="1aae8-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aae8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aae8-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1aae8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aae8-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1aae8-129">INPUTS</span></span>

### <span data-ttu-id="1aae8-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1aae8-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="1aae8-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1aae8-131">OUTPUTS</span></span>

### <span data-ttu-id="1aae8-132">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1aae8-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1aae8-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1aae8-133">NOTES</span></span>

## <span data-ttu-id="1aae8-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1aae8-134">RELATED LINKS</span></span>

[<span data-ttu-id="1aae8-135">Azure Site Recovery-cmdletar</span><span class="sxs-lookup"><span data-stu-id="1aae8-135">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
