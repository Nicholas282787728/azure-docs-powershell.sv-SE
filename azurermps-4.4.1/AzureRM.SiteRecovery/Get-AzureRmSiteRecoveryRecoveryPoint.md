---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 77AFEF57-A4ED-4F82-A3FF-0E33D7810B3B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPoint.md
ms.openlocfilehash: 68e005a4e54277ad1be304911645c3eeda455d46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757999"
---
# <span data-ttu-id="a7cf8-101">Get-AzureRmSiteRecoveryRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a7cf8-101">Get-AzureRmSiteRecoveryRecoveryPoint</span></span>

## <span data-ttu-id="a7cf8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a7cf8-102">SYNOPSIS</span></span>
<span data-ttu-id="a7cf8-103">Hämtar tillgängliga återställnings punkter för ett replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="a7cf8-103">Gets available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7cf8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a7cf8-104">SYNTAX</span></span>

### <span data-ttu-id="a7cf8-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="a7cf8-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7cf8-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="a7cf8-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7cf8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a7cf8-107">DESCRIPTION</span></span>
<span data-ttu-id="a7cf8-108">Cmdleten **Get-AzureRmSiteRecoveryRecoveryPoint** hämtar listan över tillgängliga återställnings punkter för ett replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="a7cf8-108">The **Get-AzureRmSiteRecoveryRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="a7cf8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a7cf8-109">EXAMPLES</span></span>

## <span data-ttu-id="a7cf8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a7cf8-110">PARAMETERS</span></span>

### <span data-ttu-id="a7cf8-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="a7cf8-111">-Name</span></span>
<span data-ttu-id="a7cf8-112">Anger namnet på återställnings punkten som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="a7cf8-112">Specifies the name of the recovery point this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7cf8-113">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a7cf8-113">-ReplicationProtectedItem</span></span>
<span data-ttu-id="a7cf8-114">Anger objektet skyddat objekt för Azure Site Recovery-objekt.</span><span class="sxs-lookup"><span data-stu-id="a7cf8-114">Specifies the Azure Site Recovery Replication Protected Item object.</span></span>

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

### <span data-ttu-id="a7cf8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7cf8-115">-DefaultProfile</span></span>
<span data-ttu-id="a7cf8-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a7cf8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7cf8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7cf8-117">CommonParameters</span></span>
<span data-ttu-id="a7cf8-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7cf8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7cf8-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7cf8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7cf8-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a7cf8-120">INPUTS</span></span>

### <span data-ttu-id="a7cf8-121">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a7cf8-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="a7cf8-122">Parametern ' ReplicationProtectedItem ' godkänner värdet av typen ' ASRReplicationProtectedItem ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a7cf8-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="a7cf8-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a7cf8-123">OUTPUTS</span></span>

### <span data-ttu-id="a7cf8-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. SiteRecovery. ASRRecoveryPoint, Microsoft. Azure. commands. SiteRecovery, version = 2.0.1.0; Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a7cf8-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a7cf8-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a7cf8-125">NOTES</span></span>

## <span data-ttu-id="a7cf8-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a7cf8-126">RELATED LINKS</span></span>

[<span data-ttu-id="a7cf8-127">Edit-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a7cf8-127">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Edit-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="a7cf8-128">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a7cf8-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="a7cf8-129">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a7cf8-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="a7cf8-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a7cf8-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="a7cf8-131">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a7cf8-131">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)
