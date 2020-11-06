---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 86A60FD6-551A-4A6B-A4D1-466F33CE714A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoveryapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
ms.openlocfilehash: 97ebacf9f5c51778122bfb8e8157692b7f1dfd03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582927"
---
# <span data-ttu-id="10100-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="10100-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span></span>

## <span data-ttu-id="10100-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10100-102">SYNOPSIS</span></span>
<span data-ttu-id="10100-103">Ändrar en återställnings punkt för ett misslyckat överskyddat objekt innan redundansväxling genomförs.</span><span class="sxs-lookup"><span data-stu-id="10100-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10100-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10100-104">SYNTAX</span></span>

```
Start-AzureRmSiteRecoveryApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10100-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10100-105">DESCRIPTION</span></span>
<span data-ttu-id="10100-106">**Start-AzureRmSiteRecoveryApplyRecoveryPoint** ändrar en återställnings punkt för ett misslyckat överskyddat objekt innan redundansväxlingen genomförs.</span><span class="sxs-lookup"><span data-stu-id="10100-106">The **Start-AzureRmSiteRecoveryApplyRecoveryPoint** changes a recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="10100-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10100-107">EXAMPLES</span></span>

## <span data-ttu-id="10100-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10100-108">PARAMETERS</span></span>

### <span data-ttu-id="10100-109">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="10100-109">-DataEncryptionPrimaryCertFile</span></span>
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

### <span data-ttu-id="10100-110">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="10100-110">-DataEncryptionSecondaryCertFile</span></span>
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

### <span data-ttu-id="10100-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10100-111">-DefaultProfile</span></span>
<span data-ttu-id="10100-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="10100-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10100-113">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="10100-113">-RecoveryPoint</span></span>
<span data-ttu-id="10100-114">Anger återställnings punkt objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="10100-114">Specifies the recovery point object that this cmdlet changes.</span></span>

```yaml
Type: ASRRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10100-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="10100-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="10100-116">Anger objektet replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="10100-116">Specifies the Replication Protected Item object.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10100-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10100-117">CommonParameters</span></span>
<span data-ttu-id="10100-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10100-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10100-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10100-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10100-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10100-120">INPUTS</span></span>

### <span data-ttu-id="10100-121">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="10100-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="10100-122">Parametern ' ReplicationProtectedItem ' godkänner värdet av typen ' ASRReplicationProtectedItem ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="10100-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="10100-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10100-123">OUTPUTS</span></span>

### <span data-ttu-id="10100-124">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="10100-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="10100-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10100-125">NOTES</span></span>

## <span data-ttu-id="10100-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10100-126">RELATED LINKS</span></span>

[<span data-ttu-id="10100-127">Azure Site Recovery-cmdletar</span><span class="sxs-lookup"><span data-stu-id="10100-127">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
