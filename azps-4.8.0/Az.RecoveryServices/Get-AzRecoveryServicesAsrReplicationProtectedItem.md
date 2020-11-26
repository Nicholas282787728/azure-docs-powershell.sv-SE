---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: ceb49a3ea46915dbdc881e42974d0204d213e384
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259921"
---
# <span data-ttu-id="9c1ae-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9c1ae-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="9c1ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9c1ae-102">SYNOPSIS</span></span>
<span data-ttu-id="9c1ae-103">Hämtar egenskaperna för en Azure Site Recovery-replikerade objekt.</span><span class="sxs-lookup"><span data-stu-id="9c1ae-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

## <span data-ttu-id="9c1ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9c1ae-104">SYNTAX</span></span>

### <span data-ttu-id="9c1ae-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="9c1ae-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c1ae-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="9c1ae-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c1ae-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="9c1ae-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c1ae-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="9c1ae-108">ByProtectableItemObject</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c1ae-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9c1ae-109">DESCRIPTION</span></span>
<span data-ttu-id="9c1ae-110">Cmdleten **Get-AzRecoveryServicesAsrReplicationProtectedItem** får egenskaperna för alla eller det angivna skyddade ASR-objektet från den angivna ASR-skyddsagenten.</span><span class="sxs-lookup"><span data-stu-id="9c1ae-110">The **Get-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="9c1ae-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9c1ae-111">EXAMPLES</span></span>

### <span data-ttu-id="9c1ae-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9c1ae-112">Example 1</span></span>
```powershell
PS C:\> $ReplicationProtectedItems = Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="9c1ae-113">Här listas alla replikerade objekt i den angivna tjänsten för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="9c1ae-113">Lists all replication protected items in the specified ASR protection container.</span></span>

### <span data-ttu-id="9c1ae-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9c1ae-114">Example 2</span></span>

<span data-ttu-id="9c1ae-115">Hämtar egenskaperna för en Azure Site Recovery-replikerade objekt.</span><span class="sxs-lookup"><span data-stu-id="9c1ae-115">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span> <span data-ttu-id="9c1ae-116">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="9c1ae-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesAsrReplicationProtectedItem -FriendlyName XXXXXXXXXX -ProtectionContainer $PrimaryContainer
```

## <span data-ttu-id="9c1ae-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9c1ae-117">PARAMETERS</span></span>

### <span data-ttu-id="9c1ae-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c1ae-118">-DefaultProfile</span></span>
<span data-ttu-id="9c1ae-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9c1ae-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9c1ae-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="9c1ae-120">-FriendlyName</span></span>
<span data-ttu-id="9c1ae-121">Anger det egna namnet på det replikerade objekt som ska visas.</span><span class="sxs-lookup"><span data-stu-id="9c1ae-121">Specifies the friendly name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="9c1ae-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="9c1ae-122">-Name</span></span>
<span data-ttu-id="9c1ae-123">Anger namnet på det replikerade objekt som ska visas.</span><span class="sxs-lookup"><span data-stu-id="9c1ae-123">Specifies the name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="9c1ae-124">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="9c1ae-124">-ProtectableItem</span></span>
<span data-ttu-id="9c1ae-125">Anger ett objekt som skyddas av ASR.</span><span class="sxs-lookup"><span data-stu-id="9c1ae-125">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="9c1ae-126">Cmdleten får det skyddade objektet för ASR-replikering som motsvarar det angivna objektet för skyddad automatisk system återställning om objektet är skyddat.</span><span class="sxs-lookup"><span data-stu-id="9c1ae-126">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

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

### <span data-ttu-id="9c1ae-127">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="9c1ae-127">-ProtectionContainer</span></span>
<span data-ttu-id="9c1ae-128">Anger ASR-systemobjektet för ASR-skyddsagenten som motsvarar det replikerade objektet.</span><span class="sxs-lookup"><span data-stu-id="9c1ae-128">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

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

### <span data-ttu-id="9c1ae-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c1ae-129">CommonParameters</span></span>
<span data-ttu-id="9c1ae-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c1ae-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c1ae-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c1ae-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c1ae-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9c1ae-132">INPUTS</span></span>

### <span data-ttu-id="9c1ae-133">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="9c1ae-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

### <span data-ttu-id="9c1ae-134">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="9c1ae-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="9c1ae-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9c1ae-135">OUTPUTS</span></span>

### <span data-ttu-id="9c1ae-136">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9c1ae-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="9c1ae-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9c1ae-137">NOTES</span></span>

## <span data-ttu-id="9c1ae-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9c1ae-138">RELATED LINKS</span></span>

[<span data-ttu-id="9c1ae-139">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9c1ae-139">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="9c1ae-140">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9c1ae-140">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="9c1ae-141">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9c1ae-141">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)