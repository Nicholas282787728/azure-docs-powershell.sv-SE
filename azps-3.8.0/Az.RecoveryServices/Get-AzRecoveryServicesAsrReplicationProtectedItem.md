---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 3c89133b18f1425f65ab9430765f0a2a9a7cfafe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088627"
---
# <span data-ttu-id="7ec5e-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7ec5e-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="7ec5e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ec5e-102">SYNOPSIS</span></span>
<span data-ttu-id="7ec5e-103">Hämtar egenskaperna för en Azure Site Recovery-replikerade objekt.</span><span class="sxs-lookup"><span data-stu-id="7ec5e-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

## <span data-ttu-id="7ec5e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ec5e-104">SYNTAX</span></span>

### <span data-ttu-id="7ec5e-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="7ec5e-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ec5e-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="7ec5e-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ec5e-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="7ec5e-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ec5e-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="7ec5e-108">ByProtectableItemObject</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ec5e-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ec5e-109">DESCRIPTION</span></span>
<span data-ttu-id="7ec5e-110">Cmdleten **Get-AzRecoveryServicesAsrReplicationProtectedItem** får egenskaperna för alla eller det angivna skyddade ASR-objektet från den angivna ASR-skyddsagenten.</span><span class="sxs-lookup"><span data-stu-id="7ec5e-110">The **Get-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="7ec5e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ec5e-111">EXAMPLES</span></span>

### <span data-ttu-id="7ec5e-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7ec5e-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="7ec5e-113">Här listas alla replikerade objekt i den angivna tjänsten för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="7ec5e-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="7ec5e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ec5e-114">PARAMETERS</span></span>

### <span data-ttu-id="7ec5e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ec5e-115">-DefaultProfile</span></span>
<span data-ttu-id="7ec5e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7ec5e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7ec5e-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7ec5e-117">-FriendlyName</span></span>
<span data-ttu-id="7ec5e-118">Anger det egna namnet på det replikerade objekt som ska visas.</span><span class="sxs-lookup"><span data-stu-id="7ec5e-118">Specifies the friendly name of the replication protected item to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ec5e-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="7ec5e-119">-Name</span></span>
<span data-ttu-id="7ec5e-120">Anger namnet på det replikerade objekt som ska visas.</span><span class="sxs-lookup"><span data-stu-id="7ec5e-120">Specifies the name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="7ec5e-121">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7ec5e-121">-ProtectableItem</span></span>
<span data-ttu-id="7ec5e-122">Anger ett objekt som skyddas av ASR.</span><span class="sxs-lookup"><span data-stu-id="7ec5e-122">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="7ec5e-123">Cmdleten får det skyddade objektet för ASR-replikering som motsvarar det angivna objektet för skyddad automatisk system återställning om objektet är skyddat.</span><span class="sxs-lookup"><span data-stu-id="7ec5e-123">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ec5e-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7ec5e-124">-ProtectionContainer</span></span>
<span data-ttu-id="7ec5e-125">Anger ASR-systemobjektet för ASR-skyddsagenten som motsvarar det replikerade objektet.</span><span class="sxs-lookup"><span data-stu-id="7ec5e-125">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ec5e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ec5e-126">CommonParameters</span></span>
<span data-ttu-id="7ec5e-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ec5e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ec5e-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ec5e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ec5e-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ec5e-129">INPUTS</span></span>

### <span data-ttu-id="7ec5e-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7ec5e-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

### <span data-ttu-id="7ec5e-131">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7ec5e-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="7ec5e-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ec5e-132">OUTPUTS</span></span>

### <span data-ttu-id="7ec5e-133">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7ec5e-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="7ec5e-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ec5e-134">NOTES</span></span>

## <span data-ttu-id="7ec5e-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ec5e-135">RELATED LINKS</span></span>

[<span data-ttu-id="7ec5e-136">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7ec5e-136">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="7ec5e-137">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7ec5e-137">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="7ec5e-138">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7ec5e-138">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)