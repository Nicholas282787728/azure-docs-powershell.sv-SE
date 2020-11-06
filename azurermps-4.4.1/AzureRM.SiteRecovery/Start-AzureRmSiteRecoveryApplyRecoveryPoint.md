---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 86A60FD6-551A-4A6B-A4D1-466F33CE714A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
ms.openlocfilehash: d77ed7723ef9875413c551912563b4ee2f4ae306
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575803"
---
# <span data-ttu-id="c11fd-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="c11fd-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span></span>

## <span data-ttu-id="c11fd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c11fd-102">SYNOPSIS</span></span>
<span data-ttu-id="c11fd-103">Ändrar en återställnings punkt för ett misslyckat överskyddat objekt innan redundansväxling genomförs.</span><span class="sxs-lookup"><span data-stu-id="c11fd-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c11fd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c11fd-104">SYNTAX</span></span>

```
Start-AzureRmSiteRecoveryApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c11fd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c11fd-105">DESCRIPTION</span></span>
<span data-ttu-id="c11fd-106">**Start-AzureRmSiteRecoveryApplyRecoveryPoint** ändrar en återställnings punkt för ett misslyckat överskyddat objekt innan redundansväxlingen genomförs.</span><span class="sxs-lookup"><span data-stu-id="c11fd-106">The **Start-AzureRmSiteRecoveryApplyRecoveryPoint** changes a recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="c11fd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c11fd-107">EXAMPLES</span></span>

## <span data-ttu-id="c11fd-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c11fd-108">PARAMETERS</span></span>

### <span data-ttu-id="c11fd-109">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="c11fd-109">-DataEncryptionPrimaryCertFile</span></span>
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

### <span data-ttu-id="c11fd-110">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="c11fd-110">-DataEncryptionSecondaryCertFile</span></span>
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

### <span data-ttu-id="c11fd-111">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="c11fd-111">-RecoveryPoint</span></span>
<span data-ttu-id="c11fd-112">Anger återställnings punkt objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="c11fd-112">Specifies the recovery point object that this cmdlet changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11fd-113">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c11fd-113">-ReplicationProtectedItem</span></span>
<span data-ttu-id="c11fd-114">Anger objektet replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="c11fd-114">Specifies the Replication Protected Item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c11fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c11fd-115">-DefaultProfile</span></span>
<span data-ttu-id="c11fd-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c11fd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c11fd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c11fd-117">CommonParameters</span></span>
<span data-ttu-id="c11fd-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c11fd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c11fd-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c11fd-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c11fd-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c11fd-120">INPUTS</span></span>

### <span data-ttu-id="c11fd-121">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c11fd-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="c11fd-122">Parametern ' ReplicationProtectedItem ' godkänner värdet av typen ' ASRReplicationProtectedItem ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c11fd-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="c11fd-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c11fd-123">OUTPUTS</span></span>

### <span data-ttu-id="c11fd-124">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c11fd-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c11fd-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c11fd-125">NOTES</span></span>

## <span data-ttu-id="c11fd-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c11fd-126">RELATED LINKS</span></span>

[<span data-ttu-id="c11fd-127">Azure Site Recovery-cmdletar</span><span class="sxs-lookup"><span data-stu-id="c11fd-127">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
