---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 77AFEF57-A4ED-4F82-A3FF-0E33D7810B3B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPoint.md
ms.openlocfilehash: 42a0a96a32bf1b7f556ee2787f43a5777afa1115
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582983"
---
# <span data-ttu-id="fb004-101">Get-AzureRmSiteRecoveryRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="fb004-101">Get-AzureRmSiteRecoveryRecoveryPoint</span></span>

## <span data-ttu-id="fb004-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb004-102">SYNOPSIS</span></span>
<span data-ttu-id="fb004-103">Hämtar tillgängliga återställnings punkter för ett replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="fb004-103">Gets available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb004-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb004-104">SYNTAX</span></span>

### <span data-ttu-id="fb004-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="fb004-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb004-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="fb004-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb004-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb004-107">DESCRIPTION</span></span>
<span data-ttu-id="fb004-108">Cmdleten **Get-AzureRmSiteRecoveryRecoveryPoint** hämtar listan över tillgängliga återställnings punkter för ett replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="fb004-108">The **Get-AzureRmSiteRecoveryRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="fb004-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb004-109">EXAMPLES</span></span>

## <span data-ttu-id="fb004-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb004-110">PARAMETERS</span></span>

### <span data-ttu-id="fb004-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb004-111">-DefaultProfile</span></span>
<span data-ttu-id="fb004-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fb004-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb004-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="fb004-113">-Name</span></span>
<span data-ttu-id="fb004-114">Anger namnet på återställnings punkten som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="fb004-114">Specifies the name of the recovery point this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb004-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fb004-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="fb004-116">Anger objektet skyddat objekt för Azure Site Recovery-objekt.</span><span class="sxs-lookup"><span data-stu-id="fb004-116">Specifies the Azure Site Recovery Replication Protected Item object.</span></span>

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

### <span data-ttu-id="fb004-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb004-117">CommonParameters</span></span>
<span data-ttu-id="fb004-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb004-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb004-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb004-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb004-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb004-120">INPUTS</span></span>

### <span data-ttu-id="fb004-121">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fb004-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="fb004-122">Parametern ' ReplicationProtectedItem ' godkänner värdet av typen ' ASRReplicationProtectedItem ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="fb004-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="fb004-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb004-123">OUTPUTS</span></span>

### <span data-ttu-id="fb004-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. SiteRecovery. ASRRecoveryPoint, Microsoft. Azure. commands. SiteRecovery, version = 2.0.1.0; Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fb004-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="fb004-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb004-125">NOTES</span></span>

## <span data-ttu-id="fb004-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb004-126">RELATED LINKS</span></span>

[<span data-ttu-id="fb004-127">Edit-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fb004-127">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Edit-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="fb004-128">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fb004-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="fb004-129">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fb004-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="fb004-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fb004-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="fb004-131">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fb004-131">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)
