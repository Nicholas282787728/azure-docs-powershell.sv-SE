---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 67e38be81ddce808151824ee307f27dd758768ea
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523990"
---
# <span data-ttu-id="eb397-101">Get-AzRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="eb397-101">Get-AzRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="eb397-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb397-102">SYNOPSIS</span></span>
<span data-ttu-id="eb397-103">Hämtar tillgängliga återställnings punkter för ett replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="eb397-103">Gets the available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="eb397-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb397-104">SYNTAX</span></span>

### <span data-ttu-id="eb397-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="eb397-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb397-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="eb397-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb397-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb397-107">DESCRIPTION</span></span>
<span data-ttu-id="eb397-108">Cmdleten **Get-AzRecoveryServicesAsrRecoveryPoint** hämtar listan över tillgängliga återställnings punkter för ett replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="eb397-108">The **Get-AzRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="eb397-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb397-109">EXAMPLES</span></span>

### <span data-ttu-id="eb397-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="eb397-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="eb397-111">Hämtar återställnings punkter för det angivna skyddade objektet för ASR-replikering.</span><span class="sxs-lookup"><span data-stu-id="eb397-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="eb397-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb397-112">PARAMETERS</span></span>

### <span data-ttu-id="eb397-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb397-113">-DefaultProfile</span></span>
<span data-ttu-id="eb397-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eb397-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="eb397-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="eb397-115">-Name</span></span>
<span data-ttu-id="eb397-116">Anger namnet på återställnings punkten som ska visas.</span><span class="sxs-lookup"><span data-stu-id="eb397-116">Specifies the name of the recovery point to get.</span></span>

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

### <span data-ttu-id="eb397-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="eb397-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="eb397-118">Anger objektet skyddat objekt för Azure Site Recovery för vilket du vill få en lista över tillgängliga återställnings punkter.</span><span class="sxs-lookup"><span data-stu-id="eb397-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

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

### <span data-ttu-id="eb397-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb397-119">CommonParameters</span></span>
<span data-ttu-id="eb397-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb397-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb397-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb397-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb397-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb397-122">INPUTS</span></span>

### <span data-ttu-id="eb397-123">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="eb397-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="eb397-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb397-124">OUTPUTS</span></span>

### <span data-ttu-id="eb397-125">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="eb397-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span></span>

## <span data-ttu-id="eb397-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb397-126">NOTES</span></span>

## <span data-ttu-id="eb397-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb397-127">RELATED LINKS</span></span>

[<span data-ttu-id="eb397-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="eb397-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="eb397-129">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="eb397-129">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="eb397-130">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="eb397-130">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="eb397-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="eb397-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="eb397-132">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="eb397-132">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
