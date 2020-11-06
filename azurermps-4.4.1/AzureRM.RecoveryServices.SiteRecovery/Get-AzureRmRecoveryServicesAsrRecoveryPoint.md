---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 96a30621bc545b635262fd7937e0e55739d0be7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585371"
---
# <span data-ttu-id="877f0-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="877f0-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="877f0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="877f0-102">SYNOPSIS</span></span>
<span data-ttu-id="877f0-103">Hämtar tillgängliga återställnings punkter för ett replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="877f0-103">Gets the available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="877f0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="877f0-104">SYNTAX</span></span>

### <span data-ttu-id="877f0-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="877f0-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [<CommonParameters>]
```

### <span data-ttu-id="877f0-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="877f0-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -Name <String>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [<CommonParameters>]
```

## <span data-ttu-id="877f0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="877f0-107">DESCRIPTION</span></span>
<span data-ttu-id="877f0-108">Cmdleten **Get-AzureRmRecoveryServicesAsrRecoveryPoint** hämtar listan över tillgängliga återställnings punkter för ett replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="877f0-108">The **Get-AzureRmRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="877f0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="877f0-109">EXAMPLES</span></span>

### <span data-ttu-id="877f0-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="877f0-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="877f0-111">Hämtar återställnings punkter för det angivna skyddade objektet för ASR-replikering.</span><span class="sxs-lookup"><span data-stu-id="877f0-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="877f0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="877f0-112">PARAMETERS</span></span>

### <span data-ttu-id="877f0-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="877f0-113">-Name</span></span>
<span data-ttu-id="877f0-114">Anger namnet på återställnings punkten som ska visas.</span><span class="sxs-lookup"><span data-stu-id="877f0-114">Specifies the name of the recovery point to get.</span></span>

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

### <span data-ttu-id="877f0-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="877f0-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="877f0-116">Anger objektet skyddat objekt för Azure Site Recovery för vilket du vill få en lista över tillgängliga återställnings punkter.</span><span class="sxs-lookup"><span data-stu-id="877f0-116">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

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

### <span data-ttu-id="877f0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="877f0-117">CommonParameters</span></span>
<span data-ttu-id="877f0-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="877f0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="877f0-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="877f0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="877f0-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="877f0-120">INPUTS</span></span>

### <span data-ttu-id="877f0-121">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="877f0-121">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="877f0-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="877f0-122">OUTPUTS</span></span>

### <span data-ttu-id="877f0-123">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPoint, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="877f0-123">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="877f0-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="877f0-124">NOTES</span></span>

## <span data-ttu-id="877f0-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="877f0-125">RELATED LINKS</span></span>

[<span data-ttu-id="877f0-126">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="877f0-126">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="877f0-127">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="877f0-127">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="877f0-128">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="877f0-128">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="877f0-129">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="877f0-129">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="877f0-130">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="877f0-130">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
