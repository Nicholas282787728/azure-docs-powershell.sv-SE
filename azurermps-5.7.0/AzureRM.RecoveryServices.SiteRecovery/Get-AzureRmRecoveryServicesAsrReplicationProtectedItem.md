---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 90b615edefe860e084de0040a13c1ba5a1ff39ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575561"
---
# <span data-ttu-id="916e9-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="916e9-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="916e9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="916e9-102">SYNOPSIS</span></span>
<span data-ttu-id="916e9-103">Hämtar egenskaperna för en Azure Site Recovery-replikerade objekt.</span><span class="sxs-lookup"><span data-stu-id="916e9-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="916e9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="916e9-104">SYNTAX</span></span>

### <span data-ttu-id="916e9-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="916e9-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="916e9-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="916e9-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="916e9-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="916e9-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="916e9-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="916e9-108">ByProtectableItemObject</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="916e9-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="916e9-109">DESCRIPTION</span></span>
<span data-ttu-id="916e9-110">Cmdleten **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** får egenskaperna för alla eller det angivna skyddade ASR-objektet från den angivna ASR-skyddsagenten.</span><span class="sxs-lookup"><span data-stu-id="916e9-110">The **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="916e9-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="916e9-111">EXAMPLES</span></span>

### <span data-ttu-id="916e9-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="916e9-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="916e9-113">Här listas alla replikerade objekt i den angivna tjänsten för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="916e9-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="916e9-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="916e9-114">PARAMETERS</span></span>

### <span data-ttu-id="916e9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="916e9-115">-DefaultProfile</span></span>
<span data-ttu-id="916e9-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="916e9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="916e9-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="916e9-117">-FriendlyName</span></span>
<span data-ttu-id="916e9-118">Anger det egna namnet på det replikerade objekt som ska visas.</span><span class="sxs-lookup"><span data-stu-id="916e9-118">Specifies the friendly name of the replication protected item to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="916e9-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="916e9-119">-Name</span></span>
<span data-ttu-id="916e9-120">Anger namnet på det replikerade objekt som ska visas.</span><span class="sxs-lookup"><span data-stu-id="916e9-120">Specifies the name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="916e9-121">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="916e9-121">-ProtectableItem</span></span>
<span data-ttu-id="916e9-122">Anger ett objekt som skyddas av ASR.</span><span class="sxs-lookup"><span data-stu-id="916e9-122">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="916e9-123">Cmdleten får det skyddade objektet för ASR-replikering som motsvarar det angivna objektet för skyddad automatisk system återställning om objektet är skyddat.</span><span class="sxs-lookup"><span data-stu-id="916e9-123">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="916e9-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="916e9-124">-ProtectionContainer</span></span>
<span data-ttu-id="916e9-125">Anger ASR-systemobjektet för ASR-skyddsagenten som motsvarar det replikerade objektet.</span><span class="sxs-lookup"><span data-stu-id="916e9-125">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="916e9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="916e9-126">CommonParameters</span></span>
<span data-ttu-id="916e9-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="916e9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="916e9-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="916e9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="916e9-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="916e9-129">INPUTS</span></span>

### <span data-ttu-id="916e9-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="916e9-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>
<span data-ttu-id="916e9-131">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="916e9-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="916e9-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="916e9-132">OUTPUTS</span></span>

### <span data-ttu-id="916e9-133">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="916e9-133">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="916e9-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="916e9-134">NOTES</span></span>

## <span data-ttu-id="916e9-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="916e9-135">RELATED LINKS</span></span>

[<span data-ttu-id="916e9-136">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="916e9-136">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="916e9-137">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="916e9-137">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="916e9-138">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="916e9-138">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
