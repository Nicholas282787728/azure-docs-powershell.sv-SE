---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 21a01ae07c383484a6ec8e17d9b09a93671bfbe2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575138"
---
# <span data-ttu-id="15d37-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="15d37-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="15d37-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="15d37-102">SYNOPSIS</span></span>
<span data-ttu-id="15d37-103">Hämtar tillgängliga återställnings punkter för ett replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="15d37-103">Gets the available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15d37-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="15d37-104">SYNTAX</span></span>

### <span data-ttu-id="15d37-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="15d37-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15d37-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="15d37-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -Name <String>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15d37-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="15d37-107">DESCRIPTION</span></span>
<span data-ttu-id="15d37-108">Cmdleten **Get-AzureRmRecoveryServicesAsrRecoveryPoint** hämtar listan över tillgängliga återställnings punkter för ett replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="15d37-108">The **Get-AzureRmRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="15d37-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="15d37-109">EXAMPLES</span></span>

### <span data-ttu-id="15d37-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="15d37-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="15d37-111">Hämtar återställnings punkter för det angivna skyddade objektet för ASR-replikering.</span><span class="sxs-lookup"><span data-stu-id="15d37-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="15d37-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="15d37-112">PARAMETERS</span></span>

### <span data-ttu-id="15d37-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15d37-113">-DefaultProfile</span></span>
<span data-ttu-id="15d37-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="15d37-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="15d37-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="15d37-115">-Name</span></span>
<span data-ttu-id="15d37-116">Anger namnet på återställnings punkten som ska visas.</span><span class="sxs-lookup"><span data-stu-id="15d37-116">Specifies the name of the recovery point to get.</span></span>

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

### <span data-ttu-id="15d37-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="15d37-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="15d37-118">Anger objektet skyddat objekt för Azure Site Recovery för vilket du vill få en lista över tillgängliga återställnings punkter.</span><span class="sxs-lookup"><span data-stu-id="15d37-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

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

### <span data-ttu-id="15d37-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15d37-119">CommonParameters</span></span>
<span data-ttu-id="15d37-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15d37-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15d37-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15d37-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15d37-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="15d37-122">INPUTS</span></span>

### <span data-ttu-id="15d37-123">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="15d37-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="15d37-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="15d37-124">OUTPUTS</span></span>

### <span data-ttu-id="15d37-125">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPoint, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="15d37-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="15d37-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="15d37-126">NOTES</span></span>

## <span data-ttu-id="15d37-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="15d37-127">RELATED LINKS</span></span>

[<span data-ttu-id="15d37-128">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="15d37-128">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="15d37-129">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="15d37-129">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="15d37-130">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="15d37-130">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="15d37-131">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="15d37-131">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="15d37-132">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="15d37-132">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
